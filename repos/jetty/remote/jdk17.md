## `jetty:jdk17`

```console
$ docker pull jetty@sha256:ccf96597493110567ca82bc7b464155abbeb76288febaf7fa570bc83d67fd077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:jdk17` - linux; amd64

```console
$ docker pull jetty@sha256:69cf506d39eb7505b582e462e1404bdc34cb985c0870a96874f1e3e55865c1d6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252511194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9743ea05fbc65088f991f86d91be1fa6068ffd3cd1e8fa6aa9b30c5a24b2ad2d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 28 Oct 2021 01:22:47 GMT
ADD file:45a1eba89256c6e3801f14738faca9e260b17b306f0fc8769ba0b0f94f0fdf68 in / 
# Thu, 28 Oct 2021 01:22:47 GMT
CMD ["/bin/bash"]
# Thu, 28 Oct 2021 01:44:41 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 28 Oct 2021 01:45:58 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Thu, 28 Oct 2021 01:45:58 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Oct 2021 01:45:58 GMT
ENV LANG=C.UTF-8
# Thu, 28 Oct 2021 01:45:59 GMT
ENV JAVA_VERSION=17.0.1
# Thu, 28 Oct 2021 01:46:10 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-x64_bin.tar.gz'; 			downloadSha256='1c0a73cbb863aad579b967316bf17673b8f98a9bb938602a140ba2e5c38f880a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='86653d48787e5a1c029df10da7808194fe8bd931ddd72ff3d42850bf1afb317e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 28 Oct 2021 01:46:11 GMT
CMD ["jshell"]
# Thu, 28 Oct 2021 02:46:00 GMT
ENV JETTY_VERSION=9.4.44.v20210927
# Thu, 28 Oct 2021 02:46:01 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 28 Oct 2021 02:46:01 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 28 Oct 2021 02:46:01 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 28 Oct 2021 02:46:01 GMT
ENV PATH=/usr/local/jetty/bin:/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Oct 2021 02:46:01 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.44.v20210927/jetty-home-9.4.44.v20210927.tar.gz
# Thu, 28 Oct 2021 02:46:02 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Thu, 28 Oct 2021 02:46:11 GMT
RUN set -xe ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		for server in 			ha.pool.sks-keyservers.net 			pgp.mit.edu 			hkp://p80.pool.sks-keyservers.net:80 			hkp://keyserver.ubuntu.com:80 			keyserver.pgp.com 			ipv4.pool.sks-keyservers.net ; 		do 			if gpg --batch --keyserver "$server" --recv-keys "$key"; then 				break; 			fi; 		done; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 28 Oct 2021 02:46:11 GMT
WORKDIR /var/lib/jetty
# Thu, 28 Oct 2021 02:46:11 GMT
COPY multi:6f466bb575b852e6668f47004d8edb31588ff8e21b73080bf09d6ed8d3dcb588 in / 
# Thu, 28 Oct 2021 02:46:11 GMT
USER jetty
# Thu, 28 Oct 2021 02:46:11 GMT
EXPOSE 8080
# Thu, 28 Oct 2021 02:46:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Oct 2021 02:46:12 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:f420596490555ff89c8ec7d6b74b4e46c2b3b98dc775c9d19494d8afeb475852`  
		Last Modified: Thu, 28 Oct 2021 01:24:04 GMT  
		Size: 42.0 MB (41970837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a9c63ed3ba0226d765a092dd6fcc06fe5ece8a2dd0fd11e1add9c0ddee488e`  
		Last Modified: Thu, 28 Oct 2021 01:52:24 GMT  
		Size: 13.5 MB (13491622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf092705b191dbeb36cf56fddcc2e45ab0778a28ddc4c4a29c2acf3077c43f10`  
		Last Modified: Thu, 28 Oct 2021 01:54:15 GMT  
		Size: 187.2 MB (187170433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0813bdcf639246d981237fbcf2493cd15cc9bda140f865a35ec149f1b262178b`  
		Last Modified: Thu, 28 Oct 2021 02:48:38 GMT  
		Size: 9.9 MB (9876865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ba7089dcc57525b2eef977a0fedbd667178d00cb08c8f463493b105c452de73`  
		Last Modified: Thu, 28 Oct 2021 02:48:37 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:jdk17` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:09d4d15be4b1579eb2ce4b15a926c0fee7b4f4ab8d04366a91987015f6e6eac7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (252008417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56240f2790b0192c8f688033871288b4c9dd17f5e633f5c6e4d5b30a64bdaec`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Thu, 28 Oct 2021 01:43:49 GMT
ADD file:accebe81069e9a5a2fa2b5311f1fd53f84fc7cc12b93d70f150e3ee0c4d1853c in / 
# Thu, 28 Oct 2021 01:43:50 GMT
CMD ["/bin/bash"]
# Thu, 28 Oct 2021 02:15:05 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 28 Oct 2021 02:17:07 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Thu, 28 Oct 2021 02:17:07 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Oct 2021 02:17:08 GMT
ENV LANG=C.UTF-8
# Thu, 28 Oct 2021 02:17:09 GMT
ENV JAVA_VERSION=17.0.1
# Thu, 28 Oct 2021 02:17:21 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-x64_bin.tar.gz'; 			downloadSha256='1c0a73cbb863aad579b967316bf17673b8f98a9bb938602a140ba2e5c38f880a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='86653d48787e5a1c029df10da7808194fe8bd931ddd72ff3d42850bf1afb317e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 28 Oct 2021 02:17:21 GMT
CMD ["jshell"]
# Thu, 28 Oct 2021 02:57:24 GMT
ENV JETTY_VERSION=9.4.44.v20210927
# Thu, 28 Oct 2021 02:57:25 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 28 Oct 2021 02:57:26 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 28 Oct 2021 02:57:27 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 28 Oct 2021 02:57:28 GMT
ENV PATH=/usr/local/jetty/bin:/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Oct 2021 02:57:29 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/9.4.44.v20210927/jetty-home-9.4.44.v20210927.tar.gz
# Thu, 28 Oct 2021 02:57:30 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Thu, 28 Oct 2021 02:57:36 GMT
RUN set -xe ; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		for server in 			ha.pool.sks-keyservers.net 			pgp.mit.edu 			hkp://p80.pool.sks-keyservers.net:80 			hkp://keyserver.ubuntu.com:80 			keyserver.pgp.com 			ipv4.pool.sks-keyservers.net ; 		do 			if gpg --batch --keyserver "$server" --recv-keys "$key"; then 				break; 			fi; 		done; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	mkdir -p "$TMPDIR" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 28 Oct 2021 02:57:36 GMT
WORKDIR /var/lib/jetty
# Thu, 28 Oct 2021 02:57:38 GMT
COPY multi:6f466bb575b852e6668f47004d8edb31588ff8e21b73080bf09d6ed8d3dcb588 in / 
# Thu, 28 Oct 2021 02:57:38 GMT
USER jetty
# Thu, 28 Oct 2021 02:57:39 GMT
EXPOSE 8080
# Thu, 28 Oct 2021 02:57:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 28 Oct 2021 02:57:41 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:42445708416d90c524044613ca219573cb3b87e3c236ae8642b0e17b341389fb`  
		Last Modified: Thu, 28 Oct 2021 01:45:02 GMT  
		Size: 41.9 MB (41879582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4f9f60b42882cee2f44d430dab6e4bd76aacf43d9e203013dc45e48cfc38eb`  
		Last Modified: Thu, 28 Oct 2021 02:28:51 GMT  
		Size: 14.3 MB (14273910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1ce40e61e1f8464f2fe3066e4712fe7d0e54db14c35a96c036ed408acb907e`  
		Last Modified: Thu, 28 Oct 2021 02:31:04 GMT  
		Size: 186.0 MB (185976782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b44bfbbc542388a8f0a52e4f6233b641ea2fcc9acf4489c5b4190d7e40e5978`  
		Last Modified: Thu, 28 Oct 2021 03:01:56 GMT  
		Size: 9.9 MB (9876708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ef92c708f8197159a3a2262de4cbfbdf94c5b896e1a96b44703e79fa9c0ab4`  
		Last Modified: Thu, 28 Oct 2021 03:01:54 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

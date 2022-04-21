## `jetty:10-jdk17-slim-openjdk`

```console
$ docker pull jetty@sha256:f712513923af6c6d519b5cd761a4b2bcf7bd1bd1fb7cf722a58d5f0a96f8b229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `jetty:10-jdk17-slim-openjdk` - linux; amd64

```console
$ docker pull jetty@sha256:dad2b909f6431b8e8bd2b42b22d28e342a81219b503800b7a520da1ff5d70f28
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232055348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403f9b29c5228aae2013a5e0a8414096c556c7741a4ae4d7ff2130e047cabaff`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:27 GMT
ADD file:8b1e79f91081eb527b455431af58e823d8b84d9d0c8e5c47cb7bda7507954ae4 in / 
# Wed, 20 Apr 2022 04:43:27 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:47:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:51:06 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Wed, 20 Apr 2022 10:51:06 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Apr 2022 10:51:06 GMT
ENV LANG=C.UTF-8
# Wed, 20 Apr 2022 10:51:06 GMT
ENV JAVA_VERSION=17.0.2
# Wed, 20 Apr 2022 10:51:21 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='0022753d0cceecacdd3a795dd4cea2bd7ffdf9dc06e22ffd1be98411742fbb44'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='13bfd976acf8803f862e82c7113fb0e9311ca5458b1decaef8a09ffd91119fa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 20 Apr 2022 10:51:22 GMT
CMD ["jshell"]
# Thu, 21 Apr 2022 01:44:40 GMT
ENV JETTY_VERSION=10.0.9
# Thu, 21 Apr 2022 01:44:40 GMT
ENV JETTY_HOME=/usr/local/jetty
# Thu, 21 Apr 2022 01:44:40 GMT
ENV JETTY_BASE=/var/lib/jetty
# Thu, 21 Apr 2022 01:44:41 GMT
ENV TMPDIR=/tmp/jetty
# Thu, 21 Apr 2022 01:44:41 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Apr 2022 01:44:41 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.9/jetty-home-10.0.9.tar.gz
# Thu, 21 Apr 2022 01:44:41 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Thu, 21 Apr 2022 01:44:58 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Thu, 21 Apr 2022 01:44:58 GMT
WORKDIR /var/lib/jetty
# Thu, 21 Apr 2022 01:44:59 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Thu, 21 Apr 2022 01:44:59 GMT
USER jetty
# Thu, 21 Apr 2022 01:44:59 GMT
EXPOSE 8080
# Thu, 21 Apr 2022 01:44:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 21 Apr 2022 01:44:59 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:1fe172e4850f03bb45d41a20174112bc119fbfec42a650edbbd8491aee32e3c3`  
		Last Modified: Wed, 20 Apr 2022 04:48:27 GMT  
		Size: 31.4 MB (31378979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d3aa8d076675d49d85180b0ced9daef210fe4fdff4bdbb422b9cf384e591d0`  
		Last Modified: Wed, 20 Apr 2022 11:01:25 GMT  
		Size: 1.6 MB (1582162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce99fdf16e86bd02f6ad66a0e1334878528b5a4b5487850a76e0c08a7a27d56`  
		Last Modified: Wed, 20 Apr 2022 11:06:39 GMT  
		Size: 187.9 MB (187900177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a12eae3fc0fbb6aa7e0262acca9270897401ae294c789e576fe745274c920340`  
		Last Modified: Thu, 21 Apr 2022 01:56:26 GMT  
		Size: 11.2 MB (11192589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe5555a961ec8eedfd714ec028b5a04fdf277063f9b97ed3b4f2f3024f41e71`  
		Last Modified: Thu, 21 Apr 2022 01:56:25 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `jetty:10-jdk17-slim-openjdk` - linux; arm64 variant v8

```console
$ docker pull jetty@sha256:253e9fe4c705b182202897114b640c91506b99e0de4231a180d176ad6a29618b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228930564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e051b7bdced743ad4cce0c7709d9d8ab8f9e9e1a98dd852fc4f2ecf44f09a85`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["java","-jar","\/usr\/local\/jetty\/start.jar"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:17 GMT
ADD file:e95289cd39de0f389d09cda9edf8476d5da371bc68d76e820c5e1c310dc54baf in / 
# Tue, 29 Mar 2022 00:43:17 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 01:18:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates p11-kit 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 01:21:25 GMT
ENV JAVA_HOME=/usr/local/openjdk-17
# Tue, 29 Mar 2022 01:21:25 GMT
ENV PATH=/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 01:21:26 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 01:21:27 GMT
ENV JAVA_VERSION=17.0.2
# Tue, 29 Mar 2022 01:21:43 GMT
RUN set -eux; 		arch="$(dpkg --print-architecture)"; 	case "$arch" in 		'amd64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='0022753d0cceecacdd3a795dd4cea2bd7ffdf9dc06e22ffd1be98411742fbb44'; 			;; 		'arm64') 			downloadUrl='https://download.java.net/java/GA/jdk17.0.2/dfd4a8d0985749f896bed50d7138ee7f/8/GPL/openjdk-17.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='13bfd976acf8803f862e82c7113fb0e9311ca5458b1decaef8a09ffd91119fa4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget --progress=dot:giga -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		{ 		echo '#!/usr/bin/env bash'; 		echo 'set -Eeuo pipefail'; 		echo 'trust extract --overwrite --format=java-cacerts --filter=ca-anchors --purpose=server-auth "$JAVA_HOME/lib/security/cacerts"'; 	} > /etc/ca-certificates/update.d/docker-openjdk; 	chmod +x /etc/ca-certificates/update.d/docker-openjdk; 	/etc/ca-certificates/update.d/docker-openjdk; 		find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf; 	ldconfig; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 01:21:43 GMT
CMD ["jshell"]
# Tue, 05 Apr 2022 17:58:35 GMT
ENV JETTY_VERSION=10.0.9
# Tue, 05 Apr 2022 17:58:36 GMT
ENV JETTY_HOME=/usr/local/jetty
# Tue, 05 Apr 2022 17:58:37 GMT
ENV JETTY_BASE=/var/lib/jetty
# Tue, 05 Apr 2022 17:58:38 GMT
ENV TMPDIR=/tmp/jetty
# Tue, 05 Apr 2022 17:58:39 GMT
ENV PATH=/usr/local/jetty/bin:/usr/local/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 17:58:40 GMT
ENV JETTY_TGZ_URL=https://repo1.maven.org/maven2/org/eclipse/jetty/jetty-home/10.0.9/jetty-home-10.0.9.tar.gz
# Tue, 05 Apr 2022 17:58:41 GMT
ENV JETTY_GPG_KEYS=AED5EE6C45D0FE8D5D1B164F27DED4BF6216DB8F 	2A684B57436A81FA8706B53C61C3351A438A3B7D 	5989BAF76217B843D66BE55B2D0E1FB8FE4B68B4 	B59B67FD7904984367F931800818D9D68FB67BAC 	BFBB21C246D7776836287A48A04E0C74ABB35FEA 	8B096546B1A8F02656B15D3B1677D141BCF3584D 	FBA2B18D238AB852DF95745C76157BDF03D0DCD6 	5C9579B3DB2E506429319AAEF33B071B29559E1E 	F254B35617DC255D9344BCFA873A8E86B4372146
# Tue, 05 Apr 2022 17:58:58 GMT
RUN set -xe ; 	export savedAptMark="$(apt-mark showmanual)" ; 	mkdir -p $TMPDIR ; 	apt-get update ; 	apt-get install -y --no-install-recommends 		ca-certificates 		p11-kit 		gnupg 		curl 		; 	export GNUPGHOME=/jetty-keys ; 	mkdir -p "$GNUPGHOME" ; 	for key in $JETTY_GPG_KEYS; do 		gpg --batch --keyserver "hkps://keyserver.ubuntu.com" --recv-keys "$key"; 	done ; 	mkdir -p "$JETTY_HOME" ; 	cd $JETTY_HOME ; 	curl -SL "$JETTY_TGZ_URL" -o jetty.tar.gz ; 	curl -SL "$JETTY_TGZ_URL.asc" -o jetty.tar.gz.asc ; 	gpg --batch --verify jetty.tar.gz.asc jetty.tar.gz ; 	tar -xvf jetty.tar.gz --strip-components=1 ; 	sed -i '/jetty-logging/d' etc/jetty.conf ; 	mkdir -p "$JETTY_BASE" ; 	cd $JETTY_BASE ; 	java -jar "$JETTY_HOME/start.jar" --create-startd 		--add-to-start="server,http,deploy,jsp,jstl,ext,resources,websocket" ; 	groupadd -r jetty && useradd -r -g jetty jetty ; 	chown -R jetty:jetty "$JETTY_HOME" "$JETTY_BASE" "$TMPDIR" ; 	usermod -d $JETTY_BASE jetty ; 	apt-mark auto '.*' > /dev/null ; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null ; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false ; 	rm -rf /var/lib/apt/lists/* ; 	rm -rf /tmp/hsperfdata_root ; 	rm -fr $JETTY_HOME/jetty.tar.gz* ; 	rm -fr /jetty-keys $GNUPGHOME ; 	rm -rf /tmp/hsperfdata_root ; 	java -jar "$JETTY_HOME/start.jar" --list-config ;
# Tue, 05 Apr 2022 17:58:59 GMT
WORKDIR /var/lib/jetty
# Tue, 05 Apr 2022 17:59:01 GMT
COPY multi:a6bf79f83e3ff0c7dc5946cd61ca0413cd3191ce9671725a647923d97a115fae in / 
# Tue, 05 Apr 2022 17:59:01 GMT
USER jetty
# Tue, 05 Apr 2022 17:59:02 GMT
EXPOSE 8080
# Tue, 05 Apr 2022 17:59:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 05 Apr 2022 17:59:04 GMT
CMD ["java" "-jar" "/usr/local/jetty/start.jar"]
```

-	Layers:
	-	`sha256:2203022c5aa978ec114a15a7cdc2c323c65922d3b0a8eab11d50811bb9ae1cfb`  
		Last Modified: Tue, 29 Mar 2022 00:50:04 GMT  
		Size: 30.1 MB (30064311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dee14fdb7a0a09a9e31998d2906081734dba985b95da3f35b7bd79d79b73330`  
		Last Modified: Tue, 29 Mar 2022 01:37:54 GMT  
		Size: 1.4 MB (1361189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175d442985953956c6a8aadc00682f2f4468d782eafeca5eee97cceed189c2c3`  
		Last Modified: Tue, 29 Mar 2022 01:42:03 GMT  
		Size: 186.5 MB (186527583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e02ade983e8975d236991e2b70fab290415cfbb15ea175610a8f268d0ab69f4`  
		Last Modified: Tue, 05 Apr 2022 18:24:47 GMT  
		Size: 11.0 MB (10976040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d1d8c2811c46d05125899fc6470cf9014fd8876c5b1c23a757fcca221ba0e7`  
		Last Modified: Tue, 05 Apr 2022 18:24:46 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

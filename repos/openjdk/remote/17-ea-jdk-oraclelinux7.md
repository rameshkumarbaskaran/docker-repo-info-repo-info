## `openjdk:17-ea-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:5457bbce3cce4e1e5c00037b8b425873af5e95ea38a8f2303ec974005f8751a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:17-ea-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:782ae62de1fdd884a4c8562814490df8ab5a8308f84b9f842bafa8126fb99688
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 MB (250859469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e80ad85db53bf01b90fa93c6d047de2d7f345f80085cc4c28b7ca27ce9d76b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 17 Jun 2021 16:51:20 GMT
ADD file:46efe0cb70a1c4f574c3b3e1fb9b9733930d246bb8077c4ec2160a840697e6c8 in / 
# Thu, 17 Jun 2021 16:51:21 GMT
CMD ["/bin/bash"]
# Thu, 17 Jun 2021 17:08:18 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 17 Jun 2021 17:08:51 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Thu, 17 Jun 2021 17:08:51 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Jun 2021 17:08:52 GMT
ENV LANG=en_US.UTF-8
# Tue, 22 Jun 2021 21:40:07 GMT
ENV JAVA_VERSION=17-ea+27
# Tue, 22 Jun 2021 21:40:17 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/27/GPL/openjdk-17-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='7e1042e3daf741aad75ebda0ea38650111475a810be8fedf38f554732d7750f4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/27/GPL/openjdk-17-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='88bdeb49442e85c19e126b720bd810bc59007973c6fc06aa6e62b609c1c44d53'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 22 Jun 2021 21:40:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7627bfb99533146fcb8374f557bc24c36505fb2ee8578ec6072a821200247bbb`  
		Last Modified: Thu, 17 Jun 2021 16:52:21 GMT  
		Size: 48.3 MB (48260810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb70fb8946cabfaff2f43cee5915a69ad662b0294e9c91d8f545898e92ed32fd`  
		Last Modified: Thu, 17 Jun 2021 17:14:39 GMT  
		Size: 15.4 MB (15426613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9133223aec0e60d5a315bc2210e4f849bf2a142fd0cf8432fcab330e4fb151`  
		Last Modified: Tue, 22 Jun 2021 21:50:02 GMT  
		Size: 187.2 MB (187172046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-ea-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0de44afb08cea8855e5bd88544bee7d8ef1bc2a5e84f0ae40bc9270acb29c6a6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.3 MB (251258482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b502846ec13aaad0825c3574251b4ff10aaaa97d4f56b4f14d94f5305348d828`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 17 Jun 2021 16:51:08 GMT
ADD file:256f7e1c19fbbacd7c7650e1e9991f3617703ba349f259624d78e4393e945665 in / 
# Thu, 17 Jun 2021 16:51:08 GMT
CMD ["/bin/bash"]
# Thu, 17 Jun 2021 17:08:43 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 17 Jun 2021 17:10:00 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Thu, 17 Jun 2021 17:10:00 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Jun 2021 17:10:00 GMT
ENV LANG=en_US.UTF-8
# Tue, 22 Jun 2021 21:58:55 GMT
ENV JAVA_VERSION=17-ea+27
# Tue, 22 Jun 2021 21:59:11 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/27/GPL/openjdk-17-ea+27_linux-x64_bin.tar.gz'; 			downloadSha256='7e1042e3daf741aad75ebda0ea38650111475a810be8fedf38f554732d7750f4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/27/GPL/openjdk-17-ea+27_linux-aarch64_bin.tar.gz'; 			downloadSha256='88bdeb49442e85c19e126b720bd810bc59007973c6fc06aa6e62b609c1c44d53'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 22 Jun 2021 21:59:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9a3d615f016c21e1c5fef521352cdd990a61abfd09a26d7124c61e33b2cab56a`  
		Last Modified: Thu, 17 Jun 2021 16:52:10 GMT  
		Size: 48.9 MB (48858581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b4a33d75d2c35cdf1c0dc42b99124399c0375b12141be4bddb4b819732453cb`  
		Last Modified: Thu, 17 Jun 2021 17:23:33 GMT  
		Size: 16.4 MB (16419706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a534b066360103c8aec52d489b992d52cb18216b5a547bd8e67fe3a893eeeb39`  
		Last Modified: Tue, 22 Jun 2021 22:14:53 GMT  
		Size: 186.0 MB (185980195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `openjdk:16-oraclelinux7`

```console
$ docker pull openjdk@sha256:00f41eb4d3bca497ce8a9e2d736dae3fb9e71bba324c16c15e26bc3d65f1870c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:16-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:ed99b8ae52ba669e9b883232e58b001380899400d833a0b4e2669b5a848a4306
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 MB (248466186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24d99308f1d021fed54bdb0ac2bcf7dfcf453d9e429510cf7d150baedea02a01`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Mar 2021 00:21:32 GMT
ADD file:837f2bca2cab135736ad43644356710dcac6516fdfc2023d239d157d1fa4ba7c in / 
# Wed, 17 Mar 2021 00:21:32 GMT
CMD ["/bin/bash"]
# Wed, 17 Mar 2021 00:38:33 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 17 Mar 2021 00:39:40 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Wed, 17 Mar 2021 00:39:41 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Mar 2021 00:39:41 GMT
ENV LANG=en_US.UTF-8
# Wed, 17 Mar 2021 00:39:41 GMT
ENV JAVA_VERSION=16
# Wed, 17 Mar 2021 00:40:11 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk16/7863447f0ab643c585b9bdebf67c69db/36/GPL/openjdk-16_linux-x64_bin.tar.gz'; 			downloadSha256='e952958f16797ad7dc7cd8b724edd69ec7e0e0434537d80d6b5165193e33b931'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk16/7863447f0ab643c585b9bdebf67c69db/36/GPL/openjdk-16_linux-aarch64_bin.tar.gz'; 			downloadSha256='273d3ae0ff14af801c5ffa71fd081f1cc505354f308ce11c77af55302c83d2bf'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 17 Mar 2021 00:40:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:401a42e1eb4fe87d89990847d6ef97767b5ac57457c8001203ee2ea137736907`  
		Last Modified: Wed, 17 Mar 2021 00:22:34 GMT  
		Size: 48.3 MB (48263709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f752366003eed4ac964ebb4be3453e3f19d854828f4f50ff708900bb4c42924`  
		Last Modified: Wed, 17 Mar 2021 00:45:21 GMT  
		Size: 15.4 MB (15429957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1732f8e5f3a680df1c8cbe1b117b74c444eb60ec303806ee41a127a82bd7b921`  
		Last Modified: Wed, 17 Mar 2021 00:46:27 GMT  
		Size: 184.8 MB (184772520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:53b53beb4c222ec0c5462a83abdfb5fcbf7d66e9728c07c76b664608683bb3cc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244468303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ac814122e3cb68a91903accaea8e098d46913ca80afb44d70d7b8f82c7a8b9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 12 Feb 2021 01:00:40 GMT
ADD file:25b64ec41b7ca742c671c416e08a7bee3224e4052650624ef31b5583b1c412df in / 
# Fri, 12 Feb 2021 01:00:41 GMT
CMD ["/bin/bash"]
# Fri, 12 Feb 2021 01:19:33 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 12 Feb 2021 01:20:59 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Fri, 12 Feb 2021 01:21:00 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Feb 2021 01:21:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 12 Feb 2021 01:21:01 GMT
ENV JAVA_VERSION=16
# Fri, 12 Feb 2021 23:46:52 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk16/7863447f0ab643c585b9bdebf67c69db/36/GPL/openjdk-16_linux-x64_bin.tar.gz'; 			downloadSha256='e952958f16797ad7dc7cd8b724edd69ec7e0e0434537d80d6b5165193e33b931'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk16/7863447f0ab643c585b9bdebf67c69db/36/GPL/openjdk-16_linux-aarch64_bin.tar.gz'; 			downloadSha256='273d3ae0ff14af801c5ffa71fd081f1cc505354f308ce11c77af55302c83d2bf'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 12 Feb 2021 23:46:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:da6ef06bd6983a3815530ecb4b6d3bcef6c011f03daa80be12f60c382e0c23e9`  
		Last Modified: Fri, 12 Feb 2021 01:01:42 GMT  
		Size: 48.9 MB (48854102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2cbabffc67d7d6521300614c7fd34cc6a54a4697d98c388898fc060b0f77d3`  
		Last Modified: Fri, 12 Feb 2021 01:26:00 GMT  
		Size: 16.5 MB (16465019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2658c85e5c0dd06c2bddcebe2cd9323d9894b58d578db1074348b620d9f531`  
		Last Modified: Fri, 12 Feb 2021 23:54:10 GMT  
		Size: 179.1 MB (179149182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

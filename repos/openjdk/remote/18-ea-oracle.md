## `openjdk:18-ea-oracle`

```console
$ docker pull openjdk@sha256:2261965eb21c8d5b8140f9736a66d1059bb2aad89f61cffc6426c0eb2d84a449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-ea-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:945721339060f2e747ccafa82da2c77f9d9a8dbc278333e411af91c303640aba
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243656373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e08365f5b2f6efae41b301bb4eb7e1162c53f7081c205bd00edc5e4b36544383`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 03 Nov 2021 22:20:09 GMT
ADD file:ee2c184d933cfe1848f54f94d92f5c14d073160b62ec403259b18392d4ec6e1b in / 
# Wed, 03 Nov 2021 22:20:10 GMT
CMD ["/bin/bash"]
# Wed, 03 Nov 2021 22:37:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 03 Nov 2021 22:37:07 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Wed, 03 Nov 2021 22:37:07 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Nov 2021 22:37:07 GMT
ENV LANG=C.UTF-8
# Fri, 12 Nov 2021 00:20:00 GMT
ENV JAVA_VERSION=18-ea+23
# Fri, 12 Nov 2021 00:20:12 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/23/GPL/openjdk-18-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='e9f310e519b12280fc023ab4b734e533377e212ae77da8981f462c2849851316'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/23/GPL/openjdk-18-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='11b235ab4e5dc79031e5c08593080c58ec66b96b530e023e5c789b040d0095a3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 12 Nov 2021 00:20:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0a6167eaa66c8f2dc1c8dbed1a335f3d4052409454c9f7fbcd8fc35d8576a7e2`  
		Last Modified: Wed, 03 Nov 2021 22:21:16 GMT  
		Size: 42.0 MB (41968115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a88dabbf57eeb24f57debafeba0a2f7b2f4e4e76d1aa9a3bd27edf0682e0f15`  
		Last Modified: Wed, 03 Nov 2021 22:43:12 GMT  
		Size: 13.5 MB (13491241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdbf78086c0903c7a7d8cd82882740071f6094d0f5b54eee270bcbbecb919f5`  
		Last Modified: Fri, 12 Nov 2021 00:27:23 GMT  
		Size: 188.2 MB (188197017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-ea-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2a8fa2dc7aefe403176754aba789bbf4c1d8e44d9c44b7caa8f4a535f3228b9f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243435930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6f1ffeac55988ad3f47890ff834fe612c02e41fe80424425f3a63774738987`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Nov 2021 08:24:53 GMT
ADD file:98b355b05026edaab234cff8ee34d8335b233cbaa04a19ac82df4a2b0c7fdc4d in / 
# Thu, 18 Nov 2021 08:24:54 GMT
CMD ["/bin/bash"]
# Thu, 18 Nov 2021 10:14:56 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 18 Nov 2021 10:14:57 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Thu, 18 Nov 2021 10:14:58 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 10:14:59 GMT
ENV LANG=C.UTF-8
# Thu, 18 Nov 2021 10:15:00 GMT
ENV JAVA_VERSION=18-ea+23
# Thu, 18 Nov 2021 10:15:11 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/23/GPL/openjdk-18-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='e9f310e519b12280fc023ab4b734e533377e212ae77da8981f462c2849851316'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/23/GPL/openjdk-18-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='11b235ab4e5dc79031e5c08593080c58ec66b96b530e023e5c789b040d0095a3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 18 Nov 2021 10:15:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1bdb3a9e404c972ab03f65fd56b5b815b51d6a68324015dc69707d48e2ba3cdf`  
		Last Modified: Thu, 18 Nov 2021 08:26:02 GMT  
		Size: 42.0 MB (42010198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9356b5c0bb88b90b52af9c2836e152e11b910a0e88807e8327df1e2a965a7d1`  
		Last Modified: Thu, 18 Nov 2021 10:27:05 GMT  
		Size: 14.3 MB (14300065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ef24cabbf88317b7f8d03e6274850f4c3806362ffed88512f6703824acbb0e`  
		Last Modified: Thu, 18 Nov 2021 10:27:21 GMT  
		Size: 187.1 MB (187125667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

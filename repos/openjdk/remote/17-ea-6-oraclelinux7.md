## `openjdk:17-ea-6-oraclelinux7`

```console
$ docker pull openjdk@sha256:760c0146fa04688bedd3da8f3507669b1422dd563e5640adb1a00cb0f55ac49b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:17-ea-6-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:4b3678241472faa476204ba7da2af91861acde5f2707f004ca5fd4a52a576555
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.3 MB (249349671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc8bffe47d8ad95e99d721a7ef60ed188263675d91f386a2093697ac774a9c9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Jan 2021 00:31:31 GMT
ADD file:dee09ad1ed4e7359b14fabc84890b1fb687ad4efe75f7c4800c0a907fd4f70a3 in / 
# Fri, 15 Jan 2021 00:31:32 GMT
CMD ["/bin/bash"]
# Fri, 15 Jan 2021 00:58:14 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 15 Jan 2021 00:58:14 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 Jan 2021 00:58:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Fri, 15 Jan 2021 00:58:15 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Jan 2021 01:21:59 GMT
ENV JAVA_VERSION=17-ea+6
# Sat, 23 Jan 2021 01:22:13 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk17/6/GPL/openjdk-17-ea+6_linux-aarch64_bin.tar.gz; 			downloadSha256=fc7ad87123841b528112c6fa94883b28dc3bb0ea174d3a3795fe2c2873a68f6f; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk17/6/GPL/openjdk-17-ea+6_linux-x64_bin.tar.gz; 			downloadSha256=f9082a010d2be7b1a1b462d86345d797f311bde30ddf2ccefe7e718ec49de334; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 23 Jan 2021 01:22:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:980316e412373040bc280150078ae453b259ece36b750a0a9b6f4c99751ce4f9`  
		Last Modified: Wed, 06 Jan 2021 20:24:02 GMT  
		Size: 48.3 MB (48260808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7699f318b6b854fb950c083e0fed757fff0549df020432861c6b50802ec82b2`  
		Last Modified: Fri, 15 Jan 2021 01:09:18 GMT  
		Size: 15.4 MB (15431689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac1da8318c444d3d8ebcfb47cbf8e789f84b78a9f262c0c9b3f31e7112cfbe0`  
		Last Modified: Sat, 23 Jan 2021 01:30:05 GMT  
		Size: 185.7 MB (185657174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-ea-6-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:55df098e4b6c77c9e5f7b09c5ed0bae1033459130bd1feae727a0e09fcaf0881
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.4 MB (245356566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df01beed5c8eb9ac39d9c0419fca650f15fc5512490e041b841ff29a6b20bb64`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Jan 2021 00:06:30 GMT
ADD file:d4d5ffcc8d57e27f8de10063c4e347d2f4da299f62166d6f6387a7714f5e0f06 in / 
# Fri, 15 Jan 2021 00:06:33 GMT
CMD ["/bin/bash"]
# Fri, 15 Jan 2021 00:45:52 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 15 Jan 2021 00:45:53 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 Jan 2021 00:45:54 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Fri, 15 Jan 2021 00:45:55 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Jan 2021 01:42:34 GMT
ENV JAVA_VERSION=17-ea+6
# Sat, 23 Jan 2021 01:43:27 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk17/6/GPL/openjdk-17-ea+6_linux-aarch64_bin.tar.gz; 			downloadSha256=fc7ad87123841b528112c6fa94883b28dc3bb0ea174d3a3795fe2c2873a68f6f; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk17/6/GPL/openjdk-17-ea+6_linux-x64_bin.tar.gz; 			downloadSha256=f9082a010d2be7b1a1b462d86345d797f311bde30ddf2ccefe7e718ec49de334; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 23 Jan 2021 01:43:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e2e87614faabf530f11811ae8eb1be9e586d5d923036268129a39eae319cb772`  
		Last Modified: Wed, 06 Jan 2021 20:47:54 GMT  
		Size: 48.9 MB (48858154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458e99ea3b1687330632146091a5677b179fe906820e2d98ad7b5becbcb526c1`  
		Last Modified: Fri, 15 Jan 2021 00:56:17 GMT  
		Size: 16.5 MB (16470870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d7827b7bea93c17dd31c8f6262a80bc064319730ef0174eef4f8af4f0ea883`  
		Last Modified: Sat, 23 Jan 2021 01:52:55 GMT  
		Size: 180.0 MB (180027542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

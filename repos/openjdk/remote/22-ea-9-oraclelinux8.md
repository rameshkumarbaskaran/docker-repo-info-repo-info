## `openjdk:22-ea-9-oraclelinux8`

```console
$ docker pull openjdk@sha256:3262a24414a9ce536b86ae9be280ab1405ad755f4203c376f24aab5a000c6126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-9-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:359ca59a01f1f1e7facff78481eaa6e28763351350cd859ef0e7e54a003ad043
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264784674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d02faaa090684cc7d705b850f646b632174b864429da6cb3459216974707081b`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 22 Jul 2023 01:20:32 GMT
ADD file:6d43f7bf7c8d8c056e6fcc566ccfa2c1e42be1ef095f94d6780d0ca7d9a02e6e in / 
# Sat, 22 Jul 2023 01:20:32 GMT
CMD ["/bin/bash"]
# Sat, 22 Jul 2023 01:40:55 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Sat, 22 Jul 2023 01:40:55 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Sat, 22 Jul 2023 01:40:55 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 22 Jul 2023 01:40:55 GMT
ENV LANG=C.UTF-8
# Fri, 04 Aug 2023 00:28:05 GMT
ENV JAVA_VERSION=22-ea+9
# Fri, 04 Aug 2023 00:28:18 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/9/GPL/openjdk-22-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='dd11f0f96ed6992b56452eee0683b50f1b550f74c31fb39e1eb1ff8a232caf68'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/9/GPL/openjdk-22-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='47ab1fb3cbe8174c21e10880e5de0c60d754cf5ba6d5cdfbe1a1d91b53b193bc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 04 Aug 2023 00:28:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:49bb46380f8cb3491e82d000b27a6eb26b2490291da814ce3363bbf2c8baeb1a`  
		Last Modified: Sat, 22 Jul 2023 01:21:47 GMT  
		Size: 44.9 MB (44915006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938c78e257f8d32905a5685feaf98c164b8091b3f15fb7705c4181bd3998b783`  
		Last Modified: Sat, 22 Jul 2023 01:42:50 GMT  
		Size: 15.0 MB (15009045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8760bdae2d23c39ca224829a1f6a3c23ad77b9dbb807708a97cf9ae6512bf5a7`  
		Last Modified: Fri, 04 Aug 2023 00:32:36 GMT  
		Size: 204.9 MB (204860623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-9-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:fe50740cfe6a1af06ba8eee57a9cf78c9a9a37fb06292b7fc3ac684fa248986b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.5 MB (262476343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63353369e5b2292a87888b98b18b632566392a7d203cd3ddc440363d9a5f88ce`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 22 Jul 2023 01:03:33 GMT
ADD file:49b1f7f2b2558f78918f26b488622ad08fa607583d0a45f4f116773e2c13cf96 in / 
# Sat, 22 Jul 2023 01:03:34 GMT
CMD ["/bin/bash"]
# Sat, 22 Jul 2023 01:23:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Sat, 22 Jul 2023 01:23:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Sat, 22 Jul 2023 01:23:12 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 22 Jul 2023 01:23:12 GMT
ENV LANG=C.UTF-8
# Fri, 04 Aug 2023 00:57:34 GMT
ENV JAVA_VERSION=22-ea+9
# Fri, 04 Aug 2023 00:57:44 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/9/GPL/openjdk-22-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='dd11f0f96ed6992b56452eee0683b50f1b550f74c31fb39e1eb1ff8a232caf68'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/9/GPL/openjdk-22-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='47ab1fb3cbe8174c21e10880e5de0c60d754cf5ba6d5cdfbe1a1d91b53b193bc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 04 Aug 2023 00:57:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1817bc1e6309503caf2242a5c83a4a6e9ebfdfb378d39bc92607690883a98c66`  
		Last Modified: Sat, 22 Jul 2023 01:04:31 GMT  
		Size: 43.6 MB (43623755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87786d2b4c93ec23e4ce18586fdf1f0c0ea5f810fe7a6ea02a197bf01bc37f7`  
		Last Modified: Sat, 22 Jul 2023 01:24:59 GMT  
		Size: 15.7 MB (15670540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e9da7a8b25911f00c5e89b81efd84c88aeaf7c868519c6d39cb6620b9f715`  
		Last Modified: Fri, 04 Aug 2023 01:02:08 GMT  
		Size: 203.2 MB (203182048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

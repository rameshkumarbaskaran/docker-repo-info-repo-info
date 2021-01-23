## `openjdk:16-ea-oracle`

```console
$ docker pull openjdk@sha256:50d6d6906bc2f427ef0bb35e779f3c2828a810969148dbc573a777d532406a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:16-ea-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:c2c73f853631a7f914a352f188eeb7a5bdfd62e25819d51db7e0fd40f499e441
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240112253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab5025baebc07449ac19d4c0894ea7fc6a603d1bc1d51aff7b4509d840d16ad`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Jan 2021 00:30:38 GMT
ADD file:2987f8143a9c4f758731c17e307a6c7ca9e5e1a974df3405a17d2699da7d8351 in / 
# Fri, 15 Jan 2021 00:30:39 GMT
CMD ["/bin/bash"]
# Fri, 15 Jan 2021 00:56:52 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 15 Jan 2021 00:56:53 GMT
ENV LANG=C.UTF-8
# Fri, 15 Jan 2021 00:59:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Fri, 15 Jan 2021 00:59:09 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Jan 2021 01:23:02 GMT
ENV JAVA_VERSION=16-ea+33
# Sat, 23 Jan 2021 01:24:00 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/33/GPL/openjdk-16-ea+33_linux-aarch64_bin.tar.gz; 			downloadSha256=1da1b96306a0ede9e1c7b4284772b5de3c9f8f08f895e082f561f5f3c86ea3be; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/33/GPL/openjdk-16-ea+33_linux-x64_bin.tar.gz; 			downloadSha256=ba2ac6ccca898cd63090d768b89a95fba76b6303a55c41e851d75dd0c5afcee8; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 23 Jan 2021 01:24:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a73adebe9317092fb1f120a1d0d21f460296e9bde7ac683fd452cfc628c528cf`  
		Last Modified: Wed, 06 Jan 2021 20:23:26 GMT  
		Size: 42.1 MB (42069921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b73bcd34cfec7fc27d7cd00bc22af06df0471526a6d2ceb8e77391a82f300f0`  
		Last Modified: Fri, 15 Jan 2021 01:08:29 GMT  
		Size: 13.3 MB (13277589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f070b002d4e996ca4a83633cb288926fc647b73a5780b943ea710f611cf888`  
		Last Modified: Sat, 23 Jan 2021 01:31:47 GMT  
		Size: 184.8 MB (184764743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-ea-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:72c81411f0242bafa2c1cd50cb06248fc30b3f0a7fa0927ad9b9119c3979da18
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235185778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50b6e23708d243d805ae1b19164820795b4536f006df678f6a68e91b0360a54`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Jan 2021 00:05:48 GMT
ADD file:ad2b2ddca8e17229cc8d1380ecda32c4b2c04f1e2aed8f493f745c6352b34e60 in / 
# Fri, 15 Jan 2021 00:05:49 GMT
CMD ["/bin/bash"]
# Fri, 15 Jan 2021 00:43:36 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 15 Jan 2021 00:43:38 GMT
ENV LANG=C.UTF-8
# Fri, 15 Jan 2021 00:46:48 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Fri, 15 Jan 2021 00:46:49 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Jan 2021 01:44:51 GMT
ENV JAVA_VERSION=16-ea+33
# Sat, 23 Jan 2021 01:45:38 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/33/GPL/openjdk-16-ea+33_linux-aarch64_bin.tar.gz; 			downloadSha256=1da1b96306a0ede9e1c7b4284772b5de3c9f8f08f895e082f561f5f3c86ea3be; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/33/GPL/openjdk-16-ea+33_linux-x64_bin.tar.gz; 			downloadSha256=ba2ac6ccca898cd63090d768b89a95fba76b6303a55c41e851d75dd0c5afcee8; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 23 Jan 2021 01:45:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d0eecbd2c3e7306adbf5b4a0d9bebc7d266ebe78bda044d35b0994c1cf655a54`  
		Last Modified: Wed, 06 Jan 2021 20:47:00 GMT  
		Size: 42.0 MB (41996293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8f86f1d6521cdc8416801b8dd0b15d9a5a85bfa3eb8f9afa832aa8cc652732`  
		Last Modified: Fri, 15 Jan 2021 00:55:15 GMT  
		Size: 14.1 MB (14057398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c96277d32175932acb90c97a824e0125c8ab8a399c98ee2f934393d3454835a`  
		Last Modified: Sat, 23 Jan 2021 01:54:55 GMT  
		Size: 179.1 MB (179132087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

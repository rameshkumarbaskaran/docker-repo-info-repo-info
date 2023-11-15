## `openjdk:22-oraclelinux8`

```console
$ docker pull openjdk@sha256:e580c6d6699ca207bb09f1a0580538369b66bf4caad9aa93803ca4c3c4cbfc1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:7cc6c27ac7158d8eaf704ae6361867a6b31ef4a839fce482fb75336a199cfb6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.4 MB (264421341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee98c271db44dd47d7a3047146809b397bfdfbae94fc60f2d9ef23c60254dd1`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Oct 2023 18:27:20 GMT
ADD file:0f45bdf93b14a2ab9389b71d23b6c7f6d2935c8016e3b6422814f8fc79bef986 in / 
# Fri, 20 Oct 2023 18:27:20 GMT
CMD ["/bin/bash"]
# Fri, 20 Oct 2023 18:45:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 20 Oct 2023 18:45:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 20 Oct 2023 18:45:06 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Oct 2023 18:45:06 GMT
ENV LANG=C.UTF-8
# Wed, 15 Nov 2023 05:27:29 GMT
ENV JAVA_VERSION=22-ea+23
# Wed, 15 Nov 2023 05:27:44 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/23/GPL/openjdk-22-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='fd781d8f07801adbe2c55425b595cf97d4652de7f27a56d90a5daabd8d899a22'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/23/GPL/openjdk-22-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5480254852c4d9b56987eab704922c5174895ef4b11407a0e79c887bf89ffe24'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 15 Nov 2023 05:27:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8e0176adc18c476bdfcc701f01cda5acf49bc8e6d7fadac8072091a43fafbb25`  
		Last Modified: Fri, 20 Oct 2023 18:28:56 GMT  
		Size: 44.3 MB (44279620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7fcefe71b24cef619772a3adab6474d1dee79d5ec55a8ac900504be9b669d3`  
		Last Modified: Fri, 20 Oct 2023 18:46:04 GMT  
		Size: 15.0 MB (15016123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab735ccd038eb0bbfd7a706529a9eaa6bf93e96cb17ffe44eb5e29486f3a595a`  
		Last Modified: Wed, 15 Nov 2023 05:30:14 GMT  
		Size: 205.1 MB (205125598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5553d5af16ea10508906049f32254c6d30ad28c3828b27515ad4e89883531f3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262671200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2da2f999c9b36c81269122bb65c2ed2d7917bbf5da6a47c5f5951a6e4089567e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Oct 2023 18:39:12 GMT
ADD file:e189ba41c54c386435a3292026b75a1386976d3222102c16a725f58f594f284e in / 
# Fri, 20 Oct 2023 18:39:12 GMT
CMD ["/bin/bash"]
# Fri, 20 Oct 2023 19:20:37 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 20 Oct 2023 19:20:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 20 Oct 2023 19:20:38 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Oct 2023 19:20:38 GMT
ENV LANG=C.UTF-8
# Wed, 15 Nov 2023 01:53:55 GMT
ENV JAVA_VERSION=22-ea+23
# Wed, 15 Nov 2023 01:54:19 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/23/GPL/openjdk-22-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='fd781d8f07801adbe2c55425b595cf97d4652de7f27a56d90a5daabd8d899a22'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/23/GPL/openjdk-22-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='5480254852c4d9b56987eab704922c5174895ef4b11407a0e79c887bf89ffe24'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 15 Nov 2023 01:54:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e39ec8f010eb75816ae2c21b014f7fdecffb48374079b6f1bce017214e2a45cd`  
		Last Modified: Fri, 20 Oct 2023 18:40:29 GMT  
		Size: 43.7 MB (43672784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4910a471f6760b5f0bc0ef155e7afd624a4c1ea6f09bb680d43c1041cfd4fd`  
		Last Modified: Fri, 20 Oct 2023 19:21:34 GMT  
		Size: 15.7 MB (15660393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675a151cd5f5435a340e3b099b2dc93eefd64bb635c67030bd031929ab0a41a6`  
		Last Modified: Wed, 15 Nov 2023 01:57:56 GMT  
		Size: 203.3 MB (203338023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `openjdk:21-ea-oracle`

```console
$ docker pull openjdk@sha256:4a808477c34648997aff1cc99677345bcb0ee6a29547cd7fd26c2d6dd6c9f08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-ea-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:606c11db1dd23c1113db7ddef8f34ead09fe5c22fb3cf3c6ecd376ab116fd547
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259104581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3703db29b56f6f67040d1a3250dfa432edd8502d94bf8b09b06aec9fc30e7d61`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Mar 2023 20:22:31 GMT
ADD file:eca2b657866c594c67fc9041ad2a4a309e62fc8338add46c3917517649f748b2 in / 
# Wed, 08 Mar 2023 20:22:32 GMT
CMD ["/bin/bash"]
# Wed, 08 Mar 2023 20:53:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 08 Mar 2023 20:53:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Wed, 08 Mar 2023 20:53:15 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Mar 2023 20:53:15 GMT
ENV LANG=C.UTF-8
# Thu, 09 Mar 2023 23:26:37 GMT
ENV JAVA_VERSION=21-ea+13
# Thu, 09 Mar 2023 23:26:47 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/13/GPL/openjdk-21-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='bc6ffa91e66ea5507449ce61cc7b7090d94f844bdd1eb531b6796f4d017f93bc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/13/GPL/openjdk-21-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='47f8c074276fdfa3705653b0d8beba18bfc8e684762dd6a5b37d03c6b1db9632'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 09 Mar 2023 23:26:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:767a87c583278931a33db59dc8586fdcfa03c53a801cce573f0e861c31ec4c89`  
		Last Modified: Wed, 08 Mar 2023 20:24:06 GMT  
		Size: 44.6 MB (44557814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5754d31dea44245a0029d262dade1fe4e14228c7182d3efde4994c6a76398bc7`  
		Last Modified: Wed, 08 Mar 2023 20:56:42 GMT  
		Size: 15.0 MB (15014167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9551782366d368f77ddaf0255a532609f35a7f999e8609a1fb9f4bd1b85dd5`  
		Last Modified: Thu, 09 Mar 2023 23:29:54 GMT  
		Size: 199.5 MB (199532600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:06e7697a44a403c2dd867560f5aededc622a9d7ee2dfe3b4420c858c7b2f33ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 MB (257324509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607570c983166c7aee0cd8caf088be8c3237414ff90a61f0799915019f0dc2bc`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Mar 2023 21:02:19 GMT
ADD file:18f4bd510f88f32e538884e4e633449c2c8dbf8a5f88b6b6b165ab05872d9507 in / 
# Wed, 08 Mar 2023 21:02:19 GMT
CMD ["/bin/bash"]
# Wed, 08 Mar 2023 21:19:53 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 08 Mar 2023 21:19:53 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Wed, 08 Mar 2023 21:19:53 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Mar 2023 21:19:53 GMT
ENV LANG=C.UTF-8
# Thu, 09 Mar 2023 22:46:50 GMT
ENV JAVA_VERSION=21-ea+13
# Thu, 09 Mar 2023 22:47:05 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/13/GPL/openjdk-21-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='bc6ffa91e66ea5507449ce61cc7b7090d94f844bdd1eb531b6796f4d017f93bc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/13/GPL/openjdk-21-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='47f8c074276fdfa3705653b0d8beba18bfc8e684762dd6a5b37d03c6b1db9632'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 09 Mar 2023 22:47:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8ff0c9d62930fe3f55e00ba3be2db6be3643b07da9804d1c9b83b0d3181f0df5`  
		Last Modified: Wed, 08 Mar 2023 21:03:40 GMT  
		Size: 43.5 MB (43456139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec39ece690c19b75d657ca26bf156e883914c8bea4948e081819aff289dc43c5`  
		Last Modified: Wed, 08 Mar 2023 21:22:51 GMT  
		Size: 15.8 MB (15834481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76425c57a0e09b88ba6297cb4ea7e9df7d1e2a0e0134168030482f6eb2eaebc`  
		Last Modified: Thu, 09 Mar 2023 22:50:25 GMT  
		Size: 198.0 MB (198033889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `openjdk:21-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:4de19f05462e7c52d5be908377208a8003d74691f4965bb6065d9733d36b78f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:cf21dd7e95f31e346457e94a37fee76d2fcca7998e805f7f276320dd50e9c4cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 MB (261152969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de17652cd1a7613ec3d0d72a2298bc8ce7ab1370f9e622770f1034e1bebce380`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 22 Mar 2023 23:55:20 GMT
ADD file:1a06059b1a097ecc61cb02965fc90e00183a8653d9ae009965823226559c5be9 in / 
# Wed, 22 Mar 2023 23:55:20 GMT
CMD ["/bin/bash"]
# Thu, 23 Mar 2023 00:15:05 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 23 Mar 2023 00:15:05 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Thu, 23 Mar 2023 00:15:05 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Mar 2023 00:15:05 GMT
ENV LANG=C.UTF-8
# Tue, 28 Mar 2023 01:03:15 GMT
ENV JAVA_VERSION=21-ea+15
# Tue, 28 Mar 2023 01:03:27 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/15/GPL/openjdk-21-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='0fec1002b8c8975b181bd6966a817028d6b373cbc759254231f9b96db1fe6edd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/15/GPL/openjdk-21-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='93cc1eb6202093a127f1f9ed2e866a51dff29321f878085c18f317cefb113ffc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 28 Mar 2023 01:03:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ab8798141d463c224f18fa5dd1d249b554dda61be24da7aa516e4e2de324db76`  
		Last Modified: Wed, 22 Mar 2023 23:56:08 GMT  
		Size: 44.6 MB (44563376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363fdaa54a1583c24462f316031891a2beb8144c7ccd8851f6b6a8869b86ed3b`  
		Last Modified: Thu, 23 Mar 2023 00:15:51 GMT  
		Size: 15.0 MB (15018388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81409df49124fb9bfb3c4db9feed8d0c63da055a4b723d743918d2e0ff308af3`  
		Last Modified: Tue, 28 Mar 2023 01:05:29 GMT  
		Size: 201.6 MB (201571205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8473039b7c2ba0e3e7ee6225b37a5062ba14bd949fa4e335688cfbccbd4f0245
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.3 MB (259328852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b6f4eed7220907963e1cedef695e65aaec03af3f0eb813a2ca2406456aabd7`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 22 Mar 2023 23:59:36 GMT
ADD file:b4a46acde2a8ffdb8874f11aadcfc90177b15422278a1b8fa87e7ed9c97cf2a4 in / 
# Wed, 22 Mar 2023 23:59:36 GMT
CMD ["/bin/bash"]
# Thu, 23 Mar 2023 00:23:23 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 23 Mar 2023 00:23:24 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Thu, 23 Mar 2023 00:23:24 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Mar 2023 00:23:24 GMT
ENV LANG=C.UTF-8
# Mon, 27 Mar 2023 22:47:17 GMT
ENV JAVA_VERSION=21-ea+15
# Mon, 27 Mar 2023 22:47:29 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/15/GPL/openjdk-21-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='0fec1002b8c8975b181bd6966a817028d6b373cbc759254231f9b96db1fe6edd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/15/GPL/openjdk-21-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='93cc1eb6202093a127f1f9ed2e866a51dff29321f878085c18f317cefb113ffc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 27 Mar 2023 22:47:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:40ffb7074955cd4f083dfcadee0a1ef1e12dbe031bdf2325c8bae38711b1f70f`  
		Last Modified: Thu, 23 Mar 2023 00:00:22 GMT  
		Size: 43.5 MB (43460037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dafbc18f0b64482aa39e4830fa399092a7a9f9a39c37c154966aa80bef2ece45`  
		Last Modified: Thu, 23 Mar 2023 00:24:08 GMT  
		Size: 15.8 MB (15834377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040306b2243af2d0f0852fada111b45b46ddd4c4bc2f41be268923fb25cba07f`  
		Last Modified: Mon, 27 Mar 2023 22:49:26 GMT  
		Size: 200.0 MB (200034438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

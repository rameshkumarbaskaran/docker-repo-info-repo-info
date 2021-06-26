## `openjdk:18-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:6d80333e29cf689d2cca3d4b53ad4093de2389da56798ad537e02491fe95dadb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:b5e6ebfb95817467a4cdc12096b6f99290b7ca9f16fed325fbb0a5ff6f9a8bf9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243590464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5b477ea1614b46e6d7a75642c2160e09f73db10a09d5ee3dbfcdf731ddf396`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 02 Jun 2021 17:21:00 GMT
ADD file:b4c18f27ab03ed63f96174673a8d97d4b1b6abb552b6fe3201c6aec934e8312f in / 
# Wed, 02 Jun 2021 17:21:00 GMT
CMD ["/bin/bash"]
# Wed, 02 Jun 2021 17:37:54 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 14 Jun 2021 21:21:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Mon, 14 Jun 2021 21:21:25 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jun 2021 21:21:26 GMT
ENV LANG=C.UTF-8
# Sat, 26 Jun 2021 01:09:50 GMT
ENV JAVA_VERSION=18-ea+3
# Sat, 26 Jun 2021 01:10:01 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/3/GPL/openjdk-18-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='ff917caccd408eacd8758b82a4f9a698d872860d466efb1b23686cfbfb269559'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/3/GPL/openjdk-18-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='db2640da7cfae557c0809f69a643ada97e8048139d2a2e4a4a1f4abe1e762c7b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 26 Jun 2021 01:10:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5a581c13a8b96af42c06955acd88fdb3aff53edcbdd33faa7bca9854fd8bfbaf`  
		Last Modified: Wed, 02 Jun 2021 17:22:10 GMT  
		Size: 42.2 MB (42183647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cd02acd9c2b40dba18c3fe68882bcb5ebda0caeb5e550965d9ac81e3b55fbf`  
		Last Modified: Wed, 02 Jun 2021 17:43:15 GMT  
		Size: 13.4 MB (13400021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a44de42b12720b01e812911a98a1709713e3687bc07f0aa0f088aab384037f6`  
		Last Modified: Sat, 26 Jun 2021 01:19:23 GMT  
		Size: 188.0 MB (188006796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5eca259b971b2961a2761a3343e6b4d12285accff13ee9ca84c64a53135e3303
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243068372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12b1d04df554175313b3188f96fc9a50b5fc55720de53308a3fa8fbdfdeb01d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 02 Jun 2021 17:41:03 GMT
ADD file:78235baf524ed2a030d5aee5012599777d5026bf83699d8d03662420d6804653 in / 
# Wed, 02 Jun 2021 17:41:03 GMT
CMD ["/bin/bash"]
# Wed, 02 Jun 2021 17:58:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 14 Jun 2021 20:42:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Mon, 14 Jun 2021 20:42:14 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jun 2021 20:42:14 GMT
ENV LANG=C.UTF-8
# Sat, 26 Jun 2021 00:21:50 GMT
ENV JAVA_VERSION=18-ea+3
# Sat, 26 Jun 2021 00:22:15 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/3/GPL/openjdk-18-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='ff917caccd408eacd8758b82a4f9a698d872860d466efb1b23686cfbfb269559'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/3/GPL/openjdk-18-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='db2640da7cfae557c0809f69a643ada97e8048139d2a2e4a4a1f4abe1e762c7b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 26 Jun 2021 00:22:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4a780b35fbf92abdbd808aa7d8f30cb6c03db446424f04738aa715ba4935a1f6`  
		Last Modified: Wed, 02 Jun 2021 17:42:09 GMT  
		Size: 42.1 MB (42068993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b11c9e8386348cc9050d7280e19b5987140671e2de847d978f53d4ec578f94`  
		Last Modified: Wed, 02 Jun 2021 18:08:16 GMT  
		Size: 14.2 MB (14183644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9e1d1c3f332585d04ab923113a719c46ef479092134ba83329c45b7d52d069`  
		Last Modified: Sat, 26 Jun 2021 00:38:32 GMT  
		Size: 186.8 MB (186815735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

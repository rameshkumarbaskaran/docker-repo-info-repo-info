## `openjdk:18-ea-2-oraclelinux8`

```console
$ docker pull openjdk@sha256:36a470f5578bc24a8b9e42a43743f512e2d60dcc353015e20d1ee4bdc287a7f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-ea-2-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:20c8c248efafb7c39ebee4bb6e31d131a98d39d225c6926dd19a92b398e022b1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243605854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7122870d58e2b301d21bb0d480f177964fd8586a72f12c0ce4aa60f7b8e0b82`
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
# Tue, 22 Jun 2021 21:38:31 GMT
ENV JAVA_VERSION=18-ea+2
# Tue, 22 Jun 2021 21:38:42 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/2/GPL/openjdk-18-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='fa0458ce79f954b9271e5ff39815f02b8ccdda67e57791c644b331b59fe3e529'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/2/GPL/openjdk-18-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='b37a55b5a56bc7edee8b4870576338c53fc930259c630cda44fcd4fed8dc74b5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 22 Jun 2021 21:38:42 GMT
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
	-	`sha256:c918210deb38672bc738c2c212c27fb96ed9c238765fc0e1fc3f41c2bef6dc9d`  
		Last Modified: Tue, 22 Jun 2021 21:46:20 GMT  
		Size: 188.0 MB (188022186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-ea-2-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:90bdd8defe5dff51f205d3b3dc33f7c80563dbe884af621b5cf287ff107cb4bc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243075717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639ae9740e7467cdd0fd779b6d2f485057ae6ef911af29656455d7e0ba3084f9`
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
# Tue, 22 Jun 2021 21:56:33 GMT
ENV JAVA_VERSION=18-ea+2
# Tue, 22 Jun 2021 21:56:51 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/2/GPL/openjdk-18-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='fa0458ce79f954b9271e5ff39815f02b8ccdda67e57791c644b331b59fe3e529'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/2/GPL/openjdk-18-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='b37a55b5a56bc7edee8b4870576338c53fc930259c630cda44fcd4fed8dc74b5'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 22 Jun 2021 21:56:52 GMT
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
	-	`sha256:e9d8d9d927326981c2bce7298b5a79b5bf29d539192db3d91781826a0b5bf7d4`  
		Last Modified: Tue, 22 Jun 2021 22:10:18 GMT  
		Size: 186.8 MB (186823080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

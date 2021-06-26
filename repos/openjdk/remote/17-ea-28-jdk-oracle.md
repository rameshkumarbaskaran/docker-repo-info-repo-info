## `openjdk:17-ea-28-jdk-oracle`

```console
$ docker pull openjdk@sha256:67f82873978abc7ab04efa8a70d9fe8455a4b734970949c3bafab2f22c3e9bd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:17-ea-28-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:db6d37c82f542f00abd7e0f8adc4e8a2fdf48ed4bfeb47740d1ed89dc2817a7d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.7 MB (242694833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdfde173b0da200f4fa4696dbbf280020338bbc40455f92559379d094b8394d1`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 02 Jun 2021 17:21:00 GMT
ADD file:b4c18f27ab03ed63f96174673a8d97d4b1b6abb552b6fe3201c6aec934e8312f in / 
# Wed, 02 Jun 2021 17:21:00 GMT
CMD ["/bin/bash"]
# Wed, 02 Jun 2021 17:37:54 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 02 Jun 2021 17:37:55 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Wed, 02 Jun 2021 17:37:55 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Jun 2021 17:37:55 GMT
ENV LANG=C.UTF-8
# Sat, 26 Jun 2021 01:10:56 GMT
ENV JAVA_VERSION=17-ea+28
# Sat, 26 Jun 2021 01:11:17 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/28/GPL/openjdk-17-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='29f489da387fdabce2ebfbb74f474c424ed9c92380783da511d8ab1ed5dee912'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/28/GPL/openjdk-17-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='60752f6f44e478db934f4dc4b9a7cb715387ae964fb353e469dd986a5aeaf92b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 26 Jun 2021 01:11:17 GMT
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
	-	`sha256:22116792d3b3547f6e2f72a21506320bca7db4690f96cd9ce56e41c449f70cc2`  
		Last Modified: Sat, 26 Jun 2021 01:22:13 GMT  
		Size: 187.1 MB (187111165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-ea-28-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:370be3022990f2cc6623b266089a3984fac656c76d6da68155ec94c008d12bdb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.2 MB (242166825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f043c8407493356dc22a1c0e4f472bfbec9e45301179a1637549dc3e69121a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 02 Jun 2021 17:41:03 GMT
ADD file:78235baf524ed2a030d5aee5012599777d5026bf83699d8d03662420d6804653 in / 
# Wed, 02 Jun 2021 17:41:03 GMT
CMD ["/bin/bash"]
# Wed, 02 Jun 2021 17:58:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 02 Jun 2021 17:58:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Wed, 02 Jun 2021 17:58:07 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Jun 2021 17:58:07 GMT
ENV LANG=C.UTF-8
# Sat, 26 Jun 2021 00:23:40 GMT
ENV JAVA_VERSION=17-ea+28
# Sat, 26 Jun 2021 00:24:02 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/28/GPL/openjdk-17-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='29f489da387fdabce2ebfbb74f474c424ed9c92380783da511d8ab1ed5dee912'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/28/GPL/openjdk-17-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='60752f6f44e478db934f4dc4b9a7cb715387ae964fb353e469dd986a5aeaf92b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 26 Jun 2021 00:24:03 GMT
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
	-	`sha256:9c93edf95c00f90155baa5ed8887ca956d29247ef830ef4a464c814a785247f8`  
		Last Modified: Sat, 26 Jun 2021 00:42:03 GMT  
		Size: 185.9 MB (185914188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

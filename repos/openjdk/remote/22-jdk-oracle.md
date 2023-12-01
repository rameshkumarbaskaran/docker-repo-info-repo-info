## `openjdk:22-jdk-oracle`

```console
$ docker pull openjdk@sha256:d55e876db479cbfb0ca2a3daa1bf780a73fe7205fe8ed13320832e71a38f391d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:78d07551cbc0bafd6405854184567959812802f8946b31b9b3df86f9b19e0770
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264456411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956c4dd79a39d524a031efdda6af9f778f3fbfae9bdbda4a0348fd8d8226cfc5`
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
# Fri, 01 Dec 2023 20:54:50 GMT
ENV JAVA_VERSION=22-ea+26
# Fri, 01 Dec 2023 20:55:03 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/26/GPL/openjdk-22-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='65f135f44a1f33848f9d8398b7773807cf90eeec08d6ec8e2a9b44d81b7b6d99'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/26/GPL/openjdk-22-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='3933a8d405ab7f0293ecd4351177e731f1eacd1a96ee3f0528b9157940581ce2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 01 Dec 2023 20:55:04 GMT
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
	-	`sha256:52b877ab4882c0674ae38be155f7069f567578dea5962093207e89bed883f94e`  
		Last Modified: Fri, 01 Dec 2023 20:57:17 GMT  
		Size: 205.2 MB (205160668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0d43d0351735c4fc19a2af25d5fc4560dc0603c448f82f2c06390851281a03f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.5 MB (262546594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:203fb9323d1aac231894e70eb4a8d0fe1610d6c4fe3c54d42d473ed885efda60`
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
# Fri, 01 Dec 2023 20:58:35 GMT
ENV JAVA_VERSION=22-ea+26
# Fri, 01 Dec 2023 20:59:02 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/26/GPL/openjdk-22-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='65f135f44a1f33848f9d8398b7773807cf90eeec08d6ec8e2a9b44d81b7b6d99'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/26/GPL/openjdk-22-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='3933a8d405ab7f0293ecd4351177e731f1eacd1a96ee3f0528b9157940581ce2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 01 Dec 2023 20:59:04 GMT
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
	-	`sha256:8ab1f521a17f69fb5bfa05a08cbfea2e79d263320a357c62c680710d03c7cd00`  
		Last Modified: Fri, 01 Dec 2023 21:01:13 GMT  
		Size: 203.2 MB (203213417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

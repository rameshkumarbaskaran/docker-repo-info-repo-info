## `openjdk:18-ea-6-jdk-oracle`

```console
$ docker pull openjdk@sha256:39a7c9f8e432a9cbd7872684026fa4f827e3607d27e6708c4349691f9cedfa58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-ea-6-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:b9e42f281115a8ccf82b912d2f88b631c82c9261b0f37f79f6b7f8be207def43
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243148226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb1cc4e7f7f2317cc7499a9375225a0205f957a09bbcf3267af2688d098acbf`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jul 2021 20:20:57 GMT
ADD file:c830de449b9ecd90e02f56d99e8326701da17970fa314bd7b060fd9a7cf7ac77 in / 
# Mon, 12 Jul 2021 20:20:58 GMT
CMD ["/bin/bash"]
# Mon, 12 Jul 2021 23:33:03 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 12 Jul 2021 23:33:04 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Mon, 12 Jul 2021 23:33:04 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jul 2021 23:33:04 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jul 2021 22:20:30 GMT
ENV JAVA_VERSION=18-ea+6
# Thu, 15 Jul 2021 22:20:52 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/6/GPL/openjdk-18-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='13bb69d5907c906e8b9347e531919e17c54f6505cbb4c5fcde71f358b8afac15'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/6/GPL/openjdk-18-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='821ae9c92e8ef55f8cc0671cff324e7e866ee1acbb2d0a86f90b009b35d11925'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 15 Jul 2021 22:20:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c828c776e142cb23ad61c84403bb42deaa97efeda5e2b600df46f7dbd38ec681`  
		Last Modified: Mon, 12 Jul 2021 20:22:25 GMT  
		Size: 42.2 MB (42179737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8846dac42cae4499c0917b5bd5e81c0e6d6fcc5326d50972b3faed7ccdf688b8`  
		Last Modified: Mon, 12 Jul 2021 23:41:34 GMT  
		Size: 13.4 MB (13392657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687cc0badf0d77dbb8657d953b38fbb85f37e5df3e1973fa29702d55a7cc7f40`  
		Last Modified: Thu, 15 Jul 2021 22:27:57 GMT  
		Size: 187.6 MB (187575832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-ea-6-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:fd1d64b9dcdbb3cdf82d0ebeae8a10482bc20ef15bd28985e5d493ddb77c4b6e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242552224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8250651b605ed3d781372e82563488e0bf9564442f84971b20e16dd0574c1494`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 12 Jul 2021 20:40:32 GMT
ADD file:a184ed870dc7a85028f7ba3bd0cf3820d6f1b94ac4cea1ac94ca48c786901041 in / 
# Mon, 12 Jul 2021 20:40:33 GMT
CMD ["/bin/bash"]
# Mon, 12 Jul 2021 21:03:05 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 12 Jul 2021 21:03:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Mon, 12 Jul 2021 21:03:06 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jul 2021 21:03:06 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jul 2021 22:40:26 GMT
ENV JAVA_VERSION=18-ea+6
# Thu, 15 Jul 2021 22:40:46 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/6/GPL/openjdk-18-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='13bb69d5907c906e8b9347e531919e17c54f6505cbb4c5fcde71f358b8afac15'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/6/GPL/openjdk-18-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='821ae9c92e8ef55f8cc0671cff324e7e866ee1acbb2d0a86f90b009b35d11925'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 15 Jul 2021 22:40:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6186b25cabd91cbdd2c6bf65b0c5ef261f52719e7c6c4d6252e7082b7a51b42e`  
		Last Modified: Mon, 12 Jul 2021 20:41:48 GMT  
		Size: 42.1 MB (42072715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8304774b066b61c2ae3dc6de204cb3d384a726b9376d301afc654577b50a9c0`  
		Last Modified: Mon, 12 Jul 2021 21:15:51 GMT  
		Size: 14.2 MB (14170180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47da8fbc451d5f5cfea3100c6ada05a232645dadd3873e97acaa3107211c15d`  
		Last Modified: Thu, 15 Jul 2021 22:54:13 GMT  
		Size: 186.3 MB (186309329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

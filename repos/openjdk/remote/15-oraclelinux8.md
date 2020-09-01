## `openjdk:15-oraclelinux8`

```console
$ docker pull openjdk@sha256:36381e7bb2540e5de3faab83469f77a09ed87f34a4ba56173df9445fc0b089ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:15-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:89d18dbfd40457f2063b025a97672040759a8d8fd2eb6976c21df02f0ca2532c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262407005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e2ea6497f958c095133b118d34d23958af6d279ea9321ef52d5c801657888b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Fri, 24 Jul 2020 00:21:31 GMT
ADD file:02670bc2999f43239e261c6f4e819f10471cfababa139f0eeba033a934c44eed in / 
# Fri, 24 Jul 2020 00:21:31 GMT
CMD ["/bin/bash"]
# Wed, 26 Aug 2020 21:28:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 01 Sep 2020 01:41:13 GMT
ENV LANG=C.UTF-8
# Tue, 01 Sep 2020 01:44:30 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Tue, 01 Sep 2020 01:44:30 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Sep 2020 01:44:31 GMT
ENV JAVA_VERSION=15
# Tue, 01 Sep 2020 01:45:28 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/GA/jdk15/779bf45e88a44cbd9ea6621d33e33db1/36/GPL/openjdk-15_linux-aarch64_bin.tar.gz; 			downloadSha256=01e7e07dd8a67a65b32fdcaff75ba3f21cd9cfc749287e7c9b1c6037f96a3537; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/GA/jdk15/779bf45e88a44cbd9ea6621d33e33db1/36/GPL/openjdk-15_linux-x64_bin.tar.gz; 			downloadSha256=bb67cadee687d7b486583d03c9850342afea4593be4f436044d785fba9508fb7; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 01 Sep 2020 01:45:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1bbe67b820dbc81dda19341c188f2504cb57d03d540dc94bf12e3f752102adf8`  
		Last Modified: Fri, 24 Jul 2020 00:23:22 GMT  
		Size: 53.2 MB (53238241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c479ccfad94616e2be168f7843f91429bd9a7d0996b687d670bfe633136895a`  
		Last Modified: Wed, 26 Aug 2020 21:33:04 GMT  
		Size: 13.4 MB (13417665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aed85b309271c706801511b77c8c87206accdd35002719d23e91038010538d3`  
		Last Modified: Tue, 01 Sep 2020 01:56:06 GMT  
		Size: 195.8 MB (195751099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:15-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2a9aa2b3b181c77c795f364e3b566e79f641cbfdb5fee5186703905fb90e3d18
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242535949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac308a3165b669c95c4aa83b38e9f8fb22c10ff549cb704ab15459f6d04e420`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 May 2019 21:40:52 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Fri, 24 Jul 2020 00:53:42 GMT
ADD file:2ad87b72223c423a2c0741208d69b5b361aabaa96bfbe1510fa44745a72c0e7f in / 
# Fri, 24 Jul 2020 00:53:46 GMT
CMD ["/bin/bash"]
# Wed, 26 Aug 2020 21:35:59 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 01 Sep 2020 07:16:10 GMT
ENV LANG=C.UTF-8
# Tue, 01 Sep 2020 07:19:07 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Tue, 01 Sep 2020 07:19:07 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Sep 2020 07:19:08 GMT
ENV JAVA_VERSION=15
# Tue, 01 Sep 2020 07:19:54 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/GA/jdk15/779bf45e88a44cbd9ea6621d33e33db1/36/GPL/openjdk-15_linux-aarch64_bin.tar.gz; 			downloadSha256=01e7e07dd8a67a65b32fdcaff75ba3f21cd9cfc749287e7c9b1c6037f96a3537; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/GA/jdk15/779bf45e88a44cbd9ea6621d33e33db1/36/GPL/openjdk-15_linux-x64_bin.tar.gz; 			downloadSha256=bb67cadee687d7b486583d03c9850342afea4593be4f436044d785fba9508fb7; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 01 Sep 2020 07:19:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e618d2a55163b9d055a0c627bc7faff5f4210ee92e01ce1b82dd0738d8c5e12`  
		Last Modified: Fri, 24 Jul 2020 00:55:39 GMT  
		Size: 53.3 MB (53345174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed03d65a39d352a49fbfba9a4223490a35071d814a500f1e7a378ce915dd32f6`  
		Last Modified: Wed, 26 Aug 2020 21:40:32 GMT  
		Size: 14.3 MB (14331702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e4174c0175d9cebb35db0691b218fc161798b557f59a8cc1aaba6edc31e897`  
		Last Modified: Tue, 01 Sep 2020 07:27:38 GMT  
		Size: 174.9 MB (174859073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

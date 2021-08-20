## `openjdk:18-ea-oracle`

```console
$ docker pull openjdk@sha256:7019eb5dfeceffcfe1f515d0d44417505ffee974daed92cf25dd88a6ee8ad897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-ea-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:a51329ba8e8277de5897f952e5761888a6c948662658bcd4c5eea38723d39971
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (243007987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32042fd4ceba65a866100167d2d2b8db32551df3ad567d46879061851c0a8296`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 12 Aug 2021 19:20:55 GMT
ADD file:ab982d6f37710c434f7ef9650c722d3c6333906cbb9344bf91e79068088bcc69 in / 
# Thu, 12 Aug 2021 19:20:56 GMT
CMD ["/bin/bash"]
# Thu, 12 Aug 2021 19:37:56 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 12 Aug 2021 19:37:56 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Thu, 12 Aug 2021 19:37:56 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Aug 2021 19:37:57 GMT
ENV LANG=C.UTF-8
# Thu, 19 Aug 2021 22:28:31 GMT
ENV JAVA_VERSION=18-ea+11
# Thu, 19 Aug 2021 22:28:42 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/11/GPL/openjdk-18-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='593243ad4eb9339cec9d7675ff01fb4d7b816c1b1f68d4e54d0dc4f99d8f55f5'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/11/GPL/openjdk-18-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='8efa12ef6e1acab1a4cc5dba5a45dcb828fa0265e409cd0cf2e8e9eec4ad8f0f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 19 Aug 2021 22:28:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c67289558ae5eb060942db5bf46d182448587a87e21c680a0486b147d4b9a0b4`  
		Last Modified: Thu, 12 Aug 2021 19:22:09 GMT  
		Size: 42.2 MB (42158041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12787f1f3888c64bfc9e779a9705ecc45ae1a60b3757074b6f16cf1d8553cac8`  
		Last Modified: Thu, 12 Aug 2021 19:43:29 GMT  
		Size: 13.4 MB (13373335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e9bb0f2f3b77f5830a49731bbb65df402d8aa9a69c6a6f02cf4929cfb3d33dc`  
		Last Modified: Thu, 19 Aug 2021 22:34:00 GMT  
		Size: 187.5 MB (187476611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-ea-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:db64d59ae4b041c20593f2c6b809ac50018eca66b37876c02ae28e1fb61502ba
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242442112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7fdaa6d8af89598df138fd71d27141c87660fe921f98f0c81e288cbbf7f8a2`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 13 Aug 2021 02:58:07 GMT
ADD file:3a5bc6124c8d78438880a95007baec403400e29f09317331e09ba7d65a0aaff0 in / 
# Fri, 13 Aug 2021 02:58:08 GMT
CMD ["/bin/bash"]
# Fri, 13 Aug 2021 05:39:58 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 13 Aug 2021 05:39:58 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Fri, 13 Aug 2021 05:39:59 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Aug 2021 05:39:59 GMT
ENV LANG=C.UTF-8
# Thu, 19 Aug 2021 20:40:32 GMT
ENV JAVA_VERSION=18-ea+11
# Thu, 19 Aug 2021 20:40:55 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/11/GPL/openjdk-18-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='593243ad4eb9339cec9d7675ff01fb4d7b816c1b1f68d4e54d0dc4f99d8f55f5'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/11/GPL/openjdk-18-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='8efa12ef6e1acab1a4cc5dba5a45dcb828fa0265e409cd0cf2e8e9eec4ad8f0f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 19 Aug 2021 20:40:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:757bb77daa0e625f3aaa9e22fcc2dda31fa9d6e50f482403ab7be9f030a1a19f`  
		Last Modified: Fri, 13 Aug 2021 02:59:14 GMT  
		Size: 42.1 MB (42054178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d701f3bd7e43b3fb331b6b15362e9dbd4abd27a5c29f2301d998cc782a0ba1`  
		Last Modified: Fri, 13 Aug 2021 05:50:47 GMT  
		Size: 14.2 MB (14163676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b2425ed9084c925015c60bd07a7682e2cb1f09ba43e0444911912acb4a64f1`  
		Last Modified: Thu, 19 Aug 2021 20:51:26 GMT  
		Size: 186.2 MB (186224258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `openjdk:8-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:b07315cf0074847861612338cf67100d646f7e1a106c4193cddff330c2f1708b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:8-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:8593be7fddeb23e2a23c4f705606e1d54ed69c60f24d4547489f75dd2df3414d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.7 MB (169699703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f7de9a825cd97fe4f3e2aec6188f0b6cf7cd02446d236bbcb4e7205d9f425b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 24 Feb 2022 01:15:28 GMT
ADD file:a953cc04974b35909ddbd8826601c0824f8cc920ebc522046d4ca64e69c2c26f in / 
# Thu, 24 Feb 2022 01:15:29 GMT
CMD ["/bin/bash"]
# Thu, 24 Feb 2022 01:47:39 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 24 Feb 2022 01:51:56 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Thu, 24 Feb 2022 01:51:56 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Feb 2022 01:51:57 GMT
ENV LANG=en_US.UTF-8
# Thu, 24 Feb 2022 01:51:57 GMT
ENV JAVA_VERSION=8u322
# Thu, 24 Feb 2022 01:53:07 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:5269884ada0dd8683c910050c7cf3a447be8fcb9f733519f759745b117b217cc`  
		Last Modified: Thu, 24 Feb 2022 01:16:17 GMT  
		Size: 48.3 MB (48331243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48833246028b375ed9389617e9b863bfab004c27db95b93b1e8b7c646ce3f9a1`  
		Last Modified: Thu, 24 Feb 2022 01:58:10 GMT  
		Size: 15.4 MB (15402391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384953eb9974b232c8d4da291feb760e81ea3ca9b317bf8703f55e28ed301d8d`  
		Last Modified: Thu, 24 Feb 2022 02:02:33 GMT  
		Size: 106.0 MB (105966069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:8-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:630896e9bfcc97e44e9ec813f9aec67237b506e1de42863d9e86514e8116fa5e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170328322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdd34c55d555164d6885488bdd61afc3e3986a7ac146d6efbdaabfccc8d90ff7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:48 GMT
ADD file:933bf8bd076f0c42499df14ceb4b409753b2ce9f8b0bd81331ac2630b6dab149 in / 
# Fri, 25 Feb 2022 02:07:49 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 02:27:32 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 25 Feb 2022 02:37:45 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Fri, 25 Feb 2022 02:37:46 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Feb 2022 02:37:47 GMT
ENV LANG=en_US.UTF-8
# Fri, 25 Feb 2022 02:37:48 GMT
ENV JAVA_VERSION=8u322
# Fri, 25 Feb 2022 02:39:13 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:5148c102f8614047b0330785165cb7096428df640af91104fbe61a7ebb5b8713`  
		Last Modified: Fri, 25 Feb 2022 02:09:24 GMT  
		Size: 48.9 MB (48901247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5afd0c7f5b0b7ae1e56ff4afb456806881a77fe14b8769883e0684cbcb9ac76`  
		Last Modified: Fri, 25 Feb 2022 02:48:54 GMT  
		Size: 16.4 MB (16445028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca551bd06edb7fb5285276d231d6bd939b62b2b33cbf6c9212694c7d773fa9c5`  
		Last Modified: Fri, 25 Feb 2022 02:57:05 GMT  
		Size: 105.0 MB (104982047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `openjdk:8-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:a9b93f09b141d4ffdf1b8c09209a010e81eee9f75e6eefeec9a5b71e21fe4084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:8-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:06c407fa1e0b5a25ebfd1cd236b9ec4c37fb9b57ba2931abbc328bb17d9d8a1d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168839521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43571fa68ecc53aa215ba604eceb163236676a698f7db0908855accf3aecac8a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 May 2022 20:58:56 GMT
ADD file:8ac79c33c3bdf8a0a1c23cc009fabc3ead9d97891d701ad21090a6bc542521e2 in / 
# Thu, 12 May 2022 20:58:56 GMT
CMD ["/bin/bash"]
# Thu, 12 May 2022 22:41:56 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 12 May 2022 22:43:54 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Thu, 12 May 2022 22:43:54 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 May 2022 22:43:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 12 May 2022 22:43:54 GMT
ENV JAVA_VERSION=8u332
# Thu, 12 May 2022 22:44:05 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:cd32cd816e68367704ec22e6e4d27af6a08b27e32aca3d0bd7a47424e37d0b91`  
		Last Modified: Thu, 12 May 2022 20:59:41 GMT  
		Size: 48.8 MB (48758049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d60946da119889a74d287d76661db4bd1631a2fbdcf7e72d140b5e4f25273b`  
		Last Modified: Thu, 12 May 2022 22:47:50 GMT  
		Size: 14.2 MB (14245376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:900bb975c909d6ffe272e36b2daf763b2bb4a546043236f5ac210af24a8000b6`  
		Last Modified: Thu, 12 May 2022 22:50:49 GMT  
		Size: 105.8 MB (105836096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:8-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8a8ac33b2b321cd112efbb3e90b5f9c782d654bbc82d92e3628a00454ab1c468
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169420617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07cad857e84a22e69833c69cbb3ce4a85d5753cc69ebacea9189e0dd0c652ba4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 May 2022 22:09:29 GMT
ADD file:b866e521d7e920b2210ec5ba4013715f28d1ad0636a38a13cec969d5b3586d44 in / 
# Thu, 12 May 2022 22:09:30 GMT
CMD ["/bin/bash"]
# Fri, 13 May 2022 00:26:03 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 13 May 2022 00:30:01 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Fri, 13 May 2022 00:30:02 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 May 2022 00:30:03 GMT
ENV LANG=en_US.UTF-8
# Fri, 13 May 2022 00:30:04 GMT
ENV JAVA_VERSION=8u332
# Fri, 13 May 2022 00:30:21 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:fa569c775ec815d1a2d6e7b4f6e989b8afe4f0749c119d04101e4cb016365983`  
		Last Modified: Thu, 12 May 2022 22:10:25 GMT  
		Size: 49.3 MB (49340765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a850683079b99a0cee3fbeb957ff22bf46a963d7306f33b059cba19183ee75a`  
		Last Modified: Fri, 13 May 2022 00:37:40 GMT  
		Size: 15.3 MB (15269457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cbcba0e737b24b5fda6905e206fc7bec0e3236ac34ef7cb55ce9f1c9c03dfe8`  
		Last Modified: Fri, 13 May 2022 00:41:37 GMT  
		Size: 104.8 MB (104810395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

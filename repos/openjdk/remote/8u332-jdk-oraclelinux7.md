## `openjdk:8u332-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:85b0f75b61698276157a7c9545a76f318f36984f94a61c306bdd5dac9ee72f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:8u332-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:da327fb549b4a7c04b6dcf13b1c927d555f59d27440564c1d6b2d1c2df264caa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168830028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0decfaff433e335325afd28b12199649c6bf246ea12ea7afeb688014570c5411`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Jun 2022 01:20:22 GMT
ADD file:5e615d6d49ec50cba937fa86f5fb7d6a4a7e680b2b4f5b659e879b95304c0417 in / 
# Thu, 16 Jun 2022 01:20:22 GMT
CMD ["/bin/bash"]
# Tue, 28 Jun 2022 00:27:27 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 28 Jun 2022 00:32:47 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Tue, 28 Jun 2022 00:32:47 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jun 2022 00:32:47 GMT
ENV LANG=en_US.UTF-8
# Tue, 28 Jun 2022 00:32:47 GMT
ENV JAVA_VERSION=8u332
# Tue, 28 Jun 2022 00:32:56 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:63183c9b4598e16c4cef95f706d50ff6c928de41f391cd513495b27eaa27bf89`  
		Last Modified: Thu, 16 Jun 2022 01:21:08 GMT  
		Size: 48.8 MB (48757931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27f2a0cb669162a36b2576cd36536ebb88d2e0ccedba24fe92c1b0a992569e5`  
		Last Modified: Tue, 28 Jun 2022 00:38:26 GMT  
		Size: 14.2 MB (14236080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66aea8b3c9fd840e5759b9754fcb092806369d1455cbb8a73a55d0290966aab7`  
		Last Modified: Tue, 28 Jun 2022 00:48:17 GMT  
		Size: 105.8 MB (105836017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:8u332-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:00f42e06a0f475be5795272a378e6dea5741f71c01307e038474785429e9cc55
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169418722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed7930e3cf6a71be76c8e18701256f62577a74cec9c9dee240584fdaf41786d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Jun 2022 01:12:02 GMT
ADD file:3c802f9fbd1a9a4878df064e2b268b017930633407658a3f9d29e53eb74552fa in / 
# Thu, 16 Jun 2022 01:12:03 GMT
CMD ["/bin/bash"]
# Tue, 28 Jun 2022 00:41:52 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 28 Jun 2022 00:49:18 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Tue, 28 Jun 2022 00:49:19 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jun 2022 00:49:20 GMT
ENV LANG=en_US.UTF-8
# Tue, 28 Jun 2022 00:49:21 GMT
ENV JAVA_VERSION=8u332
# Tue, 28 Jun 2022 00:49:34 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:9071f63390163e069a5245aea05c5a92f0dd4a4a48483db57c4c3c0d557be5e7`  
		Last Modified: Thu, 16 Jun 2022 01:12:57 GMT  
		Size: 49.3 MB (49343296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e959388b0464e301c8f837d6139ee9789051dee894111f69643a0c73900dfa9`  
		Last Modified: Tue, 28 Jun 2022 00:59:49 GMT  
		Size: 15.3 MB (15265029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b577e2981e50102710cb95c0c626dd4d664c29ac1a7e0e5bc5f34744b7706d84`  
		Last Modified: Tue, 28 Jun 2022 01:11:53 GMT  
		Size: 104.8 MB (104810397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

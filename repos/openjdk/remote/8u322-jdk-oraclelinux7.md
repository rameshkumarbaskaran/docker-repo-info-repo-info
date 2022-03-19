## `openjdk:8u322-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:92636fa9e3da7596f344a3024e210de93eaa777cf868239adcf6f200afaa012e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:8u322-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:a7d84e3c79f219617a3ca92ab034380afa321839d49653522964d6d888eba14c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.9 MB (168930039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4a96ce76938db3db1549f0a878801d8d6edfdc57556864c18d76d4c4c602c6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Mar 2022 23:22:25 GMT
ADD file:19ae95221a518b3855b98aeb91f6c13f250d6caa59ee16bf155d73f7f5cdcc41 in / 
# Fri, 18 Mar 2022 23:22:26 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 10:18:15 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Sat, 19 Mar 2022 10:28:27 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Sat, 19 Mar 2022 10:28:27 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:28:27 GMT
ENV LANG=en_US.UTF-8
# Sat, 19 Mar 2022 10:28:27 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 10:28:35 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:fb9cda09c679c7a8d70feb22223b7546c2d4d46d555312571fa2e3cc65347d9b`  
		Last Modified: Fri, 18 Mar 2022 23:23:20 GMT  
		Size: 48.7 MB (48745506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f858fe6b2907e344c8421154471dfeff5be2cb6510210efa614c5d1eacf06d25`  
		Last Modified: Sat, 19 Mar 2022 10:35:39 GMT  
		Size: 14.2 MB (14218591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da97be2741dc010901d331d9693c0e8d5e85f82ff08b2a187f9d27e3b59f3ef3`  
		Last Modified: Sat, 19 Mar 2022 10:47:29 GMT  
		Size: 106.0 MB (105965942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:8u322-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d45fe6b0fcb33da8759204bd2a4ad2d8f40a4cccccead67d92aca3c7a54c29af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.6 MB (169600579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd65f6fa746f484147f7f7695b9cef50d5f4d9516ded06ea43d7ae1268f0140`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 19 Mar 2022 01:00:51 GMT
ADD file:a5f18f088f362b979701dd9843b784391fd01ee9f85e19b4a66089ccba650d8a in / 
# Sat, 19 Mar 2022 01:00:51 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 07:23:15 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Sat, 19 Mar 2022 07:33:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Sat, 19 Mar 2022 07:33:25 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 07:33:26 GMT
ENV LANG=en_US.UTF-8
# Sat, 19 Mar 2022 07:33:27 GMT
ENV JAVA_VERSION=8u322
# Sat, 19 Mar 2022 07:35:04 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_linux_8u322b06.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_aarch64_linux_8u322b06.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:141b1a23f5c914f6ea3d33bbb54ee6e46d83e342a4f16e079f825362e6db5a24`  
		Last Modified: Sat, 19 Mar 2022 01:01:46 GMT  
		Size: 49.3 MB (49339592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdcf257e8020deec6d6f5ad76b9c36d1eca4b42e96527feb4c52735766f320b7`  
		Last Modified: Sat, 19 Mar 2022 07:44:40 GMT  
		Size: 15.3 MB (15278942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65ecbc6cb59cfc1c0d35cea65a1d893dc4b54743358791ff278d726e957042d`  
		Last Modified: Sat, 19 Mar 2022 07:52:35 GMT  
		Size: 105.0 MB (104982045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

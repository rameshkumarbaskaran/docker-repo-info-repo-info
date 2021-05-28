## `openjdk:8-jdk-oracle`

```console
$ docker pull openjdk@sha256:db3e7d70fb22987d932a70775cc25e3a56dcc5b7a35734de7c0244b825de34fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:8-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:d29aa153eb3df3445aa6a10607fff04bdad051b297d3f0f4205d0916804fffce
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.4 MB (161412954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a199e431fee21d245a0ac315ab6fa66239db10d825b83a389a7461fae79e57f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 May 2021 18:22:12 GMT
ADD file:9e4bcf8e1c3b7657912e93a0b82bf37752a310fa3041ec461562c85d65529ad3 in / 
# Fri, 28 May 2021 18:22:12 GMT
CMD ["/bin/bash"]
# Fri, 28 May 2021 18:39:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 28 May 2021 18:41:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Fri, 28 May 2021 18:41:06 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 May 2021 18:41:06 GMT
ENV LANG=C.UTF-8
# Fri, 28 May 2021 18:41:07 GMT
ENV JAVA_VERSION=8u292
# Fri, 28 May 2021 18:41:14 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_x64_linux_8u292b10.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_aarch64_linux_8u292b10.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:daa797b1cf01195cd47497fc9ddbf3fc4404f3fc012110f206b7fa3dd531e43d`  
		Last Modified: Fri, 28 May 2021 18:23:25 GMT  
		Size: 42.2 MB (42183040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e7f736a217a7dd2e90a8ba647050e6374f7c3f746ad3256682302739a73ee7`  
		Last Modified: Fri, 28 May 2021 18:44:27 GMT  
		Size: 13.4 MB (13401079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e89adf60f965af42e619ed8a9d68b73cc121a2785f507ca657893a202124c01`  
		Last Modified: Fri, 28 May 2021 18:48:27 GMT  
		Size: 105.8 MB (105828835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:8-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4d12334961c6900d4bf04aabeed51fa8143b4a638ea996c7d65d535ca9e03d31
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161058593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7f4b434c318f948f789056654ba2bcf85573c0063e77647e7dfb543198dcba`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 17 Apr 2021 00:43:47 GMT
ADD file:2afad2b68d4889be2ef517aea246957975145f8ad99a3e9e6a01baf79f67d5e2 in / 
# Sat, 17 Apr 2021 00:43:51 GMT
CMD ["/bin/bash"]
# Thu, 27 May 2021 08:36:19 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 27 May 2021 08:43:57 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Thu, 27 May 2021 08:43:57 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 May 2021 08:43:57 GMT
ENV LANG=C.UTF-8
# Thu, 27 May 2021 08:43:57 GMT
ENV JAVA_VERSION=8u292
# Thu, 27 May 2021 08:44:04 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_x64_linux_8u292b10.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_aarch64_linux_8u292b10.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:4b26d50a92155f32c82c580c6abd80083d4fff230a35ef647094df38f4475f9f`  
		Last Modified: Sat, 17 Apr 2021 00:45:12 GMT  
		Size: 42.0 MB (41996718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f165b404d40aab21b88837e6a2c21b279a81827c7f906a6c56c6690bf3425c`  
		Last Modified: Thu, 27 May 2021 08:52:17 GMT  
		Size: 14.2 MB (14184544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9f4d6e74a07cfc5f7ab623bbbb98df08b730ce8862dc5b0a55ab604cedaf58`  
		Last Modified: Thu, 27 May 2021 09:05:14 GMT  
		Size: 104.9 MB (104877331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `openjdk:11-oraclelinux7`

```console
$ docker pull openjdk@sha256:1d2880908c791d866cccba3551f59df5d26e22e4c8e002691512a508087f205c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:11-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:55da90fa1f70fa063522b4b0e70ffaa069fbbb7c9d257fd9677bee174a79a75d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.5 MB (266507251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b93b6df98fb66cc319e940e4268575e72c384a7d258992055d9cd140c6c9d9c`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 01 May 2021 04:45:56 GMT
ADD file:31ad06acd4a00f68bd8424f227970a5247493c5cc2d4e4d2b40c55e336119324 in / 
# Sat, 01 May 2021 04:45:57 GMT
CMD ["/bin/bash"]
# Sat, 01 May 2021 05:02:18 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Sat, 01 May 2021 05:03:28 GMT
ENV JAVA_HOME=/usr/java/openjdk-11
# Sat, 01 May 2021 05:03:29 GMT
ENV PATH=/usr/java/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 01 May 2021 05:03:29 GMT
ENV LANG=en_US.UTF-8
# Sat, 01 May 2021 05:03:29 GMT
ENV JAVA_VERSION=11.0.11+9
# Sat, 01 May 2021 05:03:43 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_11.0.11_9.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_11.0.11_9.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 01 May 2021 05:03:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5ef5e09557a1ca0ce2f2f8486a7db9555bf280058aaa8a883f7dfe0da5505b1e`  
		Last Modified: Sat, 01 May 2021 04:47:02 GMT  
		Size: 48.3 MB (48265270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75544f3e96e157c8633ccb0a7bd3d63eac5c09949dd7fa57d238ed37c62a0332`  
		Last Modified: Sat, 01 May 2021 05:07:32 GMT  
		Size: 15.4 MB (15422103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3e269e6a56ba1ec10fd4bb12995be1565f902b43ad9c594d2599ac51f09b33`  
		Last Modified: Sat, 01 May 2021 05:09:36 GMT  
		Size: 202.8 MB (202819878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:11-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:cabc6169fde8686f93f73e38886ffe1682b0325ebf32ada366429b9416ba6fb8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.8 MB (265782821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a264881130f2be31bd6cbf9d0d511bb6da960322cbbcaaf59a9a842f5c0d114a`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 01 May 2021 02:34:14 GMT
ADD file:f71ab8aa2d773f52af43dee8a58345e3c64f23cf6dc9722fc2116449655ca0ce in / 
# Sat, 01 May 2021 02:34:16 GMT
CMD ["/bin/bash"]
# Sat, 01 May 2021 02:59:26 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Sat, 01 May 2021 03:01:34 GMT
ENV JAVA_HOME=/usr/java/openjdk-11
# Sat, 01 May 2021 03:01:36 GMT
ENV PATH=/usr/java/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 01 May 2021 03:01:37 GMT
ENV LANG=en_US.UTF-8
# Sat, 01 May 2021 03:01:38 GMT
ENV JAVA_VERSION=11.0.11+9
# Sat, 01 May 2021 03:02:11 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_x64_linux_11.0.11_9.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.11%2B9/OpenJDK11U-jdk_aarch64_linux_11.0.11_9.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 01 May 2021 03:02:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dbfc55cb74dd07b793cdc9b4bc835fcfdb6091dad8e24cd2a6fe84ec70a2c3a6`  
		Last Modified: Sat, 01 May 2021 02:35:18 GMT  
		Size: 48.9 MB (48874038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0431cdcee2306a17be0ad5fd6791cd432218c8671e4eb75ea3a708d15ef0c6c4`  
		Last Modified: Sat, 01 May 2021 03:07:27 GMT  
		Size: 16.5 MB (16472881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948de3585117ba706c13e5d20e72844a0d999dc64dc42e25dc47abd9a20159a8`  
		Last Modified: Sat, 01 May 2021 03:10:20 GMT  
		Size: 200.4 MB (200435902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

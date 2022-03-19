## `openjdk:11-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:90e5d0ecb8312ec2375d0bd45fa0afc436ae62e0468cc699d55f3b3253869e91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:11-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:5384d6a86314b3cecffc3469143f26a65ddea5882a004c2281b963db8b2de828
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.1 MB (266109907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fcaf210b3c6f3e3c68f03d3017034fb2bd1cb14124634d1b5c7f5d10b39307f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 18 Mar 2022 23:22:25 GMT
ADD file:19ae95221a518b3855b98aeb91f6c13f250d6caa59ee16bf155d73f7f5cdcc41 in / 
# Fri, 18 Mar 2022 23:22:26 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 10:18:15 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Sat, 19 Mar 2022 10:24:22 GMT
ENV JAVA_HOME=/usr/java/openjdk-11
# Sat, 19 Mar 2022 10:24:22 GMT
ENV PATH=/usr/java/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:24:23 GMT
ENV LANG=en_US.UTF-8
# Sat, 19 Mar 2022 10:24:23 GMT
ENV JAVA_VERSION=11.0.14.1
# Sat, 19 Mar 2022 10:24:58 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 19 Mar 2022 10:24:59 GMT
CMD ["jshell"]
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
	-	`sha256:eb406cc1e4cfbfd589b6b742ee0d8b8ba40d6a9f59fb9c5d55be01a4c35e05e4`  
		Last Modified: Sat, 19 Mar 2022 10:43:46 GMT  
		Size: 203.1 MB (203145810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:11-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b788e4157bf35e66679c3e48706cd8801ded1c150dc4aa62aec0c6878f910649
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.4 MB (265391427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1167e9baf7044cfa05fe9d06605b32e0938ecebe3c6a36dd7f29056461eb5359`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 19 Mar 2022 01:00:51 GMT
ADD file:a5f18f088f362b979701dd9843b784391fd01ee9f85e19b4a66089ccba650d8a in / 
# Sat, 19 Mar 2022 01:00:51 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 07:23:15 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Sat, 19 Mar 2022 07:28:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-11
# Sat, 19 Mar 2022 07:28:50 GMT
ENV PATH=/usr/java/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 07:28:51 GMT
ENV LANG=en_US.UTF-8
# Sat, 19 Mar 2022 07:28:52 GMT
ENV JAVA_VERSION=11.0.14.1
# Sat, 19 Mar 2022 07:30:53 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_linux_11.0.14.1_1.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_aarch64_linux_11.0.14.1_1.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 19 Mar 2022 07:30:53 GMT
CMD ["jshell"]
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
	-	`sha256:23375f772ccab2a1650b95c673494a63a14d6336198ff62d0bd359102628d157`  
		Last Modified: Sat, 19 Mar 2022 07:50:37 GMT  
		Size: 200.8 MB (200772893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

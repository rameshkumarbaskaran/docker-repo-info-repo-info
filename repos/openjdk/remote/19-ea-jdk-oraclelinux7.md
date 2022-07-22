## `openjdk:19-ea-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:420aa53350fbd3cd8212b5416d5c4ecf99f150dbd5a3d40e9cb444c14d36e236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-ea-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:11af272bd757d2e5f49fa9156b7f3631316a59018a754e733a0e603ff5344cb6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259178029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f60c981ede27ddb2ae304f5cfaaca5dd342ae28784ed863f91a40f487cba21`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:58 GMT
ADD file:50fb7d83a9d57e5a0a6af5e5daf27e464ae8a28c196ce6bad6c254dfc1774cdd in / 
# Tue, 05 Jul 2022 22:20:58 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 22:50:15 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 05 Jul 2022 22:50:56 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Tue, 05 Jul 2022 22:50:56 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Jul 2022 22:50:56 GMT
ENV LANG=en_US.UTF-8
# Thu, 21 Jul 2022 23:23:16 GMT
ENV JAVA_VERSION=19-ea+32
# Thu, 21 Jul 2022 23:23:26 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/32/GPL/openjdk-19-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='6c0b4944ebcb35d07dc3a8a2d8f947a7b9d78f1d4bc6ef6ff9076bf64c756677'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/32/GPL/openjdk-19-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='f8737a9614ca447d0f646a7680843edd8f98973b47191f7ecb487b26419edd82'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 21 Jul 2022 23:23:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:66fb3478003364657ac7751c40e41a135e02975f9459f652b1df23e3896b5fac`  
		Last Modified: Tue, 05 Jul 2022 22:22:18 GMT  
		Size: 48.8 MB (48762895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8f0f1eb3582fe120c104ded4086894e324ef46a631953f821f879e3e7a6a26`  
		Last Modified: Tue, 05 Jul 2022 22:58:49 GMT  
		Size: 14.2 MB (14245779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecd548616f52d5b1e3f763b187e0a584ead05af66c759da0202315b2261152e`  
		Last Modified: Thu, 21 Jul 2022 23:34:57 GMT  
		Size: 196.2 MB (196169355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d28723da22690a5573b03b420c793c8fb68fef13d02436d79d837ad46801a009
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259625948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd225f75b89f37f14cf9c0fcca26f883fcc061b52e7fc93bb392ee18aa6695e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 Jul 2022 22:43:37 GMT
ADD file:6d5eeb6c0921661dff8e0b6a89c3272aa52f72b5926d62ae482a85c8ef6458a3 in / 
# Tue, 05 Jul 2022 22:43:38 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 23:05:04 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 05 Jul 2022 23:06:33 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Tue, 05 Jul 2022 23:06:34 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Jul 2022 23:06:35 GMT
ENV LANG=en_US.UTF-8
# Thu, 21 Jul 2022 23:43:30 GMT
ENV JAVA_VERSION=19-ea+32
# Thu, 21 Jul 2022 23:43:50 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/32/GPL/openjdk-19-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='6c0b4944ebcb35d07dc3a8a2d8f947a7b9d78f1d4bc6ef6ff9076bf64c756677'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/32/GPL/openjdk-19-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='f8737a9614ca447d0f646a7680843edd8f98973b47191f7ecb487b26419edd82'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 21 Jul 2022 23:43:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:456ca0cbf3e695c518e5d5c4cb5ff9f99bb999a28b5ec7da3b4ca48d3cf80e6b`  
		Last Modified: Tue, 05 Jul 2022 22:45:10 GMT  
		Size: 49.3 MB (49342729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7981fd8b8b8e53f7977497096fa392e1d14f1e3dd10684ac47d3fa4688b887e7`  
		Last Modified: Tue, 05 Jul 2022 23:21:54 GMT  
		Size: 15.3 MB (15264543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4ebff069beebf32d37da3f0e752f90e039e35b20edaa5cae7bb7cb89f80e40`  
		Last Modified: Fri, 22 Jul 2022 00:03:41 GMT  
		Size: 195.0 MB (195018676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

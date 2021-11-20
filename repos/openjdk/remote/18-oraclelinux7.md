## `openjdk:18-oraclelinux7`

```console
$ docker pull openjdk@sha256:330467bfec2d0e87550455ccf5af767335e231533828e3029178b15106a72165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:157d4cccb9720ba91b63d5b1a2396c875bf8be5c9bc5e9908883beb33e7aacd4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.3 MB (252259574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b130f8c114ee9da346ac5174e2cde3822963ecfff1c03d28ed6d5e8f7edb3f28`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 28 Oct 2021 01:23:11 GMT
ADD file:1ba19f36d1d89d348cc182f0c7feb2c27bcca7bd084032525deaba8822462091 in / 
# Thu, 28 Oct 2021 01:23:11 GMT
CMD ["/bin/bash"]
# Thu, 28 Oct 2021 01:45:25 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 28 Oct 2021 01:45:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Thu, 28 Oct 2021 01:45:25 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Oct 2021 01:45:25 GMT
ENV LANG=en_US.UTF-8
# Fri, 19 Nov 2021 23:44:20 GMT
ENV JAVA_VERSION=18-ea+24
# Fri, 19 Nov 2021 23:44:31 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/24/GPL/openjdk-18-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='be728d2d5f8887ffc348d5a3293938e069c24be47e082a0b61aea61ce328aa03'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/24/GPL/openjdk-18-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='672dcbf3233da1ea245a7991fbeee867817d7024dc5c7e1b533240e642c27626'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 19 Nov 2021 23:44:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a755c2d4aa362701b6bb477a4b1cb2594cb0dca6d0e6839e07b0636fb824c7f7`  
		Last Modified: Thu, 28 Oct 2021 01:24:42 GMT  
		Size: 48.3 MB (48328962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d0464e417ebb82551686797f3772337ca857388f6f2209630af5603196a562`  
		Last Modified: Thu, 28 Oct 2021 01:53:12 GMT  
		Size: 15.4 MB (15399150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63820d966db5bc2b4a571295313ad313de79c02e10766a3ba99455a467cce4e2`  
		Last Modified: Fri, 19 Nov 2021 23:51:45 GMT  
		Size: 188.5 MB (188531462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:84da8d461d5841259a183049d6f97a046a5551dd44e017d603a169851182f6e5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252796855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f5b4d436118ed954a6b0184a147e8bf7750ef3eecf346eff91d1cad1c55f3b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 28 Oct 2021 01:44:12 GMT
ADD file:f997c704e003e7bef1e40d457d005aa07a60cb4c37255cc2711119deb3e6df7d in / 
# Thu, 28 Oct 2021 01:44:13 GMT
CMD ["/bin/bash"]
# Thu, 28 Oct 2021 02:16:09 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 28 Oct 2021 02:16:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Thu, 28 Oct 2021 02:16:11 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Oct 2021 02:16:12 GMT
ENV LANG=en_US.UTF-8
# Fri, 19 Nov 2021 23:04:42 GMT
ENV JAVA_VERSION=18-ea+24
# Fri, 19 Nov 2021 23:04:59 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/24/GPL/openjdk-18-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='be728d2d5f8887ffc348d5a3293938e069c24be47e082a0b61aea61ce328aa03'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/24/GPL/openjdk-18-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='672dcbf3233da1ea245a7991fbeee867817d7024dc5c7e1b533240e642c27626'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 19 Nov 2021 23:04:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9e1221f69ca9b4fd1daae21b9a20e7225f6ca7d0e34e9e998bc6600de1a3836a`  
		Last Modified: Thu, 28 Oct 2021 01:45:43 GMT  
		Size: 48.9 MB (48905370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b5770e043e6b3a738c83528c0b9c0c9be1c26e18eea50e4a5c270c853ccb2e`  
		Last Modified: Thu, 28 Oct 2021 02:29:48 GMT  
		Size: 16.5 MB (16454087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4462d9e24c5c369f0ef356f55f9f318f0d3f12f3541ebdd1bff78579cc660365`  
		Last Modified: Fri, 19 Nov 2021 23:17:25 GMT  
		Size: 187.4 MB (187437398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

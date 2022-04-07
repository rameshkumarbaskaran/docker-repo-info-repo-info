## `openjdk:19-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:0c223cdf8b70724c44dd7b746dcd7a452d0d0a231a61e7c896349257aafbe59f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:f78872a0ca1ada040758a0edc494863146acae50f9a5cdbfe43a7b55d0dd9d28
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.8 MB (248813881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c53518ac75cfefcaa56f6626d31f801e0f9702829a1a414e5d4533ac3ba4006`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Mar 2022 18:35:47 GMT
ADD file:eaa532cad071c531a759e73fd0fd381f440f180ab45b05a74314f10b0374df67 in / 
# Tue, 29 Mar 2022 18:35:47 GMT
CMD ["/bin/bash"]
# Tue, 29 Mar 2022 23:06:25 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 29 Mar 2022 23:06:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Tue, 29 Mar 2022 23:06:26 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 23:06:26 GMT
ENV LANG=C.UTF-8
# Thu, 07 Apr 2022 01:23:31 GMT
ENV JAVA_VERSION=19-ea+16
# Thu, 07 Apr 2022 01:24:03 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/16/GPL/openjdk-19-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='b05028cc6cc85bf33f794ced3ee4f4d319ab4763ef08791ac8150e8118af7625'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/16/GPL/openjdk-19-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='0ac68de33e762ed1768bbf8aa33e93aa2ce796b6034595cf70744b07031e7fc3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 07 Apr 2022 01:24:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e4430e06691f65e516df7d62db0ee5393acea9ade644cc6bc620efef0956dd17`  
		Last Modified: Tue, 29 Mar 2022 18:36:53 GMT  
		Size: 42.1 MB (42113609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ce5342b806de618f4fa582eca53ecee5a73ef976daa060d249227e1927d814`  
		Last Modified: Tue, 29 Mar 2022 23:18:03 GMT  
		Size: 13.5 MB (13524329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77df2c3f4f212d8ada91856c952adbaed46ead33f58f5e34cdaea5ff178c475`  
		Last Modified: Thu, 07 Apr 2022 01:32:15 GMT  
		Size: 193.2 MB (193175943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:de4efc83c752c2f656e9e0b7953ffc3314e5f322a28910eb8ee590d934a2f21c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248379473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c84c6b74a1af700014a94bdfa364108662d91ea1bdb63bdbcf847409b5dda95c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Mar 2022 18:27:10 GMT
ADD file:08d6d9fea731c201f517e2e96a93c19200773de2ddaa9bed138d10224f7d61e7 in / 
# Tue, 29 Mar 2022 18:27:11 GMT
CMD ["/bin/bash"]
# Wed, 30 Mar 2022 08:57:29 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 30 Mar 2022 08:57:29 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Wed, 30 Mar 2022 08:57:30 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:57:31 GMT
ENV LANG=C.UTF-8
# Thu, 07 Apr 2022 00:44:39 GMT
ENV JAVA_VERSION=19-ea+16
# Thu, 07 Apr 2022 00:45:00 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/16/GPL/openjdk-19-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='b05028cc6cc85bf33f794ced3ee4f4d319ab4763ef08791ac8150e8118af7625'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/16/GPL/openjdk-19-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='0ac68de33e762ed1768bbf8aa33e93aa2ce796b6034595cf70744b07031e7fc3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 07 Apr 2022 00:45:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:293fbd461d2c2a94e5d457aa3c7b18429b8457b06d5c2ad1a57113b1cac6d657`  
		Last Modified: Tue, 29 Mar 2022 18:28:25 GMT  
		Size: 42.0 MB (42019098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d200eb5167ed838a74239544d81e10c3d37a59ea571f23c1d6ed6e0c207cf997`  
		Last Modified: Wed, 30 Mar 2022 09:18:31 GMT  
		Size: 14.3 MB (14293802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c27ed3551e28cb4f901aa4314ecbbd3f759eae3e5a46ea84edfc5a0ac8f91df`  
		Last Modified: Thu, 07 Apr 2022 00:58:27 GMT  
		Size: 192.1 MB (192066573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

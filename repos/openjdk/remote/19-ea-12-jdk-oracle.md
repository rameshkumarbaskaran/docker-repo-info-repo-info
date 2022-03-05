## `openjdk:19-ea-12-jdk-oracle`

```console
$ docker pull openjdk@sha256:b74901b6c85c40e582aac91c96d2f800b79c61cb25eb9dcb9c55c48effefbc6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-ea-12-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:b0e57990b302ad85e7737b7eabc49c9936c4aa0bc69ad8d7cecc0f4186548475
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248437532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f55fff24a3ffde42f5e732eea425786b2e90270acdc4933b380ef36b792a7e1`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:20 GMT
ADD file:b6480acd933244be4e731db5554fd5341361b4d26356e9dea6db584cea3e137c in / 
# Fri, 25 Feb 2022 02:07:20 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 03:37:26 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 25 Feb 2022 03:37:26 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Fri, 25 Feb 2022 03:37:26 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Feb 2022 03:37:27 GMT
ENV LANG=C.UTF-8
# Sat, 05 Mar 2022 02:03:40 GMT
ENV JAVA_VERSION=19-ea+12
# Sat, 05 Mar 2022 02:04:06 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/12/GPL/openjdk-19-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='5bb24f4e4ddcb4a2a81f9a32174afccc0a94f0ba3fbd7b8e48212fc6091199ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/12/GPL/openjdk-19-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='f1b776f48f8612b3a60854a24d329a174266c2db4a9552a078652a6c495f4775'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 05 Mar 2022 02:04:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a2af32d411b4106f43f8ff56651eed59979576281483ccfb3b9f4a7cf1f5944b`  
		Last Modified: Fri, 25 Feb 2022 02:08:31 GMT  
		Size: 41.9 MB (41881280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab18c3f6beb4d98c3f94f4e60b6130e29bc5110daaf90f15eb717e0bd61a1cd6`  
		Last Modified: Fri, 25 Feb 2022 05:31:17 GMT  
		Size: 13.5 MB (13503410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d73d5f7b67a17972df53407d96cc7f8f31ebe159173f1c1e8b5e01ba8227685`  
		Last Modified: Sat, 05 Mar 2022 02:11:30 GMT  
		Size: 193.1 MB (193052842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-12-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:930f7129eb9b879735fd32cef1019e1ec7dab5c29487b22d7a56a8a263a0f89a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.3 MB (248339337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e552a1350b05145b00c0ec7fba3d151feb244c0aa12cc3fc3219d86f4f356ac7`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:20 GMT
ADD file:99a87d6732159802bc46dd7fcfa5c22f7bcb1faacab59f6e5b8c5284bd3ab861 in / 
# Fri, 25 Feb 2022 02:07:21 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 02:25:40 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 25 Feb 2022 02:25:41 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Fri, 25 Feb 2022 02:25:42 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Feb 2022 02:25:43 GMT
ENV LANG=C.UTF-8
# Sat, 05 Mar 2022 02:55:10 GMT
ENV JAVA_VERSION=19-ea+12
# Sat, 05 Mar 2022 02:55:25 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/12/GPL/openjdk-19-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='5bb24f4e4ddcb4a2a81f9a32174afccc0a94f0ba3fbd7b8e48212fc6091199ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/12/GPL/openjdk-19-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='f1b776f48f8612b3a60854a24d329a174266c2db4a9552a078652a6c495f4775'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 05 Mar 2022 02:55:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63ea605e0f838cb587cea4b75125afc43e9d339ddc5233440e9a29b7c5ba12d5`  
		Last Modified: Fri, 25 Feb 2022 02:08:42 GMT  
		Size: 42.0 MB (41951862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca767a5052236a4d74f577a368b70a4d1d5482f19c0b1c405b8fc19598510e3b`  
		Last Modified: Fri, 25 Feb 2022 02:47:46 GMT  
		Size: 14.3 MB (14304339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c02b918e48f4ce4c9126e571d58d99a7ca12c70bba18d45a88978acc67301b7a`  
		Last Modified: Sat, 05 Mar 2022 03:08:49 GMT  
		Size: 192.1 MB (192083136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

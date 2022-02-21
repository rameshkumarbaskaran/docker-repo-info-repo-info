## `openjdk:18-oraclelinux7`

```console
$ docker pull openjdk@sha256:c2e084d23b90cc5a3b60dc8492431a0eadd32ccc7fa5eebc7a41e4cd93877a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:b9c104f13360e3a47ec5f290a5be796cad4c0be66bfe2d5313d9a2c7038c4194
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252389591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf61a9c2b5e41474459719b6fc7892a4b0078a6bfa706a423d1b4e84edf2e04`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 12 Jan 2022 22:34:30 GMT
ADD file:18acb1f3ef1ffe1aeaff1aa22861026180d22104f6f14dd8bc4656777800fd9f in / 
# Wed, 12 Jan 2022 22:34:30 GMT
CMD ["/bin/bash"]
# Wed, 12 Jan 2022 22:51:37 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 12 Jan 2022 22:52:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Wed, 12 Jan 2022 22:52:20 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jan 2022 22:52:20 GMT
ENV LANG=en_US.UTF-8
# Mon, 21 Feb 2022 18:27:04 GMT
ENV JAVA_VERSION=18
# Mon, 21 Feb 2022 18:27:15 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-x64_bin.tar.gz'; 			downloadSha256='0f60aef7b8504983d6e374fe94d09a7bedcf05ec559e812d801a33bd4ebd23d0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-aarch64_bin.tar.gz'; 			downloadSha256='dff2860ba24c3f70f32ad3ac9b03f768dd28044bbda87c9607654fd03795c2ab'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 21 Feb 2022 18:27:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1e1d49338f200e5dab7ef55f9d3a37259af48812603e07ae59e43615f9038b27`  
		Last Modified: Wed, 12 Jan 2022 22:35:18 GMT  
		Size: 48.3 MB (48330956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c20bdba8622bf1a49d6c3edad81bd7ef39ec5a507eb70d2e536a70e60263ba4`  
		Last Modified: Wed, 12 Jan 2022 23:00:42 GMT  
		Size: 15.4 MB (15388577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec120dc46e92361aee17701725994c344c16adc489f00206ac6d9040348bdc8a`  
		Last Modified: Mon, 21 Feb 2022 18:38:39 GMT  
		Size: 188.7 MB (188670058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ad3ee28a3d8cf1272bd35206e0d431e2fc8c56a161f5cf044909a5634f869a0a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (252959710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a289caf526f0a56df0031bf5b1edcc1b566b32d03fe633b364cabc1b182f9700`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 12 Jan 2022 21:41:07 GMT
ADD file:64aef77ed2e10e924b07f118b92f579949f920597f01ce3580c3cd17fc289b87 in / 
# Wed, 12 Jan 2022 21:41:08 GMT
CMD ["/bin/bash"]
# Wed, 12 Jan 2022 21:58:19 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 12 Jan 2022 21:59:37 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Wed, 12 Jan 2022 21:59:37 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jan 2022 21:59:38 GMT
ENV LANG=en_US.UTF-8
# Mon, 21 Feb 2022 18:43:38 GMT
ENV JAVA_VERSION=18
# Mon, 21 Feb 2022 18:44:00 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-x64_bin.tar.gz'; 			downloadSha256='0f60aef7b8504983d6e374fe94d09a7bedcf05ec559e812d801a33bd4ebd23d0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-aarch64_bin.tar.gz'; 			downloadSha256='dff2860ba24c3f70f32ad3ac9b03f768dd28044bbda87c9607654fd03795c2ab'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 21 Feb 2022 18:44:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:89ad662320eff0a72aa4fc7f7af6e2a2ffe2dc642aacc7fcf25ada107b2cc3de`  
		Last Modified: Wed, 12 Jan 2022 21:42:00 GMT  
		Size: 48.9 MB (48902767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcbd5e1a30531d664d4f4f1f2c5a28be251ea96d8b492a51eabd8b7339c2f97`  
		Last Modified: Wed, 12 Jan 2022 22:12:56 GMT  
		Size: 16.5 MB (16464202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2dac3804d1196959287b2345add44b804295454c91041d1ef5c7416f2741466`  
		Last Modified: Mon, 21 Feb 2022 19:01:42 GMT  
		Size: 187.6 MB (187592741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

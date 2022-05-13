## `openjdk:19-ea-21-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:a81539ce8aeca1b07b0166e9667aa172f6750138244e12ea80e8ecaef237b92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-ea-21-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:414383a96ea60b3c56df4044e0f9b5686fcaec105b1484404ee3767097e548a8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257752294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fc1317702b17d212829afdf80ecbef403eacd2984e4a254545f70aeec1c3ad`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 12 May 2022 20:58:56 GMT
ADD file:8ac79c33c3bdf8a0a1c23cc009fabc3ead9d97891d701ad21090a6bc542521e2 in / 
# Thu, 12 May 2022 20:58:56 GMT
CMD ["/bin/bash"]
# Thu, 12 May 2022 22:41:56 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 12 May 2022 22:41:57 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Thu, 12 May 2022 22:41:57 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 May 2022 22:41:57 GMT
ENV LANG=en_US.UTF-8
# Thu, 12 May 2022 22:41:57 GMT
ENV JAVA_VERSION=19-ea+21
# Thu, 12 May 2022 22:42:09 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/21/GPL/openjdk-19-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='8723353dfc5a3dd34d01b96faddc950c48f450083519a62b287fcb1ef82fc446'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/21/GPL/openjdk-19-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='6e9719e928c6bfa2ed1e3ed7885bc2ff3751e0a8a6c5dde6808dddbd239cba32'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 12 May 2022 22:42:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd32cd816e68367704ec22e6e4d27af6a08b27e32aca3d0bd7a47424e37d0b91`  
		Last Modified: Thu, 12 May 2022 20:59:41 GMT  
		Size: 48.8 MB (48758049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d60946da119889a74d287d76661db4bd1631a2fbdcf7e72d140b5e4f25273b`  
		Last Modified: Thu, 12 May 2022 22:47:50 GMT  
		Size: 14.2 MB (14245376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c517280ab2abbb03b2c0c50e047177406b2d31cd4502e6d835704bf57a24a73a`  
		Last Modified: Thu, 12 May 2022 22:48:03 GMT  
		Size: 194.7 MB (194748869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-21-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2a033c12b1861f36a94821c15cf97d12281fd4481f78e0510434d0cdb2fc3a63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.2 MB (258221687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b857a3a8a5f143b039ebba2d4630b37c32795f7f88f06bf986bfa50ae5f411`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 12 May 2022 22:09:29 GMT
ADD file:b866e521d7e920b2210ec5ba4013715f28d1ad0636a38a13cec969d5b3586d44 in / 
# Thu, 12 May 2022 22:09:30 GMT
CMD ["/bin/bash"]
# Fri, 13 May 2022 00:26:03 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 13 May 2022 00:26:04 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Fri, 13 May 2022 00:26:05 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 May 2022 00:26:06 GMT
ENV LANG=en_US.UTF-8
# Fri, 13 May 2022 00:26:07 GMT
ENV JAVA_VERSION=19-ea+21
# Fri, 13 May 2022 00:26:26 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/21/GPL/openjdk-19-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='8723353dfc5a3dd34d01b96faddc950c48f450083519a62b287fcb1ef82fc446'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/21/GPL/openjdk-19-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='6e9719e928c6bfa2ed1e3ed7885bc2ff3751e0a8a6c5dde6808dddbd239cba32'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 13 May 2022 00:26:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fa569c775ec815d1a2d6e7b4f6e989b8afe4f0749c119d04101e4cb016365983`  
		Last Modified: Thu, 12 May 2022 22:10:25 GMT  
		Size: 49.3 MB (49340765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a850683079b99a0cee3fbeb957ff22bf46a963d7306f33b059cba19183ee75a`  
		Last Modified: Fri, 13 May 2022 00:37:40 GMT  
		Size: 15.3 MB (15269457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4744bcee98e2b01488a98c1e066fca41206462eb6606a9e9c1abd17f51f258`  
		Last Modified: Fri, 13 May 2022 00:37:55 GMT  
		Size: 193.6 MB (193611465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `openjdk:19-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:cdaa7b0f188510323dc4c8d22d2682019b7984cc6cde674c8d03659343fecd32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:e7111e57963a4ede84d62b076d5e5d7913a5afb883a87d01275b3329f9a6d2f9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256789530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f0d153b51435d6def9ce0f76e1cab3c11d8acdd0e0f0bc91fafc5f2537d55b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:48 GMT
ADD file:91284124cb9327f41cef52acd3563b18b3470a9c4354f2e2ecdf45e23330437f in / 
# Fri, 25 Feb 2022 02:07:49 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 03:38:09 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 25 Feb 2022 03:38:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Fri, 25 Feb 2022 03:38:10 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Feb 2022 03:38:10 GMT
ENV LANG=en_US.UTF-8
# Sat, 05 Mar 2022 02:04:12 GMT
ENV JAVA_VERSION=19-ea+12
# Sat, 05 Mar 2022 02:04:23 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/12/GPL/openjdk-19-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='5bb24f4e4ddcb4a2a81f9a32174afccc0a94f0ba3fbd7b8e48212fc6091199ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/12/GPL/openjdk-19-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='f1b776f48f8612b3a60854a24d329a174266c2db4a9552a078652a6c495f4775'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 05 Mar 2022 02:04:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:564e69ebc2e04e046f0b9f0d3a96822dabef192300736d02dc92c3f23e3fd084`  
		Last Modified: Fri, 25 Feb 2022 02:09:09 GMT  
		Size: 48.3 MB (48330862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a747076cd653f857a43ad06edf375d2d7f9d70470d618d826d9fd2239d9431e4`  
		Last Modified: Fri, 25 Feb 2022 05:32:07 GMT  
		Size: 15.4 MB (15402277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f003f0b973b8d32c7cc6d9565325000adebd11e24bb2b3d55135c85559ee41`  
		Last Modified: Sat, 05 Mar 2022 02:12:17 GMT  
		Size: 193.1 MB (193056391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:04bde8be23787fe4251924a43b836c5d4e271b75ca558500b6d82cbe629ea2ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.4 MB (257429341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6b9af422da9251be1fa0f23b1728884de7579fb42afeced03dbfcb3eefb9ec`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:48 GMT
ADD file:933bf8bd076f0c42499df14ceb4b409753b2ce9f8b0bd81331ac2630b6dab149 in / 
# Fri, 25 Feb 2022 02:07:49 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 02:27:32 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 25 Feb 2022 02:27:32 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Fri, 25 Feb 2022 02:27:33 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Feb 2022 02:27:34 GMT
ENV LANG=en_US.UTF-8
# Sat, 05 Mar 2022 02:55:38 GMT
ENV JAVA_VERSION=19-ea+12
# Sat, 05 Mar 2022 02:55:55 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/12/GPL/openjdk-19-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='5bb24f4e4ddcb4a2a81f9a32174afccc0a94f0ba3fbd7b8e48212fc6091199ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/12/GPL/openjdk-19-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='f1b776f48f8612b3a60854a24d329a174266c2db4a9552a078652a6c495f4775'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 05 Mar 2022 02:55:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5148c102f8614047b0330785165cb7096428df640af91104fbe61a7ebb5b8713`  
		Last Modified: Fri, 25 Feb 2022 02:09:24 GMT  
		Size: 48.9 MB (48901247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5afd0c7f5b0b7ae1e56ff4afb456806881a77fe14b8769883e0684cbcb9ac76`  
		Last Modified: Fri, 25 Feb 2022 02:48:54 GMT  
		Size: 16.4 MB (16445028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740c88b1ac6b9a4655d590e86935f4fe3f8dd7dc6ce4514b8c38d9d3ec3652bf`  
		Last Modified: Sat, 05 Mar 2022 03:09:49 GMT  
		Size: 192.1 MB (192083066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

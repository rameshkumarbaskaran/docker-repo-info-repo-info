## `openjdk:16-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:a212237b84b66a334e612c5ebe95a311a0e6e4b54ee41d079cb4f95a4b2eb43e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:16-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:a0738774faea0af0c02866d0d27bbd68f5db3ad4db785034d74b5e93548d446a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248444729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aad9d17d57792667385a5fd6bca457aac84ad43f7fc9090471b9821898e2c8d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 13 Oct 2021 18:30:19 GMT
ADD file:a6def617e1c0cf7def2d3ce3c79073621ed8efb37deed65fb49e7fc0a6d8ea37 in / 
# Wed, 13 Oct 2021 18:30:20 GMT
CMD ["/bin/bash"]
# Wed, 13 Oct 2021 18:48:31 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 13 Oct 2021 18:50:07 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Wed, 13 Oct 2021 18:50:07 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Oct 2021 18:50:07 GMT
ENV LANG=en_US.UTF-8
# Wed, 13 Oct 2021 18:50:08 GMT
ENV JAVA_VERSION=16.0.2
# Wed, 13 Oct 2021 18:50:19 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk16.0.2/d4a915d82b4c4fbb9bde534da945d746/7/GPL/openjdk-16.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='6c714ded7d881ca54970ec949e283f43d673a142fda1de79b646ddd619da9c0c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk16.0.2/d4a915d82b4c4fbb9bde534da945d746/7/GPL/openjdk-16.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='1ffb9c7748334945d9056b3324de3f797d906fce4dad86beea955153aa1e28fe'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 13 Oct 2021 18:50:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e0ada0403966475cc22d4e65b5fd1bde8aac848d542317ef0154b8961c767d23`  
		Last Modified: Wed, 13 Oct 2021 18:31:57 GMT  
		Size: 48.2 MB (48235779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4ebd61f33542411694b578674a48c8a09f401b78b67f813518bff7eb70dbbb`  
		Last Modified: Wed, 13 Oct 2021 18:57:37 GMT  
		Size: 15.4 MB (15397943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd949ccb20f6e5d50f3093e8f8e365288b3909fec2132f8cfaaf330bc8739785`  
		Last Modified: Wed, 13 Oct 2021 19:00:51 GMT  
		Size: 184.8 MB (184811007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0d940a19933cfa9aa0635ee175337e6ce0239e2e7c027382907b2846d084caab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244456763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46ddb8f04269eef29cb7fd483a5107042306e725cfb2839aae6e19085088aba`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 14 Oct 2021 03:43:46 GMT
ADD file:fca1474953cf608c9b2613787e7e7b859d458af91405a97dbd4ee57c63565185 in / 
# Thu, 14 Oct 2021 03:43:47 GMT
CMD ["/bin/bash"]
# Thu, 14 Oct 2021 05:43:29 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 14 Oct 2021 05:46:07 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Thu, 14 Oct 2021 05:46:08 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Oct 2021 05:46:09 GMT
ENV LANG=en_US.UTF-8
# Thu, 14 Oct 2021 05:46:10 GMT
ENV JAVA_VERSION=16.0.2
# Thu, 14 Oct 2021 05:46:25 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk16.0.2/d4a915d82b4c4fbb9bde534da945d746/7/GPL/openjdk-16.0.2_linux-x64_bin.tar.gz'; 			downloadSha256='6c714ded7d881ca54970ec949e283f43d673a142fda1de79b646ddd619da9c0c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk16.0.2/d4a915d82b4c4fbb9bde534da945d746/7/GPL/openjdk-16.0.2_linux-aarch64_bin.tar.gz'; 			downloadSha256='1ffb9c7748334945d9056b3324de3f797d906fce4dad86beea955153aa1e28fe'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 14 Oct 2021 05:46:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1322b24b1fa49fc9b6d0dad59ae623077ce5c89f6aca858053f6d7e45222e954`  
		Last Modified: Thu, 14 Oct 2021 03:45:17 GMT  
		Size: 48.8 MB (48820013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15dfa211810869c7e6ae1a8fdb375623b16dc354d9e55dd50190c994ba3b3263`  
		Last Modified: Thu, 14 Oct 2021 05:58:58 GMT  
		Size: 16.4 MB (16447841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45283f793e1297a09d40f0310d506bacec95a66d6fa65802ae60520018357e6`  
		Last Modified: Thu, 14 Oct 2021 06:02:39 GMT  
		Size: 179.2 MB (179188909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

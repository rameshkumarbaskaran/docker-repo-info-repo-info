## `openjdk:20-ea-3-oraclelinux7`

```console
$ docker pull openjdk@sha256:68f8402dc5f75df5dfd68108960feb4576f3ca12c688db84411243a04919897e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-3-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:124a97de44eff9cf18483dacc75dacf477774c06e5acfa7fef1857a4542c7e8a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260147579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de641d5693675f503a9dcb9e02f7771acadddc19a8a44456b8ade7be9c60cdf`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Jun 2022 01:20:22 GMT
ADD file:5e615d6d49ec50cba937fa86f5fb7d6a4a7e680b2b4f5b659e879b95304c0417 in / 
# Thu, 16 Jun 2022 01:20:22 GMT
CMD ["/bin/bash"]
# Tue, 28 Jun 2022 00:27:27 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 28 Jun 2022 00:27:28 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Tue, 28 Jun 2022 00:27:28 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jun 2022 00:27:28 GMT
ENV LANG=en_US.UTF-8
# Tue, 28 Jun 2022 00:27:28 GMT
ENV JAVA_VERSION=20-ea+3
# Tue, 28 Jun 2022 00:27:50 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/3/GPL/openjdk-20-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='8f930cbbf2c85c0cfe87eef8646d1e038fe51d19132613e868e96118b1e0f8d0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/3/GPL/openjdk-20-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='d7b270b059fe08487492d38760e0e821b3a7be20864205d7ab0b5e5206109bda'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 28 Jun 2022 00:27:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63183c9b4598e16c4cef95f706d50ff6c928de41f391cd513495b27eaa27bf89`  
		Last Modified: Thu, 16 Jun 2022 01:21:08 GMT  
		Size: 48.8 MB (48757931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27f2a0cb669162a36b2576cd36536ebb88d2e0ccedba24fe92c1b0a992569e5`  
		Last Modified: Tue, 28 Jun 2022 00:38:26 GMT  
		Size: 14.2 MB (14236080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4d7ac8f26782f398f7b206d6b488b5b2abceb969fafdbddaa7a2e8d110c1a7`  
		Last Modified: Tue, 28 Jun 2022 00:38:39 GMT  
		Size: 197.2 MB (197153568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-3-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7420775eeab2534536debe4a8b5c3ed753782d2b77f92b81993fc39970f8db11
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.6 MB (260601127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a1a5441434caaf2189679ef945e787c5f58126f54b9e0fdf4763166d446134`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Jun 2022 01:12:02 GMT
ADD file:3c802f9fbd1a9a4878df064e2b268b017930633407658a3f9d29e53eb74552fa in / 
# Thu, 16 Jun 2022 01:12:03 GMT
CMD ["/bin/bash"]
# Tue, 28 Jun 2022 00:41:52 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 28 Jun 2022 00:41:52 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Tue, 28 Jun 2022 00:41:53 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jun 2022 00:41:54 GMT
ENV LANG=en_US.UTF-8
# Tue, 28 Jun 2022 00:41:55 GMT
ENV JAVA_VERSION=20-ea+3
# Tue, 28 Jun 2022 00:42:12 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/3/GPL/openjdk-20-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='8f930cbbf2c85c0cfe87eef8646d1e038fe51d19132613e868e96118b1e0f8d0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/3/GPL/openjdk-20-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='d7b270b059fe08487492d38760e0e821b3a7be20864205d7ab0b5e5206109bda'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 28 Jun 2022 00:42:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9071f63390163e069a5245aea05c5a92f0dd4a4a48483db57c4c3c0d557be5e7`  
		Last Modified: Thu, 16 Jun 2022 01:12:57 GMT  
		Size: 49.3 MB (49343296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e959388b0464e301c8f837d6139ee9789051dee894111f69643a0c73900dfa9`  
		Last Modified: Tue, 28 Jun 2022 00:59:49 GMT  
		Size: 15.3 MB (15265029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a9a1412d21ef1408c6befde35ffee833fefa23442010bbb726ddb4b238c7c5`  
		Last Modified: Tue, 28 Jun 2022 01:00:06 GMT  
		Size: 196.0 MB (195992802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

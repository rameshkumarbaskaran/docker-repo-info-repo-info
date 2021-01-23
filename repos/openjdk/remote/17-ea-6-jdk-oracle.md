## `openjdk:17-ea-6-jdk-oracle`

```console
$ docker pull openjdk@sha256:02406d17bdeb2308311aef58c63553c229c59bd8fa70e1e0236f0db7f92d2b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:17-ea-6-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:c9d187577eb44c77e1526eab742dc3d1048dee881320a852780abc767dc433c3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (241003057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c765036142afd56dec1f02119f61be06e43a9fcfed3ec2b3f465ec025f4be2cc`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Jan 2021 00:30:38 GMT
ADD file:2987f8143a9c4f758731c17e307a6c7ca9e5e1a974df3405a17d2699da7d8351 in / 
# Fri, 15 Jan 2021 00:30:39 GMT
CMD ["/bin/bash"]
# Fri, 15 Jan 2021 00:56:52 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 15 Jan 2021 00:56:53 GMT
ENV LANG=C.UTF-8
# Fri, 15 Jan 2021 00:56:53 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Fri, 15 Jan 2021 00:56:53 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Jan 2021 01:20:53 GMT
ENV JAVA_VERSION=17-ea+6
# Sat, 23 Jan 2021 01:21:53 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk17/6/GPL/openjdk-17-ea+6_linux-aarch64_bin.tar.gz; 			downloadSha256=fc7ad87123841b528112c6fa94883b28dc3bb0ea174d3a3795fe2c2873a68f6f; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk17/6/GPL/openjdk-17-ea+6_linux-x64_bin.tar.gz; 			downloadSha256=f9082a010d2be7b1a1b462d86345d797f311bde30ddf2ccefe7e718ec49de334; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 23 Jan 2021 01:21:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a73adebe9317092fb1f120a1d0d21f460296e9bde7ac683fd452cfc628c528cf`  
		Last Modified: Wed, 06 Jan 2021 20:23:26 GMT  
		Size: 42.1 MB (42069921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b73bcd34cfec7fc27d7cd00bc22af06df0471526a6d2ceb8e77391a82f300f0`  
		Last Modified: Fri, 15 Jan 2021 01:08:29 GMT  
		Size: 13.3 MB (13277589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493be4992cb769d2ae7c819461bc2d4fcf9c2667012a06335b602e7d223e25d5`  
		Last Modified: Sat, 23 Jan 2021 01:29:26 GMT  
		Size: 185.7 MB (185655547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-ea-6-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a2676c4b9687256bfd7bedda1c434fc03c745e5822c46389be0a71249db7765c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236081698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95273f4d922a3eeb3f806a529f284fa0c6b0415f7d58e0a1e8482f7d4475297`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Jan 2021 00:05:48 GMT
ADD file:ad2b2ddca8e17229cc8d1380ecda32c4b2c04f1e2aed8f493f745c6352b34e60 in / 
# Fri, 15 Jan 2021 00:05:49 GMT
CMD ["/bin/bash"]
# Fri, 15 Jan 2021 00:43:36 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 15 Jan 2021 00:43:38 GMT
ENV LANG=C.UTF-8
# Fri, 15 Jan 2021 00:43:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Fri, 15 Jan 2021 00:43:39 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Jan 2021 01:41:26 GMT
ENV JAVA_VERSION=17-ea+6
# Sat, 23 Jan 2021 01:42:17 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk17/6/GPL/openjdk-17-ea+6_linux-aarch64_bin.tar.gz; 			downloadSha256=fc7ad87123841b528112c6fa94883b28dc3bb0ea174d3a3795fe2c2873a68f6f; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk17/6/GPL/openjdk-17-ea+6_linux-x64_bin.tar.gz; 			downloadSha256=f9082a010d2be7b1a1b462d86345d797f311bde30ddf2ccefe7e718ec49de334; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 23 Jan 2021 01:42:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d0eecbd2c3e7306adbf5b4a0d9bebc7d266ebe78bda044d35b0994c1cf655a54`  
		Last Modified: Wed, 06 Jan 2021 20:47:00 GMT  
		Size: 42.0 MB (41996293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8f86f1d6521cdc8416801b8dd0b15d9a5a85bfa3eb8f9afa832aa8cc652732`  
		Last Modified: Fri, 15 Jan 2021 00:55:15 GMT  
		Size: 14.1 MB (14057398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78e30b9c900d42c704f6fa328fab53959b870dc32dbb61458833e1b6c5bfd45`  
		Last Modified: Sat, 23 Jan 2021 01:52:05 GMT  
		Size: 180.0 MB (180028007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

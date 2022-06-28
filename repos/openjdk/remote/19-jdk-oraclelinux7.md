## `openjdk:19-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:6c73689953e789bcd3b63cf9b3b640596b5084a3443ba5a02ec8ad796b53ecb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:bfc1b2d12d6c8735fceef2ab99b2da5862a71fdd8534be9e8f8a121face93b37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 MB (259143974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd311c3693f6724d95af70f7ffcdc663757e92b9c932f1ddd91600608db7102`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Jun 2022 01:20:22 GMT
ADD file:5e615d6d49ec50cba937fa86f5fb7d6a4a7e680b2b4f5b659e879b95304c0417 in / 
# Thu, 16 Jun 2022 01:20:22 GMT
CMD ["/bin/bash"]
# Tue, 28 Jun 2022 00:27:27 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 28 Jun 2022 00:29:46 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Tue, 28 Jun 2022 00:29:46 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jun 2022 00:29:46 GMT
ENV LANG=en_US.UTF-8
# Tue, 28 Jun 2022 00:29:46 GMT
ENV JAVA_VERSION=19-ea+28
# Tue, 28 Jun 2022 00:29:56 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/28/GPL/openjdk-19-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='4a6c13cb4b548d924142b11ae8fbff7f5a9c2813f7663023389866e8c15cd2ee'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/28/GPL/openjdk-19-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='f553cff91a88a315ad6af41f8c7a4a4b7b72a2bec9886e136841f2bedd87421d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 28 Jun 2022 00:29:57 GMT
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
	-	`sha256:b2d59ecd3407f7d053e3df1e5d9baf873ffc3f35bcef2ccea36c9e5bc9d50a3d`  
		Last Modified: Tue, 28 Jun 2022 00:42:49 GMT  
		Size: 196.1 MB (196149963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7e0bdbae06064e3fbe21cf6e782ec73e0e28cde8aaf8acabe87574780d716cb5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259588581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fbf216589864a1312297c7b6fe057364bfc09f01b919f5522bc251ddfd2b23`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Jun 2022 01:12:02 GMT
ADD file:3c802f9fbd1a9a4878df064e2b268b017930633407658a3f9d29e53eb74552fa in / 
# Thu, 16 Jun 2022 01:12:03 GMT
CMD ["/bin/bash"]
# Tue, 28 Jun 2022 00:41:52 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 28 Jun 2022 00:44:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Tue, 28 Jun 2022 00:44:26 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jun 2022 00:44:27 GMT
ENV LANG=en_US.UTF-8
# Tue, 28 Jun 2022 00:44:28 GMT
ENV JAVA_VERSION=19-ea+28
# Tue, 28 Jun 2022 00:44:46 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/28/GPL/openjdk-19-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='4a6c13cb4b548d924142b11ae8fbff7f5a9c2813f7663023389866e8c15cd2ee'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/28/GPL/openjdk-19-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='f553cff91a88a315ad6af41f8c7a4a4b7b72a2bec9886e136841f2bedd87421d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 28 Jun 2022 00:44:46 GMT
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
	-	`sha256:d4c5ca9ccb92211d1e69439b33dea5e12bf078de51276d5a502915c3b1a52083`  
		Last Modified: Tue, 28 Jun 2022 01:05:08 GMT  
		Size: 195.0 MB (194980256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `openjdk:19-ea-13-jdk-oracle`

```console
$ docker pull openjdk@sha256:886539a199530900a418ac4362a4690308fdfc0b8bfbe3d1586599cd5b391c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-ea-13-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:366ea2ccea1839541fe069dfa38d7a478811121b860c3cd9e400092af2d5f00b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 MB (248461952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783f1afbd8f6487c64e90beb205708722003ad646d5d417a69faf18cebc57694`
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
# Mon, 14 Mar 2022 20:13:51 GMT
ENV JAVA_VERSION=19-ea+13
# Mon, 14 Mar 2022 20:14:17 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='6aff2a07ccdd649641741facf16a0001568e7af829e0e8cbd1257db42b6911f4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2b13aabf01d1fad49c3dd5cde37bb53683a97b33d3d58030c10e1fad270f8c76'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 14 Mar 2022 20:14:18 GMT
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
	-	`sha256:e79769d8f651f7d59f4c971eafa5b12d405195ba37d62b5e6044a7f04fc5c3f2`  
		Last Modified: Mon, 14 Mar 2022 20:21:40 GMT  
		Size: 193.1 MB (193077262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-13-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d56c3b9a38f939c4f67b526a5064a9c5502978cb38b3d3faf9e8339200bfcd0c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248370692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b64375a5c163df45eba3e5a6b21e1e61bc8736127a076b484723c91a3053bd`
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
# Mon, 14 Mar 2022 19:04:42 GMT
ENV JAVA_VERSION=19-ea+13
# Mon, 14 Mar 2022 19:05:00 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='6aff2a07ccdd649641741facf16a0001568e7af829e0e8cbd1257db42b6911f4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2b13aabf01d1fad49c3dd5cde37bb53683a97b33d3d58030c10e1fad270f8c76'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 14 Mar 2022 19:05:00 GMT
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
	-	`sha256:fd09006ab7f6aebcc7f828bcf45721c3205c40c5724d48ca3793fb36ab20466e`  
		Last Modified: Mon, 14 Mar 2022 19:18:23 GMT  
		Size: 192.1 MB (192114491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

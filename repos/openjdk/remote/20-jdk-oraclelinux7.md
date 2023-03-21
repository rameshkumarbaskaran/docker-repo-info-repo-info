## `openjdk:20-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:080cb15ba494a7cc562b00b2f8bff2c320c4707c0ce8f64068bd41d0093a3387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:ce65761a7b2a0e7c1932e7c157cf8bf5c7ea1d9c407f1b81118053f8d8ac8fb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.9 MB (262851148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2d7e3d4f1ef5b33cdaeea90be94d88131897fc7ea51895e2f10b722e3e073d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Mar 2023 19:26:42 GMT
ADD file:c2562ae661b3cd914b2c0dd27aba7ee36bffbeb92415b7b80c111a5d563d07ed in / 
# Tue, 21 Mar 2023 19:26:43 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2023 20:47:46 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 21 Mar 2023 20:48:08 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Tue, 21 Mar 2023 20:48:09 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Mar 2023 20:48:09 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Mar 2023 20:48:09 GMT
ENV JAVA_VERSION=20
# Tue, 21 Mar 2023 20:48:19 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk20/bdc68b4b9cbc4ebcb30745c85038d91d/36/GPL/openjdk-20_linux-x64_bin.tar.gz'; 			downloadSha256='bb863b2d542976d1ae4b7b81af3e78b1e4247a64644350b552d298d8dc5980dc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk20/bdc68b4b9cbc4ebcb30745c85038d91d/36/GPL/openjdk-20_linux-aarch64_bin.tar.gz'; 			downloadSha256='b671dd1513e7bd4f3de6b1424a90a4998997a67593bf259936d55f5e83e31959'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 21 Mar 2023 20:48:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ec521688c56b41126476e7ab1f7ab7305384f5b5326e80a8ba52b8d4deead22`  
		Last Modified: Tue, 21 Mar 2023 19:27:26 GMT  
		Size: 50.5 MB (50471128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea283652a57d33ca137043965b4c70fa3e5d30b9487b344159545deda829f9b`  
		Last Modified: Tue, 21 Mar 2023 20:49:09 GMT  
		Size: 14.3 MB (14252036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ecb184b93656a6e820be5a0b5c6b3011d8068a835addaee5c011c070f7a52fa`  
		Last Modified: Tue, 21 Mar 2023 20:50:01 GMT  
		Size: 198.1 MB (198127984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e8286cfcef98a780d2a1e91107274ff760c52e68d19014761c2a08d6a7b5f0ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.9 MB (262905634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a7bc0f1183d5cc737d4211c75fa7f6bd49cf06f4c3578a7389c57f6e47e9d2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Mar 2023 19:44:52 GMT
ADD file:a9428dda3ec7ae554537bb583832aa2d30484c863bf95c68e460df5858c4c0bf in / 
# Tue, 21 Mar 2023 19:44:53 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2023 21:03:26 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 21 Mar 2023 21:03:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Tue, 21 Mar 2023 21:03:49 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Mar 2023 21:03:49 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Mar 2023 21:03:49 GMT
ENV JAVA_VERSION=20
# Tue, 21 Mar 2023 21:04:00 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk20/bdc68b4b9cbc4ebcb30745c85038d91d/36/GPL/openjdk-20_linux-x64_bin.tar.gz'; 			downloadSha256='bb863b2d542976d1ae4b7b81af3e78b1e4247a64644350b552d298d8dc5980dc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk20/bdc68b4b9cbc4ebcb30745c85038d91d/36/GPL/openjdk-20_linux-aarch64_bin.tar.gz'; 			downloadSha256='b671dd1513e7bd4f3de6b1424a90a4998997a67593bf259936d55f5e83e31959'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 21 Mar 2023 21:04:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:41dbc375a859f3e982b6147e2fd05b413e6995b4b728c27f1b851f64a31c004c`  
		Last Modified: Tue, 21 Mar 2023 19:45:30 GMT  
		Size: 51.0 MB (51027591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d7ddfee215622f57465bb8dace7332092902d9c16c5bfa61ec64821d8cbb5c`  
		Last Modified: Tue, 21 Mar 2023 21:04:45 GMT  
		Size: 15.2 MB (15249122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5bd21b267f5353b1e34222e0b601bdac080366d7024a855065e2812e52f8436`  
		Last Modified: Tue, 21 Mar 2023 21:05:32 GMT  
		Size: 196.6 MB (196628921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

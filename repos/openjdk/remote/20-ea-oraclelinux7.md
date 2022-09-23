## `openjdk:20-ea-oraclelinux7`

```console
$ docker pull openjdk@sha256:9b23acda7161f4b929766966ed3ba10d8c29d085838df18a0a38172a1a67b865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:92f43cfa687be3f0664a6b5acd01e22d8d9cd5175150731652aedfe81b275f17
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260854277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a511fe90c925d11d4617bfeaee3803a3a25a8efc692f78ff60b4ca5c4da0919`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 22 Sep 2022 18:21:00 GMT
ADD file:bc2c7ba728e9e4bfc9aa5e6072db4cbab3cadbd76aff485b6afd233dcdfbdb1e in / 
# Thu, 22 Sep 2022 18:21:00 GMT
CMD ["/bin/bash"]
# Thu, 22 Sep 2022 18:37:37 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 22 Sep 2022 18:37:37 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Thu, 22 Sep 2022 18:37:37 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Sep 2022 18:37:37 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 Sep 2022 00:33:13 GMT
ENV JAVA_VERSION=20-ea+16
# Fri, 23 Sep 2022 00:33:26 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/16/GPL/openjdk-20-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='d344bfe23128ba5fd037d6de49cb434376becafdbcf5e7b506fbe5294681c695'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/16/GPL/openjdk-20-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='2d21dff3559d40a9100d98d4ca3d9b07f77f7e0dfea8273b09d4be7f22794fac'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Sep 2022 00:33:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a2a00260331c858dbb0d8dae185769162dbb3e7cb3342d52798d837e7a156c45`  
		Last Modified: Thu, 22 Sep 2022 18:21:50 GMT  
		Size: 49.8 MB (49796793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00f9fe80a003e345fd0fbed09df87921267e2893a69170bde00961786a40f31`  
		Last Modified: Thu, 22 Sep 2022 18:40:40 GMT  
		Size: 14.2 MB (14223074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36609c4cb3c53acf812a3a502acbb1f9989a7f6f6e68e386446b7c0e56612619`  
		Last Modified: Fri, 23 Sep 2022 00:38:01 GMT  
		Size: 196.8 MB (196834410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3d9d2ec70f2fcc93282001942d6959ff034f7235e265a870b90758c12313543f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261059378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9841dd38b010b58f5bf018ae89df249d40217080e5a2f63ec3d37a1ae6a7cec`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 22 Sep 2022 18:41:04 GMT
ADD file:fd12a0d7821d135c61925e186ce7d33634745a38f1db7d39d2f06a27585fbeab in / 
# Thu, 22 Sep 2022 18:41:05 GMT
CMD ["/bin/bash"]
# Thu, 22 Sep 2022 19:00:03 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 22 Sep 2022 19:00:03 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Thu, 22 Sep 2022 19:00:04 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Sep 2022 19:00:05 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 Sep 2022 00:51:05 GMT
ENV JAVA_VERSION=20-ea+16
# Fri, 23 Sep 2022 00:51:22 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/16/GPL/openjdk-20-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='d344bfe23128ba5fd037d6de49cb434376becafdbcf5e7b506fbe5294681c695'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/16/GPL/openjdk-20-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='2d21dff3559d40a9100d98d4ca3d9b07f77f7e0dfea8273b09d4be7f22794fac'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Sep 2022 00:51:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63b915e1b20e56956b453bc1d5b77fa94f0901ef3367114af0ce6baff9e507a3`  
		Last Modified: Thu, 22 Sep 2022 18:42:03 GMT  
		Size: 50.4 MB (50377925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c29288401cec214da58d603f66600fe99310ca836e0f5a37863ecb4d0cc448`  
		Last Modified: Thu, 22 Sep 2022 19:06:21 GMT  
		Size: 15.3 MB (15263714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be047b34b15a0dd53f4e9902ea515431479ef57b9ee079a00f9ec0f1c8298199`  
		Last Modified: Fri, 23 Sep 2022 00:58:58 GMT  
		Size: 195.4 MB (195417739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

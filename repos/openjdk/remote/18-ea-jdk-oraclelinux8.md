## `openjdk:18-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:30882929002f549ea15d4fdc02c0fb2080ef9ae157d6c9fb949e1dcf737554da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:4bb73c25d5c1b643d96548f49189789c8dce599aceae9a9dab0b63748f684c44
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243806926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157c4e76f36104f701713c2f9fabac3290c0a35c8ac634afd535cfff61006c03`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Nov 2021 16:05:57 GMT
ADD file:977d9a2c7a8ab07ec719edd585faf23ef08768a09abf97a80d62d2091936b052 in / 
# Thu, 18 Nov 2021 16:05:58 GMT
CMD ["/bin/bash"]
# Thu, 18 Nov 2021 17:33:38 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 18 Nov 2021 17:33:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Thu, 18 Nov 2021 17:33:39 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 17:33:39 GMT
ENV LANG=C.UTF-8
# Thu, 18 Nov 2021 17:33:39 GMT
ENV JAVA_VERSION=18-ea+23
# Thu, 18 Nov 2021 17:33:59 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/23/GPL/openjdk-18-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='e9f310e519b12280fc023ab4b734e533377e212ae77da8981f462c2849851316'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/23/GPL/openjdk-18-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='11b235ab4e5dc79031e5c08593080c58ec66b96b530e023e5c789b040d0095a3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 18 Nov 2021 17:34:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0a39cfde620ea7949c12d65ef5a24d4b6f737bb5a2f57d9a4a16013c060c9c67`  
		Last Modified: Thu, 18 Nov 2021 16:07:11 GMT  
		Size: 42.1 MB (42098006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a90c9cadc5331c54e5f53b906e967fe1942c54666e8da9bf055c378d02b2ad`  
		Last Modified: Thu, 18 Nov 2021 17:43:13 GMT  
		Size: 13.5 MB (13511675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6da1fe6812ea2ec39f0250dc78349d20476a44d1a7aa035090a48755ce177e7`  
		Last Modified: Thu, 18 Nov 2021 17:43:29 GMT  
		Size: 188.2 MB (188197245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2a8fa2dc7aefe403176754aba789bbf4c1d8e44d9c44b7caa8f4a535f3228b9f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243435930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6f1ffeac55988ad3f47890ff834fe612c02e41fe80424425f3a63774738987`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Nov 2021 08:24:53 GMT
ADD file:98b355b05026edaab234cff8ee34d8335b233cbaa04a19ac82df4a2b0c7fdc4d in / 
# Thu, 18 Nov 2021 08:24:54 GMT
CMD ["/bin/bash"]
# Thu, 18 Nov 2021 10:14:56 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 18 Nov 2021 10:14:57 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Thu, 18 Nov 2021 10:14:58 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 10:14:59 GMT
ENV LANG=C.UTF-8
# Thu, 18 Nov 2021 10:15:00 GMT
ENV JAVA_VERSION=18-ea+23
# Thu, 18 Nov 2021 10:15:11 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/23/GPL/openjdk-18-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='e9f310e519b12280fc023ab4b734e533377e212ae77da8981f462c2849851316'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/23/GPL/openjdk-18-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='11b235ab4e5dc79031e5c08593080c58ec66b96b530e023e5c789b040d0095a3'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 18 Nov 2021 10:15:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1bdb3a9e404c972ab03f65fd56b5b815b51d6a68324015dc69707d48e2ba3cdf`  
		Last Modified: Thu, 18 Nov 2021 08:26:02 GMT  
		Size: 42.0 MB (42010198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9356b5c0bb88b90b52af9c2836e152e11b910a0e88807e8327df1e2a965a7d1`  
		Last Modified: Thu, 18 Nov 2021 10:27:05 GMT  
		Size: 14.3 MB (14300065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ef24cabbf88317b7f8d03e6274850f4c3806362ffed88512f6703824acbb0e`  
		Last Modified: Thu, 18 Nov 2021 10:27:21 GMT  
		Size: 187.1 MB (187125667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `openjdk:20-oraclelinux8`

```console
$ docker pull openjdk@sha256:bf6d1522d515146eb49ca9dcb7499a67ea8706d9500700381aa662402cd47dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:e2f179028bf2ac2c9804d6279bdc2939f5f04d2bee6e6ecbeb78eb5b1a267427
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 MB (249658711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563d3b4bce0639044aafb9ee8b46bb3707055f051efde7458eeedfe837a3eccd`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Sep 2022 21:20:28 GMT
ADD file:e00d9d8d8f616feec8c064f2250e4836ea3b533ead0611d1af2245974abb4e88 in / 
# Wed, 14 Sep 2022 21:20:28 GMT
CMD ["/bin/bash"]
# Wed, 14 Sep 2022 21:37:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 14 Sep 2022 21:37:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Wed, 14 Sep 2022 21:37:14 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Sep 2022 21:37:14 GMT
ENV LANG=C.UTF-8
# Fri, 23 Sep 2022 00:28:35 GMT
ENV JAVA_VERSION=20-ea+16
# Fri, 23 Sep 2022 00:33:04 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/16/GPL/openjdk-20-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='d344bfe23128ba5fd037d6de49cb434376becafdbcf5e7b506fbe5294681c695'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/16/GPL/openjdk-20-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='2d21dff3559d40a9100d98d4ca3d9b07f77f7e0dfea8273b09d4be7f22794fac'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Sep 2022 00:33:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:051f419db9dd9462e8995886d24f592c26cef792cc915dfbc7548e0b19aa55fe`  
		Last Modified: Wed, 14 Sep 2022 21:21:25 GMT  
		Size: 40.6 MB (40590248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa51c6010a14c1984cbdea1332a5d2f77bf6e0141bc497b44dca611e21f9b391`  
		Last Modified: Wed, 14 Sep 2022 21:41:16 GMT  
		Size: 12.2 MB (12232427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170948c9d5de83d9eaf3aef02c1c16877cd0df7b0f08a41ba3b17042ba20bac8`  
		Last Modified: Fri, 23 Sep 2022 00:37:13 GMT  
		Size: 196.8 MB (196836036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2ef287a36b37a30c1c7f8a0fed4bc78cb84fc679567aedd55584bca309c70b68
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 MB (247882875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67700239f50c69173cb8d864016ee5805c026ed4f115266e2ff8ef327a2b4018`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Sep 2022 21:41:16 GMT
ADD file:30401488699aa4b911abaeec83f0938e0fede937c09940369ec58cc56eae4624 in / 
# Wed, 14 Sep 2022 21:41:17 GMT
CMD ["/bin/bash"]
# Wed, 14 Sep 2022 22:01:28 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 14 Sep 2022 22:01:28 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Wed, 14 Sep 2022 22:01:29 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Sep 2022 22:01:30 GMT
ENV LANG=C.UTF-8
# Fri, 23 Sep 2022 00:50:20 GMT
ENV JAVA_VERSION=20-ea+16
# Fri, 23 Sep 2022 00:50:51 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/16/GPL/openjdk-20-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='d344bfe23128ba5fd037d6de49cb434376becafdbcf5e7b506fbe5294681c695'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/16/GPL/openjdk-20-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='2d21dff3559d40a9100d98d4ca3d9b07f77f7e0dfea8273b09d4be7f22794fac'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 23 Sep 2022 00:50:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9a8b791677e1fdf76ff862b55362355b48c8636d0eabf606d1af65888ab73ec8`  
		Last Modified: Wed, 14 Sep 2022 21:42:22 GMT  
		Size: 39.4 MB (39409909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1458b25adde8441e97a5f07c35975478bc0d77410ada29b87b31f52fbbaf994`  
		Last Modified: Wed, 14 Sep 2022 22:09:27 GMT  
		Size: 13.1 MB (13055052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4614eb61bfdddcf36b1e60cbef013e1bd129fbb885a7dd3d6fa4a5b36213ec`  
		Last Modified: Fri, 23 Sep 2022 00:58:01 GMT  
		Size: 195.4 MB (195417914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `openjdk:21-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:84da747d9d906553839dc0108b7b1271607a363989637cfa293e32860d5834eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:1021056a31b73417e6624d8145bc62bb8014b2e3aa40be93f8f6894c4137bfda
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262787179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52aa27f3d3bf71858e6f124070d7c50d6851b2f7efb617005d5528f14d64d3fe`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 May 2023 21:20:28 GMT
ADD file:e15c235506d8dd134e69d458a7c0afefef1522e9d0cfb28e3538760ddf032785 in / 
# Wed, 24 May 2023 21:20:29 GMT
CMD ["/bin/bash"]
# Wed, 24 May 2023 21:44:56 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 24 May 2023 21:44:56 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Wed, 24 May 2023 21:44:56 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 May 2023 21:44:56 GMT
ENV LANG=C.UTF-8
# Wed, 24 May 2023 21:44:56 GMT
ENV JAVA_VERSION=21-ea+23
# Wed, 24 May 2023 21:45:06 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/23/GPL/openjdk-21-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='f3644497f76a889a341866ea29e2b3ce1c82772b1a0a827388d36cf2fd180263'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/23/GPL/openjdk-21-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='3241d3b6b20a9520ee937d7aab42daa55e86cc251ca77f0643e4425ccf7b1348'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 24 May 2023 21:45:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:90e2fb2facff1c5093f0ebfa9d08fde487930822d9ac278bb2df0195610f1d13`  
		Last Modified: Wed, 24 May 2023 21:21:24 GMT  
		Size: 44.9 MB (44873648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0845850e9baa985b97efc76bed4795ff90eb1249ecf4531667da84d4be1fcdf`  
		Last Modified: Wed, 24 May 2023 21:45:40 GMT  
		Size: 15.0 MB (15010668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06c8d09236e38c5c7a175012d1a5faef42e265122b65b8a2705ba98ae7763a5`  
		Last Modified: Wed, 24 May 2023 21:45:52 GMT  
		Size: 202.9 MB (202902863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:27f52854c43307c0f923e67f26a1d9f661ac20831b6c724e4de0a6a60eafe279
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261121088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec2089cc4b709fb37808e9d16785253780275e1058d570026a03b68e0529e945`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 May 2023 21:44:09 GMT
ADD file:8c6f57a98019c407c59b2adbf7da54536eff3a7ca62c46883bbc60975b39ad04 in / 
# Wed, 24 May 2023 21:44:09 GMT
CMD ["/bin/bash"]
# Wed, 24 May 2023 22:03:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 24 May 2023 22:03:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Wed, 24 May 2023 22:03:14 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 May 2023 22:03:14 GMT
ENV LANG=C.UTF-8
# Thu, 25 May 2023 23:39:43 GMT
ENV JAVA_VERSION=21-ea+24
# Thu, 25 May 2023 23:39:56 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/24/GPL/openjdk-21-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='437e740a3ee795a3cf08d6cf5006d03668023151200d5e09ada16d94ef30db22'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/24/GPL/openjdk-21-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='ecabd8a50340461d04d06b8f587bf06c614aed9cb441ee3ff9577e1b10e53035'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 25 May 2023 23:39:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0bb308beee4aa3eb768d546b1ee61303d6f190f63bed75dc7f88ecc26018a944`  
		Last Modified: Wed, 24 May 2023 21:44:58 GMT  
		Size: 43.8 MB (43791991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da95086478e81c9f4c37c04e50d244968af554844dd950bcb04b5f0171653f64`  
		Last Modified: Wed, 24 May 2023 22:03:55 GMT  
		Size: 15.9 MB (15852529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c427e1a7c7546fe45ab6f18696b7bf1e8173249c96d70f910136d2f0663221`  
		Last Modified: Thu, 25 May 2023 23:42:01 GMT  
		Size: 201.5 MB (201476568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

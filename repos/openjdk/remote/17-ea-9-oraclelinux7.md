## `openjdk:17-ea-9-oraclelinux7`

```console
$ docker pull openjdk@sha256:19e65365fd94320d5f764a73ed7969cae9d4c813bccfdf87af303561519e9b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:17-ea-9-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:942c537de2d8c07342ea4b16f62a9e62b48cb89e60726d9d40f7339d78501d4e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.4 MB (249395558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b63dd57a98892aab7ea0a7d854b1ca8ee1fc5ac2f59875e7cb29161bf80a106`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 12 Feb 2021 00:53:29 GMT
ADD file:361f165903526126476b03dd2afac1fff0b334906bb56d024e5aee87b948b0cf in / 
# Fri, 12 Feb 2021 00:53:29 GMT
CMD ["/bin/bash"]
# Fri, 12 Feb 2021 01:11:19 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 12 Feb 2021 01:11:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Fri, 12 Feb 2021 01:11:19 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Feb 2021 01:11:19 GMT
ENV LANG=en_US.UTF-8
# Fri, 12 Feb 2021 23:41:41 GMT
ENV JAVA_VERSION=17-ea+9
# Fri, 12 Feb 2021 23:41:56 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/9/GPL/openjdk-17-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='0ed9bba55c54c5949c2f9116ef5bf936b3c55ec39531f317492bdca43a1c1fa8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/9/GPL/openjdk-17-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='1922fd3e81bec1b42c8660d990ccc7fdb36210792f59cbe307691b7d3fa4c967'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 12 Feb 2021 23:41:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a61503a3b32ea964eb926d54dcfe6cd7e21f4e0cca1b1373df21cf904388c445`  
		Last Modified: Fri, 12 Feb 2021 00:54:42 GMT  
		Size: 48.3 MB (48263629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2d02ff646cdda3eb210d43b22353e431d4fa3a204470452ad0a0508cdbf87d`  
		Last Modified: Fri, 12 Feb 2021 01:18:03 GMT  
		Size: 15.4 MB (15437000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7603a7e58d4aea6ccb47fd8f9c0387bfd8a1f1cc9b3125326320a3d15095b452`  
		Last Modified: Fri, 12 Feb 2021 23:52:38 GMT  
		Size: 185.7 MB (185694929 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-ea-9-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e3f941ee618f858f3408dfabed20607801daf7b4d0bd39c7c914243067f7272a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.4 MB (245409948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d4cfd74bfe3e362af93336890495560430a459fff82a69f557dce18d7a4431`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 12 Feb 2021 01:00:40 GMT
ADD file:25b64ec41b7ca742c671c416e08a7bee3224e4052650624ef31b5583b1c412df in / 
# Fri, 12 Feb 2021 01:00:41 GMT
CMD ["/bin/bash"]
# Fri, 12 Feb 2021 01:19:33 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 12 Feb 2021 01:19:34 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Fri, 12 Feb 2021 01:19:35 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Feb 2021 01:19:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 12 Feb 2021 23:43:13 GMT
ENV JAVA_VERSION=17-ea+9
# Fri, 12 Feb 2021 23:43:56 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/9/GPL/openjdk-17-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='0ed9bba55c54c5949c2f9116ef5bf936b3c55ec39531f317492bdca43a1c1fa8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/9/GPL/openjdk-17-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='1922fd3e81bec1b42c8660d990ccc7fdb36210792f59cbe307691b7d3fa4c967'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 12 Feb 2021 23:43:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:da6ef06bd6983a3815530ecb4b6d3bcef6c011f03daa80be12f60c382e0c23e9`  
		Last Modified: Fri, 12 Feb 2021 01:01:42 GMT  
		Size: 48.9 MB (48854102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2cbabffc67d7d6521300614c7fd34cc6a54a4697d98c388898fc060b0f77d3`  
		Last Modified: Fri, 12 Feb 2021 01:26:00 GMT  
		Size: 16.5 MB (16465019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb453494b905d6f28b40376a190fe0c588717534d74e2badaf13c08ee23941d7`  
		Last Modified: Fri, 12 Feb 2021 23:51:46 GMT  
		Size: 180.1 MB (180090827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

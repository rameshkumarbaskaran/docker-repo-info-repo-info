## `openjdk:17-ea-25-oraclelinux7`

```console
$ docker pull openjdk@sha256:2b0b236f8135d7ae2ba5b1a5f225d8a6c7585c3234ac5e4b235f01329543729c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:17-ea-25-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:4a52b2677b5be55aeb04b25ab2208b6c1fc471ab11ca69bd3a5a9ed31ca7fa4f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249776256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a12c71d039989f48b76e714659caa9a2cad83be5967a4e64f57c46465cc6806`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 01 Jun 2021 15:21:43 GMT
ADD file:6853efe982f87a3475099ab9aaa2ec9797afac58ee8dfc54d912b966bc3405ea in / 
# Tue, 01 Jun 2021 15:21:44 GMT
CMD ["/bin/bash"]
# Tue, 01 Jun 2021 15:38:40 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 01 Jun 2021 15:38:40 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Tue, 01 Jun 2021 15:38:40 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Jun 2021 15:38:41 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jun 2021 18:21:45 GMT
ENV JAVA_VERSION=17-ea+25
# Fri, 04 Jun 2021 18:21:55 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/25/GPL/openjdk-17-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='5da8f12ebc9f3c601a838d3b49222015ad418ccde5bdf7bc36dceaf5e7fd9976'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/25/GPL/openjdk-17-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='149a417622b53f0933df2a9200126c7313bc13923d80b58ee041085aa087f62b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 04 Jun 2021 18:21:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cbf629395cd4d267c366a2b3ac4cfbe6a6c5cfd5bdd8e89a7157e0901e898cf4`  
		Last Modified: Tue, 01 Jun 2021 15:22:47 GMT  
		Size: 48.3 MB (48260748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf25dc842172d49c0f45cec26c8fe86f7a083e2e5ce7a5e6d84d2b4cd2d46ba`  
		Last Modified: Tue, 01 Jun 2021 15:43:59 GMT  
		Size: 15.4 MB (15425936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980f566889546fb73045021ebb0cbd5f4d0d4b3e371ffb90ad22945bd815801`  
		Last Modified: Fri, 04 Jun 2021 18:27:43 GMT  
		Size: 186.1 MB (186089572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-ea-25-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a97f8cc69e0de32e9c8b141f3a04606d935014846dd14a4e004a4ef8aff7d33b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247395568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709ef449ef559c1070a527561faf3b71276c018beacf4e8ac8f0568e2a2b9e44`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 01 Jun 2021 14:41:12 GMT
ADD file:3f30763d6f4fa6cd26708a9eda4872cc48b0c874b7837e0682ea4b4ed7ac5fb2 in / 
# Tue, 01 Jun 2021 14:41:12 GMT
CMD ["/bin/bash"]
# Tue, 01 Jun 2021 14:58:49 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 01 Jun 2021 14:58:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Tue, 01 Jun 2021 14:58:50 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Jun 2021 14:58:50 GMT
ENV LANG=en_US.UTF-8
# Fri, 04 Jun 2021 18:43:00 GMT
ENV JAVA_VERSION=17-ea+25
# Fri, 04 Jun 2021 18:43:16 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/25/GPL/openjdk-17-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='5da8f12ebc9f3c601a838d3b49222015ad418ccde5bdf7bc36dceaf5e7fd9976'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/25/GPL/openjdk-17-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='149a417622b53f0933df2a9200126c7313bc13923d80b58ee041085aa087f62b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 04 Jun 2021 18:43:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5216e6356b12c39a03d420e358911905653d063185ac40b7250d625cfcd46024`  
		Last Modified: Tue, 01 Jun 2021 14:42:13 GMT  
		Size: 48.9 MB (48857508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0104ba284443f9b2819e0f98ad5efb21b57c2cf4d49bd3d3cbd1af4ad0ac2c85`  
		Last Modified: Tue, 01 Jun 2021 15:09:33 GMT  
		Size: 16.4 MB (16419323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179dd5fab917dec17b87e8fb097a54769b7bda9e1dd69fd9e4b3adb7499f18ba`  
		Last Modified: Fri, 04 Jun 2021 18:54:02 GMT  
		Size: 182.1 MB (182118737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

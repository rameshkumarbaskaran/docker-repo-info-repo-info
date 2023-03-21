## `openjdk:21-ea-oraclelinux7`

```console
$ docker pull openjdk@sha256:4d6388fb73a51d4eb515843b00647f36b753867876484bb94802d52b93acbaab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-ea-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:479fce92de0f78c796aaeb64e103baf615d2e61184d49cbe0e956ea21033ebb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266164993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7bb4edf9bc684fb0858dc0e8a36e3985656dd647f794ebddb938144f37512b8`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Mar 2023 19:26:42 GMT
ADD file:c2562ae661b3cd914b2c0dd27aba7ee36bffbeb92415b7b80c111a5d563d07ed in / 
# Tue, 21 Mar 2023 19:26:43 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2023 20:47:46 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 21 Mar 2023 20:47:46 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Tue, 21 Mar 2023 20:47:46 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Mar 2023 20:47:46 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Mar 2023 20:47:47 GMT
ENV JAVA_VERSION=21-ea+14
# Tue, 21 Mar 2023 20:47:56 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/14/GPL/openjdk-21-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='5ff9e95f12627e7f9c4b2e61d4ddfa5eb224f6106eff7620a487244be71d9787'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/14/GPL/openjdk-21-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='32b9ef0cafec4114aac8917e9ad754c7a3bdcfbc47143e4e5182757a0311ae66'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 21 Mar 2023 20:47:57 GMT
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
	-	`sha256:2b984e7880638e9a4d1dbcc94e4f7cf9b1d3353f5630923e8034099b2a7dd5ed`  
		Last Modified: Tue, 21 Mar 2023 20:49:22 GMT  
		Size: 201.4 MB (201441829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ba3c4acd76c473852e327c1ede84891d429e89f6b52d81207b702d6234304e12
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266193780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83060b935b98006f98d1181ba8908ba0e4dd43fa34a9b6ba98c3cf098c65952`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Mar 2023 19:44:52 GMT
ADD file:a9428dda3ec7ae554537bb583832aa2d30484c863bf95c68e460df5858c4c0bf in / 
# Tue, 21 Mar 2023 19:44:53 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2023 21:03:26 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 21 Mar 2023 21:03:26 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Tue, 21 Mar 2023 21:03:26 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Mar 2023 21:03:27 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Mar 2023 21:03:27 GMT
ENV JAVA_VERSION=21-ea+14
# Tue, 21 Mar 2023 21:03:39 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/14/GPL/openjdk-21-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='5ff9e95f12627e7f9c4b2e61d4ddfa5eb224f6106eff7620a487244be71d9787'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/14/GPL/openjdk-21-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='32b9ef0cafec4114aac8917e9ad754c7a3bdcfbc47143e4e5182757a0311ae66'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 21 Mar 2023 21:03:41 GMT
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
	-	`sha256:611777f1f37ddb1cd7f279d072a87a59c8c9303eaec1dd9461bd9138bd5bf5c9`  
		Last Modified: Tue, 21 Mar 2023 21:04:55 GMT  
		Size: 199.9 MB (199917067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `openjdk:22-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:d304845a6a8c359458aba7b13446891e0499834b714285d57c3491fb25f86bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:4d8c5b5ebbed517c5285a7fbb17720b063d5dd3a4858e6e435e1405cb3950d25
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.6 MB (264597842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7dcdf456e88050cd77dca1aad45b3f79eebe5778727e87a02ae0accb57f1701`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 04 Jun 2023 17:54:32 GMT
ADD file:39d09c6c7c3a0f64981f5cbcb12cc8f0128979c3d4b91d74c84fe62aca5ea87e in / 
# Sun, 04 Jun 2023 17:54:32 GMT
CMD ["/bin/bash"]
# Sun, 04 Jun 2023 19:01:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 12 Jun 2023 22:26:29 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Mon, 12 Jun 2023 22:26:29 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jun 2023 22:26:29 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jun 2023 22:26:29 GMT
ENV JAVA_VERSION=22-ea+1
# Mon, 12 Jun 2023 22:26:40 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='50bf6303955ea128be3eb7ad9bc10f5e7eeacf9d3f81349a4d60a164fe7d0318'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='6ca14677cb2db094acbc9b084d0a85c9e004aff9826977e0b9b35e5f9a55b550'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Jun 2023 22:26:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3e0c3751e6482e67b70ffad144b2cb9aec9be672df2642a322e875e51b748aeb`  
		Last Modified: Sun, 04 Jun 2023 17:55:32 GMT  
		Size: 44.9 MB (44872720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5b8981d150f5706ec1b30f459a99b1c25abb86225512911608e4175546c8d9`  
		Last Modified: Sun, 04 Jun 2023 19:02:11 GMT  
		Size: 15.0 MB (15004426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede12e8bc9615c77ffdc13709569c7eea1c5e9f139b87d298d66056e999aebbd`  
		Last Modified: Mon, 12 Jun 2023 22:29:14 GMT  
		Size: 204.7 MB (204720696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c9570e934c44ed253516668006de9447398f919d7e01574a0694291754bf9ba3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262678261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6212db0c2caf6323075f3b0c1cede93424132cc0c709ac56e1fb1ef20e6cc440`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 02 Jun 2023 22:40:44 GMT
ADD file:ae7c6036695430900f5ff735197e9c0281881b97faaea00e40263ca539fe7fff in / 
# Fri, 02 Jun 2023 22:40:45 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 22:57:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 12 Jun 2023 21:45:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Mon, 12 Jun 2023 21:45:38 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jun 2023 21:45:38 GMT
ENV LANG=C.UTF-8
# Mon, 12 Jun 2023 21:45:38 GMT
ENV JAVA_VERSION=22-ea+1
# Mon, 12 Jun 2023 21:45:54 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='50bf6303955ea128be3eb7ad9bc10f5e7eeacf9d3f81349a4d60a164fe7d0318'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='6ca14677cb2db094acbc9b084d0a85c9e004aff9826977e0b9b35e5f9a55b550'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Jun 2023 21:45:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2ae143351a4fc570e80462825e827f3afbbabc4488aeae617542d42b521e5248`  
		Last Modified: Fri, 02 Jun 2023 22:41:37 GMT  
		Size: 43.8 MB (43787831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76745f42ba06c52f3c8c98a56266981889c3e5541a95f8478f09f378b9807208`  
		Last Modified: Fri, 02 Jun 2023 22:58:08 GMT  
		Size: 15.8 MB (15841478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb9326c55c0ee4fa3118e56f2a7daf288cdc0518a08b4be5cb16a1caf06e9cb`  
		Last Modified: Mon, 12 Jun 2023 21:48:34 GMT  
		Size: 203.0 MB (203048952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

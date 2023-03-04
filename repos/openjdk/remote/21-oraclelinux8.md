## `openjdk:21-oraclelinux8`

```console
$ docker pull openjdk@sha256:dc75c108bf727828fa1c4448c22f8829b8632c2b410e85888d751de13e94d1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:1701adf157c95c087b8081c0640a056ffd5227f08609e3fb4847070d9f4506e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.0 MB (258984636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddee7e928668137f2b5f49e8635b86b26089d1e224c67f10b84455f0e1c704a4`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 24 Feb 2023 00:20:27 GMT
ADD file:9c8b13ccecebc19a9105d94b9b8060d87741d158a6de27ec96b14028de164443 in / 
# Fri, 24 Feb 2023 00:20:28 GMT
CMD ["/bin/bash"]
# Fri, 24 Feb 2023 00:40:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 24 Feb 2023 00:40:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Fri, 24 Feb 2023 00:40:14 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Feb 2023 00:40:15 GMT
ENV LANG=C.UTF-8
# Sat, 04 Mar 2023 00:26:33 GMT
ENV JAVA_VERSION=21-ea+12
# Sat, 04 Mar 2023 00:26:44 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/12/GPL/openjdk-21-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='da247094c9b9e7b4ab18b5e36adc89e3b7f6ee77192816ce059b933e23e09fca'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/12/GPL/openjdk-21-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='ea0bf5244a8b27f1c111cb40cb161186c9217f0bbc31e3a019b81c21505c8f18'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 04 Mar 2023 00:26:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b4ddc423e0463a3d58b6c40ac1d97a950af62e9db703bb4c9d55afad67394149`  
		Last Modified: Fri, 24 Feb 2023 00:21:21 GMT  
		Size: 44.6 MB (44556861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f918ee7b32337dedda10e8566b1e5d96678ad53c0527e878e3866a6f713189e`  
		Last Modified: Fri, 24 Feb 2023 00:42:24 GMT  
		Size: 15.0 MB (15015003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01533598c6b6fc158484d225582e84137d8e373325ca068c925422f4021be278`  
		Last Modified: Sat, 04 Mar 2023 00:29:50 GMT  
		Size: 199.4 MB (199412772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3e70d66d972d793c323a1b664dd75f982e6edbe6885a47b47d4ee15fcdd15c7e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 MB (257195974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e85b40c58fcc771f2ea2e56460183bf840610869d4cfd76b0c7481c4b0e77d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Feb 2023 23:40:03 GMT
ADD file:b9db410ba951fb740a34187417442b96a27a7fd918b16023c16cb1b0777b292f in / 
# Thu, 23 Feb 2023 23:40:04 GMT
CMD ["/bin/bash"]
# Thu, 23 Feb 2023 23:58:51 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 23 Feb 2023 23:58:52 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Thu, 23 Feb 2023 23:58:52 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Feb 2023 23:58:52 GMT
ENV LANG=C.UTF-8
# Sat, 04 Mar 2023 00:11:53 GMT
ENV JAVA_VERSION=21-ea+12
# Sat, 04 Mar 2023 00:12:03 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/12/GPL/openjdk-21-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='da247094c9b9e7b4ab18b5e36adc89e3b7f6ee77192816ce059b933e23e09fca'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/12/GPL/openjdk-21-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='ea0bf5244a8b27f1c111cb40cb161186c9217f0bbc31e3a019b81c21505c8f18'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 04 Mar 2023 00:12:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fdf42ad2544e3a5379ea5e0050457e87df46409adba81dba4686a3efc595ccd2`  
		Last Modified: Thu, 23 Feb 2023 23:40:48 GMT  
		Size: 43.5 MB (43461050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2911a20ed1ec4cf4241519f3d97458f77a1eaded44c42d9ae79a999075ef4c`  
		Last Modified: Fri, 24 Feb 2023 00:01:00 GMT  
		Size: 15.8 MB (15838054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c920c315fdcded4804c28a2b34071caece23765f39c71f590b64628c4e55ad00`  
		Last Modified: Sat, 04 Mar 2023 00:15:19 GMT  
		Size: 197.9 MB (197896870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

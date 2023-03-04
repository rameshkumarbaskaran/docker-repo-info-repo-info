## `openjdk:21-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:ba1b0912a932d36bbac7476f5de0aef0d8533bce47994f8270fc5fb9c0bd2c6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:8477467cdc8de2fe2f376ea66098adf93cd12c8af905ea5f0887eb22c31f79e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.1 MB (264124338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdefac679b3aea4809ed6d7e44e0e08ce6f1bbbba9df7a19388bceef3aabdf36`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Jan 2023 23:36:36 GMT
ADD file:eefc8abcbb6ec3141573da12cc99f3d9592d5a0bd105bb189e0e1db15c0d1bf5 in / 
# Fri, 27 Jan 2023 23:36:37 GMT
CMD ["/bin/bash"]
# Fri, 27 Jan 2023 23:54:48 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 27 Jan 2023 23:54:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Fri, 27 Jan 2023 23:54:49 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Jan 2023 23:54:49 GMT
ENV LANG=en_US.UTF-8
# Sat, 04 Mar 2023 00:26:48 GMT
ENV JAVA_VERSION=21-ea+12
# Sat, 04 Mar 2023 00:26:57 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/12/GPL/openjdk-21-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='da247094c9b9e7b4ab18b5e36adc89e3b7f6ee77192816ce059b933e23e09fca'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/12/GPL/openjdk-21-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='ea0bf5244a8b27f1c111cb40cb161186c9217f0bbc31e3a019b81c21505c8f18'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 04 Mar 2023 00:26:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e048d0a387420acfdb05a1ec44ed79aa01be81adcd731b3100359277ca89d08b`  
		Last Modified: Fri, 27 Jan 2023 23:38:26 GMT  
		Size: 50.5 MB (50466577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde4d617b6d23e9a10ad76ad56ca1591c532861de431f66e6e735233eef43807`  
		Last Modified: Sat, 28 Jan 2023 00:00:16 GMT  
		Size: 14.2 MB (14244027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e4702d6c433a1d549757c82faa42633ef5cbc35dd5104a4a497d3ed71b84fd`  
		Last Modified: Sat, 04 Mar 2023 00:30:37 GMT  
		Size: 199.4 MB (199413734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:dc02382a5a53fcf19b5b37cbe366fa4da68c4931151c34d54b7ef62be012b886
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264199580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80b5a2c70751c0c96afcd0c31d7724c3e8b05659824fc0fc483b8cf4f266346`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Jan 2023 22:41:24 GMT
ADD file:1081f67c6d4b6b053a45161b9968a0371ed81fc45f61729a33bffa9a470ec646 in / 
# Fri, 27 Jan 2023 22:41:25 GMT
CMD ["/bin/bash"]
# Fri, 27 Jan 2023 22:59:27 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 27 Jan 2023 22:59:27 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Fri, 27 Jan 2023 22:59:27 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Jan 2023 22:59:27 GMT
ENV LANG=en_US.UTF-8
# Sat, 04 Mar 2023 00:12:06 GMT
ENV JAVA_VERSION=21-ea+12
# Sat, 04 Mar 2023 00:12:18 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/12/GPL/openjdk-21-ea+12_linux-x64_bin.tar.gz'; 			downloadSha256='da247094c9b9e7b4ab18b5e36adc89e3b7f6ee77192816ce059b933e23e09fca'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/12/GPL/openjdk-21-ea+12_linux-aarch64_bin.tar.gz'; 			downloadSha256='ea0bf5244a8b27f1c111cb40cb161186c9217f0bbc31e3a019b81c21505c8f18'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 04 Mar 2023 00:12:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:114f8bb3e448153115527e27f088f4ed8912d567d8785d54c82dbf490230f6d0`  
		Last Modified: Fri, 27 Jan 2023 22:43:00 GMT  
		Size: 51.0 MB (51033896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc016fcb2fb8b8e69042ed80b5f1629423ef745bcb1ac72c0501de8b7b02850`  
		Last Modified: Fri, 27 Jan 2023 23:05:00 GMT  
		Size: 15.3 MB (15268160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3531704e76da3bd4ed8f87e535fcf581dd35085b61fa5d3d023f4286a2c7e63`  
		Last Modified: Sat, 04 Mar 2023 00:16:01 GMT  
		Size: 197.9 MB (197897524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `openjdk:21-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:40780fc541461d3b3bfedfdbfd7bcab4c4b12577b25a8357a3c5a1600b666fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:b214e02eeb7be006095db0037af29e694c6b9880101720494e3294f0fc6c9c33
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.0 MB (256037500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f81654c27e80a57b363d9951608a2b18a8a52d5e4cc4d4a80e16221b3d444a5`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Jan 2023 23:36:12 GMT
ADD file:f2aead35bfc542632b7274d3b1132eb2bb3752d6cb61414febbffb746120622c in / 
# Fri, 27 Jan 2023 23:36:13 GMT
CMD ["/bin/bash"]
# Fri, 27 Jan 2023 23:54:19 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 27 Jan 2023 23:54:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Fri, 27 Jan 2023 23:54:20 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Jan 2023 23:54:20 GMT
ENV LANG=C.UTF-8
# Mon, 30 Jan 2023 19:20:02 GMT
ENV JAVA_VERSION=21-ea+7
# Mon, 30 Jan 2023 19:20:16 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/7/GPL/openjdk-21-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='16ab024c51a97fa3197449b0aa716f54351fb28a1d69de7b1ea0753f5d044a9c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/7/GPL/openjdk-21-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='22f7979fb746761c266f83579819fdea9109ce2d7340205faa330747bb2187c2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 30 Jan 2023 19:20:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:39fbafb6c7ef40878b859fd0e4475c5ebd2ddfa8ed785a588594e8731b7cd0e8`  
		Last Modified: Fri, 27 Jan 2023 23:37:50 GMT  
		Size: 44.6 MB (44561081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70086a6ca030344addd4b8e51d50d209385d29d8e70c28a102f5d9668e8535b9`  
		Last Modified: Fri, 27 Jan 2023 23:59:16 GMT  
		Size: 12.3 MB (12251614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ffa86f9ea48e63b4bf5f551ec2c0e073995696153889d01271d3c9cf20e377`  
		Last Modified: Mon, 30 Jan 2023 19:26:32 GMT  
		Size: 199.2 MB (199224805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6e3edc94fc4a87fbf0a817066988cd5c07adda4f785240624f052d6e16b88756
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.2 MB (254229748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:203b2f14172dc2bc5c29c3b2398d9f23e5ad70fcc888e743343353bddd0b0062`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Jan 2023 22:41:06 GMT
ADD file:63b5b4161762e1845c1eb2bb2c967a07179819b4a1f12ab7596d9c6bd15c9cbd in / 
# Fri, 27 Jan 2023 22:41:06 GMT
CMD ["/bin/bash"]
# Fri, 27 Jan 2023 22:58:45 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 27 Jan 2023 22:58:45 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Fri, 27 Jan 2023 22:58:45 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Jan 2023 22:58:45 GMT
ENV LANG=C.UTF-8
# Mon, 30 Jan 2023 19:41:55 GMT
ENV JAVA_VERSION=21-ea+7
# Mon, 30 Jan 2023 19:42:07 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/7/GPL/openjdk-21-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='16ab024c51a97fa3197449b0aa716f54351fb28a1d69de7b1ea0753f5d044a9c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/7/GPL/openjdk-21-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='22f7979fb746761c266f83579819fdea9109ce2d7340205faa330747bb2187c2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 30 Jan 2023 19:42:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d26cdabfc8c6a31055d655a58d8a8f9757f43e1ce58451b8b6b02c5dd6e6d482`  
		Last Modified: Fri, 27 Jan 2023 22:42:28 GMT  
		Size: 43.5 MB (43456742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175fa1491e9fc183c9d73f4393db52b943e03e50258cf81fd2c6970905be7318`  
		Last Modified: Fri, 27 Jan 2023 23:04:19 GMT  
		Size: 13.1 MB (13068665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e807a201975ffb3e70dc6c045f15b11ff4b53840993332285b358baeae894e88`  
		Last Modified: Mon, 30 Jan 2023 19:48:18 GMT  
		Size: 197.7 MB (197704341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

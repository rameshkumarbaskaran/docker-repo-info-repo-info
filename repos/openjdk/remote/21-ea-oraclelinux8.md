## `openjdk:21-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:a788cda7dee175dc1ebec1241919c1ab6f74c5b73d8498b674df6d366c2f3a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:fec28f00f19ddb0af231369eff64d73b89b5ea23bca90d1efb9e67e262a17167
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263736540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce186f750105aa2f21562107dbd043a17e94e1c7f1b8b35f25e5f4d3c142055a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Jul 2023 02:04:16 GMT
ADD file:7a7c6d19e1a4f691c6bd96ea6b7568f6cc041fce11298e57d51913b978e9e7e3 in / 
# Tue, 04 Jul 2023 02:04:17 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 17:47:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 04 Jul 2023 17:48:37 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Tue, 04 Jul 2023 17:48:37 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 17:48:37 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 17:48:37 GMT
ENV JAVA_VERSION=21-ea+29
# Tue, 04 Jul 2023 17:48:47 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/29/GPL/openjdk-21-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='414ca270602b11d0b674c105d1d5577793c9db79e2947187e663dba4750cbf9b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/29/GPL/openjdk-21-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='ddfa7ea3dd22c846676b4def3aef78a5411c208987ace8f47bbcfafd33f26f46'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 04 Jul 2023 17:48:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e2c03c89dcad02e83fe01768b82c438fcf60b831104614ca96ed5d8df01db295`  
		Last Modified: Tue, 04 Jul 2023 02:05:27 GMT  
		Size: 44.9 MB (44876686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1589371ef7dbf0bbba39e839420d2a593e729690f3c9a3a1cc86d3cd6b47912`  
		Last Modified: Tue, 04 Jul 2023 17:50:16 GMT  
		Size: 15.0 MB (14998167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8177c4c6970a08e970d3c4ab9e55b66fa148cbe3dc7cad43dbe1b34a9b55d2de`  
		Last Modified: Tue, 04 Jul 2023 17:52:17 GMT  
		Size: 203.9 MB (203861687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:77c3e36ab0766ab3e652661f47f068a82b9cb9aa7dadeaa30d4bec83e7693192
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261482394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8680ccffd8d8802d1686900f160836f0c0f0cd4d734e0c0dc31bbb3f120de33`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Jul 2023 00:52:20 GMT
ADD file:1313260ee8b32fa94bcf06c44034cd7e4f9baf44c7df9e74facfe21323b37292 in / 
# Tue, 04 Jul 2023 00:52:21 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 01:17:20 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 04 Jul 2023 01:18:57 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Tue, 04 Jul 2023 01:18:57 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 01:18:57 GMT
ENV LANG=C.UTF-8
# Tue, 04 Jul 2023 01:18:57 GMT
ENV JAVA_VERSION=21-ea+29
# Tue, 04 Jul 2023 01:19:06 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/29/GPL/openjdk-21-ea+29_linux-x64_bin.tar.gz'; 			downloadSha256='414ca270602b11d0b674c105d1d5577793c9db79e2947187e663dba4750cbf9b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/29/GPL/openjdk-21-ea+29_linux-aarch64_bin.tar.gz'; 			downloadSha256='ddfa7ea3dd22c846676b4def3aef78a5411c208987ace8f47bbcfafd33f26f46'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 04 Jul 2023 01:19:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:29e800056b7e3d5007df41c0ad55416bb45d5863affcf39316c5755e71b20a30`  
		Last Modified: Tue, 04 Jul 2023 00:53:16 GMT  
		Size: 43.6 MB (43595268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4e6eec249ed9ec194f18c4c5eda620b32132cc41a2083ec5505ff863774f15`  
		Last Modified: Tue, 04 Jul 2023 01:21:26 GMT  
		Size: 15.7 MB (15676974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1372d1f23e10b416844666f2ef75e8d30cda06791458ed603914ab857e61d9de`  
		Last Modified: Tue, 04 Jul 2023 01:24:49 GMT  
		Size: 202.2 MB (202210152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

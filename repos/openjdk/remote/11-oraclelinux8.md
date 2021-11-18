## `openjdk:11-oraclelinux8`

```console
$ docker pull openjdk@sha256:cb17cc3eae0a629248d16bd6a8125ad2f777b4143ebd59650ccad770806d31a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:11-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:0ae26611d3d8321d98ae3d8f1d28d8f94acf5cd8670c99afb66cd0f94aff889c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258621781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:943710528bfe4a890ddb05f321c37d78b3e8130ab4048000dc9fad12d9cea915`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Nov 2021 16:05:57 GMT
ADD file:977d9a2c7a8ab07ec719edd585faf23ef08768a09abf97a80d62d2091936b052 in / 
# Thu, 18 Nov 2021 16:05:58 GMT
CMD ["/bin/bash"]
# Thu, 18 Nov 2021 17:33:38 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 18 Nov 2021 17:35:46 GMT
ENV JAVA_HOME=/usr/java/openjdk-11
# Thu, 18 Nov 2021 17:35:46 GMT
ENV PATH=/usr/java/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 17:35:47 GMT
ENV LANG=C.UTF-8
# Thu, 18 Nov 2021 17:35:47 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 18 Nov 2021 17:36:17 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 18 Nov 2021 17:36:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0a39cfde620ea7949c12d65ef5a24d4b6f737bb5a2f57d9a4a16013c060c9c67`  
		Last Modified: Thu, 18 Nov 2021 16:07:11 GMT  
		Size: 42.1 MB (42098006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a90c9cadc5331c54e5f53b906e967fe1942c54666e8da9bf055c378d02b2ad`  
		Last Modified: Thu, 18 Nov 2021 17:43:13 GMT  
		Size: 13.5 MB (13511675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843f90f724e524ecdb60b182f8f7d9a5078926dcf7dab47aa76301139f226428`  
		Last Modified: Thu, 18 Nov 2021 17:46:15 GMT  
		Size: 203.0 MB (203012100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:11-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b0d90a2731ad3c9c87a2eb20f94ae871329e72b47a55f9e01dc273841ceb6541
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.9 MB (256914698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c9122ed0d2c16b2bfaa498b6071100e3967409f414f68f49e5323dfe59e935`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Nov 2021 08:24:53 GMT
ADD file:98b355b05026edaab234cff8ee34d8335b233cbaa04a19ac82df4a2b0c7fdc4d in / 
# Thu, 18 Nov 2021 08:24:54 GMT
CMD ["/bin/bash"]
# Thu, 18 Nov 2021 10:14:56 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 18 Nov 2021 10:17:05 GMT
ENV JAVA_HOME=/usr/java/openjdk-11
# Thu, 18 Nov 2021 10:17:06 GMT
ENV PATH=/usr/java/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 10:17:07 GMT
ENV LANG=C.UTF-8
# Thu, 18 Nov 2021 10:17:08 GMT
ENV JAVA_VERSION=11.0.13
# Thu, 18 Nov 2021 10:17:45 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_linux_11.0.13_8.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_aarch64_linux_11.0.13_8.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 18 Nov 2021 10:17:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1bdb3a9e404c972ab03f65fd56b5b815b51d6a68324015dc69707d48e2ba3cdf`  
		Last Modified: Thu, 18 Nov 2021 08:26:02 GMT  
		Size: 42.0 MB (42010198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9356b5c0bb88b90b52af9c2836e152e11b910a0e88807e8327df1e2a965a7d1`  
		Last Modified: Thu, 18 Nov 2021 10:27:05 GMT  
		Size: 14.3 MB (14300065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb37b76916e227555461c698852cc65db7311865bdf8117414afb3d3ee0d86c3`  
		Last Modified: Thu, 18 Nov 2021 10:30:27 GMT  
		Size: 200.6 MB (200604435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

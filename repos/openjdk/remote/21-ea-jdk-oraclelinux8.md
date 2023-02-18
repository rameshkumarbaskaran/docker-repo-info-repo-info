## `openjdk:21-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:b77bd700c98bc25a120976dd8bdd00d5eb1c8c8883f8db494d010fc0617a5694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:737372ce6009311599e740c70a51e285adeb9963fe95a9070d95f243aafabc51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256138689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5297afd7720ef5d3d3fdf00f91615ae584d9b7a2f8f3c483bf66f672d2155a18`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Feb 2023 19:27:31 GMT
ADD file:6a3fb962576ab4237e9335cfcf419249f08417e28cfbb633d7cc6f26f1f85287 in / 
# Wed, 08 Feb 2023 19:27:32 GMT
CMD ["/bin/bash"]
# Wed, 08 Feb 2023 19:44:53 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 08 Feb 2023 19:44:53 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Wed, 08 Feb 2023 19:44:54 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Feb 2023 19:44:54 GMT
ENV LANG=C.UTF-8
# Fri, 17 Feb 2023 23:24:56 GMT
ENV JAVA_VERSION=21-ea+10
# Fri, 17 Feb 2023 23:25:06 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/10/GPL/openjdk-21-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='e60198534add038869d333ae9564ff8be298d712c5518b865952d66d07638b7b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/10/GPL/openjdk-21-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='eb5e840f2f81330fa3080312da34ce1daabb27138bbebdbb5ea409d79a970e6c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 17 Feb 2023 23:25:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:197c1adcd755131915cd019bdd58658d44445b3638f65449932c18ee39b6047c`  
		Last Modified: Wed, 08 Feb 2023 19:29:00 GMT  
		Size: 44.6 MB (44555906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b698b7af4b18900b53c768746b1dfb603dfb9aec1eea328fdac86d37001e2a`  
		Last Modified: Wed, 08 Feb 2023 19:48:51 GMT  
		Size: 12.3 MB (12256034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:556edaf26a195a792ca6b891ab1b82f2b48bc4dcec2145838e279a4a565af9fa`  
		Last Modified: Fri, 17 Feb 2023 23:28:06 GMT  
		Size: 199.3 MB (199326749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:753aacf9826a29688ed85d447a532ffb5e3e746ccc99cff1bb61d96ba1d53c06
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254344252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3327722b437239f79e9e5ca0d95a5938ebad4544c34a81531ee428ad12bb43e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Feb 2023 19:44:57 GMT
ADD file:b0d30d32b82572c00d83e2fd97813f8b9ff4c6a92efcd3696df1120df4c1065f in / 
# Wed, 08 Feb 2023 19:44:58 GMT
CMD ["/bin/bash"]
# Wed, 08 Feb 2023 20:04:19 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 08 Feb 2023 20:04:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Wed, 08 Feb 2023 20:04:19 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Feb 2023 20:04:19 GMT
ENV LANG=C.UTF-8
# Fri, 17 Feb 2023 23:34:52 GMT
ENV JAVA_VERSION=21-ea+10
# Fri, 17 Feb 2023 23:35:06 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/10/GPL/openjdk-21-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='e60198534add038869d333ae9564ff8be298d712c5518b865952d66d07638b7b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/10/GPL/openjdk-21-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='eb5e840f2f81330fa3080312da34ce1daabb27138bbebdbb5ea409d79a970e6c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 17 Feb 2023 23:35:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7d4ed4ca78bc8f807025d2f2a491ee60099ed37ad040ce330257955d319a347f`  
		Last Modified: Wed, 08 Feb 2023 19:46:11 GMT  
		Size: 43.5 MB (43456591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb69dde29350e5a2369237cbe74bc3c8c50699d796a4fd09120ea4a5b1f26be9`  
		Last Modified: Wed, 08 Feb 2023 20:08:29 GMT  
		Size: 13.1 MB (13073762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b17954959807e29332489ab1cc5d4bb751876e1ed303767935ad557174c3632`  
		Last Modified: Fri, 17 Feb 2023 23:38:45 GMT  
		Size: 197.8 MB (197813899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

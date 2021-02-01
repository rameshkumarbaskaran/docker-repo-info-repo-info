## `openjdk:16-ea-oraclelinux7`

```console
$ docker pull openjdk@sha256:eecb3e1a2b6a51bc5086c4df388eba21f153f775bab700f70059591e6837298e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:16-ea-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:e840bd3072fd7ab63e2f8fde1bbbad6a956c0ed3d4e410b61cb2289a8aff37d3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 MB (248456934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f46130ac052baa4d2b7f7a4b80d81d5f9cb553d7e8661538e979107733814f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Jan 2021 00:31:31 GMT
ADD file:dee09ad1ed4e7359b14fabc84890b1fb687ad4efe75f7c4800c0a907fd4f70a3 in / 
# Fri, 15 Jan 2021 00:31:32 GMT
CMD ["/bin/bash"]
# Fri, 15 Jan 2021 00:58:14 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Mon, 01 Feb 2021 19:48:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Mon, 01 Feb 2021 19:48:13 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:48:14 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Feb 2021 19:48:14 GMT
ENV JAVA_VERSION=16-ea+34
# Mon, 01 Feb 2021 19:48:50 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk16/34/GPL/openjdk-16-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='11fd069e3a17a17268b9bb0c8bfd440016af686acfe8d3a4bfd71381fbce22dc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk16/34/GPL/openjdk-16-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='9c294a8b7c440c45968fc16d3aa3261be71b00a7fad22b7aafa2a7b7381e5f2c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 01 Feb 2021 19:48:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:980316e412373040bc280150078ae453b259ece36b750a0a9b6f4c99751ce4f9`  
		Last Modified: Wed, 06 Jan 2021 20:24:02 GMT  
		Size: 48.3 MB (48260808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7699f318b6b854fb950c083e0fed757fff0549df020432861c6b50802ec82b2`  
		Last Modified: Fri, 15 Jan 2021 01:09:18 GMT  
		Size: 15.4 MB (15431689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b58780f738b2d8d5e622211c21b8e2afe970840651b92c39f88e247216c12ca6`  
		Last Modified: Mon, 01 Feb 2021 20:04:00 GMT  
		Size: 184.8 MB (184764437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-ea-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6f863ecd6ceea92c737c459c3b94aaadfd5201726bfccf71381783316217560d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244461990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f45250327491f1e59cb2cbd63af01b4aed98a7692a38acf1e1fb7d6602c2f46`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 01 Feb 2021 21:01:37 GMT
ADD file:515797e9c94114d9811e4f5e7ef89e24a7c02f5496694320cf17c5b2c2c62577 in / 
# Mon, 01 Feb 2021 21:01:39 GMT
CMD ["/bin/bash"]
# Mon, 01 Feb 2021 21:07:57 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Mon, 01 Feb 2021 21:09:40 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Mon, 01 Feb 2021 21:09:40 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 21:09:41 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Feb 2021 21:09:42 GMT
ENV JAVA_VERSION=16-ea+34
# Mon, 01 Feb 2021 21:10:04 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk16/34/GPL/openjdk-16-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='11fd069e3a17a17268b9bb0c8bfd440016af686acfe8d3a4bfd71381fbce22dc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk16/34/GPL/openjdk-16-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='9c294a8b7c440c45968fc16d3aa3261be71b00a7fad22b7aafa2a7b7381e5f2c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 01 Feb 2021 21:10:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:679e771030bbd97d6d7a7cf8b0a2290601de0b646eaa29d88c48562a70464c12`  
		Last Modified: Mon, 01 Feb 2021 21:03:42 GMT  
		Size: 48.9 MB (48851459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff96049663e262709e8d337b37d084629a90f0707979070456acf5338444948`  
		Last Modified: Mon, 01 Feb 2021 21:16:24 GMT  
		Size: 16.5 MB (16466150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23b82c99626ce7229faa11e62ee45c6ee4f8fa63bc1727665f67e07c581fd41`  
		Last Modified: Mon, 01 Feb 2021 21:18:10 GMT  
		Size: 179.1 MB (179144381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

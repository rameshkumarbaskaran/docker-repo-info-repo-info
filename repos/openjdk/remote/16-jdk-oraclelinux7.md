## `openjdk:16-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:b1a549dfc63f36dda3b9c1be385a7a0525d974a363be973c6c515024ffecd5ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:16-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:63ca7b482bc0d152504e7c2a4c7fe8d7866acb4021ea65fb7b11954279c46477
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 MB (248485297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457668a7547fe45234e2402c21bf97318a19c0ce71cfb5343eeccd56bdafef6a`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 01 May 2021 04:45:56 GMT
ADD file:31ad06acd4a00f68bd8424f227970a5247493c5cc2d4e4d2b40c55e336119324 in / 
# Sat, 01 May 2021 04:45:57 GMT
CMD ["/bin/bash"]
# Sat, 01 May 2021 05:02:18 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Sat, 01 May 2021 05:03:00 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Sat, 01 May 2021 05:03:00 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 01 May 2021 05:03:00 GMT
ENV LANG=en_US.UTF-8
# Sat, 01 May 2021 05:03:01 GMT
ENV JAVA_VERSION=16.0.1
# Sat, 01 May 2021 05:03:11 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk16.0.1/7147401fd7354114ac51ef3e1328291f/9/GPL/openjdk-16.0.1_linux-x64_bin.tar.gz'; 			downloadSha256='b1198ffffb7d26a3fdedc0fa599f60a0d12aa60da1714b56c1defbce95d8b235'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk16.0.1/7147401fd7354114ac51ef3e1328291f/9/GPL/openjdk-16.0.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='602b005074777df2a0b4306e20152a6446803edd87ccbab95b2f313c4d9be6ba'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 01 May 2021 05:03:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5ef5e09557a1ca0ce2f2f8486a7db9555bf280058aaa8a883f7dfe0da5505b1e`  
		Last Modified: Sat, 01 May 2021 04:47:02 GMT  
		Size: 48.3 MB (48265270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75544f3e96e157c8633ccb0a7bd3d63eac5c09949dd7fa57d238ed37c62a0332`  
		Last Modified: Sat, 01 May 2021 05:07:32 GMT  
		Size: 15.4 MB (15422103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead5862a1fcf145b64f967b2a882ab392998f1d3d2c1f0bb3ce326c53dab8a81`  
		Last Modified: Sat, 01 May 2021 05:08:39 GMT  
		Size: 184.8 MB (184797924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1acffde8ce5dde01c192aea552d7b4e833acb000346464651b5685ad81a090c1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244528651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cef24cd1784eb5b96fc3d6698c36f32ae865eac80ed64e0b12da51e7d64a162`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 01 May 2021 02:34:14 GMT
ADD file:f71ab8aa2d773f52af43dee8a58345e3c64f23cf6dc9722fc2116449655ca0ce in / 
# Sat, 01 May 2021 02:34:16 GMT
CMD ["/bin/bash"]
# Sat, 01 May 2021 02:59:26 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Sat, 01 May 2021 03:00:33 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Sat, 01 May 2021 03:00:35 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 01 May 2021 03:00:36 GMT
ENV LANG=en_US.UTF-8
# Sat, 01 May 2021 03:00:38 GMT
ENV JAVA_VERSION=16.0.1
# Sat, 01 May 2021 03:01:06 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk16.0.1/7147401fd7354114ac51ef3e1328291f/9/GPL/openjdk-16.0.1_linux-x64_bin.tar.gz'; 			downloadSha256='b1198ffffb7d26a3fdedc0fa599f60a0d12aa60da1714b56c1defbce95d8b235'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk16.0.1/7147401fd7354114ac51ef3e1328291f/9/GPL/openjdk-16.0.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='602b005074777df2a0b4306e20152a6446803edd87ccbab95b2f313c4d9be6ba'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 01 May 2021 03:01:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dbfc55cb74dd07b793cdc9b4bc835fcfdb6091dad8e24cd2a6fe84ec70a2c3a6`  
		Last Modified: Sat, 01 May 2021 02:35:18 GMT  
		Size: 48.9 MB (48874038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0431cdcee2306a17be0ad5fd6791cd432218c8671e4eb75ea3a708d15ef0c6c4`  
		Last Modified: Sat, 01 May 2021 03:07:27 GMT  
		Size: 16.5 MB (16472881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa5b017e9e98a8160cdcb9e7464b6288c0cb1cebc2f683672473a5288c09f37`  
		Last Modified: Sat, 01 May 2021 03:08:58 GMT  
		Size: 179.2 MB (179181732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

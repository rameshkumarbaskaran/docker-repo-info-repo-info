## `openjdk:oraclelinux7`

```console
$ docker pull openjdk@sha256:af48988bc41f51b1a7de7a48973e8e20fe2661e82638d75635119b1432aa428d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:e8c50a5ba2f8691f62ea5ad952a9ee886e60f58a1abe3f0e2f580eccb4fdeb86
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260271309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c42f56dca1bd06cf4ed0fa0a98f0bf97c8516cbe079cdf6c9c5bfd9fd83a9cf9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Sep 2020 21:23:41 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-amd64/7-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 7 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Fri, 30 Oct 2020 02:06:29 GMT
ADD file:145961aa92d5a9c6b87e124b38a59e7a4a08910f8cb21414300096f88cc5cb82 in / 
# Fri, 30 Oct 2020 02:06:29 GMT
CMD ["/bin/bash"]
# Fri, 30 Oct 2020 04:38:46 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 30 Oct 2020 04:38:46 GMT
ENV LANG=en_US.UTF-8
# Fri, 30 Oct 2020 04:39:46 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Fri, 30 Oct 2020 04:39:46 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 Oct 2020 04:39:47 GMT
ENV JAVA_VERSION=15.0.1
# Fri, 30 Oct 2020 04:40:02 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-aarch64_bin.tar.gz; 			downloadSha256=6a62b7ec065280bad978a3322733a089153dec5ebf5ba81fd2fa361382dbc7b0; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-x64_bin.tar.gz; 			downloadSha256=83ec3a7b1649a6b31e021cde1e58ab447b07fb8173489f27f427e731c89ed84a; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 30 Oct 2020 04:40:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0df82e2779b8235d6babd25457b87762ea8300fb3797ea03adccf472e7a598df`  
		Last Modified: Fri, 30 Oct 2020 02:08:45 GMT  
		Size: 48.3 MB (48259572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6cf1bd0da100f7cdd56c4dba13c55e8927426cdf47857604dacc67dc2763ea`  
		Last Modified: Fri, 30 Oct 2020 04:43:13 GMT  
		Size: 16.2 MB (16232304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9628c98a82ec472d29782374636f624f294f497176da0c13c89b6f39cf67149`  
		Last Modified: Fri, 30 Oct 2020 04:44:49 GMT  
		Size: 195.8 MB (195779433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a0fcaf7be448d993aa844dfcd96c140ea984213adcc1cbb9b97e401904f453ba
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240235130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10dfa8d6359efb4aa4bb8c194307571ede8752ffedb124575a5087380d92dc45`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Sep 2020 20:41:36 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-arm64v8/7-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 7 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Wed, 18 Nov 2020 21:39:27 GMT
ADD file:f4a327657a328a670e79dc5abbe14d34c0f6083bc105b04205bb7b6007009f5c in / 
# Wed, 18 Nov 2020 21:39:30 GMT
CMD ["/bin/bash"]
# Wed, 18 Nov 2020 22:29:47 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 18 Nov 2020 22:29:48 GMT
ENV LANG=en_US.UTF-8
# Wed, 18 Nov 2020 22:31:02 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Wed, 18 Nov 2020 22:31:03 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Nov 2020 22:31:04 GMT
ENV JAVA_VERSION=15.0.1
# Wed, 18 Nov 2020 22:31:45 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-aarch64_bin.tar.gz; 			downloadSha256=6a62b7ec065280bad978a3322733a089153dec5ebf5ba81fd2fa361382dbc7b0; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-x64_bin.tar.gz; 			downloadSha256=83ec3a7b1649a6b31e021cde1e58ab447b07fb8173489f27f427e731c89ed84a; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 18 Nov 2020 22:31:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:436adcdab5ec3071ba37753f4a768eb644a6d3b209b6c68878fbd4ff8f133edd`  
		Last Modified: Wed, 18 Nov 2020 21:40:29 GMT  
		Size: 48.9 MB (48865849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63ac2a3436373a229835a88787a306790127dbf63f5fe9ba4a0745aae062aeb`  
		Last Modified: Wed, 18 Nov 2020 22:34:42 GMT  
		Size: 16.5 MB (16482372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cddafe56ab59131ed5585c0b72b71301384058fa2ce90b84f169cda882208bd`  
		Last Modified: Wed, 18 Nov 2020 22:36:41 GMT  
		Size: 174.9 MB (174886909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

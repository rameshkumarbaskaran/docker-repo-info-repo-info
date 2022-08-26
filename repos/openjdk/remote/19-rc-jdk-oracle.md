## `openjdk:19-rc-jdk-oracle`

```console
$ docker pull openjdk@sha256:192cadaa11e9d787c53063017ed25fb6f7e6e38b93a943546bae4af2419a347e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-rc-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:2bdfb5d6f33737690ef1986259ae03c6262b98f3d604abf86e6a04c538f88497
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 MB (247941633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe5315ac24955ae7987db1b31aa18f4464d010967686e944eefef9d10dc982d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 26 Aug 2022 21:25:57 GMT
ADD file:923c2af16ef366fe4e85b8ba8979b8a31da0cdbc606c08148463849bf66c395b in / 
# Fri, 26 Aug 2022 21:25:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Aug 2022 21:43:52 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 26 Aug 2022 21:45:41 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Fri, 26 Aug 2022 21:45:41 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Aug 2022 21:45:41 GMT
ENV LANG=C.UTF-8
# Fri, 26 Aug 2022 21:45:41 GMT
ENV JAVA_VERSION=19
# Fri, 26 Aug 2022 21:45:54 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk19/877d6127e982470ba2a7faa31cc93d04/36/GPL/openjdk-19_linux-x64_bin.tar.gz'; 			downloadSha256='f47aba585cfc9ecff1ed8e023524e8309f4315ed8b80100b40c7dcc232c12f96'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk19/877d6127e982470ba2a7faa31cc93d04/36/GPL/openjdk-19_linux-aarch64_bin.tar.gz'; 			downloadSha256='682bfb48158ca198393c4b7fd38f873e8d6316b0bc6511a07e917f7f0f3afb03'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 26 Aug 2022 21:45:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ee4ca39e1b6ea333d785f1cbc6b64b874a4f16f1200dad9e17d2015c925d1d57`  
		Last Modified: Fri, 26 Aug 2022 21:27:39 GMT  
		Size: 39.5 MB (39520501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f806f92441177162c8149eb36189b0eae2287007a7837b949d24fb72102008`  
		Last Modified: Fri, 26 Aug 2022 21:49:14 GMT  
		Size: 12.2 MB (12237733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b11390d2894ede6b9b09715add64eb2074e3124e707bee1f55e9a7e0603763`  
		Last Modified: Fri, 26 Aug 2022 21:53:18 GMT  
		Size: 196.2 MB (196183399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-rc-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7db8703448afc2865dab8b6ee6513da24816370e873f921f01792c64f37b7caa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246387345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01f2b29f2621586662115f27ed16b684271ae582b87fb6af607f68864499679`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 24 Aug 2022 19:54:55 GMT
ADD file:2016956ebf5b305d0029ca641d3175f879fb9c5f35f801b5c52927afeb8f8422 in / 
# Wed, 24 Aug 2022 19:54:56 GMT
CMD ["/bin/bash"]
# Wed, 24 Aug 2022 23:30:51 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 24 Aug 2022 23:32:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Wed, 24 Aug 2022 23:32:50 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Aug 2022 23:32:51 GMT
ENV LANG=C.UTF-8
# Wed, 24 Aug 2022 23:32:52 GMT
ENV JAVA_VERSION=19
# Wed, 24 Aug 2022 23:33:28 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk19/877d6127e982470ba2a7faa31cc93d04/36/GPL/openjdk-19_linux-x64_bin.tar.gz'; 			downloadSha256='f47aba585cfc9ecff1ed8e023524e8309f4315ed8b80100b40c7dcc232c12f96'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk19/877d6127e982470ba2a7faa31cc93d04/36/GPL/openjdk-19_linux-aarch64_bin.tar.gz'; 			downloadSha256='682bfb48158ca198393c4b7fd38f873e8d6316b0bc6511a07e917f7f0f3afb03'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 24 Aug 2022 23:33:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4fad3655bea38b31843315fea6a076b3b13bee189d1b3d017cf9beb5feb39909`  
		Last Modified: Wed, 24 Aug 2022 19:56:49 GMT  
		Size: 38.3 MB (38320858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299639459c280cc4a1b9d1299ff192e2925aef24610273aa1288cbbecdd6e689`  
		Last Modified: Wed, 24 Aug 2022 23:40:50 GMT  
		Size: 13.0 MB (13041901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d1ec959eed504aa09994e9c2d4205d2c4e64d5cb165df226364a2045c4adb6`  
		Last Modified: Wed, 24 Aug 2022 23:43:04 GMT  
		Size: 195.0 MB (195024586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

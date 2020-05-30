## `openjdk:15-oracle`

```console
$ docker pull openjdk@sha256:ffe7d8b4f1a8c1310dbef7acbf7769ed09ab980b889016676dceeb69e4e01ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:15-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:2b3783bcc6cec6b060c6219c8e69ef09750edf6ae51fa3617312b6269477f0e0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253654599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60de42bf9f2621c3078a15f6f0e11a6af9df792bccb47f09a4d07fa214c87a1d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Mon, 04 May 2020 20:20:53 GMT
ADD file:d23891d2372d6aae3d738388c74dacd92f9406083ee0c1ac0e2bfd140f92ec2b in / 
# Mon, 04 May 2020 20:20:53 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2020 20:38:21 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Mon, 04 May 2020 20:38:21 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2020 20:38:21 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Mon, 04 May 2020 20:38:21 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 May 2020 00:32:50 GMT
ENV JAVA_VERSION=15-ea+25
# Sat, 30 May 2020 00:33:22 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/25/GPL/openjdk-15-ea+25_linux-aarch64_bin.tar.gz; 			downloadSha256=32bd13e6fc92dba80d7eb504435a7bd9cbdb0aec2246476eb893b3ef5c5e8f66; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/25/GPL/openjdk-15-ea+25_linux-x64_bin.tar.gz; 			downloadSha256=6380fb115db35eea50760346cb4828d7e4054481f025acd84e3b39a3bc2d61eb; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o /openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Sat, 30 May 2020 00:33:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:83755823a002357171a0b229ef5769a60db47a90b624adc45f8c6b7cd1d1394f`  
		Last Modified: Mon, 04 May 2020 20:22:07 GMT  
		Size: 43.5 MB (43455265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e105caaf23acf967db67aa1f683d428603dbb51e12295bfe8f5df6a4cce8bb`  
		Last Modified: Mon, 04 May 2020 20:40:58 GMT  
		Size: 14.8 MB (14758294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c40c9f65704026d328aa09a6a5a3e3e42c81ac9941fbdda37bddf4304e0492a8`  
		Last Modified: Sat, 30 May 2020 00:35:59 GMT  
		Size: 195.4 MB (195441040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:15-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9b2f94d88654938b5af1552bcc8dc418c4c0259cba63aa12d948780b69e09dc4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233904096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f752b18e31aa244962721172b3929b42f80481aeb36bfddbc43f673541dd414`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 May 2019 21:40:52 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Mon, 04 May 2020 20:42:34 GMT
ADD file:b059ded860ba734fbe035c768d5c7e01a82decd7db5ca12f093672dab3b204c3 in / 
# Mon, 04 May 2020 20:42:37 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2020 01:43:47 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 22 May 2020 01:43:48 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2020 01:43:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Fri, 22 May 2020 01:43:49 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 May 2020 00:56:31 GMT
ENV JAVA_VERSION=15-ea+25
# Sat, 30 May 2020 00:58:00 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/25/GPL/openjdk-15-ea+25_linux-aarch64_bin.tar.gz; 			downloadSha256=32bd13e6fc92dba80d7eb504435a7bd9cbdb0aec2246476eb893b3ef5c5e8f66; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk15/25/GPL/openjdk-15-ea+25_linux-x64_bin.tar.gz; 			downloadSha256=6380fb115db35eea50760346cb4828d7e4054481f025acd84e3b39a3bc2d61eb; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o /openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Sat, 30 May 2020 00:58:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fa5299bfe4aa00db1c3f39321cc679889e30f51f690a75b8c75163698c4c7831`  
		Last Modified: Mon, 04 May 2020 20:43:38 GMT  
		Size: 44.1 MB (44074523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342df9bce1d80b8bdf565c6ceb8cbb008ee180f7fd52e3006d84ae4f81d0dc67`  
		Last Modified: Fri, 22 May 2020 01:48:19 GMT  
		Size: 15.0 MB (15028449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a74a4c61c5d13d07495e5c258bd4d7c34d2e267dead470535c47573edb2231`  
		Last Modified: Sat, 30 May 2020 01:03:51 GMT  
		Size: 174.8 MB (174801124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

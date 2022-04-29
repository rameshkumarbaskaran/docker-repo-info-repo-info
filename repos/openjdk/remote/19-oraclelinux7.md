## `openjdk:19-oraclelinux7`

```console
$ docker pull openjdk@sha256:e52ef5c1750c34b1f84143ae0e3d1995ee1656dfe9975184b4be53c7ac7ec4e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:b44530770ea968458f9ec38235971c554a1d97362807115add9ca687756ef044
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257663369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:977975e484796d9c69be16d6326a8a6c123836007f248935e8a983bc1d971aa2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Mar 2022 18:36:11 GMT
ADD file:b0df42f2bb614be48861be26e670ab6a81c1549d24e64b5e355980adcf0074be in / 
# Tue, 29 Mar 2022 18:36:11 GMT
CMD ["/bin/bash"]
# Tue, 29 Mar 2022 23:06:58 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 29 Mar 2022 23:06:58 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Tue, 29 Mar 2022 23:06:58 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 23:06:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Apr 2022 23:20:38 GMT
ENV JAVA_VERSION=19-ea+20
# Thu, 28 Apr 2022 23:20:47 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/20/GPL/openjdk-19-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='e5667a2a1208eb3042dd0c3187dd61d10b435204e4d26e466b8f2c7a5d988ce6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/20/GPL/openjdk-19-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5ff38640a2b5097e460a7dd54544f0cbe19b041262549cd3d1015fc81eec50f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 28 Apr 2022 23:20:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9347a8f0b30748522f1f50b679f9f2d0c3eea2bb49da98bb4f38a8c8619b7bf8`  
		Last Modified: Tue, 29 Mar 2022 18:37:31 GMT  
		Size: 48.8 MB (48757483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80558a30268385e2f78e93d6dcd977e92f7c76354c6ca130dd3ac4cb4b90f212`  
		Last Modified: Tue, 29 Mar 2022 23:18:51 GMT  
		Size: 14.2 MB (14239096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dade85d7b26fc1e92c679fe95cf337cc48a7f375f59159ef185cd612b1a599c5`  
		Last Modified: Thu, 28 Apr 2022 23:28:28 GMT  
		Size: 194.7 MB (194666790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:95274ee29a881b5a7141c6bc19fd2f464a84017670f7d4078aa28674d9259c22
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.1 MB (258121760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7a14721b2a461911cd8b4b13a6bdc710f6d461afc1c219f3851482ce9dcae0`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Mar 2022 18:27:34 GMT
ADD file:90c167a56275b374fb1719a6f499aea26290701a7baef901065a814af0e9e7c0 in / 
# Tue, 29 Mar 2022 18:27:35 GMT
CMD ["/bin/bash"]
# Wed, 30 Mar 2022 08:58:30 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 30 Mar 2022 08:58:31 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Wed, 30 Mar 2022 08:58:32 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:58:33 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Apr 2022 23:41:14 GMT
ENV JAVA_VERSION=19-ea+20
# Thu, 28 Apr 2022 23:41:30 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/20/GPL/openjdk-19-ea+20_linux-x64_bin.tar.gz'; 			downloadSha256='e5667a2a1208eb3042dd0c3187dd61d10b435204e4d26e466b8f2c7a5d988ce6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/20/GPL/openjdk-19-ea+20_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5ff38640a2b5097e460a7dd54544f0cbe19b041262549cd3d1015fc81eec50f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 28 Apr 2022 23:41:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b8909fcd1d3ed60203b3ef173f01925cfd334ae0874f19f3d19876d262428e7e`  
		Last Modified: Tue, 29 Mar 2022 18:29:06 GMT  
		Size: 49.3 MB (49339436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053940d29ef2ce62ec889516ac542e5db9ba471201782b15c2890f3f0be5b92c`  
		Last Modified: Wed, 30 Mar 2022 09:19:27 GMT  
		Size: 15.3 MB (15253020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040206c8f8748631dde4f2eb5e8d5bab87f83d2c94347c2445067b3887173aae`  
		Last Modified: Thu, 28 Apr 2022 23:55:32 GMT  
		Size: 193.5 MB (193529304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

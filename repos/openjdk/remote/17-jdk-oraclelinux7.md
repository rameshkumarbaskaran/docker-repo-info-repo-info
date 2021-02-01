## `openjdk:17-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:49ef6f302fa1381c56fab3be02867b8fb5b3ee2b115bc05806eaf7ac5618bddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:17-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:929c01c36df64ae835f1331dc98ab4b2fdf9153be251c2548d65108d8dc5c395
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.3 MB (249343121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15bb31b2788c79197db39da9f26972295aa9b1097c92d345e38391355c6c8a88`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 15 Jan 2021 00:31:31 GMT
ADD file:dee09ad1ed4e7359b14fabc84890b1fb687ad4efe75f7c4800c0a907fd4f70a3 in / 
# Fri, 15 Jan 2021 00:31:32 GMT
CMD ["/bin/bash"]
# Fri, 15 Jan 2021 00:58:14 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Mon, 01 Feb 2021 19:44:50 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Mon, 01 Feb 2021 19:44:51 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:44:51 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Feb 2021 19:44:51 GMT
ENV JAVA_VERSION=17-ea+7
# Mon, 01 Feb 2021 19:45:05 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/7/GPL/openjdk-17-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='0e340613945c78b2eb714ba0850604a1a80a9678ba0e8d81f66629c0ca2c36b1'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/7/GPL/openjdk-17-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='f3f80fc9b41cfddd89d263ae66c0f514aaeb3db2eadd6c9bf3c31e1b2cdcf44e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 01 Feb 2021 19:45:05 GMT
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
	-	`sha256:73c3d49f1d06670ac272e0308f30a80bcba24be000797e40956d99c4652c044a`  
		Last Modified: Mon, 01 Feb 2021 20:01:19 GMT  
		Size: 185.7 MB (185650624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:275ffe48e991cd71474f154f2506418129c97373a3bebcf785232443e0510f7f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245338541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e4b0b90d53bb98437d3b3342ae82e705ed369b9333c8dd6f2eee382b9494d7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 01 Feb 2021 21:01:37 GMT
ADD file:515797e9c94114d9811e4f5e7ef89e24a7c02f5496694320cf17c5b2c2c62577 in / 
# Mon, 01 Feb 2021 21:01:39 GMT
CMD ["/bin/bash"]
# Mon, 01 Feb 2021 21:07:57 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Mon, 01 Feb 2021 21:07:58 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Mon, 01 Feb 2021 21:07:59 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 21:07:59 GMT
ENV LANG=en_US.UTF-8
# Mon, 01 Feb 2021 21:08:00 GMT
ENV JAVA_VERSION=17-ea+7
# Mon, 01 Feb 2021 21:08:23 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/7/GPL/openjdk-17-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='0e340613945c78b2eb714ba0850604a1a80a9678ba0e8d81f66629c0ca2c36b1'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/7/GPL/openjdk-17-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='f3f80fc9b41cfddd89d263ae66c0f514aaeb3db2eadd6c9bf3c31e1b2cdcf44e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 01 Feb 2021 21:08:25 GMT
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
	-	`sha256:8958fdc16bc40803d98fd887fa57e1a77cfc2b6606f2cb5094e4fa7bf7c306ea`  
		Last Modified: Mon, 01 Feb 2021 21:16:44 GMT  
		Size: 180.0 MB (180020932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

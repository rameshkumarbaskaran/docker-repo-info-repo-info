## `openjdk:19-ea-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:474fd953fc7c7ccad9ba80c3e22e58f21c6370eb7929849de9ec298d60aed03b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-ea-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:9bc5ad9383d65466243a96fdda20a58f2be740d064f3d55853eed833accdb2b2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253921778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b1b6c037180f6ac93b5a09c9d819f27faac4fa1211471bc3e645eb02c471bd`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 24 Feb 2022 01:15:28 GMT
ADD file:a953cc04974b35909ddbd8826601c0824f8cc920ebc522046d4ca64e69c2c26f in / 
# Thu, 24 Feb 2022 01:15:29 GMT
CMD ["/bin/bash"]
# Thu, 24 Feb 2022 01:47:39 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 24 Feb 2022 01:47:40 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Thu, 24 Feb 2022 01:47:40 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 24 Feb 2022 01:47:40 GMT
ENV LANG=en_US.UTF-8
# Thu, 24 Feb 2022 01:47:40 GMT
ENV JAVA_VERSION=19-ea+10
# Thu, 24 Feb 2022 01:48:13 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/10/GPL/openjdk-19-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='21260b7e784c0e74c6730bdbaac70484fde42cf2839b2188dd2c4811d04660d8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/10/GPL/openjdk-19-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='e41beaf49bdb16dc2eeec5e7e7c535f19444e221daf1cbb97d6e2b7981583156'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 24 Feb 2022 01:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5269884ada0dd8683c910050c7cf3a447be8fcb9f733519f759745b117b217cc`  
		Last Modified: Thu, 24 Feb 2022 01:16:17 GMT  
		Size: 48.3 MB (48331243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48833246028b375ed9389617e9b863bfab004c27db95b93b1e8b7c646ce3f9a1`  
		Last Modified: Thu, 24 Feb 2022 01:58:10 GMT  
		Size: 15.4 MB (15402391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7672cb2613e7de3ffdf3872aacd6b01893206f5e16223740cd3f182fcc75a8`  
		Last Modified: Thu, 24 Feb 2022 01:58:23 GMT  
		Size: 190.2 MB (190188144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f7a877abd72f159fd4d04cc2a205da7c3418829a37dfc26836b99565922fc3ae
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 MB (254572612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bfaae239a0f2a55d94ba97cc3ab6e1cae1634bd34b834951fe9c2b69aca6e25`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:48 GMT
ADD file:933bf8bd076f0c42499df14ceb4b409753b2ce9f8b0bd81331ac2630b6dab149 in / 
# Fri, 25 Feb 2022 02:07:49 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 02:27:32 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 25 Feb 2022 02:27:32 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Fri, 25 Feb 2022 02:27:33 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Feb 2022 02:27:34 GMT
ENV LANG=en_US.UTF-8
# Fri, 25 Feb 2022 02:27:35 GMT
ENV JAVA_VERSION=19-ea+10
# Fri, 25 Feb 2022 02:27:55 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/10/GPL/openjdk-19-ea+10_linux-x64_bin.tar.gz'; 			downloadSha256='21260b7e784c0e74c6730bdbaac70484fde42cf2839b2188dd2c4811d04660d8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/10/GPL/openjdk-19-ea+10_linux-aarch64_bin.tar.gz'; 			downloadSha256='e41beaf49bdb16dc2eeec5e7e7c535f19444e221daf1cbb97d6e2b7981583156'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 25 Feb 2022 02:27:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5148c102f8614047b0330785165cb7096428df640af91104fbe61a7ebb5b8713`  
		Last Modified: Fri, 25 Feb 2022 02:09:24 GMT  
		Size: 48.9 MB (48901247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5afd0c7f5b0b7ae1e56ff4afb456806881a77fe14b8769883e0684cbcb9ac76`  
		Last Modified: Fri, 25 Feb 2022 02:48:54 GMT  
		Size: 16.4 MB (16445028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3237b3e4aef297d02561c2c1c5c657693dca7d4a5da21d095d84def23f084c0`  
		Last Modified: Fri, 25 Feb 2022 02:49:21 GMT  
		Size: 189.2 MB (189226337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

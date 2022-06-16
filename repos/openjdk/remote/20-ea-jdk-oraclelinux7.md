## `openjdk:20-ea-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:a3dcac23394f225a6b3f9386dafc36801eccca5e97704e6869cdb2743de09ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:5bfe7da0089b465d369fa357c1da498d0a86d54387bf37d14f28e807e17e6a3a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260102107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7c6cc325b9415974fa381849df27aa81c586a0fed2b85c4967102b3e915d52`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Jun 2022 01:20:22 GMT
ADD file:5e615d6d49ec50cba937fa86f5fb7d6a4a7e680b2b4f5b659e879b95304c0417 in / 
# Thu, 16 Jun 2022 01:20:22 GMT
CMD ["/bin/bash"]
# Thu, 16 Jun 2022 01:22:07 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 16 Jun 2022 01:22:07 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Thu, 16 Jun 2022 01:22:07 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jun 2022 01:22:08 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Jun 2022 01:22:08 GMT
ENV JAVA_VERSION=20-ea+1
# Thu, 16 Jun 2022 01:22:17 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/1/GPL/openjdk-20-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='0abed92a0e13e5d0f0d02463a90b21a040db83ea57617f5c61c5547862152766'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/1/GPL/openjdk-20-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='898a2f8ca4e530d154e94ca685ef4f03341cd78f3514661a03c8f87bfbdd2371'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 16 Jun 2022 01:22:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63183c9b4598e16c4cef95f706d50ff6c928de41f391cd513495b27eaa27bf89`  
		Last Modified: Thu, 16 Jun 2022 01:21:08 GMT  
		Size: 48.8 MB (48757931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb5aec2fa88dbfc29b4af04e13302acbb1298cf96be28433c81b5293be618be`  
		Last Modified: Thu, 16 Jun 2022 01:31:20 GMT  
		Size: 14.2 MB (14236378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcc323a40b1c21dcc1650364d51c4d48921bf7510aafe6d522174d4eb77259b`  
		Last Modified: Thu, 16 Jun 2022 01:31:33 GMT  
		Size: 197.1 MB (197107798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a2121707c59be608d297784940a090e26cb0495f6280e60517229d09cd7ca965
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.6 MB (260557845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61bf67e1131ee92777a5654e86c95e31f96f3b666fdbf596a735db9005bbd447`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Jun 2022 01:12:02 GMT
ADD file:3c802f9fbd1a9a4878df064e2b268b017930633407658a3f9d29e53eb74552fa in / 
# Thu, 16 Jun 2022 01:12:03 GMT
CMD ["/bin/bash"]
# Thu, 16 Jun 2022 02:52:59 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 16 Jun 2022 02:53:00 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Thu, 16 Jun 2022 02:53:01 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jun 2022 02:53:02 GMT
ENV LANG=en_US.UTF-8
# Thu, 16 Jun 2022 02:53:03 GMT
ENV JAVA_VERSION=20-ea+1
# Thu, 16 Jun 2022 02:53:21 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/1/GPL/openjdk-20-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='0abed92a0e13e5d0f0d02463a90b21a040db83ea57617f5c61c5547862152766'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/1/GPL/openjdk-20-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='898a2f8ca4e530d154e94ca685ef4f03341cd78f3514661a03c8f87bfbdd2371'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 16 Jun 2022 02:53:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9071f63390163e069a5245aea05c5a92f0dd4a4a48483db57c4c3c0d557be5e7`  
		Last Modified: Thu, 16 Jun 2022 01:12:57 GMT  
		Size: 49.3 MB (49343296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e709d91969def8bffeaecd5e24c79283c0850fbc3e9924fe9ae16ad997e75ac`  
		Last Modified: Thu, 16 Jun 2022 03:07:48 GMT  
		Size: 15.3 MB (15264634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68347634e9f59181fb2b04bf456d4f35c5dab88daab96dba63594e6bef51be61`  
		Last Modified: Thu, 16 Jun 2022 03:08:01 GMT  
		Size: 195.9 MB (195949915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `openjdk:18-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:0e65e6c7fe04a93530095461d395cda84f070fa31c9f663d2bef2b09d089ad7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:222eb0b2007a22bdb18c0133f1002f58e96c8d1319d0111e618ea58237dc3736
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252356981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50847aa138563250d858eea4c25bee2877125557af1efa38b356520c1a15d32e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 12 Jan 2022 22:34:30 GMT
ADD file:18acb1f3ef1ffe1aeaff1aa22861026180d22104f6f14dd8bc4656777800fd9f in / 
# Wed, 12 Jan 2022 22:34:30 GMT
CMD ["/bin/bash"]
# Wed, 12 Jan 2022 22:51:37 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 12 Jan 2022 22:52:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Wed, 12 Jan 2022 22:52:20 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jan 2022 22:52:20 GMT
ENV LANG=en_US.UTF-8
# Wed, 12 Jan 2022 22:52:20 GMT
ENV JAVA_VERSION=18-ea+30
# Wed, 12 Jan 2022 22:52:36 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/30/GPL/openjdk-18-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='4e34f307a3d9b1c020a864e863a0f47c701036592d634da55c6e548d101526ed'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/30/GPL/openjdk-18-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='10fd6ab1369a4cd536570c4cccfd2aead86bfd733fd7171de74e0b979c04b96e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 12 Jan 2022 22:52:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1e1d49338f200e5dab7ef55f9d3a37259af48812603e07ae59e43615f9038b27`  
		Last Modified: Wed, 12 Jan 2022 22:35:18 GMT  
		Size: 48.3 MB (48330956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c20bdba8622bf1a49d6c3edad81bd7ef39ec5a507eb70d2e536a70e60263ba4`  
		Last Modified: Wed, 12 Jan 2022 23:00:42 GMT  
		Size: 15.4 MB (15388577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dddb23c7e196898ea9f08a2827fd9d2ce7cba935911ee5c75ca89d7ee3358e2`  
		Last Modified: Wed, 12 Jan 2022 23:01:46 GMT  
		Size: 188.6 MB (188637448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:2cbecdb483c468bc8865ff73d17a39426055f26108fe33a62ce7ea0ffc3a1811
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.9 MB (252936029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea90b78f00955b5d3ba1c5edb0d1539d499dce74586c71199d288b59c044ff3e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 12 Jan 2022 21:41:07 GMT
ADD file:64aef77ed2e10e924b07f118b92f579949f920597f01ce3580c3cd17fc289b87 in / 
# Wed, 12 Jan 2022 21:41:08 GMT
CMD ["/bin/bash"]
# Wed, 12 Jan 2022 21:58:19 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 12 Jan 2022 21:59:37 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Wed, 12 Jan 2022 21:59:37 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jan 2022 21:59:38 GMT
ENV LANG=en_US.UTF-8
# Wed, 12 Jan 2022 21:59:39 GMT
ENV JAVA_VERSION=18-ea+30
# Wed, 12 Jan 2022 21:59:56 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/30/GPL/openjdk-18-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='4e34f307a3d9b1c020a864e863a0f47c701036592d634da55c6e548d101526ed'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/30/GPL/openjdk-18-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='10fd6ab1369a4cd536570c4cccfd2aead86bfd733fd7171de74e0b979c04b96e'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 12 Jan 2022 21:59:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:89ad662320eff0a72aa4fc7f7af6e2a2ffe2dc642aacc7fcf25ada107b2cc3de`  
		Last Modified: Wed, 12 Jan 2022 21:42:00 GMT  
		Size: 48.9 MB (48902767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcbd5e1a30531d664d4f4f1f2c5a28be251ea96d8b492a51eabd8b7339c2f97`  
		Last Modified: Wed, 12 Jan 2022 22:12:56 GMT  
		Size: 16.5 MB (16464202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b005f44e239f58d9bc6281d503926f0077637fc7e3aba912d49a436201b36bc`  
		Last Modified: Wed, 12 Jan 2022 22:14:20 GMT  
		Size: 187.6 MB (187569060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

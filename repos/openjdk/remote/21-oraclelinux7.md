## `openjdk:21-oraclelinux7`

```console
$ docker pull openjdk@sha256:dfb91794c910eb159facb02504b4750fe62cf244c085431a9f7e8ea25c2b4596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:21-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:5db7913cc3b172c72bea9bc424323e200d4651d2f97ffafa9b8cd413c45eac50
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.2 MB (264239598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edcc14f6a48b4a5c752ddc579f4591751352fd367c03635025441d68c5d7c2e5`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Mar 2023 20:22:54 GMT
ADD file:e205deb729daf99a168c27d3f97cd2b69e736fc9d4bee9ea220ec86921574a0f in / 
# Wed, 08 Mar 2023 20:22:55 GMT
CMD ["/bin/bash"]
# Wed, 08 Mar 2023 20:54:26 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 08 Mar 2023 20:54:26 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Wed, 08 Mar 2023 20:54:26 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Mar 2023 20:54:26 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Mar 2023 23:26:51 GMT
ENV JAVA_VERSION=21-ea+13
# Thu, 09 Mar 2023 23:27:01 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/13/GPL/openjdk-21-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='bc6ffa91e66ea5507449ce61cc7b7090d94f844bdd1eb531b6796f4d017f93bc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/13/GPL/openjdk-21-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='47f8c074276fdfa3705653b0d8beba18bfc8e684762dd6a5b37d03c6b1db9632'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 09 Mar 2023 23:27:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7b659169cb9226d08443358aa4e8147f3144614ac33f7a41217b0cf62a4d3326`  
		Last Modified: Wed, 08 Mar 2023 20:24:41 GMT  
		Size: 50.5 MB (50467964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efc12c70e0ba49ea5eb742d598c3d36a33b4d7407f8be1a8ac8641ad14e0a56`  
		Last Modified: Wed, 08 Mar 2023 20:57:27 GMT  
		Size: 14.2 MB (14236997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d77454673e5cbff3f6e61ab8804dd4f82c78800e9327e5152b5549fdfdc0d8c`  
		Last Modified: Thu, 09 Mar 2023 23:30:39 GMT  
		Size: 199.5 MB (199534637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7486d81255eb2d70f890b26b59544e4e6e60da7bdf9731956d29855c56f7395e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.3 MB (264313520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a20b205ffc9c2e01168b9ad4be40218e2404cae2102a33c82f5e926c2be285f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Mar 2023 21:02:36 GMT
ADD file:d11a3555d107d9db5ab5621675aa2ecf27ec872cc591769bdc75129ff602dfd7 in / 
# Wed, 08 Mar 2023 21:02:37 GMT
CMD ["/bin/bash"]
# Wed, 08 Mar 2023 21:20:32 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 08 Mar 2023 21:20:32 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Wed, 08 Mar 2023 21:20:32 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Mar 2023 21:20:32 GMT
ENV LANG=en_US.UTF-8
# Thu, 09 Mar 2023 22:47:09 GMT
ENV JAVA_VERSION=21-ea+13
# Thu, 09 Mar 2023 22:47:23 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/13/GPL/openjdk-21-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='bc6ffa91e66ea5507449ce61cc7b7090d94f844bdd1eb531b6796f4d017f93bc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/13/GPL/openjdk-21-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='47f8c074276fdfa3705653b0d8beba18bfc8e684762dd6a5b37d03c6b1db9632'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 09 Mar 2023 22:47:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4b689a883b146569199f6bfaadce974725d68f1cd14d01950efe476637febe12`  
		Last Modified: Wed, 08 Mar 2023 21:04:11 GMT  
		Size: 51.0 MB (51027010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ce6fa2927eee2bba1cdfc5060760f859a7073e02bf271b9b61999943c2211d`  
		Last Modified: Wed, 08 Mar 2023 21:23:34 GMT  
		Size: 15.2 MB (15249325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b148a0bea3a28668db198ea6edc19e9605ede5ea08c641d6ec5e4f9265b4857`  
		Last Modified: Thu, 09 Mar 2023 22:51:06 GMT  
		Size: 198.0 MB (198037185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

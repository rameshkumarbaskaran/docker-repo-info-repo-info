## `openjdk:20-ea-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:0b24897ef543738d59b276409220ae00aa9ddef8c83ce1b4f9f9c864d80f8fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:672957d60ea9f1d21faec3becc9d997644503e4bf1a14509c69494baf08c7bbf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (261025633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f31b9d55785ac8dda57655da65a18b4adb4d18a90e8e40979f77138aaf56337`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Oct 2022 20:32:03 GMT
ADD file:d7b7ed3315719e2a7f19233b68dbf42298d9d6e1a882de7154751ad29710eeac in / 
# Fri, 07 Oct 2022 20:32:03 GMT
CMD ["/bin/bash"]
# Fri, 07 Oct 2022 20:50:44 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 07 Oct 2022 20:50:45 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Fri, 07 Oct 2022 20:50:45 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Oct 2022 20:50:45 GMT
ENV LANG=en_US.UTF-8
# Fri, 07 Oct 2022 23:45:56 GMT
ENV JAVA_VERSION=20-ea+18
# Fri, 07 Oct 2022 23:46:10 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/18/GPL/openjdk-20-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='1081d9b6e6439841c3665fe65caf47431f7a6208ff6da8ee66a617a5577754c1'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/18/GPL/openjdk-20-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='92161bb7811ac65f8a1deddef23028d817634cab1605a7255aefb517c2a2f6f8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 07 Oct 2022 23:46:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0056409b8e897373ba0cef19c5e1f387c06dafd5e11f3f2f0f22d34c8acb6717`  
		Last Modified: Fri, 07 Oct 2022 20:34:25 GMT  
		Size: 49.9 MB (49869229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f738e86ce06f94dc5d19ca70ae49d8b2442605a4c05912a8a401f2a0d6da130a`  
		Last Modified: Fri, 07 Oct 2022 20:54:58 GMT  
		Size: 14.2 MB (14241449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9575a61324bfc4d3187096921e2a9cac5c1ec4a36363c84c59aee86533212322`  
		Last Modified: Fri, 07 Oct 2022 23:50:38 GMT  
		Size: 196.9 MB (196914955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7214f65e8cd0393fbaba02f8c9c37e7c18c9a7cca1a38f0a5a4fb589ed989a56
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 MB (261160431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92cac1a00f06eae4c47624bbb6b770dfba712fa979dbf24485a0e6579269e3b9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Oct 2022 20:52:08 GMT
ADD file:bd392af27b158db82c5b1c7acfd7aa49ada7d4eda11ea878a109b9c92f64b349 in / 
# Fri, 07 Oct 2022 20:52:09 GMT
CMD ["/bin/bash"]
# Fri, 07 Oct 2022 21:14:39 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 07 Oct 2022 21:14:39 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Fri, 07 Oct 2022 21:14:40 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Oct 2022 21:14:41 GMT
ENV LANG=en_US.UTF-8
# Fri, 07 Oct 2022 21:14:42 GMT
ENV JAVA_VERSION=20-ea+17
# Fri, 07 Oct 2022 21:15:00 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/17/GPL/openjdk-20-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='9d46acb0892a134f62ab21fca33fdef1da5d579f61ddbd0ae3ff0b4d33c5eca2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/17/GPL/openjdk-20-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='31245b15195bf9f12a6db08474bfcbd1ddbccc76436372bf4db538c6ede8f976'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 07 Oct 2022 21:15:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e5c63cf456b69584a9fa30dc0b1a5bca10abe38570de2326383f28a61ba1733`  
		Last Modified: Fri, 07 Oct 2022 20:54:19 GMT  
		Size: 50.4 MB (50440495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ebea763a2ab54a09b2c1fb8539a9b9f04dd09c1dbfc8c2ac2cf27892200da8`  
		Last Modified: Fri, 07 Oct 2022 21:22:10 GMT  
		Size: 15.3 MB (15260688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108da7f7d8f0c94a2839a6fe3826e2c0b5a70db8810564cb80fe3a0351916a4b`  
		Last Modified: Fri, 07 Oct 2022 21:22:25 GMT  
		Size: 195.5 MB (195459248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

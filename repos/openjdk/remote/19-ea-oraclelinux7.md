## `openjdk:19-ea-oraclelinux7`

```console
$ docker pull openjdk@sha256:300c98ffcbc4abd42a34949afd258a13ad1c3ed00774176ddbc32981105f1a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-ea-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:cb0c7164665dc0fca3006b7f5b8d4d04c3dac11e90a34732b1939cd8ac60a919
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.5 MB (257537700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b892ad94b069d78fa304e668dba33ad7d4d9467c1a0aec0135e88f46cf9de14c`
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
# Tue, 19 Apr 2022 02:53:40 GMT
ENV JAVA_VERSION=19-ea+18
# Tue, 19 Apr 2022 02:53:49 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/18/GPL/openjdk-19-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='c79b13e466464b0054cad0301cf53bcd4b083d591f5fe61e932f39d34063f93b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/18/GPL/openjdk-19-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='eeec6bd83fea107d1c6de91d7eb2936b7829e8315e81458beb4e401a9f51f006'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 19 Apr 2022 02:53:50 GMT
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
	-	`sha256:6fb4fae90e6bca1feb5c57ac07fc97e12c859e27f21a93a3548b2261c27ca6fd`  
		Last Modified: Tue, 19 Apr 2022 03:01:26 GMT  
		Size: 194.5 MB (194541121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:43d03a451b2c01c5ba105334f32049253e22838d3d2716e7ef5421e87389e4cb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (257991387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1790f2f30fd7bbbdaf2d25932b8f0cbaf2c46e4e3f40178256ddfb371c71181`
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
# Tue, 19 Apr 2022 03:31:37 GMT
ENV JAVA_VERSION=19-ea+18
# Tue, 19 Apr 2022 03:31:54 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/18/GPL/openjdk-19-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='c79b13e466464b0054cad0301cf53bcd4b083d591f5fe61e932f39d34063f93b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/18/GPL/openjdk-19-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='eeec6bd83fea107d1c6de91d7eb2936b7829e8315e81458beb4e401a9f51f006'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 19 Apr 2022 03:31:55 GMT
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
	-	`sha256:89ebd9c5ea1311dd41f25490ea2ff3c6f089077ef6eef544fb852419b2de23da`  
		Last Modified: Tue, 19 Apr 2022 03:45:57 GMT  
		Size: 193.4 MB (193398931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

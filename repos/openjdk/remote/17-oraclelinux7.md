## `openjdk:17-oraclelinux7`

```console
$ docker pull openjdk@sha256:4e8aefb69d0ff6d44d26542a32425de37aab0f038d7206cee00b04db9a9c1c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:17-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:67252fb431a8346b76044acde42f271578405de52a1e9f9aa4ae88265e5398f6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 MB (249706758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4e9e699c97d252334fed9221fa490d9b72f54268386007cfd0b9986624af2d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 06 May 2021 00:10:37 GMT
ADD file:7532c4c6850a2e95d341f39828f60573728d50ba1fc6264ed19bb36eb4b24d1c in / 
# Thu, 06 May 2021 00:10:37 GMT
CMD ["/bin/bash"]
# Thu, 06 May 2021 00:27:43 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 06 May 2021 00:27:43 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Thu, 06 May 2021 00:27:43 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 00:27:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 11 May 2021 00:14:55 GMT
ENV JAVA_VERSION=17-ea+21
# Tue, 11 May 2021 00:15:09 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/21/GPL/openjdk-17-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='2a923efe7bd6c682d5550551a16dadfe8057b0106e0b4b4aad2aa56b8bed4c19'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/21/GPL/openjdk-17-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='bb389fe6915c9e70e639db6ab630342a5ccc275f5a06aaded43321eeea9ba6ee'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 11 May 2021 00:15:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:22f7711cf64307564c3293688489295d9458bac2ca47cd6576382cfb75c9d2b9`  
		Last Modified: Thu, 06 May 2021 00:11:49 GMT  
		Size: 48.3 MB (48258661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87180291cc45c5c610f6909495ba989b36ef14701a331d8689e264f9d7c23796`  
		Last Modified: Thu, 06 May 2021 00:32:56 GMT  
		Size: 15.4 MB (15423518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a5acd9d928315c8d432dd2b3edf7d0aa53ff7458db91c67b866dfb4441c533`  
		Last Modified: Tue, 11 May 2021 00:21:54 GMT  
		Size: 186.0 MB (186024579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7fb309a17320b4052441f7b6a58ca378e7447133bf668b2b6f64fdd4381bea20
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247446315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd3a9c892b561528176c6569265990965a46edbd0c5d43b81c960ee5cd467d3`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 06 May 2021 00:13:32 GMT
ADD file:57303578fa11d312dcc51eb7aef116316c2b60e48b533a1471e2f2ba915ee46a in / 
# Thu, 06 May 2021 00:13:35 GMT
CMD ["/bin/bash"]
# Thu, 06 May 2021 00:32:13 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 06 May 2021 00:32:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Thu, 06 May 2021 00:32:15 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 May 2021 00:32:16 GMT
ENV LANG=en_US.UTF-8
# Tue, 11 May 2021 01:44:38 GMT
ENV JAVA_VERSION=17-ea+21
# Tue, 11 May 2021 01:45:05 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/21/GPL/openjdk-17-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='2a923efe7bd6c682d5550551a16dadfe8057b0106e0b4b4aad2aa56b8bed4c19'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/21/GPL/openjdk-17-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='bb389fe6915c9e70e639db6ab630342a5ccc275f5a06aaded43321eeea9ba6ee'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 11 May 2021 01:45:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6d575bf1166e11ab792c567b7bdfab507a987976bc375994e3516987e6e1e600`  
		Last Modified: Thu, 06 May 2021 00:14:38 GMT  
		Size: 48.9 MB (48869643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7892e1551bf2c1decd5f1f367d2f9dbf15317e29aa12b267cf59b9c255a91b34`  
		Last Modified: Thu, 06 May 2021 00:39:13 GMT  
		Size: 16.5 MB (16472243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82bf6b7023399005511c6bdf3af1a934da7f9a88a52b64b25ce310faa54dbf76`  
		Last Modified: Tue, 11 May 2021 01:51:47 GMT  
		Size: 182.1 MB (182104429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `openjdk:22-ea-oraclelinux7`

```console
$ docker pull openjdk@sha256:b2cdb57b8ad24f3ef1f12e274c2d07da355f82b766b1fdfa5c779e225abd12a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:22-ea-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:d540ba2b6dc8ae42f78482c1f52f8dcc0bababcca927480722385204fa70b46d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.7 MB (269677630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa70a982b4e313ae558839182363c95190c7d7a72854d01c60b81ffb61a2d5c0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Jun 2023 07:21:40 GMT
ADD file:733a37449d62d6e9f530185b9244e06cd8ff0ee896632576ae644437d0a1f852 in / 
# Wed, 14 Jun 2023 07:21:40 GMT
CMD ["/bin/bash"]
# Wed, 14 Jun 2023 09:56:49 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 14 Jun 2023 09:56:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Wed, 14 Jun 2023 09:56:49 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 09:56:49 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Sep 2023 19:44:01 GMT
ENV JAVA_VERSION=22-ea+14
# Fri, 08 Sep 2023 19:44:11 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/14/GPL/openjdk-22-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='2d6b271eaaecdedb8eee2e64b7cca4f36000039d3bdfe618460424fb8e449fcc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/14/GPL/openjdk-22-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='62b2cad2a14380255f3f0dee68193a8d2953c0b8cce04eae1f65427d4ab2b707'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 08 Sep 2023 19:44:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:70e9ff4420fbc58483e68c13199a06c24b14013b2548998a7e367f59ca5157bc`  
		Last Modified: Wed, 14 Jun 2023 07:22:30 GMT  
		Size: 50.5 MB (50484765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4714d29e017353e367cfbeb707bad46a96692fceb51533b3749c668baf3b5b8f`  
		Last Modified: Wed, 14 Jun 2023 09:58:27 GMT  
		Size: 14.2 MB (14242764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655abdf204fbd88aca3642da3287a6d8653a73547442ff359f2a8565d3aff0ef`  
		Last Modified: Fri, 08 Sep 2023 19:47:23 GMT  
		Size: 205.0 MB (204950101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:22-ea-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ff2121ea14211d217f872f48d85d338ec12ea06539fa116652e67c8dfcd82088
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.6 MB (269553797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f39e25fb4cba5231567308a1da900100debb5fb496039b8e9a7379a6c05974`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Jun 2023 03:45:43 GMT
ADD file:a9ba9c7acb256e802c7248b56f377a6f0ea08b1b61e11e482516633a13f4d686 in / 
# Wed, 14 Jun 2023 03:45:44 GMT
CMD ["/bin/bash"]
# Wed, 14 Jun 2023 04:08:20 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 14 Jun 2023 04:08:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Wed, 14 Jun 2023 04:08:20 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 04:08:20 GMT
ENV LANG=en_US.UTF-8
# Fri, 08 Sep 2023 21:01:11 GMT
ENV JAVA_VERSION=22-ea+14
# Fri, 08 Sep 2023 21:01:24 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/14/GPL/openjdk-22-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='2d6b271eaaecdedb8eee2e64b7cca4f36000039d3bdfe618460424fb8e449fcc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/14/GPL/openjdk-22-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='62b2cad2a14380255f3f0dee68193a8d2953c0b8cce04eae1f65427d4ab2b707'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 08 Sep 2023 21:01:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:52fd87ed40fcddc3fe63b876d1f94f6edae688637a5cc56983dced68a50c953e`  
		Last Modified: Wed, 14 Jun 2023 03:46:28 GMT  
		Size: 51.1 MB (51052081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39aeb39f5d39e6fb51e698f8f5e6416d0689047f9392a9bd3f97f28c4d5d5596`  
		Last Modified: Wed, 14 Jun 2023 04:10:01 GMT  
		Size: 15.2 MB (15238146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05c65f1312aac2d4b1b14e6a5192e04c370253ae796dc1a974bd6df18c4baef`  
		Last Modified: Fri, 08 Sep 2023 21:04:31 GMT  
		Size: 203.3 MB (203263570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

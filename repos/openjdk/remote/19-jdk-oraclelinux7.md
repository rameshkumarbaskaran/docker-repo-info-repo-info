## `openjdk:19-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:926e5a90b2c45c822f311eef408cf5b9a92564b405fc1e43917e55ebcf2e7fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:0f53b17885273476866ff7bd8eb95ff0b32a33dfb22b8446aa2e4016bd8fb3ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.3 MB (253251793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d841eec04e06803f9bb7f6aa6d0ca28ee2fba7a889c5e7312c18a580959c4f5`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 12 Jan 2022 22:34:30 GMT
ADD file:18acb1f3ef1ffe1aeaff1aa22861026180d22104f6f14dd8bc4656777800fd9f in / 
# Wed, 12 Jan 2022 22:34:30 GMT
CMD ["/bin/bash"]
# Wed, 12 Jan 2022 22:51:37 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 12 Jan 2022 22:51:37 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Wed, 12 Jan 2022 22:51:38 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jan 2022 22:51:38 GMT
ENV LANG=en_US.UTF-8
# Wed, 12 Jan 2022 22:51:38 GMT
ENV JAVA_VERSION=19-ea+4
# Wed, 12 Jan 2022 22:51:53 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/4/GPL/openjdk-19-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='4fe225c20bb97b663163789ee765fd6b4c20a240ef651a62b79b120d06a480a3'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/4/GPL/openjdk-19-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='9daa5ce7b7729b226fa853caef9d97abb7b2b0b485039055b74657c3c9df3e3c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 12 Jan 2022 22:51:54 GMT
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
	-	`sha256:6576111ebf7b1615b8d5eded194d91d8338c4e5ae4bca5d3e72e1e42c97fa121`  
		Last Modified: Wed, 12 Jan 2022 23:00:55 GMT  
		Size: 189.5 MB (189532260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ae441140d9c2ddec797e5428f7dcd8942b1b30d30cad9421c4f1bc1995e544d0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253819144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bafdd599c4f656d7244e76c914d0c2a6d689d8350690e9c7eb17e9f66c41c497`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 12 Jan 2022 21:41:07 GMT
ADD file:64aef77ed2e10e924b07f118b92f579949f920597f01ce3580c3cd17fc289b87 in / 
# Wed, 12 Jan 2022 21:41:08 GMT
CMD ["/bin/bash"]
# Wed, 12 Jan 2022 21:58:19 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 12 Jan 2022 21:58:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Wed, 12 Jan 2022 21:58:21 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jan 2022 21:58:22 GMT
ENV LANG=en_US.UTF-8
# Wed, 12 Jan 2022 21:58:23 GMT
ENV JAVA_VERSION=19-ea+4
# Wed, 12 Jan 2022 21:58:47 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/4/GPL/openjdk-19-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='4fe225c20bb97b663163789ee765fd6b4c20a240ef651a62b79b120d06a480a3'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/4/GPL/openjdk-19-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='9daa5ce7b7729b226fa853caef9d97abb7b2b0b485039055b74657c3c9df3e3c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 12 Jan 2022 21:58:47 GMT
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
	-	`sha256:ff83585f3cadb2b579d359c0bf1cd7ac8382823f09f162a0eae069db2cd914e7`  
		Last Modified: Wed, 12 Jan 2022 22:13:10 GMT  
		Size: 188.5 MB (188452175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

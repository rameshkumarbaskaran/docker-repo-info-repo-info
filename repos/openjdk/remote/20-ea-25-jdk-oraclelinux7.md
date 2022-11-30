## `openjdk:20-ea-25-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:41f0c968dfb250846044a09c50840d9776e67a7d3680a02107321ed8119d2640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-25-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:87501a9b1131d39f1bcf0f08ee904252a59f0f3c7db6aecf66923249e05aa9d5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (262000866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577f2911f53caba69908e749d2a8fa05744e134a1f48e7526c3cff2647fd3913`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Nov 2022 19:21:24 GMT
ADD file:ec2c8d4fc7614a3584827f15c6278d01c6d7f42892747f20aeccfa2feb526412 in / 
# Tue, 29 Nov 2022 19:21:25 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 19:44:29 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 29 Nov 2022 19:44:29 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Tue, 29 Nov 2022 19:44:29 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Nov 2022 19:44:30 GMT
ENV LANG=en_US.UTF-8
# Wed, 30 Nov 2022 21:30:36 GMT
ENV JAVA_VERSION=20-ea+25
# Wed, 30 Nov 2022 21:30:46 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/25/GPL/openjdk-20-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='f0f3728ab38a39676a67fa315b43706becf96a834cef0c1d441aca4da0bf1132'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/25/GPL/openjdk-20-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='9ae88d9f0e243c3081a897ce27f30b5359ca7e926d6ad83174dd28fd1d064a04'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 30 Nov 2022 21:30:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d96bccd7291ff1dc9e55f40b596e14900d110382763aa46814bc43ac1b40f57c`  
		Last Modified: Tue, 29 Nov 2022 19:23:17 GMT  
		Size: 49.8 MB (49828163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21dc1504ba6d49eee445e92e7d82d816810257ac694a462bb310e1d2bf178fd8`  
		Last Modified: Tue, 29 Nov 2022 19:48:44 GMT  
		Size: 14.2 MB (14217773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dbb6aaf9cc5a8adc1498901feafe92e7b74ade76b69973f129d7c2b20de2895`  
		Last Modified: Wed, 30 Nov 2022 21:35:16 GMT  
		Size: 198.0 MB (197954930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-25-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:119ef01f98c5c50386e91d0004a72e4ab78993b359fe2799b46e3a37cf1afba6
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.2 MB (262158842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf0c39997dd696ab8bfda6ce004002abbffed43f649e9c8517b33013d2c8e8b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Nov 2022 19:48:43 GMT
ADD file:5019a53be0205e5de5a1e1425dc3a4e8d6300733ab4bb1cdc29a6dbfc6a6a12c in / 
# Tue, 29 Nov 2022 19:48:44 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 20:06:51 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 29 Nov 2022 20:06:51 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Tue, 29 Nov 2022 20:06:52 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Nov 2022 20:06:52 GMT
ENV LANG=en_US.UTF-8
# Wed, 30 Nov 2022 20:54:33 GMT
ENV JAVA_VERSION=20-ea+25
# Wed, 30 Nov 2022 20:54:46 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/25/GPL/openjdk-20-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='f0f3728ab38a39676a67fa315b43706becf96a834cef0c1d441aca4da0bf1132'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/25/GPL/openjdk-20-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='9ae88d9f0e243c3081a897ce27f30b5359ca7e926d6ad83174dd28fd1d064a04'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 30 Nov 2022 20:54:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:32a97da7a0b03315fbde64fde482eae59f8581d380cfa0e24b35ffd3ad1d1bf2`  
		Last Modified: Tue, 29 Nov 2022 19:50:24 GMT  
		Size: 50.4 MB (50399247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7565e5cd26c7105898fa9f6b8389575df84b097aec6966840da625b7e2a3c7e9`  
		Last Modified: Tue, 29 Nov 2022 20:10:57 GMT  
		Size: 15.3 MB (15268420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:937d58c8483096dbe258f1d6dd2182fb3cb4a74933174dbba3106d150f38823e`  
		Last Modified: Wed, 30 Nov 2022 20:59:36 GMT  
		Size: 196.5 MB (196491175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

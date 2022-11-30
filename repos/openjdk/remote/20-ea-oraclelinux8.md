## `openjdk:20-ea-oraclelinux8`

```console
$ docker pull openjdk@sha256:72946994a8e33d82fa7418eb13b48a76a2ec693104cde01e571b0f61fd1565b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:a9b95f3fa00107f572285f2d504d0b6113281e6f6894a26125abaaba6488b154
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.1 MB (254072040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac9d9779691ebb9e22aee4657a48c8f2098b87ae8d551c3638215c62f4b92cb`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Nov 2022 19:20:57 GMT
ADD file:6767deed84cff167f77f7d9f835925cd8a5d3093d0b99f0180245cfd6312ae06 in / 
# Tue, 29 Nov 2022 19:20:58 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 19:43:57 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 29 Nov 2022 19:43:57 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Tue, 29 Nov 2022 19:43:57 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Nov 2022 19:43:57 GMT
ENV LANG=C.UTF-8
# Wed, 30 Nov 2022 21:30:19 GMT
ENV JAVA_VERSION=20-ea+25
# Wed, 30 Nov 2022 21:30:30 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/25/GPL/openjdk-20-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='f0f3728ab38a39676a67fa315b43706becf96a834cef0c1d441aca4da0bf1132'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/25/GPL/openjdk-20-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='9ae88d9f0e243c3081a897ce27f30b5359ca7e926d6ad83174dd28fd1d064a04'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 30 Nov 2022 21:30:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:996f1bba14d621751efdd3a7ff3a65db06e0edb9b3e211ef1c3e68223e053af7`  
		Last Modified: Tue, 29 Nov 2022 19:22:40 GMT  
		Size: 43.9 MB (43871608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1233d0894f0a77c915206fb2429d895953c3cef4150186d415a3c1c256a7f1`  
		Last Modified: Tue, 29 Nov 2022 19:48:00 GMT  
		Size: 12.2 MB (12246997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8f32fded979e2e5a2388e1a582202308ce0d86ccb602b89faa26d4bd5867e7`  
		Last Modified: Wed, 30 Nov 2022 21:34:34 GMT  
		Size: 198.0 MB (197953435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ebd2cc586cd2a395d971bc20d3583fcd33e128c52c29ae916b40a93c8bb8be00
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.3 MB (252333877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2af0d3774010abc846077d3a98f0926b6b0632757275852bdb2c81ebc3ea43e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Nov 2022 19:48:22 GMT
ADD file:8919add412c121e3fffd8882c8379cfef3889b0d6b18afc150e1bd4a4bae08d4 in / 
# Tue, 29 Nov 2022 19:48:23 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 20:06:02 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 29 Nov 2022 20:06:03 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Tue, 29 Nov 2022 20:06:03 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Nov 2022 20:06:03 GMT
ENV LANG=C.UTF-8
# Wed, 30 Nov 2022 20:54:16 GMT
ENV JAVA_VERSION=20-ea+25
# Wed, 30 Nov 2022 20:54:25 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/25/GPL/openjdk-20-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='f0f3728ab38a39676a67fa315b43706becf96a834cef0c1d441aca4da0bf1132'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/25/GPL/openjdk-20-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='9ae88d9f0e243c3081a897ce27f30b5359ca7e926d6ad83174dd28fd1d064a04'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 30 Nov 2022 20:54:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e16f89d504be05b35448ef4e921fc7ea5f090b53960d0bc6764f6d31a0ea2f4a`  
		Last Modified: Tue, 29 Nov 2022 19:49:52 GMT  
		Size: 42.8 MB (42775103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa7949e83b2b403f5e3a79f19d33aaa5ea4a1adb33854be91352471fec3fb34`  
		Last Modified: Tue, 29 Nov 2022 20:10:17 GMT  
		Size: 13.1 MB (13066550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9de3e6687c41f68a29727cf48968c2d7b7589e5bfd7864c7c605d8f228f9df7`  
		Last Modified: Wed, 30 Nov 2022 20:58:56 GMT  
		Size: 196.5 MB (196492224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

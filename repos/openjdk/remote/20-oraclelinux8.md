## `openjdk:20-oraclelinux8`

```console
$ docker pull openjdk@sha256:eefebddf204f47f5a525f722bf69870dd41140b3908f4a2df015f618a20f3914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:b4ee01ca5c7925026250fb6971709a16f311b49e3717029b230f2da591897a1e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.0 MB (251042264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bab8184f21de35719e60326e04a9acee05af4b203e6c1f94d7d40be566b1f75`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 04 Nov 2022 23:33:07 GMT
ADD file:00e6899b8d3eccf7f795d17f9316af6ae0f3955ef2204b61bd064f5173c18357 in / 
# Fri, 04 Nov 2022 23:33:07 GMT
CMD ["/bin/bash"]
# Sat, 05 Nov 2022 02:19:43 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Sat, 05 Nov 2022 02:19:44 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Sat, 05 Nov 2022 02:19:44 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 02:19:44 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 00:55:46 GMT
ENV JAVA_VERSION=20-ea+23
# Fri, 11 Nov 2022 00:55:59 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/23/GPL/openjdk-20-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='0344aa24310a388514ddbc4a0279a9e28f222ae783ac918860ef8f13cfebabbe'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/23/GPL/openjdk-20-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='57ae94d8d6968fc4b6603eab15361e998664b7bb1707611dfa4ab9542c17fd24'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 11 Nov 2022 00:56:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:feec22b5b79860f47a87861bed3a29d5431a279cc239b44a2522a9ab5459d844`  
		Last Modified: Fri, 04 Nov 2022 23:34:48 GMT  
		Size: 40.6 MB (40580917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab968c9bcaf076780e21bb249a61cd5dfda4716508c17678f3082057a3c9b8f8`  
		Last Modified: Sat, 05 Nov 2022 02:23:30 GMT  
		Size: 12.2 MB (12229784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf6385da395568951fb61497c938edf2fd6a188ddde7d7db5494360a2511b5e`  
		Last Modified: Fri, 11 Nov 2022 01:00:08 GMT  
		Size: 198.2 MB (198231563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:922e5b024cc01a3c124a36228f4de6ab5be1a26d6c406352410a2f89cd27482b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.6 MB (252633592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f024986d3bba7bec85884a5b1abbfecb38667452062cd2a81416cda18c08026`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Nov 2022 23:40:44 GMT
ADD file:44569001378d2d59b2d169aba48a6b2b88529ca46fd5d85598eff7ca37ded076 in / 
# Tue, 15 Nov 2022 23:40:45 GMT
CMD ["/bin/bash"]
# Wed, 16 Nov 2022 01:36:22 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 16 Nov 2022 01:36:22 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Wed, 16 Nov 2022 01:36:22 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Nov 2022 01:36:22 GMT
ENV LANG=C.UTF-8
# Wed, 16 Nov 2022 01:36:22 GMT
ENV JAVA_VERSION=20-ea+23
# Wed, 16 Nov 2022 01:36:31 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/23/GPL/openjdk-20-ea+23_linux-x64_bin.tar.gz'; 			downloadSha256='0344aa24310a388514ddbc4a0279a9e28f222ae783ac918860ef8f13cfebabbe'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/23/GPL/openjdk-20-ea+23_linux-aarch64_bin.tar.gz'; 			downloadSha256='57ae94d8d6968fc4b6603eab15361e998664b7bb1707611dfa4ab9542c17fd24'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 16 Nov 2022 01:36:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:01d65ebb4955ae24720eb5c24ff08081fed75975aea7b87c96ef7e58175901e0`  
		Last Modified: Tue, 15 Nov 2022 23:41:32 GMT  
		Size: 42.8 MB (42774711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eefa7d15fae88e599b20bbe34f347a8686634ade1cdb17b1d84e66775c495fa`  
		Last Modified: Wed, 16 Nov 2022 01:39:40 GMT  
		Size: 13.1 MB (13066354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f551cf49dc2015795aba7a1c73e7beba682f8e7ce6e979af580ecb2007ba89`  
		Last Modified: Wed, 16 Nov 2022 01:39:50 GMT  
		Size: 196.8 MB (196792527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

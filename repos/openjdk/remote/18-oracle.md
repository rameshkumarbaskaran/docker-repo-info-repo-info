## `openjdk:18-oracle`

```console
$ docker pull openjdk@sha256:ae4a40888c172efdf26b9a61b0971bfc119ca297e1f1bba20c30810acb6b1e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:a02b15cef0e8afd57f3c8e1015ee5322b706a386ab30fb42ecec05e78dd3f752
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.6 MB (241555511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6479cba8248dfa2708c0ef1bb295b13e7d5c4ab37d2a26626d4cf29bdb3565`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 04 Nov 2022 23:33:07 GMT
ADD file:00e6899b8d3eccf7f795d17f9316af6ae0f3955ef2204b61bd064f5173c18357 in / 
# Fri, 04 Nov 2022 23:33:07 GMT
CMD ["/bin/bash"]
# Sat, 05 Nov 2022 02:19:43 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Sat, 05 Nov 2022 02:20:46 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Sat, 05 Nov 2022 02:20:46 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 02:20:46 GMT
ENV LANG=C.UTF-8
# Sat, 05 Nov 2022 02:20:47 GMT
ENV JAVA_VERSION=18.0.2.1
# Sat, 05 Nov 2022 02:20:57 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-x64_bin.tar.gz'; 			downloadSha256='3bfdb59fc38884672677cebca9a216902d87fe867563182ae8bc3373a65a2ebd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='79900237a5912045f8c9f1065b5204a474803cbbb4d075ab9620650fb75dfc1b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 05 Nov 2022 02:20:58 GMT
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
	-	`sha256:fc9c81bf0e32371a27f88a0c073e7ad8e547174b91403d9cb61f3fe3a3fe682d`  
		Last Modified: Sat, 05 Nov 2022 02:25:17 GMT  
		Size: 188.7 MB (188744810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:8b37c6a764601587e77e7332d4f0ade4a8c5f540abfd4ac9176b48fe4a8bc06a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243500421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd03868124e14c6713c002689047fc9af1c8cf51a9504826d60f57746cb8565`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Nov 2022 23:40:44 GMT
ADD file:44569001378d2d59b2d169aba48a6b2b88529ca46fd5d85598eff7ca37ded076 in / 
# Tue, 15 Nov 2022 23:40:45 GMT
CMD ["/bin/bash"]
# Wed, 16 Nov 2022 01:36:22 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 16 Nov 2022 01:36:54 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Wed, 16 Nov 2022 01:36:54 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Nov 2022 01:36:54 GMT
ENV LANG=C.UTF-8
# Wed, 16 Nov 2022 01:36:54 GMT
ENV JAVA_VERSION=18.0.2.1
# Wed, 16 Nov 2022 01:37:05 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-x64_bin.tar.gz'; 			downloadSha256='3bfdb59fc38884672677cebca9a216902d87fe867563182ae8bc3373a65a2ebd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='79900237a5912045f8c9f1065b5204a474803cbbb4d075ab9620650fb75dfc1b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 16 Nov 2022 01:37:07 GMT
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
	-	`sha256:c5859024cfe6649d958b48dc556a5fe8415addef31a9bb6031a7e27163ee2fbc`  
		Last Modified: Wed, 16 Nov 2022 01:41:00 GMT  
		Size: 187.7 MB (187659356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

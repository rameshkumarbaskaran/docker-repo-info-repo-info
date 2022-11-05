## `openjdk:20-ea-jdk-oracle`

```console
$ docker pull openjdk@sha256:4c417723758c95273b17f498c7455540f0c4107877b996d5ae5fc6a8eadb1d92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:20-ea-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:e01593d975793b087fe3025e5b89391661984985717c8e37ab66563070e65ae5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.1 MB (251075587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581a779eedd892d24f3fd5b2117cb266c4727151c8df70bcd4beb2d52aa5f715`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Oct 2022 17:21:44 GMT
ADD file:bb73a6f29d54ad7e2f7ec0aeeb404b06eee41432910aa60dd8f9ec5cdb904455 in / 
# Thu, 27 Oct 2022 17:21:44 GMT
CMD ["/bin/bash"]
# Thu, 27 Oct 2022 17:39:38 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 27 Oct 2022 17:39:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Thu, 27 Oct 2022 17:39:38 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Oct 2022 17:39:38 GMT
ENV LANG=C.UTF-8
# Thu, 27 Oct 2022 21:22:46 GMT
ENV JAVA_VERSION=20-ea+21
# Thu, 27 Oct 2022 21:22:59 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/21/GPL/openjdk-20-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='7cb7563541c5a384bcdac868744a5faeea2fa8bd68f5e0f2ee03ffa27d1f9d56'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/21/GPL/openjdk-20-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='f63aac8e75f05ed5212a7365be1007c6995c7f10d6f9308f8894634455d9a0f4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 27 Oct 2022 21:23:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d67a603b911ada80815df642621203365c074f4903f50aed87dcf6df07e6e4c6`  
		Last Modified: Thu, 27 Oct 2022 17:23:23 GMT  
		Size: 40.6 MB (40581871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d80422febbaefdcc8ba66af30635f777afc7bef13f71ad47f90af2a5da4e8099`  
		Last Modified: Thu, 27 Oct 2022 17:42:41 GMT  
		Size: 12.2 MB (12223871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeba562cbe47a6bb043f25a99e398b9349457aee72968db982d21b151ff8310a`  
		Last Modified: Thu, 27 Oct 2022 21:27:16 GMT  
		Size: 198.3 MB (198269845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6a3f5cd14a732c5126edd8281c561dd0ba89e65c81b020ec412536cc42f9dae4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.3 MB (249294363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd05d8a5608bce52cf940e6fa15739abbf77e40bb9d3dc77a651dcdc939e9945`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 04 Nov 2022 22:50:08 GMT
ADD file:efa6454225ba5be177493364c69d425968d42231b708b5d492a41f9ab14d64f4 in / 
# Fri, 04 Nov 2022 22:50:08 GMT
CMD ["/bin/bash"]
# Sat, 05 Nov 2022 00:48:43 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Sat, 05 Nov 2022 00:48:43 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Sat, 05 Nov 2022 00:48:43 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:48:43 GMT
ENV LANG=C.UTF-8
# Sat, 05 Nov 2022 00:48:44 GMT
ENV JAVA_VERSION=20-ea+21
# Sat, 05 Nov 2022 00:48:51 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/21/GPL/openjdk-20-ea+21_linux-x64_bin.tar.gz'; 			downloadSha256='7cb7563541c5a384bcdac868744a5faeea2fa8bd68f5e0f2ee03ffa27d1f9d56'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/21/GPL/openjdk-20-ea+21_linux-aarch64_bin.tar.gz'; 			downloadSha256='f63aac8e75f05ed5212a7365be1007c6995c7f10d6f9308f8894634455d9a0f4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 05 Nov 2022 00:48:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a13cd8cb50ab4c8c5cb15a9929fa5faf1b7833f87c827551a9a54e84789b1e0b`  
		Last Modified: Fri, 04 Nov 2022 22:51:35 GMT  
		Size: 39.4 MB (39401738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2b575a486b4b7df2602a19466f69783be33126ccdea7a939dbef7ecc85a7c7`  
		Last Modified: Sat, 05 Nov 2022 00:53:50 GMT  
		Size: 13.0 MB (13049666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3b46aefd64f29e78c2332b28f4315f522f7504164fa5a049f73e1e93974b52`  
		Last Modified: Sat, 05 Nov 2022 00:54:01 GMT  
		Size: 196.8 MB (196842959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

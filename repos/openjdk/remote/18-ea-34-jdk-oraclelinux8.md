## `openjdk:18-ea-34-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:2c0e804f22c5e1cd6d828fa0cace7d2d43dbf75e0f910333194f228937f0f86a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:18-ea-34-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:1173571f5f708420acde699eca4acaab99636a469be3dfedf001452fd7ac129f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 MB (244270464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a1af0bbecf33c2493337146eccce1842f075b144f96b88180c8485268c82a9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 04 Feb 2022 05:30:31 GMT
ADD file:17957b69b27e30b1d860c0919546da181b5e126b4aca4e1935ab44fd1832578e in / 
# Fri, 04 Feb 2022 05:30:31 GMT
CMD ["/bin/bash"]
# Fri, 04 Feb 2022 06:31:47 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 04 Feb 2022 06:32:18 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Fri, 04 Feb 2022 06:32:18 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Feb 2022 06:32:18 GMT
ENV LANG=C.UTF-8
# Tue, 08 Feb 2022 03:45:00 GMT
ENV JAVA_VERSION=18-ea+34
# Tue, 08 Feb 2022 03:45:13 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/34/GPL/openjdk-18-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='6811138655a3ede61c4e551db2fcc572bbf2bdfb6752777fcbf5d5b2a0affa6b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/34/GPL/openjdk-18-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='0c60dee24ba0c181adce97eb72e4517212fe0a113ae048cb4f581e7326012812'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 08 Feb 2022 03:45:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f431a76c5f59c48efd4a4076677acaae2b540a7562de00075162ef8a340fd69b`  
		Last Modified: Fri, 04 Feb 2022 05:31:30 GMT  
		Size: 42.1 MB (42102405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0509e57e85d3b85eac03c20f8f88d1cb2481d6122bdae0020851f7022e3b31`  
		Last Modified: Fri, 04 Feb 2022 08:22:45 GMT  
		Size: 13.5 MB (13513973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1973ce4fc31407286151151c2cce29334a22f1e765b57b3d34c717d7717d7bf6`  
		Last Modified: Tue, 08 Feb 2022 03:57:54 GMT  
		Size: 188.7 MB (188654086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

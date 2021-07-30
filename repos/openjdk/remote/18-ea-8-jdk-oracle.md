## `openjdk:18-ea-8-jdk-oracle`

```console
$ docker pull openjdk@sha256:c7813bdd900c35fa9318a14a2568df21fac2c32e0aeaa05173680c19ef6aba56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:18-ea-8-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:c28bb04ef41f21afe20b56089686f8338a4936c8084bb53d99d8a628b7526627
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243123711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced75813e3403433450d9a9d1ebeb67ec4eb54921ba9c30535db2809e325cf14`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Jul 2021 01:13:10 GMT
ADD file:c047ac1784a3670f52d12ad67cf238654237149dc2c9d7b921cd005c7ec42105 in / 
# Fri, 23 Jul 2021 01:13:11 GMT
CMD ["/bin/bash"]
# Fri, 23 Jul 2021 06:40:31 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 23 Jul 2021 06:40:32 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Fri, 23 Jul 2021 06:40:32 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jul 2021 06:40:32 GMT
ENV LANG=C.UTF-8
# Fri, 30 Jul 2021 18:49:01 GMT
ENV JAVA_VERSION=18-ea+8
# Fri, 30 Jul 2021 18:49:13 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/8/GPL/openjdk-18-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='7ac0e0def1cf91833e165602d7292f6003ab5e33321ccb57e71019576d739dcd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/8/GPL/openjdk-18-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='2515fe4f653afa4a891250a6001da51e57928b159c0e95a408469053fa15a4ca'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 30 Jul 2021 18:49:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1da50e1664e1b58d93182fe5af093c642668ec93f67fcd8215b9c1979930b84d`  
		Last Modified: Fri, 23 Jul 2021 01:14:27 GMT  
		Size: 42.2 MB (42178827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c8e5a84542212d0126ce88facd146befb1c731fb4faafb50a7b96ad0568cd9`  
		Last Modified: Fri, 23 Jul 2021 06:49:18 GMT  
		Size: 13.4 MB (13390485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e0847038bd8da86775d631fbe4771bfca8f72751a9a69450f919718c84e9b6`  
		Last Modified: Fri, 30 Jul 2021 18:56:13 GMT  
		Size: 187.6 MB (187554399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

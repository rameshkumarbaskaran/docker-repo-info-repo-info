## `openjdk:jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:b502d52172c1c5ac29381b8aeb0a4416da2db32710ef41e711a77274c9b70793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:df93ea2729de42fb1c3731c473bc7e7ce1d8a64bf115c496d6bb6bd916b8ed3c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.6 MB (241550557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a5dd73d786b9ceba8f406a49ea44de2a8810def91de30430459aeaa675ec18b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Oct 2022 17:21:44 GMT
ADD file:bb73a6f29d54ad7e2f7ec0aeeb404b06eee41432910aa60dd8f9ec5cdb904455 in / 
# Thu, 27 Oct 2022 17:21:44 GMT
CMD ["/bin/bash"]
# Thu, 27 Oct 2022 17:39:38 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 27 Oct 2022 17:40:08 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Thu, 27 Oct 2022 17:40:08 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Oct 2022 17:40:08 GMT
ENV LANG=C.UTF-8
# Thu, 27 Oct 2022 17:40:08 GMT
ENV JAVA_VERSION=18.0.2.1
# Thu, 27 Oct 2022 17:40:18 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-x64_bin.tar.gz'; 			downloadSha256='3bfdb59fc38884672677cebca9a216902d87fe867563182ae8bc3373a65a2ebd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='79900237a5912045f8c9f1065b5204a474803cbbb4d075ab9620650fb75dfc1b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 27 Oct 2022 17:40:19 GMT
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
	-	`sha256:459f461374cc70f7259f4e2b6307c6f9bf711dba3037540f2254ba873b2d32c6`  
		Last Modified: Thu, 27 Oct 2022 17:43:55 GMT  
		Size: 188.7 MB (188744815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6085fce176343e6748607803a74872953c522ab5e157daee4d1b782a2dfe3725
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240110745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a0ebf25a0ad31fe5828ea1b7492997670c498e0fe15d079b2ff4fd4c0610c70`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 04 Nov 2022 22:50:08 GMT
ADD file:efa6454225ba5be177493364c69d425968d42231b708b5d492a41f9ab14d64f4 in / 
# Fri, 04 Nov 2022 22:50:08 GMT
CMD ["/bin/bash"]
# Sat, 05 Nov 2022 00:48:43 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Sat, 05 Nov 2022 00:50:48 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Sat, 05 Nov 2022 00:50:48 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 00:50:48 GMT
ENV LANG=C.UTF-8
# Sat, 05 Nov 2022 00:50:48 GMT
ENV JAVA_VERSION=18.0.2.1
# Sat, 05 Nov 2022 00:50:57 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-x64_bin.tar.gz'; 			downloadSha256='3bfdb59fc38884672677cebca9a216902d87fe867563182ae8bc3373a65a2ebd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='79900237a5912045f8c9f1065b5204a474803cbbb4d075ab9620650fb75dfc1b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 05 Nov 2022 00:50:58 GMT
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
	-	`sha256:fedc660ff45bfd209b0ac28ae7621b270c6275e79147e8f130e3a6ee92f8860b`  
		Last Modified: Sat, 05 Nov 2022 00:55:29 GMT  
		Size: 187.7 MB (187659341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

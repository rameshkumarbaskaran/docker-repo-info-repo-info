## `openjdk:16-oraclelinux8`

```console
$ docker pull openjdk@sha256:71c158f549691c94837db0fb067f867dd9ca15b3b4781eb7d7fdf5e0cdee9b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:16-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:87039a6ec33bab041780fb2471acd383774674c6fa1b7f254a5dcdef65918564
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.3 MB (263322397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef66bb6a3654c59732cb4fc74c74bf7228d67e225e9d79928e9fbbce3dc25920`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Fri, 24 Jul 2020 00:21:31 GMT
ADD file:02670bc2999f43239e261c6f4e819f10471cfababa139f0eeba033a934c44eed in / 
# Fri, 24 Jul 2020 00:21:31 GMT
CMD ["/bin/bash"]
# Wed, 26 Aug 2020 21:28:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 01 Sep 2020 01:41:13 GMT
ENV LANG=C.UTF-8
# Tue, 01 Sep 2020 01:41:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Tue, 01 Sep 2020 01:41:13 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Sep 2020 01:41:13 GMT
ENV JAVA_VERSION=16-ea+13
# Tue, 01 Sep 2020 01:42:10 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/13/GPL/openjdk-16-ea+13_linux-aarch64_bin.tar.gz; 			downloadSha256=ff0e6702cc9aa6aad0d1399db28526d41e3c89d09293e3f322d3cee01b7a1d7d; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/13/GPL/openjdk-16-ea+13_linux-x64_bin.tar.gz; 			downloadSha256=c5a1067ea4822157a4476bbab01ed581d6992bd788b45505a3dd32ef4deb16b0; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 01 Sep 2020 01:42:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1bbe67b820dbc81dda19341c188f2504cb57d03d540dc94bf12e3f752102adf8`  
		Last Modified: Fri, 24 Jul 2020 00:23:22 GMT  
		Size: 53.2 MB (53238241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c479ccfad94616e2be168f7843f91429bd9a7d0996b687d670bfe633136895a`  
		Last Modified: Wed, 26 Aug 2020 21:33:04 GMT  
		Size: 13.4 MB (13417665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e9c21502f7fc706397ec47a076292b95cbb72368df14352b9b1b42a4e40794`  
		Last Modified: Tue, 01 Sep 2020 01:53:09 GMT  
		Size: 196.7 MB (196666491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:f98fee5563488d2b315a4eee00ab9d228b91cf8a919afe13e9d0da2cfab6981f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242893428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a929098107b65cadb649dfeaf1834ea41336acfe9d9ccbb29fad6c9fe3c64bc1`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 May 2019 21:40:52 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Fri, 24 Jul 2020 00:53:42 GMT
ADD file:2ad87b72223c423a2c0741208d69b5b361aabaa96bfbe1510fa44745a72c0e7f in / 
# Fri, 24 Jul 2020 00:53:46 GMT
CMD ["/bin/bash"]
# Wed, 26 Aug 2020 21:35:59 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 26 Aug 2020 21:36:01 GMT
ENV LANG=en_US.UTF-8
# Wed, 26 Aug 2020 21:36:03 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Wed, 26 Aug 2020 21:36:04 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Aug 2020 22:40:00 GMT
ENV JAVA_VERSION=16-ea+13
# Thu, 27 Aug 2020 22:40:59 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/13/GPL/openjdk-16-ea+13_linux-aarch64_bin.tar.gz; 			downloadSha256=ff0e6702cc9aa6aad0d1399db28526d41e3c89d09293e3f322d3cee01b7a1d7d; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/13/GPL/openjdk-16-ea+13_linux-x64_bin.tar.gz; 			downloadSha256=c5a1067ea4822157a4476bbab01ed581d6992bd788b45505a3dd32ef4deb16b0; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		javac --version; 	java --version
# Thu, 27 Aug 2020 22:41:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e618d2a55163b9d055a0c627bc7faff5f4210ee92e01ce1b82dd0738d8c5e12`  
		Last Modified: Fri, 24 Jul 2020 00:55:39 GMT  
		Size: 53.3 MB (53345174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed03d65a39d352a49fbfba9a4223490a35071d814a500f1e7a378ce915dd32f6`  
		Last Modified: Wed, 26 Aug 2020 21:40:32 GMT  
		Size: 14.3 MB (14331702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec44484f17e6e43a453c5bbf57ddd242457bd22262f1b913b466fc7710532eb`  
		Last Modified: Thu, 27 Aug 2020 22:44:48 GMT  
		Size: 175.2 MB (175216552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

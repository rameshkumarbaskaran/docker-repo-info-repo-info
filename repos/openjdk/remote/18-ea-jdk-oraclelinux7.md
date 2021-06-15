## `openjdk:18-ea-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:b9f246052862445874bb8028ad3bf41ec6b27389c79a306d6c0becd69a54eaf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-ea-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:33753ece3ec740e24958ddb2e8d17c31d025b4b2b1a1bcbfc0eb5ecd317a06db
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.7 MB (251655683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9533644e943bde85fa8165203fcf15ad05246155df778ddee91fe1c4a841a7f5`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 01 Jun 2021 15:21:43 GMT
ADD file:6853efe982f87a3475099ab9aaa2ec9797afac58ee8dfc54d912b966bc3405ea in / 
# Tue, 01 Jun 2021 15:21:44 GMT
CMD ["/bin/bash"]
# Tue, 01 Jun 2021 15:38:40 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Mon, 14 Jun 2021 21:21:57 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Mon, 14 Jun 2021 21:21:58 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jun 2021 21:21:58 GMT
ENV LANG=en_US.UTF-8
# Mon, 14 Jun 2021 21:21:58 GMT
ENV JAVA_VERSION=18-ea+1
# Mon, 14 Jun 2021 21:22:08 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/1/GPL/openjdk-18-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='277c0021c542fbda35d2643351148fa6cceac66b5beca24016c75fafeed815de'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/1/GPL/openjdk-18-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='6b615e986bc649e30072f1a7e88986e7a55cad95756c982a2f02f278ec8fe05c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 14 Jun 2021 21:22:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cbf629395cd4d267c366a2b3ac4cfbe6a6c5cfd5bdd8e89a7157e0901e898cf4`  
		Last Modified: Tue, 01 Jun 2021 15:22:47 GMT  
		Size: 48.3 MB (48260748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf25dc842172d49c0f45cec26c8fe86f7a083e2e5ce7a5e6d84d2b4cd2d46ba`  
		Last Modified: Tue, 01 Jun 2021 15:43:59 GMT  
		Size: 15.4 MB (15425936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b689a134986f065733ae27add97d0b6880737cca08329bae815658dfb71e713`  
		Last Modified: Mon, 14 Jun 2021 21:29:23 GMT  
		Size: 188.0 MB (187968999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-ea-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b1be31a60f61a04de073d42b901c798e78659745f8890a5d872e7b053544086b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252058783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e0e3f60f8ce066cdcd8f60c8c1775ba7e668752f1208253af835c97c4765c5`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 01 Jun 2021 14:41:12 GMT
ADD file:3f30763d6f4fa6cd26708a9eda4872cc48b0c874b7837e0682ea4b4ed7ac5fb2 in / 
# Tue, 01 Jun 2021 14:41:12 GMT
CMD ["/bin/bash"]
# Tue, 01 Jun 2021 14:58:49 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Mon, 14 Jun 2021 20:42:55 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Mon, 14 Jun 2021 20:42:55 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Jun 2021 20:42:56 GMT
ENV LANG=en_US.UTF-8
# Mon, 14 Jun 2021 20:42:56 GMT
ENV JAVA_VERSION=18-ea+1
# Mon, 14 Jun 2021 20:43:18 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/1/GPL/openjdk-18-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='277c0021c542fbda35d2643351148fa6cceac66b5beca24016c75fafeed815de'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/1/GPL/openjdk-18-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='6b615e986bc649e30072f1a7e88986e7a55cad95756c982a2f02f278ec8fe05c'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 14 Jun 2021 20:43:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5216e6356b12c39a03d420e358911905653d063185ac40b7250d625cfcd46024`  
		Last Modified: Tue, 01 Jun 2021 14:42:13 GMT  
		Size: 48.9 MB (48857508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0104ba284443f9b2819e0f98ad5efb21b57c2cf4d49bd3d3cbd1af4ad0ac2c85`  
		Last Modified: Tue, 01 Jun 2021 15:09:33 GMT  
		Size: 16.4 MB (16419323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a219136527479eb4e5e18bf8f852010616512e1ce22fb75e9b320938b2b70b`  
		Last Modified: Mon, 14 Jun 2021 20:56:56 GMT  
		Size: 186.8 MB (186781952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

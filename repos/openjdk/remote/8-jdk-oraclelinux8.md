## `openjdk:8-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:0dbcf8b68e25e94d1a833eb7dc6a578b6e6d4e28101193aa26f1285c2ad6da82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:8-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:a1cb6d6b20a7d5dc67efe45432b16cdde94110ea1c1ae371b54a59bafa703b7b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161504505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14654dc7367cae4f18f1b0e9163cce1554edb0d614db392503c23118be93c52`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 18 Nov 2021 16:05:57 GMT
ADD file:977d9a2c7a8ab07ec719edd585faf23ef08768a09abf97a80d62d2091936b052 in / 
# Thu, 18 Nov 2021 16:05:58 GMT
CMD ["/bin/bash"]
# Thu, 18 Nov 2021 17:33:38 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 18 Nov 2021 17:37:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Thu, 18 Nov 2021 17:37:09 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 17:37:09 GMT
ENV LANG=C.UTF-8
# Thu, 18 Nov 2021 17:37:10 GMT
ENV JAVA_VERSION=8u312
# Thu, 18 Nov 2021 17:37:26 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:0a39cfde620ea7949c12d65ef5a24d4b6f737bb5a2f57d9a4a16013c060c9c67`  
		Last Modified: Thu, 18 Nov 2021 16:07:11 GMT  
		Size: 42.1 MB (42098006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a90c9cadc5331c54e5f53b906e967fe1942c54666e8da9bf055c378d02b2ad`  
		Last Modified: Thu, 18 Nov 2021 17:43:13 GMT  
		Size: 13.5 MB (13511675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb4298d9047469c0552b4b97b96e2da397e2e6177251eff679379978f1f0188`  
		Last Modified: Thu, 18 Nov 2021 17:47:33 GMT  
		Size: 105.9 MB (105894824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:8-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:d66d8c5800bbe00c463f0afc6c27f3cab9e3f1ddf3fcbebd702e98bec11f985b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161216495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a626d56a754c16d29e1bab83b6e80296c360dae2dbab461fa4e96109881feab9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 18 Nov 2021 08:24:53 GMT
ADD file:98b355b05026edaab234cff8ee34d8335b233cbaa04a19ac82df4a2b0c7fdc4d in / 
# Thu, 18 Nov 2021 08:24:54 GMT
CMD ["/bin/bash"]
# Thu, 18 Nov 2021 10:14:56 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Thu, 18 Nov 2021 10:18:52 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Thu, 18 Nov 2021 10:18:52 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Nov 2021 10:18:53 GMT
ENV LANG=C.UTF-8
# Thu, 18 Nov 2021 10:18:54 GMT
ENV JAVA_VERSION=8u312
# Thu, 18 Nov 2021 10:19:16 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_x64_linux_8u312b07.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jdk_aarch64_linux_8u312b07.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:1bdb3a9e404c972ab03f65fd56b5b815b51d6a68324015dc69707d48e2ba3cdf`  
		Last Modified: Thu, 18 Nov 2021 08:26:02 GMT  
		Size: 42.0 MB (42010198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9356b5c0bb88b90b52af9c2836e152e11b910a0e88807e8327df1e2a965a7d1`  
		Last Modified: Thu, 18 Nov 2021 10:27:05 GMT  
		Size: 14.3 MB (14300065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79d2474338507e46b3c5e77f47718e040c6c5a35b7833c434752800382aff6e`  
		Last Modified: Thu, 18 Nov 2021 10:31:52 GMT  
		Size: 104.9 MB (104906232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

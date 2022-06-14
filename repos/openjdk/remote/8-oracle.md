## `openjdk:8-oracle`

```console
$ docker pull openjdk@sha256:fc553dde6045754c07dfe16837c543d65c9255b8cd2942f7145bd38068954f92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:8-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:0327f77b8cc890a27d82f8f110e2c56c4f8cb621c5fb3e7073b1dc39545c6549
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158557332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8ed8400377616ec80fd4d96b559d3ff0beba96489e9706a34dc0eac27fd3bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 14 Jun 2022 18:23:26 GMT
ADD file:837f6c6e7e20067b92edb72e78a8399e6cbbd72dab23db7b5b5a301c58d2a0de in / 
# Tue, 14 Jun 2022 18:23:26 GMT
CMD ["/bin/bash"]
# Tue, 14 Jun 2022 18:42:55 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 14 Jun 2022 18:45:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Tue, 14 Jun 2022 18:45:12 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jun 2022 18:45:12 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jun 2022 18:45:12 GMT
ENV JAVA_VERSION=8u332
# Tue, 14 Jun 2022 18:45:23 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:5f160c0f6cac587a73883b48a8857f5cce0930112792cef25c62510e256e93dc`  
		Last Modified: Tue, 14 Jun 2022 18:24:18 GMT  
		Size: 39.2 MB (39219730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb499df0377a2bd9163e9a611ce46b5379196826787392defef98dbf215a8aa4`  
		Last Modified: Tue, 14 Jun 2022 18:49:29 GMT  
		Size: 13.5 MB (13502563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a0471cd3b610d658c1e088dc1927b36b0ef17778ad533157ea4fa3ea706a44`  
		Last Modified: Tue, 14 Jun 2022 18:53:30 GMT  
		Size: 105.8 MB (105835039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:8-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3e6d3193a8329344d347bf9669e012aff37d0c76b1e5fcc393bfa780b9525c6e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157083643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419f8eda85e00f4ccc6ecf99a01c3f6325359e79170184755e50e9238d578659`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 14 Jun 2022 18:41:36 GMT
ADD file:4a6ee90ad73353bfb87b2f121e06bddaed6104536e485baa83fadbe7facc774c in / 
# Tue, 14 Jun 2022 18:41:37 GMT
CMD ["/bin/bash"]
# Tue, 14 Jun 2022 18:58:47 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 14 Jun 2022 19:02:41 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Tue, 14 Jun 2022 19:02:42 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Jun 2022 19:02:43 GMT
ENV LANG=C.UTF-8
# Tue, 14 Jun 2022 19:02:44 GMT
ENV JAVA_VERSION=8u332
# Tue, 14 Jun 2022 19:02:56 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_x64_linux_8u332b09.tar.gz'; 			;; 		'aarch64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jdk_aarch64_linux_8u332b09.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver keyserver.ubuntu.com --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:2bbc1bf883bd601c0da5735b538963308bcc17f90d36525ecc93456ffad79064`  
		Last Modified: Tue, 14 Jun 2022 18:42:39 GMT  
		Size: 38.0 MB (38012371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bde7855ef536fce06527372a019087e1972db9d092b2ec88091b6017cfc5a16`  
		Last Modified: Tue, 14 Jun 2022 19:10:59 GMT  
		Size: 14.3 MB (14260872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef1598cbffdad493dfd7ac7258dca735dcc59e6ed6044eea9d61c75d08e3651`  
		Last Modified: Tue, 14 Jun 2022 19:16:00 GMT  
		Size: 104.8 MB (104810400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

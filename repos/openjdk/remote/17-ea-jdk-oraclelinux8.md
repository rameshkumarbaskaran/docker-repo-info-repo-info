## `openjdk:17-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:6e50bada442747e55268f5e3733a29101c71461a6b901bd5cb1ac5d6267ab206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:17-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:abd47cbaca1d521ee8f4f23b627a26a7a79b4e0abdbea9435f5b03d3c44339b6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.7 MB (242735133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c182cb374f7e90c73ca982c8607c882b5d3af2d9d8ef3f377d6b5edea057c80f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 02 Jun 2021 17:21:00 GMT
ADD file:b4c18f27ab03ed63f96174673a8d97d4b1b6abb552b6fe3201c6aec934e8312f in / 
# Wed, 02 Jun 2021 17:21:00 GMT
CMD ["/bin/bash"]
# Wed, 02 Jun 2021 17:37:54 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 02 Jun 2021 17:37:55 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Wed, 02 Jun 2021 17:37:55 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Jun 2021 17:37:55 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 21:22:49 GMT
ENV JAVA_VERSION=17-ea+26
# Mon, 14 Jun 2021 21:22:59 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/26/GPL/openjdk-17-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='9efe9a6b68a24e16a2a2e34b0f33c25fe17dcdace07970840e2a9bd014d13c30'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/26/GPL/openjdk-17-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='5914ae141494689362b74b2edc546f94f3ac4a4c8d6863a20048e851a0f6213f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 14 Jun 2021 21:23:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5a581c13a8b96af42c06955acd88fdb3aff53edcbdd33faa7bca9854fd8bfbaf`  
		Last Modified: Wed, 02 Jun 2021 17:22:10 GMT  
		Size: 42.2 MB (42183647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cd02acd9c2b40dba18c3fe68882bcb5ebda0caeb5e550965d9ac81e3b55fbf`  
		Last Modified: Wed, 02 Jun 2021 17:43:15 GMT  
		Size: 13.4 MB (13400021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d558b04b7f9486d18df402f2dd765fd3dcbafa1e977313e3b3d05705a3647cc0`  
		Last Modified: Mon, 14 Jun 2021 21:31:21 GMT  
		Size: 187.2 MB (187151465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:dac07b29d45debc25116951ad7119f3e155dfc5e762546ab5cd4d046eef04054
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.2 MB (242220318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14437c7fe359f65c000d67891637a54933c33e27dd31676e2b3ad6b9cfe9810d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 02 Jun 2021 17:41:03 GMT
ADD file:78235baf524ed2a030d5aee5012599777d5026bf83699d8d03662420d6804653 in / 
# Wed, 02 Jun 2021 17:41:03 GMT
CMD ["/bin/bash"]
# Wed, 02 Jun 2021 17:58:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 02 Jun 2021 17:58:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Wed, 02 Jun 2021 17:58:07 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Jun 2021 17:58:07 GMT
ENV LANG=C.UTF-8
# Mon, 14 Jun 2021 20:44:08 GMT
ENV JAVA_VERSION=17-ea+26
# Mon, 14 Jun 2021 20:44:18 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/26/GPL/openjdk-17-ea+26_linux-x64_bin.tar.gz'; 			downloadSha256='9efe9a6b68a24e16a2a2e34b0f33c25fe17dcdace07970840e2a9bd014d13c30'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/26/GPL/openjdk-17-ea+26_linux-aarch64_bin.tar.gz'; 			downloadSha256='5914ae141494689362b74b2edc546f94f3ac4a4c8d6863a20048e851a0f6213f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 14 Jun 2021 20:44:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4a780b35fbf92abdbd808aa7d8f30cb6c03db446424f04738aa715ba4935a1f6`  
		Last Modified: Wed, 02 Jun 2021 17:42:09 GMT  
		Size: 42.1 MB (42068993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b11c9e8386348cc9050d7280e19b5987140671e2de847d978f53d4ec578f94`  
		Last Modified: Wed, 02 Jun 2021 18:08:16 GMT  
		Size: 14.2 MB (14183644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62ef88dfdd71498460ea46ba8e4705b31f1fc3d5e5fd8360139e33353ce5e0b`  
		Last Modified: Mon, 14 Jun 2021 20:59:24 GMT  
		Size: 186.0 MB (185967681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

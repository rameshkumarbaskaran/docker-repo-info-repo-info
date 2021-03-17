## `openjdk:8-oraclelinux7`

```console
$ docker pull openjdk@sha256:13a807df42790782fccebe48d5dacc0bb2db496188e8155c3852f4440e8bfafc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:8-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:3f0d23418884d9c52d4ad0b56defb3f6c17f7106771c5b4bd79b7bae5313f4f1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169496916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009b679f386125e5a41af3f63c1db6b3be3cd929ee80a663274eb573e01387d0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Mar 2021 00:21:32 GMT
ADD file:837f2bca2cab135736ad43644356710dcac6516fdfc2023d239d157d1fa4ba7c in / 
# Wed, 17 Mar 2021 00:21:32 GMT
CMD ["/bin/bash"]
# Wed, 17 Mar 2021 00:38:33 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 17 Mar 2021 00:41:39 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Wed, 17 Mar 2021 00:41:39 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Mar 2021 00:41:39 GMT
ENV LANG=en_US.UTF-8
# Wed, 17 Mar 2021 00:41:40 GMT
ENV JAVA_VERSION=8u282
# Wed, 17 Mar 2021 00:41:47 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u282-b08/OpenJDK8U-jdk_x64_linux_8u282b08.tar.gz'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/jre/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/jre/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:401a42e1eb4fe87d89990847d6ef97767b5ac57457c8001203ee2ea137736907`  
		Last Modified: Wed, 17 Mar 2021 00:22:34 GMT  
		Size: 48.3 MB (48263709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f752366003eed4ac964ebb4be3453e3f19d854828f4f50ff708900bb4c42924`  
		Last Modified: Wed, 17 Mar 2021 00:45:21 GMT  
		Size: 15.4 MB (15429957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd2cccf09c34f0dc18dc564fd965321a78a4d56490116ad01d71300c2168ffac`  
		Last Modified: Wed, 17 Mar 2021 00:48:48 GMT  
		Size: 105.8 MB (105803250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

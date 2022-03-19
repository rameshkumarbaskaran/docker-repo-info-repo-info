## `openjdk:18-jdk-oracle`

```console
$ docker pull openjdk@sha256:c3094ef06b55575e93e3d9b74360063bde28cf3243b2a7d8930f6701f47ffdfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:d94510c59a23c5ad44450d1ce1ad571e5bbfcbd1166fbcc7ffef24807d974ece
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 MB (244299578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5084fef61d82edffddc4abd4e0846d283b6c7b7b0de418fd92f2c5995f660b1c`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 18 Mar 2022 05:23:28 GMT
ADD file:09b0bc8af49fa3558fb3e8d50daa682180e194cb11ca332d03ca65059e615dfd in / 
# Fri, 18 Mar 2022 05:23:29 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 10:17:40 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Sat, 19 Mar 2022 10:21:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Sat, 19 Mar 2022 10:21:13 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:21:13 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:21:13 GMT
ENV JAVA_VERSION=18
# Sat, 19 Mar 2022 10:21:28 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-x64_bin.tar.gz'; 			downloadSha256='0f60aef7b8504983d6e374fe94d09a7bedcf05ec559e812d801a33bd4ebd23d0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-aarch64_bin.tar.gz'; 			downloadSha256='dff2860ba24c3f70f32ad3ac9b03f768dd28044bbda87c9607654fd03795c2ab'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 19 Mar 2022 10:21:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1824cb7e97fbcfc5c6ffea667f8e19cee765d015fef1b8ad70f96252d9713c95`  
		Last Modified: Fri, 18 Mar 2022 05:24:44 GMT  
		Size: 42.1 MB (42110196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db19695be7be96a8d27e754c74310c6fafa295ecdccbc10e8c5fe5b23854c2a`  
		Last Modified: Sat, 19 Mar 2022 10:34:49 GMT  
		Size: 13.5 MB (13519824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d1541fb062fbd1d6133ea069a7c1bb89a5d78164aebfe16f1cd141e9e5d8f3`  
		Last Modified: Sat, 19 Mar 2022 10:37:54 GMT  
		Size: 188.7 MB (188669558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4233de07ef80d1253426fb985658e8960ee8097cbaca7fe79ed9cffa37f858cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243902283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9027ab45bf2123cc35278b8690589f61f2568eaebd4a88806595f4475fb691`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 18 Mar 2022 00:35:35 GMT
ADD file:b16af05882bd38ac02b1f1cba2cc7e80bfbe467ce57f3cf35f1f5a551cee90fa in / 
# Fri, 18 Mar 2022 00:35:36 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 07:22:07 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Sat, 19 Mar 2022 07:24:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Sat, 19 Mar 2022 07:24:11 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 07:24:12 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 07:24:13 GMT
ENV JAVA_VERSION=18
# Sat, 19 Mar 2022 07:24:24 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-x64_bin.tar.gz'; 			downloadSha256='0f60aef7b8504983d6e374fe94d09a7bedcf05ec559e812d801a33bd4ebd23d0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18/43f95e8614114aeaa8e8a5fcf20a682d/36/GPL/openjdk-18_linux-aarch64_bin.tar.gz'; 			downloadSha256='dff2860ba24c3f70f32ad3ac9b03f768dd28044bbda87c9607654fd03795c2ab'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 19 Mar 2022 07:24:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2f8e506fd7c6683f24250871efec36e3fe21cc71090a2f5c59dccdcdfeed2311`  
		Last Modified: Fri, 18 Mar 2022 00:36:38 GMT  
		Size: 42.0 MB (42017883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5fff79dab44aae745004a90eddcd68a9db24e820f0c68e482a9508464ea719`  
		Last Modified: Sat, 19 Mar 2022 07:43:39 GMT  
		Size: 14.3 MB (14291778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a85c2ee6efbcfb29723075f0fed7e090477cef2695493873eb12862df653986b`  
		Last Modified: Sat, 19 Mar 2022 07:45:55 GMT  
		Size: 187.6 MB (187592622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

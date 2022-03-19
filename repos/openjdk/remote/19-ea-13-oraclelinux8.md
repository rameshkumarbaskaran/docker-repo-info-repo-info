## `openjdk:19-ea-13-oraclelinux8`

```console
$ docker pull openjdk@sha256:12524cb5836da9ba0fd3c66b63acdf2d861b5527cb43e519921851084f979838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-ea-13-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:29aa203c6f3722116a060464504eff150ca7bbba16b10e66bc13981d4d8be442
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.7 MB (248707294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05970c139e838f0c75bcc5aeb62d9955e89ba5816819580334ae90c67bb451b5`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 18 Mar 2022 05:23:28 GMT
ADD file:09b0bc8af49fa3558fb3e8d50daa682180e194cb11ca332d03ca65059e615dfd in / 
# Fri, 18 Mar 2022 05:23:29 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 10:17:40 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Sat, 19 Mar 2022 10:17:40 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Sat, 19 Mar 2022 10:17:41 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:17:41 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 10:17:41 GMT
ENV JAVA_VERSION=19-ea+13
# Sat, 19 Mar 2022 10:17:51 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='6aff2a07ccdd649641741facf16a0001568e7af829e0e8cbd1257db42b6911f4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2b13aabf01d1fad49c3dd5cde37bb53683a97b33d3d58030c10e1fad270f8c76'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 19 Mar 2022 10:17:52 GMT
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
	-	`sha256:98ccef5c33597d952b36e3ff75ec3bd81f7034bfb9035363d35e85deedc13331`  
		Last Modified: Sat, 19 Mar 2022 10:35:04 GMT  
		Size: 193.1 MB (193077274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-13-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:de0528007e940be8b6ad0d73d557a091818809c8ad5a4d8fd8befdf4d4990d20
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248424182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90977be360ccf552f99d00a278629b6dd9b1de91238988b8f64037aa57b34a2`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 18 Mar 2022 00:35:35 GMT
ADD file:b16af05882bd38ac02b1f1cba2cc7e80bfbe467ce57f3cf35f1f5a551cee90fa in / 
# Fri, 18 Mar 2022 00:35:36 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 07:22:07 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Sat, 19 Mar 2022 07:22:07 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Sat, 19 Mar 2022 07:22:08 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 07:22:09 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 07:22:10 GMT
ENV JAVA_VERSION=19-ea+13
# Sat, 19 Mar 2022 07:22:29 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='6aff2a07ccdd649641741facf16a0001568e7af829e0e8cbd1257db42b6911f4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/13/GPL/openjdk-19-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2b13aabf01d1fad49c3dd5cde37bb53683a97b33d3d58030c10e1fad270f8c76'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Sat, 19 Mar 2022 07:22:29 GMT
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
	-	`sha256:a48fca478378850523f239c45d9cb6dc44c1a54da3701d60f8a10d08dfe12c1d`  
		Last Modified: Sat, 19 Mar 2022 07:43:59 GMT  
		Size: 192.1 MB (192114521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

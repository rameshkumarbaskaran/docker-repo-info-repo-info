## `openjdk:20-ea-6-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:5b9282e02b4167347f6cb1f2a8b7b4fc8d6905cbe1651159ab0d3309ba1cf69f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `openjdk:20-ea-6-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e28101d82a3ca08a0be853abb64a810a1830974e1c657ce66061aeed4bc0a726
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.5 MB (260476003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d2064b05e457f434a52439ae5b40bb15e72aa29609b1a84d69cf76d7f30f8a9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 Jul 2022 22:43:37 GMT
ADD file:6d5eeb6c0921661dff8e0b6a89c3272aa52f72b5926d62ae482a85c8ef6458a3 in / 
# Tue, 05 Jul 2022 22:43:38 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 23:05:04 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 05 Jul 2022 23:05:04 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Tue, 05 Jul 2022 23:05:05 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Jul 2022 23:05:06 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Jul 2022 19:20:45 GMT
ENV JAVA_VERSION=20-ea+6
# Mon, 18 Jul 2022 19:21:03 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/6/GPL/openjdk-20-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='5ed42664253f08626aa2346712cecb58a65a08ce3d92d9e00eb39e5964dcbbba'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/6/GPL/openjdk-20-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='ad766479ae40cc35e0544ee550825fa8aa41109eae338e297d0e3c6aac0fd3b4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 18 Jul 2022 19:21:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:456ca0cbf3e695c518e5d5c4cb5ff9f99bb999a28b5ec7da3b4ca48d3cf80e6b`  
		Last Modified: Tue, 05 Jul 2022 22:45:10 GMT  
		Size: 49.3 MB (49342729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7981fd8b8b8e53f7977497096fa392e1d14f1e3dd10684ac47d3fa4688b887e7`  
		Last Modified: Tue, 05 Jul 2022 23:21:54 GMT  
		Size: 15.3 MB (15264543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83552ac19223984da64b2780f167c9d94897439496152aaf39ccc6be6940b12`  
		Last Modified: Mon, 18 Jul 2022 19:37:49 GMT  
		Size: 195.9 MB (195868731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `openjdk:22-ea-oraclelinux7`

```console
$ docker pull openjdk@sha256:d4cc464956a72a3c719ecb63f8c9fa48df12368337348032f2d548cf8acf809b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `openjdk:22-ea-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:46a2eb8e9a34a36333fea7cd7ca27d3b6a8d6b2be4beccb84759519d7cb397f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269347189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3813d9622eb114c45f8891da92f51b0064165504ca95e63077099cd6a664994d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 Mar 2023 21:40:35 GMT
ADD file:4fe62bcdc8f181de8e01e791570bbb89f29712a9aef0b329febd817f4fef8887 in / 
# Fri, 31 Mar 2023 21:40:36 GMT
CMD ["/bin/bash"]
# Fri, 31 Mar 2023 22:08:06 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Mon, 12 Jun 2023 21:46:01 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Mon, 12 Jun 2023 21:46:01 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jun 2023 21:46:01 GMT
ENV LANG=en_US.UTF-8
# Mon, 12 Jun 2023 21:46:01 GMT
ENV JAVA_VERSION=22-ea+1
# Mon, 12 Jun 2023 21:46:15 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_linux-x64_bin.tar.gz'; 			downloadSha256='50bf6303955ea128be3eb7ad9bc10f5e7eeacf9d3f81349a4d60a164fe7d0318'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/1/GPL/openjdk-22-ea+1_linux-aarch64_bin.tar.gz'; 			downloadSha256='6ca14677cb2db094acbc9b084d0a85c9e004aff9826977e0b9b35e5f9a55b550'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 12 Jun 2023 21:46:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a138fe98397d054834e86c902a0b929bd7cf0261ac671e779f872176569996ab`  
		Last Modified: Fri, 31 Mar 2023 21:42:01 GMT  
		Size: 51.1 MB (51054832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61213d9405aef8db0237e9542508819c698c4d8293ccbd8799a36206032fdd7c`  
		Last Modified: Fri, 31 Mar 2023 22:09:32 GMT  
		Size: 15.2 MB (15237973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ad2954d00d1982187ad3da557a36ebf3d145ad1c89397d883fac50e7ffcc36`  
		Last Modified: Mon, 12 Jun 2023 21:49:40 GMT  
		Size: 203.1 MB (203054384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

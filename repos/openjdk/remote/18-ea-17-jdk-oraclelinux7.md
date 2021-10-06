## `openjdk:18-ea-17-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:da0c1fea83eee870bc4a46b38427e5d78ff4e3e4b7513b09e0ca717b5baffcc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `openjdk:18-ea-17-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:59e8fcdd067d0a49a975ccd982c40faa70d3863097679688832a427fa9595322
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252058004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18781a8b988dfe5ec428699a26892df07a34b72bdddf56b52011dfc743229a98`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 29 Sep 2021 09:28:50 GMT
ADD file:affde62a0aaf80f490cc93e1f691166a15a32c6ef6bc21af35a6659d24c8b6ef in / 
# Wed, 29 Sep 2021 09:28:51 GMT
CMD ["/bin/bash"]
# Wed, 29 Sep 2021 10:14:29 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 29 Sep 2021 10:14:29 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Wed, 29 Sep 2021 10:14:30 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Sep 2021 10:14:30 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Oct 2021 18:07:20 GMT
ENV JAVA_VERSION=18-ea+17
# Wed, 06 Oct 2021 18:07:36 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/17/GPL/openjdk-18-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='3a79fd0700f8e27538bb6cdbef4f630be0efc78686b6f4c3003dcea1177a237a'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk18/17/GPL/openjdk-18-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='9ff48be04860c0632addb495dcba1d4fe519d306edd4165b17848a8d340d0340'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 06 Oct 2021 18:07:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2f5eee715870559160403451bcd7b891478e0df052b7f9456144f3e89e5b994f`  
		Last Modified: Wed, 29 Sep 2021 09:30:28 GMT  
		Size: 48.8 MB (48828923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:101207ebea4e1f8fc9adeec0fe8c82c5b0639e2e9c6f0f0bf26e459dc1665d66`  
		Last Modified: Wed, 29 Sep 2021 10:30:47 GMT  
		Size: 16.4 MB (16438786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1213de509c008de583617d04276757be77bd9e29db49f3372732474670c81d`  
		Last Modified: Wed, 06 Oct 2021 18:22:02 GMT  
		Size: 186.8 MB (186790295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

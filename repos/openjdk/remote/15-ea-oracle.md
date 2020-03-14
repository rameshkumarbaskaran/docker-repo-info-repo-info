## `openjdk:15-ea-oracle`

```console
$ docker pull openjdk@sha256:913b5b4335e7b6adcef60625fbe0d5808f3acc9ae603c3ae68b1870cd2af2357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:15-ea-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:e9a47fccf8d832f1f0960f1f2cfafa1cce05483d58c962cf5dcddd3aede8c53c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.9 MB (255914135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a53f08e35741829c8508e3718da057b2a14c987328d0b5810c9f227231a295`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Tue, 10 Mar 2020 02:20:39 GMT
ADD file:ca821d696bf87ff0b7ed9d85b5b0acc4656fc6498d2f5bd2c051bb16a99bfcbf in / 
# Tue, 10 Mar 2020 02:20:40 GMT
CMD ["/bin/bash"]
# Tue, 10 Mar 2020 02:37:57 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 10 Mar 2020 02:37:57 GMT
ENV LANG=en_US.UTF-8
# Tue, 10 Mar 2020 02:37:57 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Tue, 10 Mar 2020 02:37:58 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Mar 2020 23:01:23 GMT
ENV JAVA_VERSION=15-ea+14
# Fri, 13 Mar 2020 23:01:23 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/14/GPL/openjdk-15-ea+14_linux-x64_bin.tar.gz
# Fri, 13 Mar 2020 23:01:23 GMT
ENV JAVA_SHA256=cb73cbc3b60fb67351fd6f01924f8c6861a3951bb6e4fbae8e42dabb55ee8b75
# Fri, 13 Mar 2020 23:02:10 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Fri, 13 Mar 2020 23:02:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd17e56c322c9601c98f41573bb47bd4cd68ff386d7d07538f156a7c0ef6c650`  
		Last Modified: Tue, 10 Mar 2020 02:22:01 GMT  
		Size: 42.7 MB (42725735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdd73bb99224b1c73d7d3d8eea56a91f5e7fc73628dcfa3b5432cca23c7373d`  
		Last Modified: Tue, 10 Mar 2020 02:42:14 GMT  
		Size: 14.8 MB (14770095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4709ec81738584749c54d11b8509008456e3cb0331490e3ff06a6e23454deba6`  
		Last Modified: Fri, 13 Mar 2020 23:04:48 GMT  
		Size: 198.4 MB (198418305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

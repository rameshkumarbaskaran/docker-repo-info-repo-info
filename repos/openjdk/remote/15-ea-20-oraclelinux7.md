## `openjdk:15-ea-20-oraclelinux7`

```console
$ docker pull openjdk@sha256:4da9b5d5e701f4bc1ae812cc9421924ee67c73c71d2e54f130aae8425fadb5e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:15-ea-20-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:e20b176c46290dc7113423649f2d2d10452ce5573da755b218f7baeedbc29e18
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250517623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42745be0ddb783c9d0f570afbc128d97fa7fef083343485fc63a2a807b4a1576`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Fri, 10 Apr 2020 20:26:28 GMT
ADD file:53599f8bbed1dcb68d6fd6418597c9692c328f49a3a3864871c5237c64e00375 in / 
# Fri, 10 Apr 2020 20:26:28 GMT
CMD ["/bin/bash"]
# Fri, 10 Apr 2020 20:43:19 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 10 Apr 2020 20:43:19 GMT
ENV LANG=en_US.UTF-8
# Fri, 10 Apr 2020 20:43:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Fri, 10 Apr 2020 20:43:19 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Apr 2020 06:52:13 GMT
ENV JAVA_VERSION=15-ea+20
# Sat, 25 Apr 2020 06:52:13 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/20/GPL/openjdk-15-ea+20_linux-x64_bin.tar.gz
# Sat, 25 Apr 2020 06:52:13 GMT
ENV JAVA_SHA256=38059e0eea619775a3dd0843f386d24cf6d0289b4b511bb98acde78e9a6aac29
# Sat, 25 Apr 2020 06:52:57 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Sat, 25 Apr 2020 06:52:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:79ccf0f4e30fb9e8aa16b93e5123f4ebd2ebe8e0f8d21cc01956016f867ab3bf`  
		Last Modified: Fri, 10 Apr 2020 20:27:25 GMT  
		Size: 43.5 MB (43457734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ceb08e4244f41a1398e621d60c54d89e7f76991ffec77188bc98bb07e60001`  
		Last Modified: Fri, 10 Apr 2020 20:45:52 GMT  
		Size: 14.8 MB (14762210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07197851d8fd58fdcbba730b5ab08cc20a5b969065a869e599af1767a4b8ca`  
		Last Modified: Sat, 25 Apr 2020 06:55:30 GMT  
		Size: 192.3 MB (192297679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `openjdk:15-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:691ed84068e77af75ac5aa93b2b129e8b51af3eab1049c18e54d5a1e47b7c104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:15-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:390ac12e6f737bc3627a6e98c0d45411e4b442691e151a6321c7e8528ac08991
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.9 MB (255935926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37825e968c76b79581e4b3146108246bf017368b8addc641fe718e7ac5c3da8a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Tue, 28 Jan 2020 21:36:05 GMT
ADD file:a320cfe017a986947ac6b09db573e476eacafc80311e517efcc5e965fcc445fb in / 
# Tue, 28 Jan 2020 21:36:06 GMT
CMD ["/bin/bash"]
# Tue, 28 Jan 2020 21:53:09 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 28 Jan 2020 21:53:09 GMT
ENV LANG=en_US.UTF-8
# Tue, 28 Jan 2020 21:53:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Tue, 28 Jan 2020 21:53:10 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 29 Feb 2020 03:17:46 GMT
ENV JAVA_VERSION=15-ea+12
# Sat, 29 Feb 2020 03:17:46 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/12/GPL/openjdk-15-ea+12_linux-x64_bin.tar.gz
# Sat, 29 Feb 2020 03:17:47 GMT
ENV JAVA_SHA256=ff430463b92de38a39224ada330253f9d6381621d99a0822a40e6c6b81d68bb1
# Sat, 29 Feb 2020 03:18:41 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Sat, 29 Feb 2020 03:18:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:86607bb85307f4e017c6cc236573951482f1de084e0987480fecea9295c2f923`  
		Last Modified: Tue, 28 Jan 2020 21:37:18 GMT  
		Size: 42.7 MB (42725283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1d217c4e16034b1dca5abb6ea80aabded93c73f35686d806d9f2aa8555743da`  
		Last Modified: Tue, 28 Jan 2020 22:00:21 GMT  
		Size: 14.8 MB (14793339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f47d031db9ca0073fbb9940d8881db948af6df55dbf34c0704e7252b54c391`  
		Last Modified: Sat, 29 Feb 2020 03:23:26 GMT  
		Size: 198.4 MB (198417304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

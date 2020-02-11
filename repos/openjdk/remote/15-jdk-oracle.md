## `openjdk:15-jdk-oracle`

```console
$ docker pull openjdk@sha256:6c91e6f2cdfcbe484c64ac11cf3a6a8ee79ad619d777c80c1f6234b7c456c81c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:15-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:5d2c072dc292cbd7ba0a7f3c2d4d116495fe6f3e0eb7d0c0c67dbb38b267217e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.5 MB (256473666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8de346e7de33e7bd7cfe6e0cc51738388966c6e244c3c929c5de4b2398eb21`
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
# Tue, 11 Feb 2020 01:20:45 GMT
ENV JAVA_VERSION=15-ea+9
# Tue, 11 Feb 2020 01:20:45 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/9/GPL/openjdk-15-ea+9_linux-x64_bin.tar.gz
# Tue, 11 Feb 2020 01:20:46 GMT
ENV JAVA_SHA256=2d41cf19105bcde66f051a3861b7b97acf330b9ae2f00e644eb4f21977b95045
# Tue, 11 Feb 2020 01:22:20 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Tue, 11 Feb 2020 01:22:21 GMT
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
	-	`sha256:9a6ce6c2da15454a162cc5a8342ce753f3453d87ced11714d53ec53f27fc6640`  
		Last Modified: Tue, 11 Feb 2020 01:28:02 GMT  
		Size: 199.0 MB (198955044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

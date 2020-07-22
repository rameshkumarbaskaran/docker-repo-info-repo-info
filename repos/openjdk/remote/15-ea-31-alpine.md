## `openjdk:15-ea-31-alpine`

```console
$ docker pull openjdk@sha256:d65ba34a31964a4efc43789c806787089cdb0c1a7ef56c8dd779bda7566d9fa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:15-ea-31-alpine` - linux; amd64

```console
$ docker pull openjdk@sha256:92b0784ab566d62b01f9495945bdf1aad3c000bcdae3d0f8f78d2256f01fa1ae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.5 MB (200519682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73327305beb3885d2e76a557752fa87a44735bd08c45121fd9b3124dc409ab0`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Wed, 22 Jul 2020 01:05:44 GMT
RUN apk add --no-cache java-cacerts
# Wed, 22 Jul 2020 01:07:14 GMT
ENV JAVA_HOME=/opt/openjdk-15
# Wed, 22 Jul 2020 01:07:14 GMT
ENV PATH=/opt/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 01:07:14 GMT
ENV JAVA_VERSION=15-ea+31
# Wed, 22 Jul 2020 01:07:15 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/alpine/31/binaries/openjdk-15-ea+31_linux-x64-musl_bin.tar.gz
# Wed, 22 Jul 2020 01:07:15 GMT
ENV JAVA_SHA256=da7abd4d3b3511ed2da8aba25b7ff67863261a0c8b5e7e771cf0fbfadcc7f4fd
# Wed, 22 Jul 2020 01:08:07 GMT
RUN set -eux; 		wget -O /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java --version; 	javac --version
# Wed, 22 Jul 2020 01:08:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a2e4aad8c98294e53534e7aef0572d7a04cc37264f1b4b75d0878244e59c7f`  
		Last Modified: Wed, 22 Jul 2020 01:13:01 GMT  
		Size: 926.4 KB (926401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa15118984fa68e4bdb9010318493fccb170122e25dac619d5cefdb32c4d32b`  
		Last Modified: Wed, 22 Jul 2020 01:14:18 GMT  
		Size: 196.8 MB (196795740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

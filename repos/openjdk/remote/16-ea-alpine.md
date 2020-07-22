## `openjdk:16-ea-alpine`

```console
$ docker pull openjdk@sha256:462f2b60c595beb84d7451e52db946966047a7c026b837c3b4294559aa2ae2f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:16-ea-alpine` - linux; amd64

```console
$ docker pull openjdk@sha256:bb748b0f640054f61f09a694d6da004715f57f6c2ef6b7cad9338e1fa326dca9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.2 MB (201184259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ffaf3792f08f30b209cd9bf8f43c12e2a248fb6f56d96ecd03768408515fdb`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Wed, 22 Jul 2020 01:05:44 GMT
RUN apk add --no-cache java-cacerts
# Wed, 22 Jul 2020 01:05:44 GMT
ENV JAVA_HOME=/opt/openjdk-16
# Wed, 22 Jul 2020 01:05:45 GMT
ENV PATH=/opt/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 01:05:45 GMT
ENV JAVA_VERSION=16-ea+5
# Wed, 22 Jul 2020 01:05:45 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/alpine/5/binaries/openjdk-16-ea+5_linux-x64-musl_bin.tar.gz
# Wed, 22 Jul 2020 01:05:46 GMT
ENV JAVA_SHA256=1ec940bea148a7ececda635c209de3836fe4e6511f5d49d4248cf6d52c77aac8
# Wed, 22 Jul 2020 01:06:39 GMT
RUN set -eux; 		wget -O /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java --version; 	javac --version
# Wed, 22 Jul 2020 01:06:39 GMT
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
	-	`sha256:8508feb361c772ab65274a30ac7fa75efad23dfd034e9b70c26aa694280f0924`  
		Last Modified: Wed, 22 Jul 2020 01:13:27 GMT  
		Size: 197.5 MB (197460317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

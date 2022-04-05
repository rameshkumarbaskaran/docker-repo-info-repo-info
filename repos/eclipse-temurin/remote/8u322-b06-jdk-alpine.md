## `eclipse-temurin:8u322-b06-jdk-alpine`

```console
$ docker pull eclipse-temurin@sha256:26ef30792a544e8dcc27a4e864d7d621e8dae54f633b227ab4818c2841560734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:8u322-b06-jdk-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:23e9b9dc441ac7574e7e3c851c1b2704cc776b2cdde145bd7f454e4a6d07b219
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104824187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb7ac349d402c3f3085c09b3da8c8cd6e10dbf0d577faf26c79c4488e5d6fcb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 10:55:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 10:55:44 GMT
RUN apk add --no-cache tzdata musl-locales musl-locales-lang     && rm -rf /var/cache/apk/*
# Tue, 05 Apr 2022 10:55:44 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Tue, 05 Apr 2022 10:56:02 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c7e781064c4a63ad6cd2399b2fa34de854a7d9bfd3ad2543d34bd7ba8f818822';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Apr 2022 10:56:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 10:56:03 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3277e9a7631c57d573722746688faad867a5b43dda77316e369e08ba94b713d`  
		Last Modified: Tue, 05 Apr 2022 10:59:33 GMT  
		Size: 430.5 KB (430455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d754090646addfa1a2e82949f973d4104ae63925b2173d4b02dbd68d9b9176`  
		Last Modified: Tue, 05 Apr 2022 10:59:41 GMT  
		Size: 101.6 MB (101579014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9073ab997e7dc6a42e110aad7535551c52627e4f808b0eabe92836cdced08d6a`  
		Last Modified: Tue, 05 Apr 2022 10:59:33 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

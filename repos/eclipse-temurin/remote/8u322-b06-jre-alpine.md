## `eclipse-temurin:8u322-b06-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:e942f47ad22ba799e5b628fc8062647140e0101a130a7d25a99ec8a4f99226ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:8u322-b06-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:07bec362c88c21906413316220dc9a43298481c1f335e8a02ed90e7ee6dd392d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44982078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9984dc388a0e75bd682323f4e494bb2ddc83f5c7df878df41b57a589a0b1e4df`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 06:09:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Mar 2022 06:09:17 GMT
RUN apk add --no-cache tzdata musl-locales musl-locales-lang     && rm -rf /var/cache/apk/*
# Tue, 29 Mar 2022 06:09:17 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Tue, 29 Mar 2022 06:09:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='984f1a1f96774e6fbb644031b89de349afb354c9d12232ffb500c6a5d4013b1b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 29 Mar 2022 06:09:38 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 06:09:39 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8b72f2e4b8ed4ba22286a50d6f2bf2b7f79589f32f8c9de1f0e643014314af`  
		Last Modified: Tue, 29 Mar 2022 06:12:48 GMT  
		Size: 430.5 KB (430474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59ba94b932967721b6f8e04b7f17ee563a64377587e0bfe22744437f8d3beb1`  
		Last Modified: Tue, 29 Mar 2022 06:13:14 GMT  
		Size: 41.7 MB (41736932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92e8a382c5774ca12754a9cf07b5b3be6c9134b6c54e99a5eeec6fca927eac6`  
		Last Modified: Tue, 29 Mar 2022 06:13:10 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

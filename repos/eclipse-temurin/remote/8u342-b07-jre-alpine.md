## `eclipse-temurin:8u342-b07-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:43a61173f5d05f011d65e4dc94048326e25186cd3228f675e40b3e652cf12103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:8u342-b07-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:460805fdc38e47bb85ddd045cc2de26c67ec8585598dd3ede730c04b8cac7442
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56619072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e450b327575e371f8d0316e773919533c920f9045dcfd395d442c075494d7a1d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 01:30:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 10 Aug 2022 01:30:26 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Wed, 10 Aug 2022 01:30:26 GMT
ENV JAVA_VERSION=jdk8u342-b07
# Wed, 10 Aug 2022 01:30:55 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='dd04e366c2e03310f9522b61a09f8ca056842a739cb33651e6eac60e3305c511';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u342-b07/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u342b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 10 Aug 2022 01:30:55 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Aug 2022 01:30:56 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878a9af9475f057a355a16521c6da6195d134a78707eb526021019fe67b702b5`  
		Last Modified: Wed, 10 Aug 2022 01:35:31 GMT  
		Size: 12.1 MB (12050079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc652d29ed32602f10219a9cbb650f49cd875bd5532d54210420edb6bda5d27`  
		Last Modified: Wed, 10 Aug 2022 01:36:00 GMT  
		Size: 41.8 MB (41762779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4705cbf533a8268da315b7e840387a574a54143cd26879aa840393be6c8459`  
		Last Modified: Wed, 10 Aug 2022 01:35:55 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

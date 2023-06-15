## `eclipse-temurin:8u372-b07-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:deeea62c12e12742b3f07f0d9b8abf603e686a6d1af3c5f23cbaa6b896e1f776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:8u372-b07-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:3caa0a38391d96932bdb53abb5420f20786cea5adf5dfc978a1ffcd7a2e74885
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52822508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf79180dc43401453bd0c924ca32f33d4132259d4fff02e3448562b7d354f7cd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 05:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jun 2023 05:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 05:11:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jun 2023 05:11:54 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Thu, 15 Jun 2023 05:11:54 GMT
ENV JAVA_VERSION=jdk8u372-b07
# Thu, 15 Jun 2023 05:12:17 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='95d8cb8b5375ec00a064ed728eb60d925d44c1a79fe92f6ca7385b5863d4f78c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u372-b07/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u372b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Thu, 15 Jun 2023 05:12:17 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aadc9aaa732ac5b0edd00545607971071fa1868047a65249e483ba2443982e6`  
		Last Modified: Thu, 15 Jun 2023 05:15:34 GMT  
		Size: 7.6 MB (7648372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea77bd42506cc5608b2089b808c5387c8303e85718b83ca8c10db9915467ae3`  
		Last Modified: Thu, 15 Jun 2023 05:16:01 GMT  
		Size: 41.8 MB (41776097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a527bc02e9f1a12b45c3668e6a1b2408c19bb8120aafe6fca8a527e91d2c11`  
		Last Modified: Thu, 15 Jun 2023 05:15:56 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

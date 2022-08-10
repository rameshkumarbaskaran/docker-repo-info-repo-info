## `eclipse-temurin:11-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:ce8c2c8d15dcf427e48dd1214079fae345bee19092f7efd05218b9dec927bcad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:11-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:b0ff526032d397e33c8f6681e1ca5f753b5d31cd5b3ba1d29f33088b8155b584
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57800657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fbff52e40523afdcbe6dd9ba9851ce8ed32b15487e51f0fdd7cdd3fd6b08034`
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
# Wed, 10 Aug 2022 01:31:04 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Wed, 10 Aug 2022 01:32:03 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b7e3743aad645af22c069ed9bddbddcdc0134176f4e4089e8a228a0fbe3887d7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 10 Aug 2022 01:32:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Aug 2022 01:32:04 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:4e74dfa16b1dcb4636398f704cde909a5bbe687f7c9d5c959329d2adc6e7a650`  
		Last Modified: Wed, 10 Aug 2022 01:36:50 GMT  
		Size: 42.9 MB (42944362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7214e411b859f232b609c7708722ecf4e1ce0e250f0d16b4c801a513dd4ba977`  
		Last Modified: Wed, 10 Aug 2022 01:36:44 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

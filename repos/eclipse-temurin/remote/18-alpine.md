## `eclipse-temurin:18-alpine`

```console
$ docker pull eclipse-temurin@sha256:d4a1bac2fe9d1c431f764d9e476993b5ea59ff38bb4329feada33ac8c384e151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:18-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:395eee7faad4202055731e8f358f3174f82e94c89d5154a9a2036d651867a4cb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207753858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20d9f9ef1934b42f1ae1cc02d33932ac73a7f9539512dd5d8bb174d75eb9ced`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 01:30:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 10 Aug 2022 01:30:26 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Wed, 10 Aug 2022 01:32:54 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Wed, 10 Aug 2022 01:33:24 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='045670342a036fff98b2ee90279ed923dc8c92bebe6227a2a60f64ca84f4f7c8';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_x64_alpine-linux_hotspot_18.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 10 Aug 2022 01:33:25 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Aug 2022 01:33:26 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Aug 2022 01:33:26 GMT
CMD ["jshell"]
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
	-	`sha256:4fb9fee1c1338ebe463c13e4d7ece3e5f95cba558caa64493ce1f6cac2da0e91`  
		Last Modified: Wed, 10 Aug 2022 01:38:09 GMT  
		Size: 192.9 MB (192897563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7d5b48ab638eb446c579d5c6d665eb01c2b6816d0f7d043286e500bb729184`  
		Last Modified: Wed, 10 Aug 2022 01:37:54 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

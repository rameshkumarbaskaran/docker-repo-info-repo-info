## `eclipse-temurin:8u342-b07-jdk-alpine`

```console
$ docker pull eclipse-temurin@sha256:b57912380870baf743a25250edb8d9d75728502f231619d41e5620cd9885aec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:8u342-b07-jdk-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:25f4eeef974c62b1f1d7822b83d1a05a65cb61571dfd7c963e64e58f548f1ff7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116294351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d295e2274b6de9a9e4cbd18b548e66092acab1f05c768bab89d0a4b5df1d1f`
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
# Wed, 10 Aug 2022 01:30:38 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='fc146a83e30a8b4f17a8558b9da58eed645a615542eea7dc942278a3c60d1efe';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u342-b07/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u342b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 10 Aug 2022 01:30:38 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Aug 2022 01:30:39 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:92ed2626262f4a4682cca5c966b25aa795951923b03399ff85a2b1630ce47374`  
		Last Modified: Wed, 10 Aug 2022 01:35:39 GMT  
		Size: 101.4 MB (101438059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af018c8f8447651c72e2dadde4ad5cb0c046a5953e5d801b913a66653142d503`  
		Last Modified: Wed, 10 Aug 2022 01:35:30 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

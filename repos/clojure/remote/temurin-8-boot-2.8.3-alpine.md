## `clojure:temurin-8-boot-2.8.3-alpine`

```console
$ docker pull clojure@sha256:a3e4df8dd9e28a0f33091efaaf89dc1937ca2562da48a344c232b4858ba091d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-8-boot-2.8.3-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:49efe94ecb5051c79dbeeb3c248cc382aca26382003e8c1c40bfa8c245ce0882
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.0 MB (175974459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08466216cb8fb0f1114743c98b0dc76343be18a0f849e631316c648a3a46f7ad`
-	Default Command: `["boot","repl"]`

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
# Wed, 10 Aug 2022 05:58:20 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Aug 2022 05:58:20 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Aug 2022 05:58:20 GMT
WORKDIR /tmp
# Wed, 10 Aug 2022 05:58:21 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Wed, 10 Aug 2022 05:58:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Aug 2022 05:58:22 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Aug 2022 05:58:54 GMT
RUN boot
# Wed, 10 Aug 2022 05:58:54 GMT
CMD ["boot" "repl"]
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
	-	`sha256:77976375822eb2e8adc79a8f8174c5a7d4b72fe78652d08caee1f2d6243f6953`  
		Last Modified: Wed, 10 Aug 2022 06:04:04 GMT  
		Size: 859.3 KB (859308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c990b09df87e6abe02276b5a730cadc078bdbb3c7502440047e012d9044f1268`  
		Last Modified: Wed, 10 Aug 2022 06:04:08 GMT  
		Size: 58.8 MB (58820800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

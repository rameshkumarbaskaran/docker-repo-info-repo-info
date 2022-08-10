## `clojure:temurin-11-boot-2.8.3-alpine`

```console
$ docker pull clojure@sha256:af05f7addfdc04b87661ca8aa3d630556defad8558b12c558abf01de6bceddc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-11-boot-2.8.3-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:7d254aee2ecbd4f8ddd3c65ad7957d7fa0744414e3c8e7ba8c074cb0524f9ec6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (267989398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8383d4d8ccee5db0f7dc3b36d66cadc552ae257527109dff26a1162a7af82716`
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
# Wed, 10 Aug 2022 01:31:04 GMT
ENV JAVA_VERSION=jdk-11.0.16+8
# Wed, 10 Aug 2022 01:31:41 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='32a93bd824cf34ccdde0881699a41a12722b4d8ff1d57294b2add2102432759b';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16%2B8/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.16_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 10 Aug 2022 01:31:42 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Aug 2022 01:31:43 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Aug 2022 01:31:43 GMT
CMD ["jshell"]
# Wed, 10 Aug 2022 05:59:32 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Aug 2022 05:59:32 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Aug 2022 05:59:32 GMT
WORKDIR /tmp
# Wed, 10 Aug 2022 05:59:33 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Wed, 10 Aug 2022 05:59:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Aug 2022 05:59:33 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Aug 2022 05:59:53 GMT
RUN boot
# Wed, 10 Aug 2022 05:59:53 GMT
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
	-	`sha256:65a7c745b5187660c398c71d335a3bd951a6092d0c4c43ed1d5510faceeb8e21`  
		Last Modified: Wed, 10 Aug 2022 01:36:28 GMT  
		Size: 193.5 MB (193453405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e0394f18a9e1aa03979ddb6eea7af52707283762c71b856871b03677276922`  
		Last Modified: Wed, 10 Aug 2022 01:36:13 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78af7db3992372a42bd9a850c73befa35246157e7bd067e9d30cae5d08625b4d`  
		Last Modified: Wed, 10 Aug 2022 06:04:51 GMT  
		Size: 859.3 KB (859308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dff403e5ccde74a963690d1e01df5362e2e7e755b0c2b3ffc6fa4b653de1249`  
		Last Modified: Wed, 10 Aug 2022 06:04:54 GMT  
		Size: 58.8 MB (58820393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

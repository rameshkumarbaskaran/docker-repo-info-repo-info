## `eclipse-temurin:11-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:d53057485467c5a59aeb9b700ad566e2e4a6d1a0b51bca801909247963ae8db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:11-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:8555d6b7e5e5f75e3ed033877a6778bf4f5531895ab4d22920c42e23d0e3ba87
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57920481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e1417a4ca14fac4cbbecbe0c53b71ecaacccd8a854d618074ce802048203a50`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 16:53:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 07 Oct 2022 16:53:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Oct 2022 16:53:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 07 Oct 2022 16:53:21 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Fri, 04 Nov 2022 23:20:57 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 04 Nov 2022 23:22:13 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='96d26887d042f3c5630cca208b6cd365679a59bf9efb601b28363e827439796c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Fri, 04 Nov 2022 23:22:14 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5835cc7e6eb64b728c9694dd72d8aede877af0a2ec44f981847853af9abbf5`  
		Last Modified: Fri, 07 Oct 2022 16:57:51 GMT  
		Size: 12.0 MB (12041341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c534e4636285e454e2df74edd4725c68d0c974bf88bcdccb973f91baff68368f`  
		Last Modified: Fri, 04 Nov 2022 23:28:59 GMT  
		Size: 43.1 MB (43072924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72dfe3ef7d3ab718af9b52c1ad91b4ae47a0f5e30c0bbbc3d3ecfc70eb25e5a4`  
		Last Modified: Fri, 04 Nov 2022 23:28:53 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

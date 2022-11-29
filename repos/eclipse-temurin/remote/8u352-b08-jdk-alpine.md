## `eclipse-temurin:8u352-b08-jdk-alpine`

```console
$ docker pull eclipse-temurin@sha256:a9071af26973c97552d921f893856e95de165d73d90f4724942c7ca7357ed2b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:8u352-b08-jdk-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:6b9d78db2289428157455dc5f5f56255aaaf1ea8e1b0fcb1298a75007103bd0e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116842316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c99b6a870e0363dd1ab0ecc280aed378e5632d74b775479c487b4eec2080fabc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 22 Nov 2022 22:19:28 GMT
ADD file:587cae71969871d3c6456d844a8795df9b64b12c710c275295a1182b46f630e7 in / 
# Tue, 22 Nov 2022 22:19:29 GMT
CMD ["/bin/sh"]
# Tue, 29 Nov 2022 20:19:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 29 Nov 2022 20:19:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Nov 2022 20:19:48 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Nov 2022 20:19:50 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Tue, 29 Nov 2022 20:19:50 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Tue, 29 Nov 2022 20:19:56 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='aa782e3c561b041a5730cbe728c210e234db71fa7222bd8b661f9f4df7799375';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Tue, 29 Nov 2022 20:19:57 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:c158987b05517b6f2c5913f3acef1f2182a32345a304fe357e3ace5fadcad715`  
		Last Modified: Tue, 22 Nov 2022 22:19:52 GMT  
		Size: 3.4 MB (3370706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e5acd5897d762b9a83758d4ceae374df7b8b0367a48cc14b8a00e33998b3bf`  
		Last Modified: Tue, 29 Nov 2022 20:26:18 GMT  
		Size: 12.0 MB (12020105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d66210930567a6a06bc97c7773352e2e7518102af14179e951b2e426c13792c`  
		Last Modified: Tue, 29 Nov 2022 20:26:25 GMT  
		Size: 101.5 MB (101451345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01654942074e89972a3088bf73012c02b3c0aaa2a30c903ef009207b81d52066`  
		Last Modified: Tue, 29 Nov 2022 20:26:16 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

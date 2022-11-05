## `eclipse-temurin:8u352-b08-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:ecc4ed1ee81665ad3f2164798fee02de7da36a09f44acbe64defc86c183f0ef1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:8u352-b08-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:948752bc47bdd859018e0101c331343fb4c60c1e0fcb493bfc391a24ee72ad8c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56615642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d50b0e1b9abeb6fada64437528bf960b1cd923f7b0adaf375fac179d006ac78`
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
# Fri, 04 Nov 2022 23:19:45 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Fri, 04 Nov 2022 23:20:33 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0f4a4a3c092d8cca171fc36003ac82e2f3d8d768bd6f530a20e2a4caf79bdb9e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Fri, 04 Nov 2022 23:20:34 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:93ef75ac4dc7e5697ca99593200298c334728f7f30020e74127c150bfe5d4b62`  
		Last Modified: Fri, 04 Nov 2022 23:26:13 GMT  
		Size: 41.8 MB (41768087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59633c34ad8effe5c89e487361006a002df2efdb0d7cdc2209a2f276bafe7c58`  
		Last Modified: Fri, 04 Nov 2022 23:26:08 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eclipse-temurin:8u352-b08-jdk-alpine`

```console
$ docker pull eclipse-temurin@sha256:d1081d53865f565ce2f9dd04f0641ec06dec20556cb29443e553095e18a23214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:8u352-b08-jdk-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:f85ec08a33a2bb5ad8f4414f3363e018ed73399fd3d3fd93e5384cad8950f4f1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116298868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3de7005fe573a7208e3a12e86990aeaff4bc318a64aae3426ae9f86b0554b4c`
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
# Fri, 04 Nov 2022 23:19:54 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='aa782e3c561b041a5730cbe728c210e234db71fa7222bd8b661f9f4df7799375';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Fri, 04 Nov 2022 23:19:55 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:b4b8e2cbbc1869f89dbeb44d306f2ff9c62203d78b89eb09a297533c9950b576`  
		Last Modified: Fri, 04 Nov 2022 23:24:53 GMT  
		Size: 101.5 MB (101451311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49082d9177c89f5d1d8049a78e2847acaebf03d6295cba8b8cb0bd17dd90e13e`  
		Last Modified: Fri, 04 Nov 2022 23:24:45 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

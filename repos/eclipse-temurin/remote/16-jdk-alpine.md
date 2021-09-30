## `eclipse-temurin:16-jdk-alpine`

```console
$ docker pull eclipse-temurin@sha256:1994b82029836f840c4ca2650f07a39ac3b8b715ae320fd16bc3fe09f614fb3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:16-jdk-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:9ae3d4a6fd4758d661bbb0a31076f6347a994aa885973187504d6e55d453e935
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.7 MB (208696988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef6cff39622f79ff428ba36a792e28fea35296cd93008de6f77a1d004f9c8330`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 17 Sep 2021 21:41:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 24 Sep 2021 19:20:30 GMT
RUN apk add --no-cache tzdata musl-locales musl-locales-lang     && rm -rf /var/cache/apk/*
# Thu, 30 Sep 2021 17:20:06 GMT
ENV JAVA_VERSION=jdk-16.0.2+7
# Thu, 30 Sep 2021 17:20:20 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='85788b1a1f470ca7ddc576028f29abbc3bc3b08f82dd811a3e24371689d7dc0f';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_x64_alpine-linux_hotspot_16.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 30 Sep 2021 17:20:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Sep 2021 17:20:22 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 30 Sep 2021 17:20:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5491faa5141cd7b6b8bcb2f0546bc3268ca907c1a0835e91db57c666453bde3d`  
		Last Modified: Fri, 24 Sep 2021 19:23:00 GMT  
		Size: 408.6 KB (408594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727067180390841412d947f7964422f9c516711764eb10fb35ae337dc66677b8`  
		Last Modified: Thu, 30 Sep 2021 17:21:52 GMT  
		Size: 205.5 MB (205473787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8604c492f623b3dfc51d67f385dfb686f3b55afd7346b1e8356d9f3657e989d5`  
		Last Modified: Thu, 30 Sep 2021 17:21:37 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

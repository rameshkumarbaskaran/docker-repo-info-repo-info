## `eclipse-temurin:17-jdk-alpine`

```console
$ docker pull eclipse-temurin@sha256:7e7f5efc54fe8913ce00d2a7ab8cb8226d0d5c6065c0eceef9ba7984fd5300f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:17-jdk-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:0a2d997d610743ff75e497e18800ad2dbfca896430ec4559c5fa4b32f213845c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.1 MB (195078326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6caf7aceb0c371fff0127f8ed416fb7f6e4be8cf3ebc4261abd127291984dc7c`
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
# Fri, 05 Nov 2021 19:20:49 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Fri, 05 Nov 2021 19:21:06 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='da4845987b3348da14338a0620ef7db25870e27670e82baebcc367fa9d17c7de';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 05 Nov 2021 19:21:07 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Nov 2021 19:21:08 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 05 Nov 2021 19:21:08 GMT
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
	-	`sha256:7350cd0e887e506871e572f4eb84f758e0e7186e6a5412cc78c850ea25d1c2e3`  
		Last Modified: Fri, 05 Nov 2021 19:24:56 GMT  
		Size: 191.9 MB (191855125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab4824b2d6455ed7e7acb2aa548eae5144102979dfa32aa1d77f26a99f673be`  
		Last Modified: Fri, 05 Nov 2021 19:24:42 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

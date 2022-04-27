## `eclipse-temurin:17-alpine`

```console
$ docker pull eclipse-temurin@sha256:33c0ef386e85569340e902bc4e7ced80dd43432a22511814a0b066c837a72c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:17-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:a61d4979811b884298f93daeba374ff6b6668a769db253e79b59af50af525ffe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.1 MB (195054372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8a29432c070866c2f51b5c3e1ef4d24b915df3111f0b159e14beb5d8a40c15`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 10:55:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 10:55:44 GMT
RUN apk add --no-cache tzdata musl-locales musl-locales-lang     && rm -rf /var/cache/apk/*
# Wed, 27 Apr 2022 18:21:21 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Wed, 27 Apr 2022 18:21:37 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='5cbaece6aec44f6d3911cfa3c5a8659889e85042aff214c944c5fa1b5938a5fc';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.3_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 27 Apr 2022 18:21:38 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Apr 2022 18:21:39 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 27 Apr 2022 18:21:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3277e9a7631c57d573722746688faad867a5b43dda77316e369e08ba94b713d`  
		Last Modified: Tue, 05 Apr 2022 10:59:33 GMT  
		Size: 430.5 KB (430455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f2c97071093dd704b77dd1cbdca2551f0a13717597393d821bb8be2ea237ae`  
		Last Modified: Wed, 27 Apr 2022 18:26:33 GMT  
		Size: 191.8 MB (191809196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28060bb0256d21647977bfabfba0e316b3bd27e40a6e549ac2b825bb11610312`  
		Last Modified: Wed, 27 Apr 2022 18:26:19 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eclipse-temurin:11-alpine`

```console
$ docker pull eclipse-temurin@sha256:27799b8cc2132e874dc991e9b9eba1a71ffe7fc24be1d6e8f92175f131307cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:11-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:d4a05f85b0e0af22b6082a22f7ed97f65569a6edd4d38c12a52fa81f1d32d144
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.1 MB (197057671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73e2ea53f23f2c21774c6e7d3d00c0850f2e0eb9a0067033a293bd616c068bc1`
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
# Wed, 27 Apr 2022 18:19:51 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Wed, 27 Apr 2022 18:20:08 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b7409adf3b6d61324d734218be29b796089c1df0c994f128700c7a7fde728d1f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 27 Apr 2022 18:20:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Apr 2022 18:20:10 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 27 Apr 2022 18:20:10 GMT
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
	-	`sha256:02333c4ab4994f8f2e2efb5e745c226e5adc926e87b5bf880e038005d88e29be`  
		Last Modified: Wed, 27 Apr 2022 18:24:25 GMT  
		Size: 193.8 MB (193812495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83bc92a9dfa0d01fcb93dc443c65e056d5537dfb76ca73d86354330644e1fb3a`  
		Last Modified: Wed, 27 Apr 2022 18:24:11 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

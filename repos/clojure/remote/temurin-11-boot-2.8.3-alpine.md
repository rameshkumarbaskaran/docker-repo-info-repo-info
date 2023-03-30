## `clojure:temurin-11-boot-2.8.3-alpine`

```console
$ docker pull clojure@sha256:7bbde9d6850b52f719834b1c75bc449429a38cf41743647f152d6a3d4bdc3167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-11-boot-2.8.3-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:1d867a916375319a2cc3fd68f098867489c69b9e9ec01d3a015b52bc47da8f84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268958681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7765643d56a4451e4098b1abe3e9f5b68bd593751d8b1d7f55ea83821826b225`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:48:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Mar 2023 19:48:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Mar 2023 19:48:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 29 Mar 2023 19:48:58 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Wed, 29 Mar 2023 19:49:29 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Wed, 29 Mar 2023 19:49:39 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='42722bdbee99ad1430d6e88f17608909f26b57ab7761fb6b87ff4dbf6a8928bc';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 29 Mar 2023 19:49:42 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 29 Mar 2023 19:49:42 GMT
CMD ["jshell"]
# Thu, 30 Mar 2023 03:03:26 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 30 Mar 2023 03:03:26 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 30 Mar 2023 03:03:26 GMT
WORKDIR /tmp
# Thu, 30 Mar 2023 03:03:27 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Thu, 30 Mar 2023 03:03:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 30 Mar 2023 03:03:27 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 30 Mar 2023 03:04:03 GMT
RUN boot
# Thu, 30 Mar 2023 03:04:03 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ed194273be4d4d02a2158c3e7c9ea96095ed70f65939d53f4968b0f225c628`  
		Last Modified: Wed, 29 Mar 2023 19:52:03 GMT  
		Size: 12.0 MB (12019605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfeea393a4f62a17d4c9c493fee278eb9d53be05eefa3c6bdd7ac1fe7fb3e86c`  
		Last Modified: Wed, 29 Mar 2023 19:52:50 GMT  
		Size: 193.8 MB (193847595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5d734cfcf3c5d5f8e58118c2fd9f8c6211942c045b3764a28b2b1904963720`  
		Last Modified: Wed, 29 Mar 2023 19:52:38 GMT  
		Size: 179.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc57ee2fa363e2e6dd7cdc1c07f4a0e297ff3168df701fe8cbc037a6a89a1d9`  
		Last Modified: Thu, 30 Mar 2023 03:07:58 GMT  
		Size: 896.1 KB (896097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87361dd428b006939c4813598df19d2d4526b1fe3b4de6a7c7f97eb5c24d1b03`  
		Last Modified: Thu, 30 Mar 2023 03:08:01 GMT  
		Size: 58.8 MB (58820642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

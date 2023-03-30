## `clojure:temurin-17-boot-alpine`

```console
$ docker pull clojure@sha256:cb84dcbfcf7e6bea416e8a92c47b67e985f6fadaf2b4bae1dbba96bddd730810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-17-boot-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:2bfab092e642fefd86536cfd8c95d45fa19cfde851682771a7bac60b4f97bf52
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.9 MB (266904936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3461edcb919ae2c8ead6cfe28a0cc142f4e545a6987d0f85a01e82f5b483ed3e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
# Wed, 29 Mar 2023 19:50:07 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Wed, 29 Mar 2023 19:50:17 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0df7c1a58debee2668931ba4a07cb642475b23a5c61473761b6f293eba7c024a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 29 Mar 2023 19:50:20 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 29 Mar 2023 19:50:20 GMT
CMD ["jshell"]
# Thu, 30 Mar 2023 03:04:49 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 30 Mar 2023 03:04:50 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 30 Mar 2023 03:04:50 GMT
WORKDIR /tmp
# Thu, 30 Mar 2023 03:04:51 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Thu, 30 Mar 2023 03:04:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 30 Mar 2023 03:04:51 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 30 Mar 2023 03:05:09 GMT
RUN boot
# Thu, 30 Mar 2023 03:05:09 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 30 Mar 2023 03:05:09 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Mar 2023 03:05:09 GMT
CMD ["repl"]
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
	-	`sha256:447fb591121b7b0c1f352bc4baf3b7c840dcf32615f5b8504a4882e9048f2dca`  
		Last Modified: Wed, 29 Mar 2023 19:53:34 GMT  
		Size: 191.8 MB (191793866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93cdd4cdb2078d3e1d61a38f6f6378966a085bf96adceecceeaffa29922faedb`  
		Last Modified: Wed, 29 Mar 2023 19:53:21 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d52b522600fec76f85c7faf6df8d6e7672b7498c4a2db3764d0e3a05c70e51`  
		Last Modified: Thu, 30 Mar 2023 03:08:39 GMT  
		Size: 896.1 KB (896095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0f02f925ab87146a7e6660c0391ce896fc1d8844863141d7d47645a0b0e383`  
		Last Modified: Thu, 30 Mar 2023 03:08:42 GMT  
		Size: 58.8 MB (58820232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba51aa0e1fd6898e2393278a612c91580b6a896eaae346c3d08a33af8a82b9f9`  
		Last Modified: Thu, 30 Mar 2023 03:08:38 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clojure:temurin-8-alpine`

```console
$ docker pull clojure@sha256:1ce55dd4ec791da76466f0684edabe2a84cf2b13f14507a2d40b56fa1975b4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-8-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:8fbf86d866855fc6d53cd128cc3874661c59a5dcac244b2a9c8c3b0e02bc5f07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95262253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce770083c7a63c922b8d5499da9480f14e2a38c276159a2b62a8c8bcaa731ae`
-	Default Command: `["clj"]`

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
# Wed, 29 Mar 2023 19:48:58 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Wed, 29 Mar 2023 19:49:03 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='389c0d2ea59742103f46f1dd6d2c83e43e9f935f3f0485b1f9e74ac4e8c5ce47';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Wed, 29 Mar 2023 19:49:04 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 30 Mar 2023 03:03:12 GMT
ENV CLOJURE_VERSION=1.11.1.1257
# Thu, 30 Mar 2023 03:03:12 GMT
WORKDIR /tmp
# Thu, 30 Mar 2023 03:03:17 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "be032cf21dc67ecf072f7254a01c3587d97aa311198f53cd1a1777ddfb3e9244 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Thu, 30 Mar 2023 03:03:17 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 30 Mar 2023 03:03:17 GMT
CMD ["clj"]
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
	-	`sha256:2b41571bb2675b142d9a5fdbff0ee09d26c687e3e6df9d09f437f3909fecf98a`  
		Last Modified: Wed, 29 Mar 2023 19:52:08 GMT  
		Size: 52.5 MB (52541504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36ccf21b1cfec1e8554234a199d876fdc59f6a3906c4806eca7022fd312ea28`  
		Last Modified: Wed, 29 Mar 2023 19:52:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fa756490c768501f3c58f0e3cfc73e13081d66add19a008c5a135f2896b46a`  
		Last Modified: Thu, 30 Mar 2023 03:07:44 GMT  
		Size: 27.3 MB (27325800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f3cb9583d10ea070599a0e7e8339a1e4f5051068213252e21d879e6f240360c`  
		Last Modified: Thu, 30 Mar 2023 03:07:42 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `clojure:temurin-20-tools-deps-alpine`

```console
$ docker pull clojure@sha256:4b507dc43d03eeec3d27051720a079864b170d62c12a1349e29c58384948c7c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-20-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:92241e9441f531b4521c2ceff71bd2995a35f102fa6741834a5d3340836262df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241056882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bede0a70dd95214a9f81861af5e80e7a28f668ed97228273042ed5f423f63a2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 05:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jun 2023 05:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 05:11:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 15 Jun 2023 05:11:54 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Thu, 15 Jun 2023 05:13:51 GMT
ENV JAVA_VERSION=jdk-20.0.1+9
# Thu, 15 Jun 2023 05:14:02 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='68d0f0c468064e944e304cab64fc162335d4d9bc0ddab7e6ff7a395a0bceda74';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.1%2B9/OpenJDK20U-jdk_x64_alpine-linux_hotspot_20.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Thu, 15 Jun 2023 05:14:04 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 15 Jun 2023 05:14:04 GMT
CMD ["jshell"]
# Thu, 15 Jun 2023 09:01:22 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Thu, 15 Jun 2023 09:01:22 GMT
WORKDIR /tmp
# Thu, 15 Jun 2023 09:01:26 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Thu, 15 Jun 2023 09:01:27 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 15 Jun 2023 09:01:27 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 15 Jun 2023 09:01:27 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jun 2023 09:01:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aadc9aaa732ac5b0edd00545607971071fa1868047a65249e483ba2443982e6`  
		Last Modified: Thu, 15 Jun 2023 05:15:34 GMT  
		Size: 7.6 MB (7648372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d7d7d1600692ee70c8098f819ea5dab900fe619a1d0ce9ab60decceed7b3b7`  
		Last Modified: Thu, 15 Jun 2023 05:17:58 GMT  
		Size: 202.0 MB (201970803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d91e43deec5874b6a039c7a0713c640be552f639cdbcb59f5f31a37982f0e6`  
		Last Modified: Thu, 15 Jun 2023 05:17:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091c6803cfb1fd243f36901edf80c437373a7b646aa7218d1d508962a69d86a8`  
		Last Modified: Thu, 15 Jun 2023 09:05:12 GMT  
		Size: 28.0 MB (28038629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bcb78743d2010aa17f59e5bedf5fd5eb45008dd39313fb0ef07933a0928e479`  
		Last Modified: Thu, 15 Jun 2023 09:05:09 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63da007d04541ab266528f1ca9a31e8e3626b17f1e95062b6a6fb6346098d925`  
		Last Modified: Thu, 15 Jun 2023 09:05:09 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

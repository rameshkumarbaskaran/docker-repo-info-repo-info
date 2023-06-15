## `clojure:temurin-17-tools-deps-1.11.1.1347-alpine`

```console
$ docker pull clojure@sha256:87bec106eab37aeb5011e253eb1a0088ec97db4f91aea24af25744b16b391cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-17-tools-deps-1.11.1.1347-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:9ca2e4be58a678a7b384a2f64df174bfcf2ba544136007addf94f45ab05548c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231011939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7851e84638a3c6fe5c963ac263f972ab4997a2500ed78448d755744282b5c2`
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
# Thu, 15 Jun 2023 05:13:09 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Thu, 15 Jun 2023 05:13:19 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b6edac2fa669876ef16b4895b36b61d01066626e7a69feba2acc19760c8d18cb';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Thu, 15 Jun 2023 05:13:22 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 15 Jun 2023 05:13:22 GMT
CMD ["jshell"]
# Thu, 15 Jun 2023 09:00:43 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Thu, 15 Jun 2023 09:00:43 GMT
WORKDIR /tmp
# Thu, 15 Jun 2023 09:00:47 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Thu, 15 Jun 2023 09:00:47 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 15 Jun 2023 09:00:47 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 15 Jun 2023 09:00:47 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jun 2023 09:00:47 GMT
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
	-	`sha256:fc61c42d98a4031b53e224aa8cc9ebeed087bfcaee2312db7bdef6c15b75ace6`  
		Last Modified: Thu, 15 Jun 2023 05:17:11 GMT  
		Size: 191.9 MB (191925872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b872839787b43a160ad35873d407c6ed86e91883cc290c9b0d3eea46d171cb9`  
		Last Modified: Thu, 15 Jun 2023 05:16:58 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a948a47a4dc72397370a04ba86fb068d40434f0534aef705d95b35bd2295b03`  
		Last Modified: Thu, 15 Jun 2023 09:04:34 GMT  
		Size: 28.0 MB (28038617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe712d5111fcfbb89b9d0e598c7cbe0ec7537cd4f24ac61d00db618c86f0d4c`  
		Last Modified: Thu, 15 Jun 2023 09:04:32 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46c3aa56c6855cb0af3d2d1d3c9c427d8a43f77b22eae2025d343f939a322df`  
		Last Modified: Thu, 15 Jun 2023 09:04:32 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

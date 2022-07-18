## `eclipse-temurin:11-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:cd5d4a9b71d59707fae0f5643b504aaa16768b67f414c12eda7bca8d5819821d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:11-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:dcd7942517ac38c259af1a9af0601ae138f173616c2f0c08cdc0294027e59c16
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46417925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767c6c61c03ea82acb0ae1853adb492af127cc5af017bd28cdbbb44548037de1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:20:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 18 Jul 2022 22:20:08 GMT
RUN apk add --no-cache libretls musl-locales musl-locales-lang tzdata zlib     && rm -rf /var/cache/apk/*
# Mon, 18 Jul 2022 22:20:51 GMT
ENV JAVA_VERSION=jdk-11.0.15+10
# Mon, 18 Jul 2022 22:21:21 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='364b0f4faac666a9e81bf17b4e8b5cefa655b0f688cf3e0c1e78eb9d0ce9dca0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.15%2B10/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.15_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 18 Jul 2022 22:21:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Jul 2022 22:21:22 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d31e16dc1b50d804a50e80381050a90d4dc55a110eae65cd1cef937d3dc18d3`  
		Last Modified: Mon, 18 Jul 2022 22:24:55 GMT  
		Size: 477.8 KB (477762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c83e995281ad0deecaeb10aaac752b94902ed02d4cc6f1515eda50d214e06666`  
		Last Modified: Mon, 18 Jul 2022 22:26:18 GMT  
		Size: 43.1 MB (43141196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0d066b16e58588e12b868ad2b7c2c4d7b81011dd71df32220af9bbcefada1c`  
		Last Modified: Mon, 18 Jul 2022 22:26:11 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

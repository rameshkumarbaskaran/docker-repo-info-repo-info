## `eclipse-temurin:11-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:b4f3522498c1c019ffeee7dc8e2f4100f8028207d86c62971efe1d37e313c375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:11-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:68a61bdf11c53dd0d2396bfe631877a300db41329847b487aa06ea5a4f51cecf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45888942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e614e566385bb0aa3b8fffb10621b7281590312d1bbea37006ca93040351c197`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 17 Sep 2021 21:41:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 24 Sep 2021 19:20:30 GMT
RUN apk add --no-cache tzdata musl-locales musl-locales-lang     && rm -rf /var/cache/apk/*
# Wed, 27 Oct 2021 00:21:11 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Fri, 05 Nov 2021 19:20:20 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c7f56c8c4a5d115e13c9b595384029441008786427e7a85f91004134520f46d2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 05 Nov 2021 19:20:21 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Nov 2021 19:20:22 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:cfaece2fb47abad3ebd8253634e21c8bfaa59341127564cd31709dd4f1fbc266`  
		Last Modified: Fri, 05 Nov 2021 19:23:58 GMT  
		Size: 42.7 MB (42665742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50942bc481a1af046ec18cbc0cf723bde9154bf20cb9aa753bc0ddc5d3f9898`  
		Last Modified: Fri, 05 Nov 2021 19:23:52 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `eclipse-temurin:8-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:aa30bd70026176e6a88f6a53afbda7cb897c1299a5017d6103b9da4c8e83e0e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:8-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:1650177727f0b148e4eec186f8955aa05aed7063d36c99a6929d59c69969ef0e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44982088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4fa8e9f66be6b7ab62ec415ca3edaadd5a82b24d9c63bf75167b9b8ffb87c3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 10:55:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 05 Apr 2022 10:55:44 GMT
RUN apk add --no-cache tzdata musl-locales musl-locales-lang     && rm -rf /var/cache/apk/*
# Tue, 05 Apr 2022 10:55:44 GMT
ENV JAVA_VERSION=jdk8u322-b06
# Tue, 05 Apr 2022 10:56:15 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='984f1a1f96774e6fbb644031b89de349afb354c9d12232ffb500c6a5d4013b1b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u322-b06/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u322b06.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 05 Apr 2022 10:56:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 10:56:16 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
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
	-	`sha256:9ec148661a160328109755f5071450bdf7b1301cda01872a84c35ed421b5d464`  
		Last Modified: Tue, 05 Apr 2022 11:00:00 GMT  
		Size: 41.7 MB (41736914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bbd3c3ec4d8fbfb0344d64a4a2a57e42ab98ace37602a6a6e553244a4306e5`  
		Last Modified: Tue, 05 Apr 2022 10:59:55 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

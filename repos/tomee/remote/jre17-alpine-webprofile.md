## `tomee:jre17-alpine-webprofile`

```console
$ docker pull tomee@sha256:622c50eccec54108997ec0f049b787334fcf748c022fb62431a71b7a315170f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:jre17-alpine-webprofile` - linux; amd64

```console
$ docker pull tomee@sha256:8940f3016257d6ee0b4ee2f2530a7ada81a96b6d583f7abef6e00bfe284a1c61
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.6 MB (113582979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52627a052f3b522d71326246e0a948af50a398272e7836351ed716c614802ca`
-	Default Command: `["catalina.sh","run"]`

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
# Tue, 25 Jul 2023 22:20:35 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Tue, 25 Jul 2023 22:22:07 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4cdf34da04fe3ed705c6ca0281049baa9f772e6321a77fe395023fb8e41fdb9f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Tue, 25 Jul 2023 22:22:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 25 Jul 2023 22:54:05 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Jul 2023 22:54:05 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg
# Tue, 25 Jul 2023 22:54:05 GMT
WORKDIR /usr/local/tomee
# Tue, 25 Jul 2023 22:54:07 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/*
# Tue, 25 Jul 2023 22:54:16 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Tue, 25 Jul 2023 22:54:16 GMT
ENV TOMEE_VER=8.0.15
# Tue, 25 Jul 2023 22:54:16 GMT
ENV TOMEE_BUILD=webprofile
# Tue, 25 Jul 2023 22:54:22 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz*
# Tue, 25 Jul 2023 22:54:22 GMT
EXPOSE 8080
# Tue, 25 Jul 2023 22:54:23 GMT
CMD ["catalina.sh" "run"]
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
	-	`sha256:7b3754ec054f613a000069c77a363e424784493bd68c5642fef638c263951578`  
		Last Modified: Tue, 25 Jul 2023 22:27:46 GMT  
		Size: 47.0 MB (46963312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471372b7e15227c091e96c3ace4ffe398080745ae19f476168d5217755541d48`  
		Last Modified: Tue, 25 Jul 2023 22:27:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104e1cdd08284efaa61f9c1a028f573953f25aaaadc7dd0bdc132078a802800c`  
		Last Modified: Tue, 25 Jul 2023 23:09:46 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bcc838a40f3c544bf966ecb8f1898c1768f48515fb074aa9d9d23e7b3473ad8`  
		Last Modified: Tue, 25 Jul 2023 23:09:47 GMT  
		Size: 6.6 MB (6556639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8448e5c98a1b9885a253930f7db507a8161e1a2bd6aaafef91bf63dfb27330c8`  
		Last Modified: Tue, 25 Jul 2023 23:09:46 GMT  
		Size: 62.9 KB (62935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f1a1c275f7aca99ca49f4c41996a27eb1eb4720443cc7ee68d1bb77e967243`  
		Last Modified: Tue, 25 Jul 2023 23:09:49 GMT  
		Size: 49.0 MB (48953461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomee:alpine-plus`

```console
$ docker pull tomee@sha256:f16aeb76e67a0841ecaaf05e4f13701f7dbedfe9a08e39f537344f2c6cfe14af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:alpine-plus` - linux; amd64

```console
$ docker pull tomee@sha256:faf5494d5b9f562e79520d580b66c416ffd8a75db183653fad3e70bfaf84cf76
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138680267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace5f67507ae989d277c384c9c913ad01601ae34f22bd72aababda7009445190`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 11 Feb 2023 05:24:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Feb 2023 05:24:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 11 Feb 2023 05:24:09 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Sat, 11 Feb 2023 05:25:41 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Sat, 11 Feb 2023 05:26:14 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f3f7ef4b01143ce99651a5d14b7a96cf9f8920822291a3c2ca547232675fbda7';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Sat, 11 Feb 2023 05:26:15 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 11 Feb 2023 06:20:07 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Feb 2023 06:20:08 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 11 Feb 2023 06:20:08 GMT
WORKDIR /usr/local/tomee
# Sat, 11 Feb 2023 06:20:10 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/*
# Sat, 11 Feb 2023 06:20:19 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 11 Feb 2023 06:20:19 GMT
ENV TOMEE_VER=8.0.14
# Sat, 11 Feb 2023 06:21:19 GMT
ENV TOMEE_BUILD=plus
# Sat, 11 Feb 2023 06:21:27 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz*
# Sat, 11 Feb 2023 06:21:27 GMT
EXPOSE 8080
# Sat, 11 Feb 2023 06:21:27 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f55337210c571172bc884a7dfb6dc597adab6b6ef741c06ca3200884ffc4b2b`  
		Last Modified: Sat, 11 Feb 2023 05:28:55 GMT  
		Size: 12.0 MB (12020168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9cf576cc176415701c34f445ad129bc2968c4728320c83ceb0d336f7358ada`  
		Last Modified: Sat, 11 Feb 2023 05:30:55 GMT  
		Size: 46.7 MB (46704475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ec0e696e64003019ddc3021697396bf40d5787328bba00548cf2bae56e7c2d`  
		Last Modified: Sat, 11 Feb 2023 05:30:48 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae10793253ad0fe5d9fc6a6f37349da774c9598162ba3ad4092e1aa9de258e36`  
		Last Modified: Sat, 11 Feb 2023 06:39:30 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13fc47763fc3223667d63186e59ddfb4c7418614a10a3fbc5a6c738ef9844d5a`  
		Last Modified: Sat, 11 Feb 2023 06:39:31 GMT  
		Size: 6.5 MB (6472654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c654d977d449bf70030a62fb202390615de65b2f31022e27484d0343984b39`  
		Last Modified: Sat, 11 Feb 2023 06:39:30 GMT  
		Size: 62.9 KB (62910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3666939b93cdca7ab7a2103412d80e76ee4c6638c751f342588e2c0ddeb0508`  
		Last Modified: Sat, 11 Feb 2023 06:42:15 GMT  
		Size: 70.0 MB (70045285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

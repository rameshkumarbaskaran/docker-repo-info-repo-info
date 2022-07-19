## `tomee:alpine-plume`

```console
$ docker pull tomee@sha256:cdc326cf313c08756637e72a5c5c2d27695d1b5c651bb53225cc4a36826ae08f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:alpine-plume` - linux; amd64

```console
$ docker pull tomee@sha256:ce9487d0e44b6188bb4324ad1ce3e0e898532d1ed628d45f098f65a291912719
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134641182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8819da97d304f22981c31457ea49ea58f3d0eececa96bd9536f276e0ccccc5`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 22:20:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 18 Jul 2022 22:20:08 GMT
RUN apk add --no-cache libretls musl-locales musl-locales-lang tzdata zlib     && rm -rf /var/cache/apk/*
# Mon, 18 Jul 2022 22:21:30 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Mon, 18 Jul 2022 22:22:02 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='27e4589db9b8e6df60a75737f12ab7df63f796ecf8e46c0a196f77b2c99af1ac';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.3%2B7/OpenJDK17U-jre_x64_alpine-linux_hotspot_17.0.3_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 18 Jul 2022 22:22:03 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Jul 2022 22:22:03 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Tue, 19 Jul 2022 04:08:36 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jul 2022 04:08:36 GMT
RUN mkdir -p /usr/local/tomee
# Tue, 19 Jul 2022 04:08:36 GMT
WORKDIR /usr/local/tomee
# Tue, 19 Jul 2022 04:09:28 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl  && rm -rf /var/cache/apk/*
# Tue, 19 Jul 2022 04:09:38 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Tue, 19 Jul 2022 04:09:38 GMT
ENV TOMEE_VER=8.0.12
# Tue, 19 Jul 2022 04:09:38 GMT
ENV TOMEE_BUILD=plume
# Tue, 19 Jul 2022 04:09:46 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sha512sum -c tomee.tar.gz.sha512   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz*
# Tue, 19 Jul 2022 04:09:47 GMT
EXPOSE 8080
# Tue, 19 Jul 2022 04:09:47 GMT
CMD ["catalina.sh" "run"]
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
	-	`sha256:c9528437d731bca09b1080d1bb22e6ff8a4c2b2cc7687232ae1532e8ac8a3055`  
		Last Modified: Mon, 18 Jul 2022 22:27:10 GMT  
		Size: 46.6 MB (46582039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72d580159683167067bee5e05dfea4a4ae3db162442c3f25e6c2ea9e66a1e63`  
		Last Modified: Mon, 18 Jul 2022 22:27:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be5eed13ed3ce07197ecbe53b593937f5318a334e62e50bbd562d6fddb4a55d`  
		Last Modified: Tue, 19 Jul 2022 04:33:19 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f554a117941552cf8f3ada6d353bfa5a534e1001cd1c2e3abeb24ea7c63e2879`  
		Last Modified: Tue, 19 Jul 2022 04:35:46 GMT  
		Size: 6.8 MB (6771947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea08fe16df8d08671f0a8f93b5ea16d2d2578385f9d2db43c5088acfb18af0e`  
		Last Modified: Tue, 19 Jul 2022 04:35:45 GMT  
		Size: 62.9 KB (62908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5cbd74676e64fa895698278ea7d35cab25e2122cd1b28233de47f55196849b`  
		Last Modified: Tue, 19 Jul 2022 04:35:50 GMT  
		Size: 77.9 MB (77947390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

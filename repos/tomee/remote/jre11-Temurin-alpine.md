## `tomee:jre11-Temurin-alpine`

```console
$ docker pull tomee@sha256:8d522a83987055b5576511533a6b3d94599f8254df8ca1e75a87e4ed7a36635b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `tomee:jre11-Temurin-alpine` - linux; amd64

```console
$ docker pull tomee@sha256:6b3f0d27bcdc59d89ed079aa7d62d2a6da759d7faf61aa0278ff40dae3c7476e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.5 MB (112507747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db928e8a2e11cfd406e6cb4e6456991af11bacb39fcdc08cf24b73b4edfd131`
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
# Sat, 11 Feb 2023 05:24:47 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Sat, 11 Feb 2023 05:25:29 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='81e51ec2da61b227c522881313c7e2a090b29d6cc4171b5e1db3f3d17d863e44';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Sat, 11 Feb 2023 05:25:30 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 11 Feb 2023 06:21:39 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Feb 2023 06:21:40 GMT
RUN mkdir -p /usr/local/tomee
# Sat, 11 Feb 2023 06:21:40 GMT
WORKDIR /usr/local/tomee
# Sat, 11 Feb 2023 06:21:42 GMT
RUN apk add --no-cache gpg gpg-agent dirmngr curl   && rm -rf /var/cache/apk/*
# Sat, 11 Feb 2023 06:21:51 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 11 Feb 2023 06:21:51 GMT
ENV TOMEE_VER=8.0.14
# Sat, 11 Feb 2023 06:21:51 GMT
ENV TOMEE_BUILD=webprofile
# Sat, 11 Feb 2023 06:21:57 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && sed "s/\t/  /" tomee.tar.gz.sha512 | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz*
# Sat, 11 Feb 2023 06:21:57 GMT
EXPOSE 8080
# Sat, 11 Feb 2023 06:21:57 GMT
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
	-	`sha256:993be46f798f7c7f8b22f7f5b7f1e18e7dbdbcf3ec561fd9c6876a01124d7682`  
		Last Modified: Sat, 11 Feb 2023 05:30:08 GMT  
		Size: 43.1 MB (43093325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b782ec50ac1f7492e777dfdf96141b7d9d6aa99d6e6f2ad404bbb79824c0f59e`  
		Last Modified: Sat, 11 Feb 2023 05:30:02 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380f0042116485c16d9da3ac881236f494a3a803c40249e15a6ce8fad6bf0d1b`  
		Last Modified: Sat, 11 Feb 2023 06:43:24 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:215d4eaae4659ba53490e74355d01c5a2882ca3116e38cf27126a5125b397dfa`  
		Last Modified: Sat, 11 Feb 2023 06:43:26 GMT  
		Size: 6.5 MB (6472717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6461e3aac55b306bde0258c2437d06be2eb2c66724c9f996f0dbdcb16b997b`  
		Last Modified: Sat, 11 Feb 2023 06:43:25 GMT  
		Size: 62.9 KB (62926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dccf76fdcb2fdcc69d2b50861fb809efbd30b96e66b5aeb255eadbe363e1546`  
		Last Modified: Sat, 11 Feb 2023 06:43:27 GMT  
		Size: 47.5 MB (47483834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

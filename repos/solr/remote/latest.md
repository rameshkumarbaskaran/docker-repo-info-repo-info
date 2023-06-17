## `solr:latest`

```console
$ docker pull solr@sha256:9a2360565feec22bdc9af5fd12503681d1423b6d581262e02f88d16f6ef324ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `solr:latest` - linux; amd64

```console
$ docker pull solr@sha256:e29c8b80f1864d67f40d0fbf9cc2dc080479abffd9a5cb4fcf12eea2759898c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.3 MB (375313008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee92e4df31178121b908f977309aa653980c8ead4c00a6456d7ef802bbd01816`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:15:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:15:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:15:56 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:18:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:18:30 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Fri, 16 Jun 2023 02:19:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2ff6a4fd1fa354047c93ba8c3179967156162f27bd683aee1f6e52a480bcbe6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.7_7.tar.gz';          ;;        armhf|arm)          ESUM='5b0401199c7c9163b8395ebf25195ed395fec7b7ef7158c36302420cf993825a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.7_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cc25e74c0817cd4d943bba056b256b86e0e9148bf41d7600c5ec2e1eadb2e470';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.7_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='393f6348c6c0cb12699565cf23a7617fbfce973e6d47584a0920e99fbb1b1e3e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.7_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bb025133b96266f6415d5084bb9b260340a813968007f1d2d14690f20bd021ca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:19:05 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 05:26:45 GMT
ARG SOLR_VERSION=9.2.1
# Fri, 16 Jun 2023 05:26:45 GMT
ARG SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb
# Fri, 16 Jun 2023 05:26:46 GMT
ARG SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271
# Fri, 16 Jun 2023 05:26:46 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 16 Jun 2023 05:26:46 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 16 Jun 2023 05:26:46 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz
# Fri, 16 Jun 2023 05:26:46 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz
# Fri, 16 Jun 2023 05:26:46 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz
# Fri, 16 Jun 2023 05:27:05 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271 SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb SOLR_VERSION=9.2.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 16 Jun 2023 05:27:06 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 16 Jun 2023 05:27:06 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 16 Jun 2023 05:27:06 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 16 Jun 2023 05:27:06 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 16 Jun 2023 05:27:06 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 16 Jun 2023 05:27:06 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 16 Jun 2023 05:27:06 GMT
LABEL org.opencontainers.image.version=9.2.1
# Fri, 16 Jun 2023 05:27:07 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 16 Jun 2023 05:27:07 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 16 Jun 2023 05:27:07 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271 SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb SOLR_VERSION=9.2.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 16 Jun 2023 05:27:08 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271 SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb SOLR_VERSION=9.2.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 16 Jun 2023 05:27:08 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271 SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb SOLR_VERSION=9.2.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 16 Jun 2023 05:27:16 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271 SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb SOLR_VERSION=9.2.1
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 16 Jun 2023 05:27:16 GMT
VOLUME [/var/solr]
# Fri, 16 Jun 2023 05:27:17 GMT
EXPOSE 8983
# Fri, 16 Jun 2023 05:27:17 GMT
WORKDIR /opt/solr
# Fri, 16 Jun 2023 05:27:17 GMT
USER 8983
# Fri, 16 Jun 2023 05:27:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:27:17 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857412f02e8d49bb7e247b45ce86ce6378bd0bc5e8533e1fffa2a6e7a93aab46`  
		Last Modified: Fri, 16 Jun 2023 02:23:30 GMT  
		Size: 17.0 MB (17040964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90f618ea570e7708381040c3f1662a8ff625710ddd7b5e0145b46bdf5231985c`  
		Last Modified: Fri, 16 Jun 2023 02:24:16 GMT  
		Size: 47.0 MB (47006286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2665c89972dd3400540a4420904c1912a3990b0a3be38d49d50a94b9da26231`  
		Last Modified: Fri, 16 Jun 2023 02:24:10 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42b38db22e6b18b3bc85f4e165ec99d95cf616e24a46a16b202a4d250561d3c`  
		Last Modified: Fri, 16 Jun 2023 05:30:50 GMT  
		Size: 279.0 MB (278994099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb98ce87480dfd3e75ac21f048446ae8df10c8dedff32cd9f263d02d1a825bf8`  
		Last Modified: Fri, 16 Jun 2023 05:30:38 GMT  
		Size: 4.3 KB (4288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a37d4231e60e1d0dc230f2efc9d2560cdc8dedf9e4b250d0818da3cee7def5`  
		Last Modified: Fri, 16 Jun 2023 05:30:38 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8928bcc26c2ef972e3082782ab6af19d2073d8e99c35453e7442950937d4f2b`  
		Last Modified: Fri, 16 Jun 2023 05:30:38 GMT  
		Size: 8.3 KB (8268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a14db093f859ab0b789c47440b60c02aee9d6a13e83e9b650a7b142280b4452`  
		Last Modified: Fri, 16 Jun 2023 05:30:39 GMT  
		Size: 1.8 MB (1827683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:latest` - linux; arm variant v7

```console
$ docker pull solr@sha256:df5a4df27d6223472cdf39d015d0be71d2e3674169077c668259410ac9ed2f20
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.4 MB (369434561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d9b6bd34c3e1002a86e117f66e584a416854d27e7c66f806f1a01cf6d15fd8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 05 Jun 2023 16:59:35 GMT
ARG RELEASE
# Mon, 05 Jun 2023 16:59:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 16:59:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 16:59:35 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 16:59:40 GMT
ADD file:5425962ced738173a50965fc5cd95c79d0a319323df4a34e9da3f5037a5264c3 in / 
# Mon, 05 Jun 2023 16:59:40 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 01:25:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 01:25:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 01:25:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 01:28:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 01:28:03 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Fri, 16 Jun 2023 01:28:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2ff6a4fd1fa354047c93ba8c3179967156162f27bd683aee1f6e52a480bcbe6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.7_7.tar.gz';          ;;        armhf|arm)          ESUM='5b0401199c7c9163b8395ebf25195ed395fec7b7ef7158c36302420cf993825a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.7_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cc25e74c0817cd4d943bba056b256b86e0e9148bf41d7600c5ec2e1eadb2e470';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.7_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='393f6348c6c0cb12699565cf23a7617fbfce973e6d47584a0920e99fbb1b1e3e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.7_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bb025133b96266f6415d5084bb9b260340a813968007f1d2d14690f20bd021ca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 01:28:33 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 02:38:27 GMT
ARG SOLR_VERSION=9.2.1
# Fri, 16 Jun 2023 02:38:28 GMT
ARG SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb
# Fri, 16 Jun 2023 02:38:28 GMT
ARG SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271
# Fri, 16 Jun 2023 02:38:28 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 16 Jun 2023 02:38:28 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 16 Jun 2023 02:38:28 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz
# Fri, 16 Jun 2023 02:38:28 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz
# Fri, 16 Jun 2023 02:38:28 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz
# Fri, 16 Jun 2023 02:38:52 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271 SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb SOLR_VERSION=9.2.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 16 Jun 2023 02:38:54 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 16 Jun 2023 02:38:54 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 16 Jun 2023 02:38:54 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 16 Jun 2023 02:38:54 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 16 Jun 2023 02:38:54 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 16 Jun 2023 02:38:54 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 16 Jun 2023 02:38:55 GMT
LABEL org.opencontainers.image.version=9.2.1
# Fri, 16 Jun 2023 02:38:55 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 16 Jun 2023 02:38:55 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 16 Jun 2023 02:38:55 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271 SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb SOLR_VERSION=9.2.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 16 Jun 2023 02:38:56 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271 SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb SOLR_VERSION=9.2.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 16 Jun 2023 02:38:56 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271 SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb SOLR_VERSION=9.2.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 16 Jun 2023 02:39:05 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271 SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb SOLR_VERSION=9.2.1
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 16 Jun 2023 02:39:05 GMT
VOLUME [/var/solr]
# Fri, 16 Jun 2023 02:39:05 GMT
EXPOSE 8983
# Fri, 16 Jun 2023 02:39:05 GMT
WORKDIR /opt/solr
# Fri, 16 Jun 2023 02:39:05 GMT
USER 8983
# Fri, 16 Jun 2023 02:39:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jun 2023 02:39:06 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:de11f41b5c8ee0d3b259584977df4adb3e9b005f95756baecf491f70b498f301`  
		Last Modified: Wed, 07 Jun 2023 02:07:45 GMT  
		Size: 27.0 MB (27026252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88eb1b8897047cd0a4d969ca49bb4696512a41ef9d4466bc36e6bb42d97ca8dd`  
		Last Modified: Fri, 16 Jun 2023 01:31:49 GMT  
		Size: 17.2 MB (17168477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4e9b19cfde4210390e27af028b3821849f4637891e197e449641eb7824c5e1`  
		Last Modified: Fri, 16 Jun 2023 01:32:33 GMT  
		Size: 44.6 MB (44579970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69809a3884cff3cd2a14f35fede7e33256861cf01f1afb3f2fe52660b7fbfb72`  
		Last Modified: Fri, 16 Jun 2023 01:32:26 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15016717bbccbb8afaa8cd53f43070ec0fc4ccd1229c858a599c76179c0fee9`  
		Last Modified: Fri, 16 Jun 2023 02:42:49 GMT  
		Size: 279.0 MB (278994307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df6c3913894e2b72c13f2694b8975504ad21fcec95c266e2f9b3fe81c6c7846`  
		Last Modified: Fri, 16 Jun 2023 02:42:34 GMT  
		Size: 4.2 KB (4223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e043faaa195146204f1395ba9ffff82c7db8ad8bceb6342ba54add360a69a15c`  
		Last Modified: Fri, 16 Jun 2023 02:42:34 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a294eea0d8dce46694f985b5876d7480e52e3ab622133cca6771a36dcb330c`  
		Last Modified: Fri, 16 Jun 2023 02:42:34 GMT  
		Size: 8.3 KB (8265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32ce8d699bbfad8bd6eb33cb5bcbbe23ce1c33711b92eb2055125082aeda9d8`  
		Last Modified: Fri, 16 Jun 2023 02:42:35 GMT  
		Size: 1.7 MB (1652690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:latest` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:66509e3fc448ac1d4772e7d726c2cf22fe0d4967714e3c65afe9c65c4a495621
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.0 MB (374038205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd904f26d14316cf21764a5752c2ec1106c1a2bd920731c901a018585999f16d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 05 Jun 2023 17:11:17 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:11:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:11:17 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:11:19 GMT
ADD file:1043594b482384e967c94378b65ec4bc7a38190649a94f0325b7fb00be0a623e in / 
# Mon, 05 Jun 2023 17:11:19 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:45:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:47:57 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:47:57 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Fri, 16 Jun 2023 02:48:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2ff6a4fd1fa354047c93ba8c3179967156162f27bd683aee1f6e52a480bcbe6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.7_7.tar.gz';          ;;        armhf|arm)          ESUM='5b0401199c7c9163b8395ebf25195ed395fec7b7ef7158c36302420cf993825a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.7_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cc25e74c0817cd4d943bba056b256b86e0e9148bf41d7600c5ec2e1eadb2e470';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.7_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='393f6348c6c0cb12699565cf23a7617fbfce973e6d47584a0920e99fbb1b1e3e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.7_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bb025133b96266f6415d5084bb9b260340a813968007f1d2d14690f20bd021ca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:48:26 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 05:47:48 GMT
ARG SOLR_VERSION=9.2.1
# Fri, 16 Jun 2023 05:47:48 GMT
ARG SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb
# Fri, 16 Jun 2023 05:47:49 GMT
ARG SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271
# Fri, 16 Jun 2023 05:47:49 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 16 Jun 2023 05:47:49 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 16 Jun 2023 05:47:49 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz
# Fri, 16 Jun 2023 05:47:49 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz
# Fri, 16 Jun 2023 05:47:49 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz
# Fri, 16 Jun 2023 05:48:04 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271 SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb SOLR_VERSION=9.2.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 16 Jun 2023 05:48:06 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 16 Jun 2023 05:48:06 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 16 Jun 2023 05:48:06 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 16 Jun 2023 05:48:06 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 16 Jun 2023 05:48:06 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 16 Jun 2023 05:48:06 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 16 Jun 2023 05:48:06 GMT
LABEL org.opencontainers.image.version=9.2.1
# Fri, 16 Jun 2023 05:48:06 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 16 Jun 2023 05:48:06 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 16 Jun 2023 05:48:07 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271 SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb SOLR_VERSION=9.2.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 16 Jun 2023 05:48:07 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271 SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb SOLR_VERSION=9.2.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 16 Jun 2023 05:48:08 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271 SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb SOLR_VERSION=9.2.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 16 Jun 2023 05:48:16 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271 SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb SOLR_VERSION=9.2.1
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 16 Jun 2023 05:48:16 GMT
VOLUME [/var/solr]
# Fri, 16 Jun 2023 05:48:16 GMT
EXPOSE 8983
# Fri, 16 Jun 2023 05:48:16 GMT
WORKDIR /opt/solr
# Fri, 16 Jun 2023 05:48:16 GMT
USER 8983
# Fri, 16 Jun 2023 05:48:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jun 2023 05:48:16 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:a1df1d4a17c6a461a5967be8a40f1158e55e0ae4dc3b3b7ae64f57cae69eb7e7`  
		Last Modified: Wed, 07 Jun 2023 02:07:18 GMT  
		Size: 28.4 MB (28389201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5168066327b37e44f2a0ef7f788219bdbcd9013e4320cf4b9229ea9dfb73b561`  
		Last Modified: Fri, 16 Jun 2023 02:52:08 GMT  
		Size: 18.5 MB (18465563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78b269707ca01885483219b119ab6f03209c4c452696f1dcf105d191a7115cb`  
		Last Modified: Fri, 16 Jun 2023 02:52:47 GMT  
		Size: 46.5 MB (46488623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb861b98c25f139f6cf3783bb0c0c5a4810ad99eaba8cf8695eefe7f8614a8b`  
		Last Modified: Fri, 16 Jun 2023 02:52:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3400a3f980bb2b3adf154d3fc86f306788ac6cff76728fde865037e3ede88b68`  
		Last Modified: Fri, 16 Jun 2023 05:51:36 GMT  
		Size: 279.0 MB (278994703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11950a4bc9f97d203c1476552d153fcc683e3957621da8768cd3fa39ee02d0eb`  
		Last Modified: Fri, 16 Jun 2023 05:51:26 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042db7dc8c2d6e3b53376afc669becc9ca9910f7044388ce3d98ff880351321f`  
		Last Modified: Fri, 16 Jun 2023 05:51:26 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec7819b9a55bdc72dd442a462e31fbe1414cadd44f1bcd765716dd6b4e3c622`  
		Last Modified: Fri, 16 Jun 2023 05:51:26 GMT  
		Size: 8.3 KB (8269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da205b415c9da2bcf6f1d7532f914f0bd453728f8ec6beba5eb09cfd86cb27f`  
		Last Modified: Fri, 16 Jun 2023 05:51:27 GMT  
		Size: 1.7 MB (1687137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:latest` - linux; ppc64le

```console
$ docker pull solr@sha256:7237335d603e527c83ab9545e0865684521980f5c406a28d58969c7c6e58e70b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.7 MB (381748792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b61810d471dd4c39d87767e32a88170d6f0d0a3cf37eb7eb200614ba8e14db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 05 Jun 2023 17:01:00 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:01:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:01:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:01:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:01:03 GMT
ADD file:00c4f44b35b683caef54d5b8b0e0b1e68872f45eae17dd7543adaf6c54512447 in / 
# Mon, 05 Jun 2023 17:01:04 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:19:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 02:19:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 02:19:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:24:42 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 02:24:43 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Fri, 16 Jun 2023 02:25:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2ff6a4fd1fa354047c93ba8c3179967156162f27bd683aee1f6e52a480bcbe6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.7_7.tar.gz';          ;;        armhf|arm)          ESUM='5b0401199c7c9163b8395ebf25195ed395fec7b7ef7158c36302420cf993825a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.7_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cc25e74c0817cd4d943bba056b256b86e0e9148bf41d7600c5ec2e1eadb2e470';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.7_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='393f6348c6c0cb12699565cf23a7617fbfce973e6d47584a0920e99fbb1b1e3e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.7_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bb025133b96266f6415d5084bb9b260340a813968007f1d2d14690f20bd021ca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 02:25:43 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 16 Jun 2023 07:36:03 GMT
ARG SOLR_VERSION=9.2.1
# Fri, 16 Jun 2023 07:36:04 GMT
ARG SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb
# Fri, 16 Jun 2023 07:36:04 GMT
ARG SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271
# Fri, 16 Jun 2023 07:36:05 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 16 Jun 2023 07:36:05 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 16 Jun 2023 07:36:05 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz
# Fri, 16 Jun 2023 07:36:06 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz
# Fri, 16 Jun 2023 07:36:06 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz
# Fri, 16 Jun 2023 07:37:24 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271 SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb SOLR_VERSION=9.2.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 16 Jun 2023 07:37:29 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 16 Jun 2023 07:37:29 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 16 Jun 2023 07:37:30 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 16 Jun 2023 07:37:30 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 16 Jun 2023 07:37:31 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 16 Jun 2023 07:37:32 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 16 Jun 2023 07:37:35 GMT
LABEL org.opencontainers.image.version=9.2.1
# Fri, 16 Jun 2023 07:37:36 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 16 Jun 2023 07:37:37 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 16 Jun 2023 07:37:39 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271 SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb SOLR_VERSION=9.2.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 16 Jun 2023 07:37:41 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271 SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb SOLR_VERSION=9.2.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 16 Jun 2023 07:37:43 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271 SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb SOLR_VERSION=9.2.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 16 Jun 2023 07:38:00 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271 SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb SOLR_VERSION=9.2.1
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 16 Jun 2023 07:38:00 GMT
VOLUME [/var/solr]
# Fri, 16 Jun 2023 07:38:01 GMT
EXPOSE 8983
# Fri, 16 Jun 2023 07:38:01 GMT
WORKDIR /opt/solr
# Fri, 16 Jun 2023 07:38:02 GMT
USER 8983
# Fri, 16 Jun 2023 07:38:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jun 2023 07:38:03 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:a02dd69d9a8a1e6f4fc2ccb509fb8efd6014b00ff932a757d23b4b012a2bec49`  
		Last Modified: Fri, 16 Jun 2023 00:44:52 GMT  
		Size: 35.7 MB (35711397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67bd55325dd69030064f13098489df6ef8e45b2d52baffb366675c06f6e94418`  
		Last Modified: Fri, 16 Jun 2023 02:30:20 GMT  
		Size: 18.3 MB (18322826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef75c435e36e0d0cb9911afc443c4bf6c1769b56642390039838f6017497b2f`  
		Last Modified: Fri, 16 Jun 2023 02:31:24 GMT  
		Size: 46.9 MB (46872498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edff0610bd2e6e17f260f10d236a0fad32db564c59f810b5e30eaee37ef5faf8`  
		Last Modified: Fri, 16 Jun 2023 02:31:13 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d7ebdacee82ac6455d940b19d21bf659f1cf53c3aaa3f3e1577135b8802d3e`  
		Last Modified: Fri, 16 Jun 2023 07:43:45 GMT  
		Size: 279.0 MB (278994934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64708f76d121ff3c1262875272f841e9c3bb2244f1d305672fed751d7c638df1`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 4.3 KB (4297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495b3eb13c2abbf80d9c705cdb460f2f939de60c92c610848a2c4defab47dd11`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8695e9bc13470e29cd835a938319952511edd7c991fecadf3ed9d64c89a727b`  
		Last Modified: Fri, 16 Jun 2023 07:43:24 GMT  
		Size: 8.3 KB (8273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3227aa649395d114eef9c32c931462d8a75c9fe23aa39081891ddc6dc3c31c74`  
		Last Modified: Fri, 16 Jun 2023 07:43:25 GMT  
		Size: 1.8 MB (1834188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:latest` - linux; s390x

```console
$ docker pull solr@sha256:201f05da38804aea9bdedbdd73d128ced6e4f5fd51aa8017f2108e96242306be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.0 MB (370019627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d977dfce4e3f77c37fa0fa1826b1f3a148d03c6bc6180e1a8b4049050a7c49a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Mon, 05 Jun 2023 17:01:02 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:01:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:01:04 GMT
ADD file:2d2f31ec110b9e7ec21a9d4824a430acdaabf0b4e9c1cdd337438992859b57ae in / 
# Mon, 05 Jun 2023 17:01:04 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 18:19:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 18:19:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 18:19:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 18:21:41 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Jun 2023 18:21:42 GMT
ENV JAVA_VERSION=jdk-17.0.7+7
# Fri, 16 Jun 2023 18:22:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='2ff6a4fd1fa354047c93ba8c3179967156162f27bd683aee1f6e52a480bcbe6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.7_7.tar.gz';          ;;        armhf|arm)          ESUM='5b0401199c7c9163b8395ebf25195ed395fec7b7ef7158c36302420cf993825a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_arm_linux_hotspot_17.0.7_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='cc25e74c0817cd4d943bba056b256b86e0e9148bf41d7600c5ec2e1eadb2e470';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.7_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='393f6348c6c0cb12699565cf23a7617fbfce973e6d47584a0920e99fbb1b1e3e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_s390x_linux_hotspot_17.0.7_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='bb025133b96266f6415d5084bb9b260340a813968007f1d2d14690f20bd021ca';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.7%2B7/OpenJDK17U-jre_x64_linux_hotspot_17.0.7_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 16 Jun 2023 18:22:24 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 17 Jun 2023 10:39:39 GMT
ARG SOLR_VERSION=9.2.1
# Sat, 17 Jun 2023 10:39:40 GMT
ARG SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb
# Sat, 17 Jun 2023 10:39:40 GMT
ARG SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271
# Sat, 17 Jun 2023 10:39:40 GMT
ARG SOLR_DOWNLOAD_URL
# Sat, 17 Jun 2023 10:39:40 GMT
ARG SOLR_DOWNLOAD_SERVER
# Sat, 17 Jun 2023 10:39:40 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz
# Sat, 17 Jun 2023 10:39:40 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz
# Sat, 17 Jun 2023 10:39:40 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz
# Sat, 17 Jun 2023 10:40:07 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271 SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb SOLR_VERSION=9.2.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Sat, 17 Jun 2023 10:40:13 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 17 Jun 2023 10:40:13 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Sat, 17 Jun 2023 10:40:13 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 17 Jun 2023 10:40:13 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 17 Jun 2023 10:40:13 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 17 Jun 2023 10:40:14 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 17 Jun 2023 10:40:14 GMT
LABEL org.opencontainers.image.version=9.2.1
# Sat, 17 Jun 2023 10:40:14 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 17 Jun 2023 10:40:14 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Sat, 17 Jun 2023 10:40:14 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271 SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb SOLR_VERSION=9.2.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Sat, 17 Jun 2023 10:40:15 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271 SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb SOLR_VERSION=9.2.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Sat, 17 Jun 2023 10:40:16 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271 SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb SOLR_VERSION=9.2.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Sat, 17 Jun 2023 10:40:22 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.1/solr-9.2.1.tgz SOLR_KEYS=FDB3D11D716BB32ACF8C93AB919B21537AA80271 SOLR_SHA512=1ff1bd22255b0ae5a1ade1d03596c1f35d4fa69fa1a16e823eaa554b30ba1311f031af6e1f95a94dbdd3a1dbf308eeb068e7303b74f83584a8bb443505078cbb SOLR_VERSION=9.2.1
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Sat, 17 Jun 2023 10:40:22 GMT
VOLUME [/var/solr]
# Sat, 17 Jun 2023 10:40:22 GMT
EXPOSE 8983
# Sat, 17 Jun 2023 10:40:22 GMT
WORKDIR /opt/solr
# Sat, 17 Jun 2023 10:40:22 GMT
USER 8983
# Sat, 17 Jun 2023 10:40:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 17 Jun 2023 10:40:22 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:fab1a8aa44b00432834b7776a76fd4149ec2fee2336a3521bd5435428df7edc9`  
		Last Modified: Fri, 16 Jun 2023 18:23:35 GMT  
		Size: 28.6 MB (28644581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb41ab341d8b92d0df369d3c8554802dadb82862486ac5ae0630bdde792bcf6`  
		Last Modified: Fri, 16 Jun 2023 18:24:39 GMT  
		Size: 16.8 MB (16818357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801abaf6c0957718415df755b83d7b26e7ba64b9c41a3faaff7bc5e9fadfa95b`  
		Last Modified: Fri, 16 Jun 2023 18:25:17 GMT  
		Size: 43.8 MB (43774532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acdee84f73591a4adbc460ac7c7e5cc539c15932bd06ea8a5c2f7017d004bf5f`  
		Last Modified: Fri, 16 Jun 2023 18:25:11 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a833646dc5e347ebb401b6b9d2aabfd650a922b75a3bad6a41a8b4adf15568c7`  
		Last Modified: Sat, 17 Jun 2023 10:52:16 GMT  
		Size: 279.0 MB (278994527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897219a9eae0deb0995270461e7fef4b57ac7a53769f19b6eefcb69633280a4`  
		Last Modified: Sat, 17 Jun 2023 10:52:05 GMT  
		Size: 4.3 KB (4327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ae0aefe6884be2b7aa9915bde45ade27e551510ce88820566a8b3fd668415f`  
		Last Modified: Sat, 17 Jun 2023 10:52:05 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8928ff8f8ab194685d283fa3264a12bd1e76995cf2dd29683955b68fdcda6c`  
		Last Modified: Sat, 17 Jun 2023 10:52:05 GMT  
		Size: 8.3 KB (8265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea69f2981cb3d476c272fc16b291f0bfb578777a70190f9ae95123591d2711cb`  
		Last Modified: Sat, 17 Jun 2023 10:52:06 GMT  
		Size: 1.8 MB (1774657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

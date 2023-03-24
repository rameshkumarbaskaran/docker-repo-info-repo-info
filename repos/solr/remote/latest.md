## `solr:latest`

```console
$ docker pull solr@sha256:6a63019e5694591e2d1c53d56cdcba819235adbd1e85d91f0f82cc7562ea1ff2
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
$ docker pull solr@sha256:cbee52e4b6a1e30d450e8ca19402c3bc15d4d8e8a75ca8501cb0f7f642cc76ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.9 MB (374859971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d43c32e8ee6e715af99f55ba48e134125af6eadbc175932523f25a1070ce4f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:44:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:44:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:46:48 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:46:48 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 02:47:21 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:47:22 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_VERSION=9.2.0
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:20:06 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:20:07 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:20:52 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.version=9.2.0
# Fri, 24 Mar 2023 20:20:53 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 24 Mar 2023 20:20:53 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 24 Mar 2023 20:20:54 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 24 Mar 2023 20:20:55 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 24 Mar 2023 20:20:55 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 24 Mar 2023 20:21:03 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Mar 2023 20:21:03 GMT
VOLUME [/var/solr]
# Fri, 24 Mar 2023 20:21:03 GMT
EXPOSE 8983
# Fri, 24 Mar 2023 20:21:03 GMT
WORKDIR /opt/solr
# Fri, 24 Mar 2023 20:21:04 GMT
USER 8983
# Fri, 24 Mar 2023 20:21:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Mar 2023 20:21:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a182a611d05b01879f065473c49fb968b8d30312f931350ea07af1c46aa8b4f9`  
		Last Modified: Thu, 16 Mar 2023 02:53:08 GMT  
		Size: 17.0 MB (16975402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb51f9f63778bb9fb97f2cb054b54dfc5098aba2931664a12930c35cf464ca6`  
		Last Modified: Thu, 16 Mar 2023 02:54:00 GMT  
		Size: 46.9 MB (46935467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1365afd8cae0153f1c2bfcf8a4c9b78f2e6e0f18431b0460c63c1fede7507fee`  
		Last Modified: Thu, 16 Mar 2023 02:53:53 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b70190cd6e82c4ac613c9f0f9bf4e42155528b445617672bcd7a211b2a2104`  
		Last Modified: Fri, 24 Mar 2023 20:21:43 GMT  
		Size: 278.7 MB (278678830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c984f04f09ad32d618a63f426eb4127534ca414910aa8b56da2355a3bcf17c17`  
		Last Modified: Fri, 24 Mar 2023 20:21:31 GMT  
		Size: 4.3 KB (4295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888b9068f218433d417da0cd83cca3863ad2cbea9bab37c09fc52a63fab6206e`  
		Last Modified: Fri, 24 Mar 2023 20:21:31 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1599d0444630b3ac11f8d61742ff79acaaec1b9cfcca5e176b131ef54c22bd`  
		Last Modified: Fri, 24 Mar 2023 20:21:32 GMT  
		Size: 8.3 KB (8264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbc52fa8b34cbd17b27c7c562e83344a928724a395e74a740d6bcfbd0aca1e8`  
		Last Modified: Fri, 24 Mar 2023 20:21:32 GMT  
		Size: 1.8 MB (1827370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:latest` - linux; arm variant v7

```console
$ docker pull solr@sha256:7ce35f5dfe8a54b79e4886b38ee7bbae1768c5080b38dd88007711f1a730ca97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.0 MB (368994236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0c33c02e827728f7408559ce07896fbcd7ef42a58bd47bd0c340d122ef7c70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:31:41 GMT
ADD file:e9c3ac290fb81ae2e78de99052d776396ee3aff05e1a66fd2dccb01d7de9bb45 in / 
# Wed, 08 Mar 2023 04:31:42 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:46:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:46:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:46:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:49:36 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:49:36 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 02:50:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:50:09 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 24 Mar 2023 21:14:57 GMT
ARG SOLR_VERSION=9.2.0
# Fri, 24 Mar 2023 21:14:57 GMT
ARG SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 21:14:58 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 21:15:46 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 24 Mar 2023 21:15:47 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 24 Mar 2023 21:15:47 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 24 Mar 2023 21:15:47 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 24 Mar 2023 21:15:47 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 24 Mar 2023 21:15:48 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 24 Mar 2023 21:15:48 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 24 Mar 2023 21:15:48 GMT
LABEL org.opencontainers.image.version=9.2.0
# Fri, 24 Mar 2023 21:15:48 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 24 Mar 2023 21:15:48 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 24 Mar 2023 21:15:49 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 24 Mar 2023 21:15:49 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 24 Mar 2023 21:15:50 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 24 Mar 2023 21:15:59 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Mar 2023 21:16:00 GMT
VOLUME [/var/solr]
# Fri, 24 Mar 2023 21:16:00 GMT
EXPOSE 8983
# Fri, 24 Mar 2023 21:16:00 GMT
WORKDIR /opt/solr
# Fri, 24 Mar 2023 21:16:00 GMT
USER 8983
# Fri, 24 Mar 2023 21:16:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Mar 2023 21:16:00 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:cba1fa3bcdf4f746dcf5b8f86874cee4a6eff75dd5c5cd29e4c912574b12a1c6`  
		Last Modified: Thu, 09 Mar 2023 04:41:14 GMT  
		Size: 27.0 MB (27025397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85169cff2ee4bc04fcfaf94a937435e69eb27ca38bf1dcbd04593cccacf0d702`  
		Last Modified: Thu, 16 Mar 2023 02:56:32 GMT  
		Size: 17.1 MB (17093778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be72bd479c96978965e7a3ad3512673e6ca3b26714713ca967a807e2c0bcdb7e`  
		Last Modified: Thu, 16 Mar 2023 02:57:28 GMT  
		Size: 44.5 MB (44528811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5725cdfe807b737e733d3d3a443ffd37aef0141ba7a33fb98b334c479486085`  
		Last Modified: Thu, 16 Mar 2023 02:57:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f40c0125b4d5835619a97a6e8aa526c71d7c68b45f248b530ebb09d2d1570c6`  
		Last Modified: Fri, 24 Mar 2023 21:16:36 GMT  
		Size: 278.7 MB (278680032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c884c5595959c80781c31e89baa334da69c61145587cecf73ae8777f044fbb01`  
		Last Modified: Fri, 24 Mar 2023 21:16:20 GMT  
		Size: 4.2 KB (4224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:387e1ea0fbb6ae2834c227fdf0661b61a1dbe74918fddc3fb294bb4dbbbce8b9`  
		Last Modified: Fri, 24 Mar 2023 21:16:20 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4b5c915fbddf45760ab4310f38f8bce027f6be8d21539defc6c49238e0d1d9`  
		Last Modified: Fri, 24 Mar 2023 21:16:20 GMT  
		Size: 8.3 KB (8259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c5e2d209b82002244ea91d52f9d395d4e38adde0830ca8a1a014fd6a0fb50b`  
		Last Modified: Fri, 24 Mar 2023 21:16:21 GMT  
		Size: 1.7 MB (1653357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:latest` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:58619b9500a6637702a27985f2cf8b17cb13dae6c2673f3abaa9a1bd824277ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.6 MB (373587696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f72e1df4e02c02f553d7d54dd64951829dbdd59095775a6634ddce70eadc8a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:32:38 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:32:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:32:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:32:39 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:32:40 GMT
ADD file:79b36308bc382d9cae7197b4cecc21430f4e8f3e8bec3547d0f00bcff7681e60 in / 
# Wed, 08 Mar 2023 04:32:41 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:52:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 01:52:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 01:52:26 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 01:55:03 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:55:04 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 01:55:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 01:55:30 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_VERSION=9.2.0
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 24 Mar 2023 20:47:30 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:47:31 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:47:31 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:48:14 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 24 Mar 2023 20:48:16 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 24 Mar 2023 20:48:17 GMT
LABEL org.opencontainers.image.version=9.2.0
# Fri, 24 Mar 2023 20:48:17 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 24 Mar 2023 20:48:17 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 24 Mar 2023 20:48:17 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 24 Mar 2023 20:48:18 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 24 Mar 2023 20:48:18 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 24 Mar 2023 20:48:27 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Mar 2023 20:48:27 GMT
VOLUME [/var/solr]
# Fri, 24 Mar 2023 20:48:27 GMT
EXPOSE 8983
# Fri, 24 Mar 2023 20:48:27 GMT
WORKDIR /opt/solr
# Fri, 24 Mar 2023 20:48:28 GMT
USER 8983
# Fri, 24 Mar 2023 20:48:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Mar 2023 20:48:28 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:b2ddfd337773edbf5766dce2fdbeef139ba8c42724e29eda157c84e9f97f1bce`  
		Last Modified: Wed, 08 Mar 2023 12:37:24 GMT  
		Size: 28.4 MB (28387554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40b70fd7935308ad0e072e7e06ec8c3abdc59beae70ca716dcd04e971680865`  
		Last Modified: Thu, 16 Mar 2023 02:00:42 GMT  
		Size: 18.4 MB (18400790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33dd5efa5ce73b25dc0236fcd408527b63e42c87e6da9672a356731004b8949`  
		Last Modified: Thu, 16 Mar 2023 02:01:25 GMT  
		Size: 46.4 MB (46421360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ce9280353ea6c4511dc5378e2f0f4742d499bf6df15c8d10804513c8c5115a`  
		Last Modified: Thu, 16 Mar 2023 02:01:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab85ed965ce21582560c60a815ae59ae9cf0fcb5c9270ba02dfc5ca1c135b44f`  
		Last Modified: Fri, 24 Mar 2023 20:49:04 GMT  
		Size: 278.7 MB (278678702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a47faea25001b6a9178cab60304409e81d636878232dda7e76d519e7490bbc9`  
		Last Modified: Fri, 24 Mar 2023 20:48:54 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7792e9b554723df7cdd9593ee715d8fe16cfec71a28c58e0b01e2534e7f2c8`  
		Last Modified: Fri, 24 Mar 2023 20:48:54 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9435de9f76e1e09e2078c456e20cd6a83a757671ecc43398fed205b323cb3c6b`  
		Last Modified: Fri, 24 Mar 2023 20:48:54 GMT  
		Size: 8.3 KB (8261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fc7a7f4116bfd1b88180e25c33fa7c4d571df7caad6ffebbec7786b32b2738`  
		Last Modified: Fri, 24 Mar 2023 20:48:54 GMT  
		Size: 1.7 MB (1686320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:latest` - linux; ppc64le

```console
$ docker pull solr@sha256:f10e0c22e5adec6e85249f7eac5f7a5f930872dbd32a9cd7c770ec7ab6077b61
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.3 MB (381276492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08713b2a6558c371eb5008de184f2ae763ef7c3a322e2d740c9665f599eb2e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:16 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:20 GMT
ADD file:d7434a52d8d8aa6288e788f6fe7e156f0e11bf9b8275efaf70aab0bfc4d919cf in / 
# Wed, 08 Mar 2023 04:39:20 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 03:57:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 03:57:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 03:57:35 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 04:03:27 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 04:03:28 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 04:04:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 04:04:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 24 Mar 2023 20:16:53 GMT
ARG SOLR_VERSION=9.2.0
# Fri, 24 Mar 2023 20:16:53 GMT
ARG SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665
# Fri, 24 Mar 2023 20:16:53 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 24 Mar 2023 20:16:53 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 24 Mar 2023 20:16:54 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 24 Mar 2023 20:16:54 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:16:54 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:16:55 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:18:15 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 24 Mar 2023 20:18:18 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 24 Mar 2023 20:18:19 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 24 Mar 2023 20:18:19 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 24 Mar 2023 20:18:19 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 24 Mar 2023 20:18:20 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 24 Mar 2023 20:18:20 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 24 Mar 2023 20:18:20 GMT
LABEL org.opencontainers.image.version=9.2.0
# Fri, 24 Mar 2023 20:18:21 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 24 Mar 2023 20:18:21 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 24 Mar 2023 20:18:22 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 24 Mar 2023 20:18:24 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 24 Mar 2023 20:18:25 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 24 Mar 2023 20:18:40 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Mar 2023 20:18:41 GMT
VOLUME [/var/solr]
# Fri, 24 Mar 2023 20:18:41 GMT
EXPOSE 8983
# Fri, 24 Mar 2023 20:18:41 GMT
WORKDIR /opt/solr
# Fri, 24 Mar 2023 20:18:41 GMT
USER 8983
# Fri, 24 Mar 2023 20:18:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Mar 2023 20:18:42 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:deffc758660db3b0ee7a1f211d720633f06f27ab1e4c31db4caf8c27f4a80eeb`  
		Last Modified: Thu, 16 Mar 2023 02:22:27 GMT  
		Size: 35.7 MB (35711728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c06c33e4689e5957d961321ac18da32bea369d2eccc9173c9ad8b517f802ea`  
		Last Modified: Thu, 16 Mar 2023 04:14:09 GMT  
		Size: 18.3 MB (18257665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75be9792a67101a27b125eb6a0e465b760b4302cd2fbf3cf19338303bcfe803`  
		Last Modified: Thu, 16 Mar 2023 04:15:24 GMT  
		Size: 46.8 MB (46780948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba3f99059088b7aca45113a2e84d92786ffffd7b3920e17bc78082f1ca41023`  
		Last Modified: Thu, 16 Mar 2023 04:15:12 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a80e5b79ed57a03fbca62529db243f85c92ae5df2321c4e9f1224711e54a0d8`  
		Last Modified: Fri, 24 Mar 2023 20:19:29 GMT  
		Size: 278.7 MB (278679501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a83b0eea3048a8cc5ee14c0ed706cd75212e6513827c6e50ee8514b3a37ffa`  
		Last Modified: Fri, 24 Mar 2023 20:19:06 GMT  
		Size: 4.3 KB (4297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfda90d0edd877ecc2717bf59c6b25f8810ed05202ab28ba588f60de2cc3332e`  
		Last Modified: Fri, 24 Mar 2023 20:19:06 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffae90319602b89f29babd93a389ad3dcb0acd2637266cdb4f1e0e4b02309a2`  
		Last Modified: Fri, 24 Mar 2023 20:19:06 GMT  
		Size: 8.3 KB (8264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7a5d7ac7a4e26a6795ad596e099b124de0249d7a8cd31eff56a0786195d720`  
		Last Modified: Fri, 24 Mar 2023 20:19:07 GMT  
		Size: 1.8 MB (1833711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:latest` - linux; s390x

```console
$ docker pull solr@sha256:55d3908647c17e61e6cc73ac71deba6d9ab2a161bd4aa7b6ea15c7a7a75fab5c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.6 MB (369606057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1685dca8b24c2c5e320e5a7ef4c2bb2431ea293974475f5458fee07495a73e61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:39:24 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:39:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:39:24 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:39:26 GMT
ADD file:630f9865d3d4fd4294d45cac7cbaea83fb549c2e563de454348da964d19fbbba in / 
# Wed, 08 Mar 2023 04:39:26 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:06:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:06:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:06:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:07:58 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:07:59 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 02:08:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:08:41 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 24 Mar 2023 20:42:43 GMT
ARG SOLR_VERSION=9.2.0
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_DOWNLOAD_URL
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_DOWNLOAD_SERVER
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:42:44 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz
# Fri, 24 Mar 2023 20:43:15 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Fri, 24 Mar 2023 20:43:19 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Fri, 24 Mar 2023 20:43:19 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Fri, 24 Mar 2023 20:43:19 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Fri, 24 Mar 2023 20:43:20 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Fri, 24 Mar 2023 20:43:20 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Fri, 24 Mar 2023 20:43:20 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Fri, 24 Mar 2023 20:43:20 GMT
LABEL org.opencontainers.image.version=9.2.0
# Fri, 24 Mar 2023 20:43:20 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Fri, 24 Mar 2023 20:43:20 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Fri, 24 Mar 2023 20:43:21 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Fri, 24 Mar 2023 20:43:21 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Fri, 24 Mar 2023 20:43:22 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Fri, 24 Mar 2023 20:43:27 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.2.0/solr-9.2.0.tgz SOLR_KEYS=50E3EE1C91C7E0CB4DFB007B369424FC98F3F6EC SOLR_SHA512=f10c5e15a52882501bc29af11855066238c798658a21c8ccf780dcbdd269a1534a2d06e47f743a2c6331d4e45ab9c976cf7099337422698c4418c6373d284665 SOLR_VERSION=9.2.0
RUN set -ex;     apt-get update;     apt-get -y install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Fri, 24 Mar 2023 20:43:27 GMT
VOLUME [/var/solr]
# Fri, 24 Mar 2023 20:43:27 GMT
EXPOSE 8983
# Fri, 24 Mar 2023 20:43:27 GMT
WORKDIR /opt/solr
# Fri, 24 Mar 2023 20:43:28 GMT
USER 8983
# Fri, 24 Mar 2023 20:43:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Mar 2023 20:43:28 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:2c7366af510b72cc0b3456fb93cfa0bfc76f7d383db5cb315967e7b1ce2e0c42`  
		Last Modified: Thu, 16 Mar 2023 02:02:40 GMT  
		Size: 28.6 MB (28647599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d28ae42a862e9773a02317b5a0eeb71ddfe3a887bb001c8f23a2786c926287`  
		Last Modified: Thu, 16 Mar 2023 02:13:35 GMT  
		Size: 16.8 MB (16753284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f6bfb39a3fef3f50b4d32c5f857a5b18f142a97de79cf264830c8ca2b9864f7`  
		Last Modified: Thu, 16 Mar 2023 02:14:17 GMT  
		Size: 43.7 MB (43738850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d39319012144c92bc4367a44b2f3e4e953b589c17b4ca366d17c8743bff813f`  
		Last Modified: Thu, 16 Mar 2023 02:14:11 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f074327dc8f7e760db6a5b895eb86f852bfc333785586ee10413da37f3f222`  
		Last Modified: Fri, 24 Mar 2023 20:44:10 GMT  
		Size: 278.7 MB (278679125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b051ae3be65d0725f3676e0baa40a2410ad18f0aff69131fa9715c782378cb77`  
		Last Modified: Fri, 24 Mar 2023 20:43:59 GMT  
		Size: 4.3 KB (4330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0557baee179cb29c3fd717a2a7bb1914e6f0113559f232f327cda5d986fd9a91`  
		Last Modified: Fri, 24 Mar 2023 20:43:59 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd59caab82c0a6e67e3eeed26458e15e132ad27eb419aa32240ac3ac08575f5e`  
		Last Modified: Fri, 24 Mar 2023 20:43:59 GMT  
		Size: 8.3 KB (8259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89595dcc22b7df58249dbec6b0679a7aa1651e536af2a463aa9d3226f9acf21d`  
		Last Modified: Fri, 24 Mar 2023 20:43:59 GMT  
		Size: 1.8 MB (1774235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

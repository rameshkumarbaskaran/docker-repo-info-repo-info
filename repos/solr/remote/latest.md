## `solr:latest`

```console
$ docker pull solr@sha256:1da4855c6a3ccac1216935541e5c3281a02a249b80ba1fe0945c7553c26bbd14
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
$ docker pull solr@sha256:87c2c91166b2effd7b5c252d06181f1e89874156003048505800ab3f26dce775
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.2 MB (323206815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d5157911afde46379c02997af2aa4fac83892ab68a6bfed5e0779f98fca7591`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:31:43 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:31:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:31:43 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:31:46 GMT
ADD file:99d501af7a191308f8fe3dc3f33c63bd8b54fb749d061b1a901c423b85f8cec2 in / 
# Wed, 08 Mar 2023 04:31:46 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:45:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:45:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:45:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:48:47 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:48:47 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 02:50:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:50:01 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_VERSION=9.1.1
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 04:43:57 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 04:44:24 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 16 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=9.1.1
# Thu, 16 Mar 2023 04:44:26 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Mar 2023 04:44:26 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 16 Mar 2023 04:44:26 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Mar 2023 04:44:27 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 16 Mar 2023 04:44:27 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 16 Mar 2023 04:44:36 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 16 Mar 2023 04:44:36 GMT
VOLUME [/var/solr]
# Thu, 16 Mar 2023 04:44:36 GMT
EXPOSE 8983
# Thu, 16 Mar 2023 04:44:36 GMT
WORKDIR /opt/solr
# Thu, 16 Mar 2023 04:44:36 GMT
USER 8983
# Thu, 16 Mar 2023 04:44:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 04:44:36 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:5806a4b978689b82c0b1e370978a89d1fb81519414294a062ee8cdaae68d4cf9`  
		Last Modified: Thu, 09 Mar 2023 05:45:04 GMT  
		Size: 24.6 MB (24586482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1244137e4b88ca1866cf46370a384651ad01ecf13089022ced8c41a497b37663`  
		Last Modified: Thu, 16 Mar 2023 02:55:57 GMT  
		Size: 19.5 MB (19462442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bc0431536f0b89ee088a790995dd293ec25d3688eb9ca73359b82336dd8768`  
		Last Modified: Thu, 16 Mar 2023 02:57:05 GMT  
		Size: 44.5 MB (44529856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbabb516d40e0733a3335db3a801c1d210be0e2c9afd8adfd32db5c4cd9d518c`  
		Last Modified: Thu, 16 Mar 2023 02:56:58 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162837bfbbd64039ee4257e98c01d2ee735e529ba6c3db116879af03d10394ff`  
		Last Modified: Thu, 16 Mar 2023 04:47:30 GMT  
		Size: 233.2 MB (233220701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3741ea3b9c8f232fc4341c907a62fd01ffbdb1aa6d876d0cd2b00952d9dc4f27`  
		Last Modified: Thu, 16 Mar 2023 04:47:17 GMT  
		Size: 4.2 KB (4224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9d674ecb316d5958afe3ed25d77276f9b318841fa534a99bc3f07a4458004b`  
		Last Modified: Thu, 16 Mar 2023 04:47:17 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79817a7b907cfac994784d46ffb2efba1ca1bbde59ab25736bf121ff6cf7d16`  
		Last Modified: Thu, 16 Mar 2023 04:47:17 GMT  
		Size: 8.1 KB (8088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cd4541998525c86de76ce4b4e78a588dbcaba6f0de0c85d2ab715c6cc2250e`  
		Last Modified: Thu, 16 Mar 2023 04:47:18 GMT  
		Size: 1.4 MB (1394644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:latest` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:5fb2c69ebadcdc76017fc3a76326d24b45e0e57bcc239fc3a1c88f37f2206618
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.6 MB (329617407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a621b7f499b8a7e163383c98308d68a3ca9118674c4ff5be9134373854336693`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:34:20 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:34:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:34:20 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:34:24 GMT
ADD file:e73d5d005a3ba2c2fb3d8585a1f19daf5ea9ed75af5a2f97b1cc6f7f03db0cdc in / 
# Wed, 08 Mar 2023 04:34:24 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 01:51:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 01:51:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 01:51:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 01:54:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 01:54:31 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 01:55:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 01:55:24 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 06:14:33 GMT
ARG SOLR_VERSION=9.1.1
# Thu, 16 Mar 2023 06:14:33 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Thu, 16 Mar 2023 06:14:33 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Thu, 16 Mar 2023 06:14:34 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Mar 2023 06:14:34 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Mar 2023 06:14:34 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 06:14:34 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 06:14:34 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 06:14:52 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.version=9.1.1
# Thu, 16 Mar 2023 06:14:54 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Mar 2023 06:14:54 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 16 Mar 2023 06:14:55 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Mar 2023 06:14:55 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 16 Mar 2023 06:14:56 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 16 Mar 2023 06:15:03 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 16 Mar 2023 06:15:03 GMT
VOLUME [/var/solr]
# Thu, 16 Mar 2023 06:15:03 GMT
EXPOSE 8983
# Thu, 16 Mar 2023 06:15:03 GMT
WORKDIR /opt/solr
# Thu, 16 Mar 2023 06:15:03 GMT
USER 8983
# Thu, 16 Mar 2023 06:15:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 06:15:04 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:0c68957c744181d1b5cae80a96971c651cec74faeade53191985b92abff361da`  
		Last Modified: Wed, 08 Mar 2023 20:37:17 GMT  
		Size: 27.2 MB (27196161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f091a26bf16cf9bb9b5741a2f8b70047ee293b3a06b86283bea82ea46a9343a2`  
		Last Modified: Thu, 16 Mar 2023 02:00:21 GMT  
		Size: 20.8 MB (20810964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b693cb82e58b3095ebe84d13ae1a3782dd356f500a91d5a61a47e8235d6e2a67`  
		Last Modified: Thu, 16 Mar 2023 02:01:11 GMT  
		Size: 46.4 MB (46422408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022d34498a6f57f8c837ca795570cb62efb66090dab255070ba11325965a0200`  
		Last Modified: Thu, 16 Mar 2023 02:01:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0484642c6ee51824c667f3e27f52270960e3c92c69bc7bfa7ab2f782763fddbd`  
		Last Modified: Thu, 16 Mar 2023 06:17:19 GMT  
		Size: 233.7 MB (233731740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d5eb156f2c791d6c94fa684d3c306e30c0060b7092c019d543a6d1852a61ea`  
		Last Modified: Thu, 16 Mar 2023 06:17:10 GMT  
		Size: 4.3 KB (4328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e44d81a875819e3b33e6276257dfa34ff3fee5f4902c09c68a9a3947261064`  
		Last Modified: Thu, 16 Mar 2023 06:17:10 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af30bf8591fec4083df823499a619bb2721cd6706e16b24f875198b29d551d3`  
		Last Modified: Thu, 16 Mar 2023 06:17:10 GMT  
		Size: 8.1 KB (8086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab9e27d15fb1977ad5d628a5a3a00c2e7654d73d672edcd6fab2e1f282fe9c3`  
		Last Modified: Thu, 16 Mar 2023 06:17:11 GMT  
		Size: 1.4 MB (1443341 bytes)  
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
$ docker pull solr@sha256:73625ae96b7e71de7afb0658a6b5cc2116346256ff352f7e8416cc067e860a17
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.4 MB (325448244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946e1741c47b664fa12a4e656c2c38b91f025153a0dd9e1ec311247b5e91dace`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Wed, 08 Mar 2023 04:41:58 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:41:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:41:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:41:58 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 08 Mar 2023 04:42:00 GMT
ADD file:4463dafd3352de8c5ff87090e2f30be9bdffc3fa9d84e27b13e2364d856f82e9 in / 
# Wed, 08 Mar 2023 04:42:00 GMT
CMD ["/bin/bash"]
# Thu, 16 Mar 2023 02:05:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Mar 2023 02:05:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Mar 2023 02:05:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 16 Mar 2023 02:07:29 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 16 Mar 2023 02:07:30 GMT
ENV JAVA_VERSION=jdk-17.0.6+10
# Thu, 16 Mar 2023 02:08:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3797815cb853616b6415e1b8875cda4eaa004887561ea4ea2090d726b8d8582f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.6_10.tar.gz';          ;;        armhf|arm)          ESUM='bf7ef7ba477dc278f913e64174e76be9ae7f014c767352eae83b3f9581494fce';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_arm_linux_hotspot_17.0.6_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f11b86bfd7fa4d7a0d05040ea235102296f03eaf064253f76d7ab94baa0352e3';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.6_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='21a7156a29e7921bc7c6eadecb8ee4ac7161921cea85b75b61f0376f9c725caa';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_s390x_linux_hotspot_17.0.6_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='fe669935609086e76cb0b829e92808766cbf8cb7bda57a76b47813b08584bfd2';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.6%2B10/OpenJDK17U-jre_x64_linux_hotspot_17.0.6_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 16 Mar 2023 02:08:28 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 16 Mar 2023 19:06:16 GMT
ARG SOLR_VERSION=9.1.1
# Thu, 16 Mar 2023 19:06:16 GMT
ARG SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f
# Thu, 16 Mar 2023 19:06:16 GMT
ARG SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763
# Thu, 16 Mar 2023 19:06:16 GMT
ARG SOLR_DOWNLOAD_URL
# Thu, 16 Mar 2023 19:06:16 GMT
ARG SOLR_DOWNLOAD_SERVER
# Thu, 16 Mar 2023 19:06:16 GMT
ARG SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 19:06:16 GMT
ARG SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 19:06:17 GMT
ARG SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz
# Thu, 16 Mar 2023 19:06:36 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   apt-get update;   apt-get -y install wget gpg dirmngr;   rm -rf /var/lib/apt/lists/*;   export GNUPGHOME="/tmp/gnupg_home";   mkdir -p "$GNUPGHOME";   chmod 700 "$GNUPGHOME";   echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";   if [ -n "$SOLR_KEYS" ]; then     wget -nv "https://downloads.apache.org/solr/KEYS" -O- |       gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';     release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";     rm -rf "$GNUPGHOME"/*;     echo "${release_keys}" | gpg --batch --import;   fi;   MAX_REDIRECTS=3;   if [ -n "$SOLR_DOWNLOAD_URL" ]; then     MAX_REDIRECTS=4;     SKIP_GPG_CHECK=true;   elif [ -n "$SOLR_DOWNLOAD_SERVER" ]; then     SOLR_DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/solr-$SOLR_VERSION.tgz";   fi;   for url in $SOLR_DOWNLOAD_URL $SOLR_CLOSER_URL $SOLR_DIST_URL $SOLR_ARCHIVE_URL; do     if [ -f "/opt/solr-$SOLR_VERSION.tgz" ]; then break; fi;     echo "downloading $url";     if wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$url" -O "/opt/solr-$SOLR_VERSION.tgz"; then break; else rm -f "/opt/solr-$SOLR_VERSION.tgz"; fi;   done;   if [ ! -f "/opt/solr-$SOLR_VERSION.tgz" ]; then echo "failed all download attempts for solr-$SOLR_VERSION.tgz"; exit 1; fi;   if [ -z "$SKIP_GPG_CHECK" ]; then     echo "downloading $SOLR_ARCHIVE_URL.asc";     wget -nv "$SOLR_ARCHIVE_URL.asc" -O "/opt/solr-$SOLR_VERSION.tgz.asc";     echo "$SOLR_SHA512 */opt/solr-$SOLR_VERSION.tgz" | sha512sum -c -;     (>&2 ls -l "/opt/solr-$SOLR_VERSION.tgz" "/opt/solr-$SOLR_VERSION.tgz.asc");     gpg --batch --verify "/opt/solr-$SOLR_VERSION.tgz.asc" "/opt/solr-$SOLR_VERSION.tgz";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   { command -v gpgconf; gpgconf --kill all || :; };   rm -r "$GNUPGHOME";   tar -C /opt --extract --preserve-permissions --file "/opt/solr-$SOLR_VERSION.tgz";   rm "/opt/solr-$SOLR_VERSION.tgz"*;
# Thu, 16 Mar 2023 19:06:40 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Thu, 16 Mar 2023 19:06:40 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Thu, 16 Mar 2023 19:06:40 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Thu, 16 Mar 2023 19:06:40 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Thu, 16 Mar 2023 19:06:40 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Thu, 16 Mar 2023 19:06:40 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Thu, 16 Mar 2023 19:06:40 GMT
LABEL org.opencontainers.image.version=9.1.1
# Thu, 16 Mar 2023 19:06:40 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Thu, 16 Mar 2023 19:06:40 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0
# Thu, 16 Mar 2023 19:06:41 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Thu, 16 Mar 2023 19:06:41 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Thu, 16 Mar 2023 19:06:42 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   ln -s /opt/solr/modules /opt/solr/contrib;   ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Thu, 16 Mar 2023 19:06:47 GMT
# ARGS: SOLR_ARCHIVE_URL=https://archive.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_CLOSER_URL=http://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_DIST_URL=https://www.apache.org/dist/solr/solr/9.1.1/solr-9.1.1.tgz SOLR_KEYS=C3E7CBD9B9FE2B419EB14B89612B39A5BC981763 SOLR_SHA512=59fd47185196fc6b0fad4b6b2ba547d136cc0c688addc9833129086944cc90e185a18c33fd70523edddad1a6ebe7b4cd893be5065c2b01fe21a5026bdb7e5d9f SOLR_VERSION=9.1.1
RUN set -ex;     apt-get update;     apt-get -y install acl dirmngr lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Thu, 16 Mar 2023 19:06:47 GMT
VOLUME [/var/solr]
# Thu, 16 Mar 2023 19:06:47 GMT
EXPOSE 8983
# Thu, 16 Mar 2023 19:06:47 GMT
WORKDIR /opt/solr
# Thu, 16 Mar 2023 19:06:47 GMT
USER 8983
# Thu, 16 Mar 2023 19:06:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 19:06:48 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:422c367cdac1ee2f6bd9ea546c8e5a643af0847a822d04ba202af409973273ad`  
		Last Modified: Thu, 16 Mar 2023 01:40:19 GMT  
		Size: 27.0 MB (27016120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044a4439d496325544d92758687b7840fb4520f08dc2a7bdfa50ccf9caddc943`  
		Last Modified: Thu, 16 Mar 2023 02:13:13 GMT  
		Size: 19.5 MB (19526689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32bafb01414cb4066d7d4ab69f7546e629e9d5e9b196264d03c3f31075ca7e82`  
		Last Modified: Thu, 16 Mar 2023 02:14:03 GMT  
		Size: 43.7 MB (43739743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5dab49cd285549b2668638176d0742a54411f1ff796595daf9e0788eedfc60b`  
		Last Modified: Thu, 16 Mar 2023 02:13:57 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4d1b69532be69afef62bde7ccfbefb81e86945e7d217c6b55026025778b393`  
		Last Modified: Thu, 16 Mar 2023 19:10:20 GMT  
		Size: 233.7 MB (233657109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed118510f10ebf0927666af5dceb681f5c9a2857fadcc1b7f01ba426befd0f0`  
		Last Modified: Thu, 16 Mar 2023 19:10:09 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21da7b4450c4e862f16560122824f9516b88273eba9f3d5158745a8f0c15`  
		Last Modified: Thu, 16 Mar 2023 19:10:10 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759fe963eb61d10b8ad154b98c5e4988a64e55c97478c2f4862526e5fb8e4c3d`  
		Last Modified: Thu, 16 Mar 2023 19:10:09 GMT  
		Size: 8.1 KB (8079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a0b1d469408fb1cde24f21f6f834da6783e4e59c6c248172e19925c8019069`  
		Last Modified: Thu, 16 Mar 2023 19:10:10 GMT  
		Size: 1.5 MB (1495794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

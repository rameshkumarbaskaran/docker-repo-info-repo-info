## `solr:9-slim`

```console
$ docker pull solr@sha256:d79f55c4d4d6d47c67a44bfe57dbc85671f2cf7225f65aad1a1293ccc756234e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `solr:9-slim` - linux; amd64

```console
$ docker pull solr@sha256:ba6507dc9a8874b0352bcd63c78ecaa79a045bd13647357effef9680a896dd58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160919628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a361159baaee415c561834ca068aeb98ac6594ee1dd29e39d78d44ed509e50e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 12 Dec 2023 11:38:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:38:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:38:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:38:59 GMT
ADD file:2b3b5254f38a790d40e31cb26155609f7fc99ef7bc99eae1e0d67fa9ae605f77 in / 
# Tue, 12 Dec 2023 11:38:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:16:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:16:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:16:13 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:18:54 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:18:54 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 10:19:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:19:30 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:19:30 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:19:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 14:15:51 GMT
ARG SOLR_VERSION=9.4.0
# Sat, 16 Dec 2023 14:16:40 GMT
ARG SOLR_DIST=-slim
# Sat, 16 Dec 2023 14:16:40 GMT
ARG SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a
# Sat, 16 Dec 2023 14:16:40 GMT
ARG SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E
# Sat, 16 Dec 2023 14:16:40 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 16 Dec 2023 14:16:55 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a SOLR_VERSION=9.4.0
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Sat, 16 Dec 2023 14:16:55 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 16 Dec 2023 14:16:55 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Sat, 16 Dec 2023 14:16:55 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 16 Dec 2023 14:16:55 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 16 Dec 2023 14:16:55 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 16 Dec 2023 14:16:55 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 16 Dec 2023 14:16:55 GMT
LABEL org.opencontainers.image.version=9.4.0
# Sat, 16 Dec 2023 14:16:56 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Dec 2023 14:16:56 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 16 Dec 2023 14:16:56 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a SOLR_VERSION=9.4.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Sat, 16 Dec 2023 14:16:57 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a SOLR_VERSION=9.4.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Sat, 16 Dec 2023 14:16:57 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a SOLR_VERSION=9.4.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Sat, 16 Dec 2023 14:17:02 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a SOLR_VERSION=9.4.0
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Sat, 16 Dec 2023 14:17:02 GMT
VOLUME [/var/solr]
# Sat, 16 Dec 2023 14:17:02 GMT
EXPOSE 8983
# Sat, 16 Dec 2023 14:17:02 GMT
WORKDIR /opt/solr
# Sat, 16 Dec 2023 14:17:02 GMT
USER 8983
# Sat, 16 Dec 2023 14:17:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Dec 2023 14:17:02 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:3dd181f9be599de628e1bc6d868d517125e07f968824bcf7b7ed8d28ad1026b1`  
		Last Modified: Tue, 12 Dec 2023 12:46:19 GMT  
		Size: 30.4 MB (30446577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f838805bddf9c7d83f7f51716a77602920f9057ade57b344c071481b5214767`  
		Last Modified: Sat, 16 Dec 2023 10:23:47 GMT  
		Size: 17.5 MB (17456128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7eee5bc80e633b7f89402fb78469504f2d0662c7c827954ff259867d024278b`  
		Last Modified: Sat, 16 Dec 2023 10:24:28 GMT  
		Size: 47.1 MB (47149325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51526e7965d895bb7535ad46133791589d87f78882f553e5e63f8aed0568dabd`  
		Last Modified: Sat, 16 Dec 2023 10:24:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffcdc7c6c1603bef17eec1b194fd954703a005aff5db2d15302f85b01b494351`  
		Last Modified: Sat, 16 Dec 2023 10:24:21 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea1af49be26583c4b9d865fd15b59da626856b308ed84af4fe5e3a2c93e7b88`  
		Last Modified: Sat, 16 Dec 2023 14:25:59 GMT  
		Size: 64.0 MB (64022589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769976bbe4a9a22ba8e7fe70a26bc1b5eae75b94fa403409ab2e3a63abecbbd6`  
		Last Modified: Sat, 16 Dec 2023 14:25:58 GMT  
		Size: 4.3 KB (4294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e92fb049024a6043a9b874fc0f959da4c6c5ef5772ee6dc04ab80cd270510742`  
		Last Modified: Sat, 16 Dec 2023 14:25:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a102e84527627936ca44ac6c63e8df41567786b972cef0245429f712efba50`  
		Last Modified: Sat, 16 Dec 2023 14:25:56 GMT  
		Size: 10.8 KB (10752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2732d2f6c7c2c0ac76b4d372555221d624bd2d87035fd22fd9fb3a3b4de981b1`  
		Last Modified: Sat, 16 Dec 2023 14:25:56 GMT  
		Size: 1.8 MB (1828846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9-slim` - linux; arm variant v7

```console
$ docker pull solr@sha256:105fd4f2edef46accb56da843a518440ddf97636705bd1e2c24d21ca65c178e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155593690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec09569ebd867551a4ad0808d3313db3427ecb2a12714665e7b9e5951ac1f7cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:01 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:01 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:06 GMT
ADD file:62316c1da591602d5f15e0cda8787ce54cb80cd63ee53391aad6e4ea9cc97f06 in / 
# Tue, 12 Dec 2023 11:41:06 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 09:30:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 09:30:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 09:30:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 09:32:42 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 09:32:42 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 09:33:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 09:33:11 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 09:33:11 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 09:33:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 10:20:15 GMT
ARG SOLR_VERSION=9.4.0
# Sat, 16 Dec 2023 10:21:13 GMT
ARG SOLR_DIST=-slim
# Sat, 16 Dec 2023 10:21:13 GMT
ARG SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a
# Sat, 16 Dec 2023 10:21:13 GMT
ARG SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E
# Sat, 16 Dec 2023 10:21:13 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 16 Dec 2023 10:21:28 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a SOLR_VERSION=9.4.0
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Sat, 16 Dec 2023 10:21:29 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 16 Dec 2023 10:21:29 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Sat, 16 Dec 2023 10:21:29 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 16 Dec 2023 10:21:29 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 16 Dec 2023 10:21:29 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 16 Dec 2023 10:21:29 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 16 Dec 2023 10:21:29 GMT
LABEL org.opencontainers.image.version=9.4.0
# Sat, 16 Dec 2023 10:21:29 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Dec 2023 10:21:29 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 16 Dec 2023 10:21:30 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a SOLR_VERSION=9.4.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Sat, 16 Dec 2023 10:21:30 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a SOLR_VERSION=9.4.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Sat, 16 Dec 2023 10:21:31 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a SOLR_VERSION=9.4.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Sat, 16 Dec 2023 10:21:35 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a SOLR_VERSION=9.4.0
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Sat, 16 Dec 2023 10:21:35 GMT
VOLUME [/var/solr]
# Sat, 16 Dec 2023 10:21:35 GMT
EXPOSE 8983
# Sat, 16 Dec 2023 10:21:35 GMT
WORKDIR /opt/solr
# Sat, 16 Dec 2023 10:21:36 GMT
USER 8983
# Sat, 16 Dec 2023 10:21:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Dec 2023 10:21:36 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:bd71537214026ea993ab6e8967640e8c1258fb3402403fb3f72092e6b932621e`  
		Last Modified: Tue, 12 Dec 2023 18:24:48 GMT  
		Size: 27.5 MB (27524114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959de596b46d5f84a875b661d52b88b1ef36c9e495fb5d940044f558a80fb039`  
		Last Modified: Sat, 16 Dec 2023 09:36:30 GMT  
		Size: 17.6 MB (17587372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add53a4b1ff62bb8a21ddc789cdd787a603a9013a41caea69f6aa60823d79e01`  
		Last Modified: Sat, 16 Dec 2023 09:37:13 GMT  
		Size: 44.8 MB (44787055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14d7549b188863ae4b23b82c900ea1c60acc40569f569e7f05134bc907f8b57`  
		Last Modified: Sat, 16 Dec 2023 09:37:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b57b892dd97d81304d30bb9c848a2d7ad7b2b258d2057e39bd837330cc910c`  
		Last Modified: Sat, 16 Dec 2023 09:37:06 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895b2ea60742bfc25ba6f635bbe1818359121ebd668c3d51ea28d2a1659d08f0`  
		Last Modified: Sat, 16 Dec 2023 10:28:30 GMT  
		Size: 64.0 MB (64023990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ead9c3e580d61a80c340aece288d0cbc7f973dc3fb84f8e5ee455814cf4fb3`  
		Last Modified: Sat, 16 Dec 2023 10:28:26 GMT  
		Size: 4.2 KB (4227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879e0a58a2112e303b8e4db67b40792eba31958b6bf4240eb44191c06eaf433f`  
		Last Modified: Sat, 16 Dec 2023 10:28:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a558266c9365e0c38430b988c216566bf4cbf64fc299e5fd74b60e492c3d56`  
		Last Modified: Sat, 16 Dec 2023 10:28:26 GMT  
		Size: 10.8 KB (10752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7a9f76244c126d7d09208612607654129bffde8efa00a919be7a1a500bfe05d`  
		Last Modified: Sat, 16 Dec 2023 10:28:26 GMT  
		Size: 1.7 MB (1655064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9-slim` - linux; arm64 variant v8

```console
$ docker pull solr@sha256:592c16690373738988cfc8fdc8e588432500e1ff85c685ca581a697546e3a31f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159611321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7df9782cbe925511c1941cb68b2e5b17e993e53811463390df34cd3f5e4a779`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 12 Dec 2023 11:41:50 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:41:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:41:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:41:51 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:41:54 GMT
ADD file:50f947da69b3b6c63695be9c49eee16f7a7dcdecdceb51e5bee1609b845bf483 in / 
# Tue, 12 Dec 2023 11:41:54 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:02:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:04:31 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:04:32 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 10:04:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:04:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:04:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:04:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 16:07:56 GMT
ARG SOLR_VERSION=9.4.0
# Sat, 16 Dec 2023 16:08:54 GMT
ARG SOLR_DIST=-slim
# Sat, 16 Dec 2023 16:08:54 GMT
ARG SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a
# Sat, 16 Dec 2023 16:08:54 GMT
ARG SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E
# Sat, 16 Dec 2023 16:08:54 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 16 Dec 2023 16:09:08 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a SOLR_VERSION=9.4.0
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Sat, 16 Dec 2023 16:09:08 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 16 Dec 2023 16:09:08 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Sat, 16 Dec 2023 16:09:08 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 16 Dec 2023 16:09:08 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 16 Dec 2023 16:09:08 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 16 Dec 2023 16:09:08 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 16 Dec 2023 16:09:08 GMT
LABEL org.opencontainers.image.version=9.4.0
# Sat, 16 Dec 2023 16:09:08 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Dec 2023 16:09:08 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 16 Dec 2023 16:09:09 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a SOLR_VERSION=9.4.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Sat, 16 Dec 2023 16:09:09 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a SOLR_VERSION=9.4.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Sat, 16 Dec 2023 16:09:10 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a SOLR_VERSION=9.4.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Sat, 16 Dec 2023 16:09:14 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a SOLR_VERSION=9.4.0
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Sat, 16 Dec 2023 16:09:14 GMT
VOLUME [/var/solr]
# Sat, 16 Dec 2023 16:09:14 GMT
EXPOSE 8983
# Sat, 16 Dec 2023 16:09:14 GMT
WORKDIR /opt/solr
# Sat, 16 Dec 2023 16:09:14 GMT
USER 8983
# Sat, 16 Dec 2023 16:09:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Dec 2023 16:09:14 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:7734efb8b826f955c6a3bb51d7c84cb262d0e600ea3980f5bce69fa7f4f92d24`  
		Last Modified: Tue, 12 Dec 2023 16:00:15 GMT  
		Size: 28.4 MB (28400282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83d9c33e24ca521e40939a701f20c41285b4488136968b6007b00f5ea0e1267`  
		Last Modified: Sat, 16 Dec 2023 10:08:54 GMT  
		Size: 18.9 MB (18857814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced1602447389bf6ad2464c27ffc94e85095dbfdb47f78a2096081e80388ad97`  
		Last Modified: Sat, 16 Dec 2023 10:09:35 GMT  
		Size: 46.6 MB (46624027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6457113e3d5d5e26e07af4b78a197170e362a87e9acf2597817bf8e41b61b864`  
		Last Modified: Sat, 16 Dec 2023 10:09:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764df9f717c8b617f5bd26b1b7a44dfb44e89d4a1bc26be0eb4a08d0696d3e49`  
		Last Modified: Sat, 16 Dec 2023 10:09:30 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0434fdc49e615fa29042dca7a458afe6815000f1de2c080074aea28e814a7d70`  
		Last Modified: Sat, 16 Dec 2023 16:22:49 GMT  
		Size: 64.0 MB (64024088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa12cdb7f7a9f198a2050b145ec8312fa2e245d268d0fc14201bef165a6157ca`  
		Last Modified: Sat, 16 Dec 2023 16:22:45 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfc7ed8a45088e5994dddde4fc9955d0cecb933d84f3469a4399ec75721b3e0`  
		Last Modified: Sat, 16 Dec 2023 16:22:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b97b449b6a01c65f513368820235539e1f02c016cee221f421ec3c14c03cf79`  
		Last Modified: Sat, 16 Dec 2023 16:22:44 GMT  
		Size: 10.8 KB (10754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991f2721b8743e5c74b98e591689412913e1cb3d757cb8f8ee87b8838ccc24f2`  
		Last Modified: Sat, 16 Dec 2023 16:22:45 GMT  
		Size: 1.7 MB (1688908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9-slim` - linux; ppc64le

```console
$ docker pull solr@sha256:33062e34ca63773df22a162fb8920f386c5385b471acf0f556dbc1acba019f9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.3 MB (167253779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73aa1dec0f6f6299f74a3222e7f39673b4c2d7632a1f81beb30a17b077288bd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 12 Dec 2023 11:43:51 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:43:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:43:52 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:43:55 GMT
ADD file:bda128b553d54e39b55daceea1f0ad351c73f83835bbf65d10e5af879ce6fee7 in / 
# Tue, 12 Dec 2023 11:43:56 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:37:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:37:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:37:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:41:17 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:41:18 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 10:42:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 10:42:12 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 10:42:13 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:42:13 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 13:45:08 GMT
ARG SOLR_VERSION=9.4.0
# Sat, 16 Dec 2023 13:46:32 GMT
ARG SOLR_DIST=-slim
# Sat, 16 Dec 2023 13:46:32 GMT
ARG SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a
# Sat, 16 Dec 2023 13:46:32 GMT
ARG SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E
# Sat, 16 Dec 2023 13:46:32 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 16 Dec 2023 13:47:00 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a SOLR_VERSION=9.4.0
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Sat, 16 Dec 2023 13:47:01 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 16 Dec 2023 13:47:01 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Sat, 16 Dec 2023 13:47:01 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 16 Dec 2023 13:47:02 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 16 Dec 2023 13:47:02 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 16 Dec 2023 13:47:02 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 16 Dec 2023 13:47:03 GMT
LABEL org.opencontainers.image.version=9.4.0
# Sat, 16 Dec 2023 13:47:03 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Dec 2023 13:47:03 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 16 Dec 2023 13:47:04 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a SOLR_VERSION=9.4.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Sat, 16 Dec 2023 13:47:06 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a SOLR_VERSION=9.4.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Sat, 16 Dec 2023 13:47:07 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a SOLR_VERSION=9.4.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Sat, 16 Dec 2023 13:47:14 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a SOLR_VERSION=9.4.0
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Sat, 16 Dec 2023 13:47:14 GMT
VOLUME [/var/solr]
# Sat, 16 Dec 2023 13:47:15 GMT
EXPOSE 8983
# Sat, 16 Dec 2023 13:47:15 GMT
WORKDIR /opt/solr
# Sat, 16 Dec 2023 13:47:16 GMT
USER 8983
# Sat, 16 Dec 2023 13:47:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Dec 2023 13:47:16 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:7775720178c79208fc0d1b977c06891ef7230f39bc02e948d233c49f8a202fcf`  
		Last Modified: Sat, 16 Dec 2023 10:35:18 GMT  
		Size: 35.7 MB (35655287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5ea4a2de03097449e4184f8073a7b1f99cbf72be7cc99200a31a650ddc5512`  
		Last Modified: Sat, 16 Dec 2023 10:46:55 GMT  
		Size: 18.7 MB (18724047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50b2a976e30846fdb5868c7d0e0923e6357e75e5b9e1f6526f509271d1b3e91`  
		Last Modified: Sat, 16 Dec 2023 10:47:40 GMT  
		Size: 47.0 MB (46999654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88347adfd6b05f182859526ee82156b4194fe99cf3c13c671d912e936346879d`  
		Last Modified: Sat, 16 Dec 2023 10:47:33 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a2fff12d8e754683a9e43f9784ffb4154a256c207647cec36acd4eb9b5d134`  
		Last Modified: Sat, 16 Dec 2023 10:47:33 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:961a8c0b25c280f646cf233808b05693900e9ecc8422c57beb53de61d11f054e`  
		Last Modified: Sat, 16 Dec 2023 13:55:20 GMT  
		Size: 64.0 MB (64023272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c920b38c1f25beeefac4a6db1db9d664eee0e3759c0271225acbece2564ae0f4`  
		Last Modified: Sat, 16 Dec 2023 13:55:15 GMT  
		Size: 4.3 KB (4294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3d1af1984f19c5a79a0302301552cdf43c48466e0efc590da9ffc98ec1791d`  
		Last Modified: Sat, 16 Dec 2023 13:55:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b71d739350d011611035d1bfa99bf751908d2ea344d89e85a3c8bb3b723eff`  
		Last Modified: Sat, 16 Dec 2023 13:55:15 GMT  
		Size: 10.8 KB (10756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68aec2398c8d9159f44994a101c52ea58918964bda704a538bd8f68054cd8cad`  
		Last Modified: Sat, 16 Dec 2023 13:55:16 GMT  
		Size: 1.8 MB (1835351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `solr:9-slim` - linux; s390x

```console
$ docker pull solr@sha256:4179fa0354bb8c801f510481522fb571edd3def759f6769144a0ff1ba0be7208
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155479184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f76451339937dea2f3c2132034ecc31d6e6948cb9272497cd316af63a374fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["solr-foreground"]`

```dockerfile
# Tue, 12 Dec 2023 11:44:57 GMT
ARG RELEASE
# Tue, 12 Dec 2023 11:44:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Dec 2023 11:44:57 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 12 Dec 2023 11:44:59 GMT
ADD file:1729e720d10023da7d783040cefa8f30d3c61772a5e1ae577182a1fcba69aff1 in / 
# Tue, 12 Dec 2023 11:44:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 07:44:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 07:44:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 07:44:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 07:46:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 07:46:41 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Sat, 16 Dec 2023 07:47:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='05b192f81ed478178ba953a2a779b67fc5a810acadb633ad69f8c4412399edb8';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.9_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='c37f729200b572884b8f8e157852c739be728d61d9a1da0f920104876d324733';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_x64_linux_hotspot_17.0.9_9.tar.gz';          ;;        armhf|arm)          ESUM='5ae1f8cae358e41083a6b44f53c6f0daeb657f83c293da6c8733f68278e13703';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_arm_linux_hotspot_17.0.9_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='79c85ecf1320c67b828310167e1ced62e402bc86a5d47ca9cc7bfa3b708cb07a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.9_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='c4f2249bee785aa8c754741aa24d035e02b4e6d844e35b2b20030374d8fbab75';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jre_s390x_linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 16 Dec 2023 07:47:35 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete."
# Sat, 16 Dec 2023 07:47:35 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 07:47:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 09:20:06 GMT
ARG SOLR_VERSION=9.4.0
# Sat, 16 Dec 2023 09:21:07 GMT
ARG SOLR_DIST=-slim
# Sat, 16 Dec 2023 09:21:07 GMT
ARG SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a
# Sat, 16 Dec 2023 09:21:07 GMT
ARG SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E
# Sat, 16 Dec 2023 09:21:07 GMT
ARG SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr
# Sat, 16 Dec 2023 09:21:22 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a SOLR_VERSION=9.4.0
RUN set -ex;   apt-get update;   apt-get -y --no-install-recommends install wget gpg gnupg dirmngr;   rm -rf /var/lib/apt/lists/*;   export SOLR_BINARY="solr-$SOLR_VERSION$SOLR_DIST.tgz";   MAX_REDIRECTS=3;   case "${SOLR_DOWNLOAD_SERVER}" in     (*"apache.org"*);;     (*)       MAX_REDIRECTS=4 &&       SKIP_GPG_CHECK=true;;   esac;   export DOWNLOAD_URL="$SOLR_DOWNLOAD_SERVER/$SOLR_VERSION/$SOLR_BINARY";   echo "downloading $DOWNLOAD_URL";   if ! wget -t 10 --max-redirect $MAX_REDIRECTS --retry-connrefused -nv "$DOWNLOAD_URL" -O "/opt/$SOLR_BINARY"; then rm -f "/opt/$SOLR_BINARY"; fi;   if [ ! -f "/opt/$SOLR_BINARY" ]; then echo "failed download attempt for $SOLR_BINARY"; exit 1; fi;   echo "$SOLR_SHA512 */opt/$SOLR_BINARY" | sha512sum -c -;   if [ -z "$SKIP_GPG_CHECK" ]; then     export GNUPGHOME="/tmp/gnupg_home";     mkdir -p "$GNUPGHOME";     chmod 700 "$GNUPGHOME";     echo "disable-ipv6" >> "$GNUPGHOME/dirmngr.conf";     if [ -n "$SOLR_KEYS" ]; then       wget -nv "https://downloads.apache.org/solr/KEYS" -O- |         gpg --batch --import --key-origin 'url,https://downloads.apache.org/solr/KEYS';       release_keys="$(gpg --batch --export -a ${SOLR_KEYS})";       rm -rf "$GNUPGHOME"/*;       echo "${release_keys}" | gpg --batch --import;     fi;     echo "downloading $DOWNLOAD_URL.asc";     wget -nv "$DOWNLOAD_URL.asc" -O "/opt/$SOLR_BINARY.asc";     (>&2 ls -l "/opt/$SOLR_BINARY" "/opt/$SOLR_BINARY.asc");     gpg --batch --verify "/opt/$SOLR_BINARY.asc" "/opt/$SOLR_BINARY";     { command -v gpgconf; gpgconf --kill all || :; };     rm -r "$GNUPGHOME";   else     echo "Skipping GPG validation due to non-Apache build";   fi;   tar -C /opt --extract --preserve-permissions --file "/opt/$SOLR_BINARY";   rm "/opt/$SOLR_BINARY"*;   apt-get -y remove gpg dirmngr && apt-get -y autoremove;
# Sat, 16 Dec 2023 09:21:26 GMT
LABEL org.opencontainers.image.title=Apache Solr
# Sat, 16 Dec 2023 09:21:26 GMT
LABEL org.opencontainers.image.description=Apache Solr is the popular, blazing-fast, open source search platform built on Apache Lucene.
# Sat, 16 Dec 2023 09:21:26 GMT
LABEL org.opencontainers.image.authors=The Apache Solr Project
# Sat, 16 Dec 2023 09:21:27 GMT
LABEL org.opencontainers.image.url=https://solr.apache.org
# Sat, 16 Dec 2023 09:21:27 GMT
LABEL org.opencontainers.image.source=https://github.com/apache/solr
# Sat, 16 Dec 2023 09:21:27 GMT
LABEL org.opencontainers.image.documentation=https://solr.apache.org/guide/
# Sat, 16 Dec 2023 09:21:27 GMT
LABEL org.opencontainers.image.version=9.4.0
# Sat, 16 Dec 2023 09:21:28 GMT
LABEL org.opencontainers.image.licenses=Apache-2.0
# Sat, 16 Dec 2023 09:21:28 GMT
ENV SOLR_USER=solr SOLR_UID=8983 SOLR_GROUP=solr SOLR_GID=8983 PATH=/opt/solr/bin:/opt/solr/docker/scripts:/opt/solr/prometheus-exporter/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin SOLR_INCLUDE=/etc/default/solr.in.sh SOLR_HOME=/var/solr/data SOLR_PID_DIR=/var/solr SOLR_LOGS_DIR=/var/solr/logs LOG4J_PROPS=/var/solr/log4j2.xml SOLR_JETTY_HOST=0.0.0.0 SOLR_ZK_EMBEDDED_HOST=0.0.0.0
# Sat, 16 Dec 2023 09:21:29 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a SOLR_VERSION=9.4.0
RUN set -ex;   groupadd -r --gid "$SOLR_GID" "$SOLR_GROUP";   useradd -r --uid "$SOLR_UID" --gid "$SOLR_GID" "$SOLR_USER"
# Sat, 16 Dec 2023 09:21:29 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a SOLR_VERSION=9.4.0
RUN set -ex;   (cd /opt; ln -s solr-*/ solr);   rm -Rf /opt/solr/docs /opt/solr/docker/Dockerfile;
# Sat, 16 Dec 2023 09:21:30 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a SOLR_VERSION=9.4.0
RUN set -ex;   mkdir -p /opt/solr/server/solr/lib /docker-entrypoint-initdb.d;   cp /opt/solr/bin/solr.in.sh /etc/default/solr.in.sh;   mv /opt/solr/bin/solr.in.sh /opt/solr/bin/solr.in.sh.orig;   mv /opt/solr/bin/solr.in.cmd /opt/solr/bin/solr.in.cmd.orig;   chmod 0664 /etc/default/solr.in.sh;   mkdir -p -m0770 /var/solr;   chown -R "$SOLR_USER:0" /var/solr;   test ! -e /opt/solr/modules || ln -s /opt/solr/modules /opt/solr/contrib;   test ! -e /opt/solr/prometheus-exporter || ln -s /opt/solr/prometheus-exporter /opt/solr/modules/prometheus-exporter;
# Sat, 16 Dec 2023 09:21:35 GMT
# ARGS: SOLR_DIST=-slim SOLR_DOWNLOAD_SERVER=https://www.apache.org/dyn/closer.lua?action=download&filename=/solr/solr SOLR_KEYS=2289AC4180E130507D7A82F479C211E0AEFCA72E SOLR_SHA512=4ae8929f4c8ac275b1c9e8c45f17c3557fa34c46d9fdb171243f5c575466a9dba86216fbb0ea951a7ae9f16acf38ce292276dd9f033b82b2e5211de9d8ed397a SOLR_VERSION=9.4.0
RUN set -ex;     apt-get update;     apt-get -y --no-install-recommends install acl lsof procps wget netcat gosu tini jattach;     rm -rf /var/lib/apt/lists/*;
# Sat, 16 Dec 2023 09:21:35 GMT
VOLUME [/var/solr]
# Sat, 16 Dec 2023 09:21:35 GMT
EXPOSE 8983
# Sat, 16 Dec 2023 09:21:35 GMT
WORKDIR /opt/solr
# Sat, 16 Dec 2023 09:21:35 GMT
USER 8983
# Sat, 16 Dec 2023 09:21:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Dec 2023 09:21:36 GMT
CMD ["solr-foreground"]
```

-	Layers:
	-	`sha256:6949655473f9a6801351bc2ee9bef80a58f5ac2dd31547e0d4f473c53d282400`  
		Last Modified: Sat, 16 Dec 2023 07:42:42 GMT  
		Size: 28.7 MB (28654553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5403f046b5f4f1d04daf38495620c533cd57ec0024d621efb856eb83a6d1c33`  
		Last Modified: Sat, 16 Dec 2023 07:49:40 GMT  
		Size: 17.3 MB (17255263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84746bb02a2c09bcd3412a4ee5104e57a3d3d725f3a67c11f6341f4b83d20e4d`  
		Last Modified: Sat, 16 Dec 2023 07:50:14 GMT  
		Size: 43.8 MB (43754405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb602cccc2ab275bff1bb5e1448abb5f18c49f709c65d96153a526dc7638a99`  
		Last Modified: Sat, 16 Dec 2023 07:50:08 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b3a45421f98e08758991f8e50ccbc1d5ea9381ced8f4939e76258d8877b043`  
		Last Modified: Sat, 16 Dec 2023 07:50:08 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89dbb1ae3db6652ddf4568458d9c7f58fd3c5ad608f53a59fe1c7a0ce1d6d8ef`  
		Last Modified: Sat, 16 Dec 2023 09:27:43 GMT  
		Size: 64.0 MB (64022950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93de6cbfc416fe3e5796cd643db72ff29dc9086218212907b09ec6fc385b201b`  
		Last Modified: Sat, 16 Dec 2023 09:27:40 GMT  
		Size: 4.3 KB (4329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a662b185ec63f43bdb5d4cf518e1cb23f04e6f0ee2d3437bcb272695903fb2d`  
		Last Modified: Sat, 16 Dec 2023 09:27:40 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a332e10c298b2046746309a0c966fe29d9f629bbf5615122785f9bb2c48f55a8`  
		Last Modified: Sat, 16 Dec 2023 09:27:40 GMT  
		Size: 10.8 KB (10756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338131e81c6fedcd4acac10c535459f9d350d92999b390602ea2d6707faad8bd`  
		Last Modified: Sat, 16 Dec 2023 09:27:40 GMT  
		Size: 1.8 MB (1775813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

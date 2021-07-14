<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `websphere-liberty`

-	[`websphere-liberty:21.0.0.3-full-java11-openj9`](#websphere-liberty21003-full-java11-openj9)
-	[`websphere-liberty:21.0.0.3-full-java8-ibmjava`](#websphere-liberty21003-full-java8-ibmjava)
-	[`websphere-liberty:21.0.0.3-kernel-java11-openj9`](#websphere-liberty21003-kernel-java11-openj9)
-	[`websphere-liberty:21.0.0.3-kernel-java8-ibmjava`](#websphere-liberty21003-kernel-java8-ibmjava)
-	[`websphere-liberty:21.0.0.6-full-java11-openj9`](#websphere-liberty21006-full-java11-openj9)
-	[`websphere-liberty:21.0.0.6-full-java8-ibmjava`](#websphere-liberty21006-full-java8-ibmjava)
-	[`websphere-liberty:21.0.0.6-kernel-java11-openj9`](#websphere-liberty21006-kernel-java11-openj9)
-	[`websphere-liberty:21.0.0.6-kernel-java8-ibmjava`](#websphere-liberty21006-kernel-java8-ibmjava)
-	[`websphere-liberty:21.0.0.7-full-java11-openj9`](#websphere-liberty21007-full-java11-openj9)
-	[`websphere-liberty:21.0.0.7-full-java8-ibmjava`](#websphere-liberty21007-full-java8-ibmjava)
-	[`websphere-liberty:21.0.0.7-kernel-java11-openj9`](#websphere-liberty21007-kernel-java11-openj9)
-	[`websphere-liberty:21.0.0.7-kernel-java8-ibmjava`](#websphere-liberty21007-kernel-java8-ibmjava)
-	[`websphere-liberty:full`](#websphere-libertyfull)
-	[`websphere-liberty:full-java11-openj9`](#websphere-libertyfull-java11-openj9)
-	[`websphere-liberty:kernel`](#websphere-libertykernel)
-	[`websphere-liberty:kernel-java11-openj9`](#websphere-libertykernel-java11-openj9)
-	[`websphere-liberty:latest`](#websphere-libertylatest)

## `websphere-liberty:21.0.0.3-full-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:a4909799e8216677895c783b4e508b7b3535d7e281c43a7e2d49837865eac379
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:21.0.0.3-full-java11-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:81165cf4ea1b475c7c7caa837d9e523d61da05065945551cc94859f1a3761211
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.1 MB (331109960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf03242c0306f4b61e3c5fea49c9ec862872ad081d97e34b497abd8093c8744`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:29:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 14 Jul 2021 00:30:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:33:59 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Wed, 14 Jul 2021 00:35:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 14 Jul 2021 00:35:04 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 00:35:04 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 14 Jul 2021 00:35:41 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 14 Jul 2021 03:57:41 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 03:57:41 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 04:16:03 GMT
ARG EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f
# Wed, 14 Jul 2021 04:16:03 GMT
ARG NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8
# Wed, 14 Jul 2021 04:16:04 GMT
ARG NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075
# Wed, 14 Jul 2021 04:16:04 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.3 org.opencontainers.image.revision=cl210320210309-1101 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 04:16:04 GMT
ENV LIBERTY_VERSION=21.0.0_03
# Wed, 14 Jul 2021 04:16:04 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 04:16:04 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 04:16:13 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:16:13 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 04:16:13 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.3 BuildLabel=cl210320210309-1101
# Wed, 14 Jul 2021 04:16:13 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 04:16:15 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 04:16:15 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 04:16:15 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 04:16:16 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 04:16:24 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 04:16:24 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 14 Jul 2021 04:16:25 GMT
USER 1001
# Wed, 14 Jul 2021 04:16:25 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 04:16:25 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 04:16:25 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 14 Jul 2021 04:20:25 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 04:20:26 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 14 Jul 2021 04:23:30 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Wed, 14 Jul 2021 04:23:31 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 14 Jul 2021 04:24:05 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1182b8c86e6bb404b0d40d2cdcdcaf4347c5aad464143625307b362caff690`  
		Last Modified: Wed, 14 Jul 2021 00:44:02 GMT  
		Size: 16.0 MB (16033076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1461af6857aed41d09a8ce6e2447ad52c9cdf1e6fe2f19ddaa2ab35d21aa1b`  
		Last Modified: Wed, 14 Jul 2021 00:50:41 GMT  
		Size: 44.4 MB (44382137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b538d86edfd8bb98ca5958e79321f730b01a2adc10244bd8ff7abf2aea9b8d8`  
		Last Modified: Wed, 14 Jul 2021 00:50:36 GMT  
		Size: 4.1 MB (4134048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f289b9688849f2751466d4c24cc0ff90b3064d8ab25868671628829902cbf1d`  
		Last Modified: Wed, 14 Jul 2021 04:27:35 GMT  
		Size: 14.1 MB (14087084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bf925863e963d52a59aca1d42c1e75c75b02689d267a56ecb716c53300efbd`  
		Last Modified: Wed, 14 Jul 2021 04:27:31 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a294d7a7685d83363812d4d061e907766fe5eaa462a9c38e60ecb9f933574ca`  
		Last Modified: Wed, 14 Jul 2021 04:27:31 GMT  
		Size: 9.6 KB (9552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dfa9f9e49bd150d5fa52e6c91fed6ccbbe3b20b0d91972618d87fc513b86758`  
		Last Modified: Wed, 14 Jul 2021 04:27:31 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da039d2151be24f85d90e6a6c2038bd3cbd2511b0d2762c3ef3571bea640b35e`  
		Last Modified: Wed, 14 Jul 2021 04:27:31 GMT  
		Size: 10.5 KB (10536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95339fd4836ffd77fe4dee0c06ad8ca6eb46d11c66359346d5fc240789be9e03`  
		Last Modified: Wed, 14 Jul 2021 04:27:32 GMT  
		Size: 2.5 MB (2477910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2457b89c0a4c9fd945295f9ae220a1c80d6dd5c4eef25fa228c95a25ea5d59a7`  
		Last Modified: Wed, 14 Jul 2021 04:28:16 GMT  
		Size: 207.2 MB (207197919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169760ef75bc770d4e836bbf7dfe25897702f907b2cf9a4b04f9112c201ca95b`  
		Last Modified: Wed, 14 Jul 2021 04:28:03 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65dc8b80c2f29e707d8ac1febd35b985097ebd943aec9bb59bafd97a99f7d79a`  
		Last Modified: Wed, 14 Jul 2021 04:28:06 GMT  
		Size: 14.2 MB (14209930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.3-full-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:715200b9a12a500602cd9cd8c0f3f73e039e9dd8ae32c5ffbb7b8b3ee868856d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.9 MB (334943479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f772dc5ede3ac432288538aae2a1010a202963898f5b2f7937829c2a2d3b5a6`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 01:29:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 01:31:53 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:41:26 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Fri, 18 Jun 2021 01:43:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 01:43:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 01:43:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 18 Jun 2021 01:44:39 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 09 Jul 2021 12:06:18 GMT
ARG VERBOSE=false
# Fri, 09 Jul 2021 12:06:22 GMT
ARG OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:42:07 GMT
ARG EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f
# Fri, 09 Jul 2021 12:42:15 GMT
ARG NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8
# Fri, 09 Jul 2021 12:42:19 GMT
ARG NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075
# Fri, 09 Jul 2021 12:42:22 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.3 org.opencontainers.image.revision=cl210320210309-1101 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 09 Jul 2021 12:42:25 GMT
ENV LIBERTY_VERSION=21.0.0_03
# Fri, 09 Jul 2021 12:42:29 GMT
ARG LIBERTY_URL
# Fri, 09 Jul 2021 12:42:34 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 09 Jul 2021 12:43:09 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Jul 2021 12:43:14 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Jul 2021 12:43:17 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.3 BuildLabel=cl210320210309-1101
# Fri, 09 Jul 2021 12:43:19 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:43:30 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 09 Jul 2021 12:43:32 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Fri, 09 Jul 2021 12:43:35 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 09 Jul 2021 12:43:49 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 09 Jul 2021 12:44:09 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 09 Jul 2021 12:44:14 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 09 Jul 2021 12:44:22 GMT
USER 1001
# Fri, 09 Jul 2021 12:44:26 GMT
EXPOSE 9080 9443
# Fri, 09 Jul 2021 12:44:29 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 09 Jul 2021 12:44:32 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 09 Jul 2021 12:50:32 GMT
ARG VERBOSE=false
# Fri, 09 Jul 2021 12:50:38 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 09 Jul 2021 12:54:13 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Fri, 09 Jul 2021 12:54:25 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 09 Jul 2021 12:55:40 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b268950217e490e209e0491ae6fbd3af12b4642aefad9c0039daf7b3ea0371`  
		Last Modified: Fri, 18 Jun 2021 01:52:43 GMT  
		Size: 17.2 MB (17208433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74aa12681d5d14a96459a14094fd9b08f1379e61fa1e8979b311b55b0561dead`  
		Last Modified: Fri, 18 Jun 2021 01:57:43 GMT  
		Size: 45.1 MB (45104807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee28cff75d70e071001e265878f54c811f52ab2cf95d0cc9daa0085c8e1465d`  
		Last Modified: Fri, 18 Jun 2021 01:57:35 GMT  
		Size: 3.3 MB (3284426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8934a68406748539cbf4551dd9d89c6dd83c8049d25254d23b5e9e71549796d6`  
		Last Modified: Fri, 09 Jul 2021 13:00:25 GMT  
		Size: 14.1 MB (14088106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74cb765629f5b79b860201e16fc9679609d61ecd5352b224fda39e8b75306fb8`  
		Last Modified: Fri, 09 Jul 2021 13:00:19 GMT  
		Size: 691.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3611916086aa01fff230caa7d6eaff9d395282448609309a45e3254f74a9624`  
		Last Modified: Fri, 09 Jul 2021 13:00:19 GMT  
		Size: 9.6 KB (9552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a033803b23b91de2f3d1b82c31f0924f1ed573c0f588f870d87213b2b8058d`  
		Last Modified: Fri, 09 Jul 2021 13:00:19 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa019c53c1dc63a01b9a94250393a989f17bb8c8ffcafe66356891316deda4d`  
		Last Modified: Fri, 09 Jul 2021 13:00:19 GMT  
		Size: 10.5 KB (10541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfbb2936eb2c30638645c0cc0e459731004310f03bc7ec16f4cf3951270cee2`  
		Last Modified: Fri, 09 Jul 2021 13:00:19 GMT  
		Size: 2.5 MB (2450872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7394370022ee5afb9866df05713033193a352fec9f54f56c33b6ee9a97c48945`  
		Last Modified: Fri, 09 Jul 2021 13:01:24 GMT  
		Size: 207.2 MB (207198415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1528f2e85e96bdeae68c3b64adfe3a874e669ee0bb5a99186b7006c8ac7e6ac4`  
		Last Modified: Fri, 09 Jul 2021 13:01:04 GMT  
		Size: 945.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b1253b4cf951097021a081a348ea066d7a5fc409e86ad1be791681f36d1ce4`  
		Last Modified: Fri, 09 Jul 2021 13:01:09 GMT  
		Size: 12.3 MB (12308176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.3-full-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:3fb99a33c6ec41439b545aeedee4fb58535a11ba19adfc106b88217ae0561055
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.8 MB (327829767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f4fa026c25c84a818c65bfd90b415588f1828d83bcc7a8cd3f59ee428e29ad`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:34 GMT
ADD file:ae5354f89d91eedd0614e3e97ee59fd6e23254923062c288d775e19b137dfd1c in / 
# Tue, 13 Jul 2021 22:53:36 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:18:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Jul 2021 23:18:55 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:23:22 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Tue, 13 Jul 2021 23:24:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 13 Jul 2021 23:24:37 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jul 2021 23:24:37 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 13 Jul 2021 23:25:12 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 14 Jul 2021 00:26:14 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 00:26:15 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:50:36 GMT
ARG EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f
# Wed, 14 Jul 2021 00:50:36 GMT
ARG NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8
# Wed, 14 Jul 2021 00:50:37 GMT
ARG NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075
# Wed, 14 Jul 2021 00:50:37 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.3 org.opencontainers.image.revision=cl210320210309-1101 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 00:50:37 GMT
ENV LIBERTY_VERSION=21.0.0_03
# Wed, 14 Jul 2021 00:50:37 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 00:50:38 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 00:50:46 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:50:46 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 00:50:47 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.3 BuildLabel=cl210320210309-1101
# Wed, 14 Jul 2021 00:50:47 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:50:48 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 00:50:48 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 00:50:48 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 00:50:49 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 00:50:55 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 00:50:55 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 14 Jul 2021 00:50:55 GMT
USER 1001
# Wed, 14 Jul 2021 00:50:56 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 00:50:56 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 00:50:56 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 14 Jul 2021 00:55:09 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 00:55:10 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 14 Jul 2021 00:58:21 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Wed, 14 Jul 2021 00:58:25 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 14 Jul 2021 00:58:52 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:761fa758059faa0c80b0b90fcbcc192fc7f573da055460d5b3f019e0faceeb7a`  
		Last Modified: Tue, 13 Jul 2021 22:55:47 GMT  
		Size: 27.1 MB (27149318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0237838e148d45cea54b0d86c053131b4152f4928836cbb3a0c83ba79b538728`  
		Last Modified: Tue, 13 Jul 2021 23:32:23 GMT  
		Size: 15.7 MB (15741695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454768ac3fd4bd9b5536afd4e03c6c369d7eae1ee6b240b461dace5364b911f5`  
		Last Modified: Tue, 13 Jul 2021 23:36:09 GMT  
		Size: 43.8 MB (43840969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add6cc1d828e7c42608c4398d9d18baceea2e5104c4ff50d96eba8015aa4a896`  
		Last Modified: Tue, 13 Jul 2021 23:36:03 GMT  
		Size: 3.8 MB (3845109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53fe2ec5661d485ebb553e33cda7a75124d3d3326c46d78213cb174cc96167c`  
		Last Modified: Wed, 14 Jul 2021 01:02:18 GMT  
		Size: 14.1 MB (14087271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5bc84b15bc784178893508bc8b5b06692b70b227e0b63ddf51f048db8c0511`  
		Last Modified: Wed, 14 Jul 2021 01:02:15 GMT  
		Size: 690.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e366c33bb2a97777af7ed55c843d087a71d5ab3757e2f7e0a045518fb2d74182`  
		Last Modified: Wed, 14 Jul 2021 01:02:15 GMT  
		Size: 9.6 KB (9554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc02acc0088e74a2310df1f647646139f169f60b4434ae4e06574679ff6bc8d`  
		Last Modified: Wed, 14 Jul 2021 01:02:15 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31128c991901bd973dbe86c9c8dda73f01fc3f0bb2a867957560ed83bcd660db`  
		Last Modified: Wed, 14 Jul 2021 01:02:15 GMT  
		Size: 10.5 KB (10535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd07e9a6d1403fa04e2aef9855016844412f4982f78ae5999eb7a5edb34c449`  
		Last Modified: Wed, 14 Jul 2021 01:02:15 GMT  
		Size: 2.4 MB (2403939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c676e7d0aa82be76ad6c596f8ca91b822cc313679769f0fb0bdee01180903cf`  
		Last Modified: Wed, 14 Jul 2021 01:02:55 GMT  
		Size: 207.2 MB (207198494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37bb5837a7a8fb3b556d938675aeef99875609e2d11d4024faefcf11333808d3`  
		Last Modified: Wed, 14 Jul 2021 01:02:41 GMT  
		Size: 944.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02498f9284085ebab742079ad3b31209b31035eee4eacc499ad8f9d106d3948`  
		Last Modified: Wed, 14 Jul 2021 01:02:44 GMT  
		Size: 13.5 MB (13540977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:21.0.0.3-full-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:04850b5d9a9929bb117e61ab62954413ef2cc8e69fa159047fa11dca4778e2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:21.0.0.3-full-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:cda6d9d1f058f54290a8548938847058a905a3b49bdbe9bd604148c026b28211
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.2 MB (413182438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a3ab72ec3ca3c3420247c85c4b4263f6fcb9911961228186b4610ec057a0cc`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:19:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:19:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:19:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:19:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:19:52 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 14 Jul 2021 03:57:10 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 03:57:10 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 04:15:33 GMT
ARG EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f
# Wed, 14 Jul 2021 04:15:33 GMT
ARG NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8
# Wed, 14 Jul 2021 04:15:33 GMT
ARG NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075
# Wed, 14 Jul 2021 04:15:34 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.3 org.opencontainers.image.revision=cl210320210309-1101 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 04:15:34 GMT
ENV LIBERTY_VERSION=21.0.0_03
# Wed, 14 Jul 2021 04:15:34 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 04:15:34 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 04:15:44 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:15:44 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 04:15:45 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.3 BuildLabel=cl210320210309-1101
# Wed, 14 Jul 2021 04:15:45 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 04:15:46 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 04:15:47 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 04:15:47 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 04:15:48 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 04:15:58 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 04:15:58 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 14 Jul 2021 04:15:58 GMT
USER 1001
# Wed, 14 Jul 2021 04:15:58 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 04:15:58 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 04:15:59 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 14 Jul 2021 04:16:29 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 04:16:29 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 14 Jul 2021 04:19:42 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Wed, 14 Jul 2021 04:19:43 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 14 Jul 2021 04:20:20 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22821a14390caaab5b1f7ca9feb8e54ce64d3d81ca1fa64c6f1eee32ae92da5b`  
		Last Modified: Tue, 13 Jul 2021 23:23:03 GMT  
		Size: 3.0 MB (2959004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4403b30ef5ef8f7b37c65fc3d0a0e0d7e0fca7451dd9b42a43bee1de1f389c09`  
		Last Modified: Tue, 13 Jul 2021 23:23:13 GMT  
		Size: 129.5 MB (129536228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10d72199745009b56f78f418f97a9095a454904bad394f993393f7f1feecfd5`  
		Last Modified: Wed, 14 Jul 2021 04:27:23 GMT  
		Size: 14.0 MB (13988948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b518013c5cc1badd31dae723dbdcde785d271e7419238daf4ee93e6ac8a53187`  
		Last Modified: Wed, 14 Jul 2021 04:27:19 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea73ce22784ac15b48d7129d677b0d883e3ebb13a3c8bf0fa532f3d2541fddc`  
		Last Modified: Wed, 14 Jul 2021 04:27:19 GMT  
		Size: 9.6 KB (9553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afca36b12789fe4a6126946fb176e685863cdc7c9b588a344d7c332c9ecf7933`  
		Last Modified: Wed, 14 Jul 2021 04:27:19 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f08301c4eea896a7850e76947d8c0e3d2cfaac499f62df4e0ecf8dd366b148`  
		Last Modified: Wed, 14 Jul 2021 04:27:19 GMT  
		Size: 10.5 KB (10535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66221921700b8697ef17a84450f187b06790bd1ee1011fce836f6ac5160ffaa9`  
		Last Modified: Wed, 14 Jul 2021 04:27:20 GMT  
		Size: 5.6 MB (5647276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff3cb69b380c19f107920faf2f0563b1cec27db02013c343fbf2ed769c1ee61`  
		Last Modified: Wed, 14 Jul 2021 04:27:55 GMT  
		Size: 212.8 MB (212803810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b0bc4a4ed06358fc1c737e978a5dc230b6ff4d2be1107eac5a17ff40378035`  
		Last Modified: Wed, 14 Jul 2021 04:27:43 GMT  
		Size: 947.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed92b9b659445c103c3aa54041aae68bf92d4442c29de357f42696e4b8f1607`  
		Last Modified: Wed, 14 Jul 2021 04:27:46 GMT  
		Size: 21.5 MB (21519027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.3-full-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:b2899de168aea80e82883ef552e870821945534c799c43710047bce474c26cfb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.2 MB (413169240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd39ff9033e658c9d36c61e52cde8a9d1a9ec04dc0e3340bedbd52e79c628482`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 17 Jun 2021 23:24:58 GMT
ADD file:33bc9edd94d5731da919e83ed38bd4aa7daffcb5f629d93bbde112a795c79d48 in / 
# Thu, 17 Jun 2021 23:25:03 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:01:35 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 18 Jun 2021 02:02:36 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:02:42 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Fri, 18 Jun 2021 02:03:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 18 Jun 2021 02:04:05 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 09 Jul 2021 12:02:21 GMT
ARG VERBOSE=false
# Fri, 09 Jul 2021 12:02:27 GMT
ARG OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:38:38 GMT
ARG EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f
# Fri, 09 Jul 2021 12:38:42 GMT
ARG NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8
# Fri, 09 Jul 2021 12:38:45 GMT
ARG NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075
# Fri, 09 Jul 2021 12:38:49 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.3 org.opencontainers.image.revision=cl210320210309-1101 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 09 Jul 2021 12:38:54 GMT
ENV LIBERTY_VERSION=21.0.0_03
# Fri, 09 Jul 2021 12:39:00 GMT
ARG LIBERTY_URL
# Fri, 09 Jul 2021 12:39:11 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 09 Jul 2021 12:40:19 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Jul 2021 12:40:26 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Jul 2021 12:40:30 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.3 BuildLabel=cl210320210309-1101
# Fri, 09 Jul 2021 12:40:33 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:40:44 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 09 Jul 2021 12:40:45 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Fri, 09 Jul 2021 12:40:47 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 09 Jul 2021 12:41:11 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 09 Jul 2021 12:41:30 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 09 Jul 2021 12:41:33 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Fri, 09 Jul 2021 12:41:38 GMT
USER 1001
# Fri, 09 Jul 2021 12:41:42 GMT
EXPOSE 9080 9443
# Fri, 09 Jul 2021 12:41:45 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 09 Jul 2021 12:41:48 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 09 Jul 2021 12:44:50 GMT
ARG VERBOSE=false
# Fri, 09 Jul 2021 12:44:53 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 09 Jul 2021 12:48:56 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Fri, 09 Jul 2021 12:49:05 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 09 Jul 2021 12:50:15 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:4e37c2419ee7d7e826be5c6ee69243351aaf456d6527714660cf7e7015491051`  
		Last Modified: Thu, 17 Jun 2021 23:28:22 GMT  
		Size: 30.4 MB (30425356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8d177e4917900437a3445272639bed389b718cc65a87346ba94f6d99327f34`  
		Last Modified: Fri, 18 Jun 2021 02:07:44 GMT  
		Size: 3.1 MB (3082963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09af03e0818b00fa01f51019b91f996a958b5ffb6b7dcd23e88d4d0df759f391`  
		Last Modified: Fri, 18 Jun 2021 02:07:59 GMT  
		Size: 129.1 MB (129059791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c73ab0e009309ce6891ae8bb263b6aebd59105c1eb9179d42976e3b93c2099`  
		Last Modified: Fri, 09 Jul 2021 13:00:09 GMT  
		Size: 14.0 MB (13989397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48db10faa5d6301afba460ec5343c9d17672aacf2d5d74384f76ffe4ef38cc07`  
		Last Modified: Fri, 09 Jul 2021 13:00:04 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51767e8a50e913466e46c80f96d48d88fb454c9ec7a3048552bd9132f998571`  
		Last Modified: Fri, 09 Jul 2021 13:00:03 GMT  
		Size: 9.6 KB (9557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c2c208d08e4e5682c6c9e5af0e840de4b302a43926d712d0e24c860fe736e7`  
		Last Modified: Fri, 09 Jul 2021 13:00:03 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c1b85c34fe4c104929c4b3dcaaeabfff39b4d723c1a327a7fa006c75c21ef`  
		Last Modified: Fri, 09 Jul 2021 13:00:04 GMT  
		Size: 10.5 KB (10548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa00e1f22f20345c00e9b83e59795ccede28e9d2fc3a478ceda6d0e0a2b5cfde`  
		Last Modified: Fri, 09 Jul 2021 13:00:04 GMT  
		Size: 5.2 MB (5240830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59339f6c6f35dd96aea19001e2767b56945331ea5d2beae6b42d8c657ad2ea8`  
		Last Modified: Fri, 09 Jul 2021 13:00:54 GMT  
		Size: 212.4 MB (212400481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f137aec72486400f61d045227718ac296e993e827f3ae3789fd2a37ef98ddea`  
		Last Modified: Fri, 09 Jul 2021 13:00:34 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7ec0928d4b309060242612592beed4497a9def070b0d5d90c482dc057a41bf`  
		Last Modified: Fri, 09 Jul 2021 13:00:39 GMT  
		Size: 18.9 MB (18948399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.3-full-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:aa6b0a201c251ab1db7e08e213ad586ff923f3c915acf210f727bf07bb623830
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.9 MB (408928596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:368a2cea489521ee2a812fa7cc7e1d524c2e55e2451c79a08a85a884c598de6e`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:22 GMT
ADD file:9e621b1dfa735f1a89553f154f2a2a6f669ff610236d92d6ebf37d1f378d8ec0 in / 
# Tue, 13 Jul 2021 22:53:24 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:12:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:12:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:12:20 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:13:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:13:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 14 Jul 2021 00:25:32 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 00:25:32 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:50:04 GMT
ARG EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f
# Wed, 14 Jul 2021 00:50:04 GMT
ARG NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8
# Wed, 14 Jul 2021 00:50:05 GMT
ARG NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075
# Wed, 14 Jul 2021 00:50:05 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.3 org.opencontainers.image.revision=cl210320210309-1101 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 00:50:05 GMT
ENV LIBERTY_VERSION=21.0.0_03
# Wed, 14 Jul 2021 00:50:05 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 00:50:05 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 00:50:16 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:50:16 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 00:50:16 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.3 BuildLabel=cl210320210309-1101
# Wed, 14 Jul 2021 00:50:17 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:50:18 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 00:50:18 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 00:50:18 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 00:50:19 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 00:50:27 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 00:50:28 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 14 Jul 2021 00:50:28 GMT
USER 1001
# Wed, 14 Jul 2021 00:50:28 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 00:50:28 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 00:50:29 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 14 Jul 2021 00:51:04 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 00:51:04 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 14 Jul 2021 00:54:24 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Wed, 14 Jul 2021 00:54:28 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 14 Jul 2021 00:54:57 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:3287e09e36098b10234ccc1f8db0b48e2027ca7caa353a362d65f9b017ab802e`  
		Last Modified: Tue, 13 Jul 2021 22:55:34 GMT  
		Size: 25.4 MB (25365649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6fe4e2b151f33398a6ef48bbb5d9ace538aa5ecf3fab9182babc3a85b9166b`  
		Last Modified: Tue, 13 Jul 2021 23:16:59 GMT  
		Size: 2.7 MB (2676828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b436dddc9b46f3b9e70224bb7eab52e58419d071c07f16f9ce63c77c81e5e24`  
		Last Modified: Tue, 13 Jul 2021 23:17:08 GMT  
		Size: 126.7 MB (126676530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1998064bd8d8ea7ff4e9a8365c04a9f64b6710120fd5ddc59249584f99af2be1`  
		Last Modified: Wed, 14 Jul 2021 01:02:09 GMT  
		Size: 14.0 MB (13988617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9fc4be8562cd0c12bde799f87024d3f07d07e24b45c8c6f7b3b41825b150587`  
		Last Modified: Wed, 14 Jul 2021 01:02:06 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c647ec4aa35a0e55a99d40254aafcf8e578a6be6fcddcf52f9b66f105fdf89`  
		Last Modified: Wed, 14 Jul 2021 01:02:06 GMT  
		Size: 9.6 KB (9555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dca87ec5945d5239dee8c6f64c27da567269daece09afdf1accc33fe0807487`  
		Last Modified: Wed, 14 Jul 2021 01:02:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8201e76ed533104079b785b672c2bcb501df13efb6fb9b26d47b56f430190812`  
		Last Modified: Wed, 14 Jul 2021 01:02:06 GMT  
		Size: 10.5 KB (10537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec9f2ba4cb485906aeae84a935931a97c8b30779a7b08af65bbdee9e9ec2f5c`  
		Last Modified: Wed, 14 Jul 2021 01:02:07 GMT  
		Size: 5.8 MB (5841259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b684dacf44676c07a452133076ce32c5c2ec8e4316c466e24596d2fc3e2a2325`  
		Last Modified: Wed, 14 Jul 2021 01:02:35 GMT  
		Size: 213.0 MB (213002655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bebb361ab3285752fd6631c0235e79fa982fad4e4486d6fe3da1a6ac4b8be3c`  
		Last Modified: Wed, 14 Jul 2021 01:02:23 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba06e9a1fc6982a2c4d4a8be5a3592b05eb1f1ccc2c85867181d7281f251e872`  
		Last Modified: Wed, 14 Jul 2021 01:02:26 GMT  
		Size: 21.4 MB (21355050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:21.0.0.3-kernel-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:83d28eae1bd6ca6fcfec8bc0c433b62036d864cad02e006c191b7ddaca9f581e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:21.0.0.3-kernel-java11-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:49c841b26f88ae89a101ce01ba8e1c175871c96c0a70f46ba2ae08132eb8dd54
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.7 MB (109701165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a298ba9aa374e771ad4095708663b412d4ad0bd906c3cc5301bcdaf3fcf9bd8`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:29:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 14 Jul 2021 00:30:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:33:59 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Wed, 14 Jul 2021 00:35:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 14 Jul 2021 00:35:04 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 00:35:04 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 14 Jul 2021 00:35:41 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 14 Jul 2021 03:57:41 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 03:57:41 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 04:16:03 GMT
ARG EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f
# Wed, 14 Jul 2021 04:16:03 GMT
ARG NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8
# Wed, 14 Jul 2021 04:16:04 GMT
ARG NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075
# Wed, 14 Jul 2021 04:16:04 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.3 org.opencontainers.image.revision=cl210320210309-1101 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 04:16:04 GMT
ENV LIBERTY_VERSION=21.0.0_03
# Wed, 14 Jul 2021 04:16:04 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 04:16:04 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 04:16:13 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:16:13 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 04:16:13 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.3 BuildLabel=cl210320210309-1101
# Wed, 14 Jul 2021 04:16:13 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 04:16:15 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 04:16:15 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 04:16:15 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 04:16:16 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 04:16:24 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 04:16:24 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 14 Jul 2021 04:16:25 GMT
USER 1001
# Wed, 14 Jul 2021 04:16:25 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 04:16:25 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 04:16:25 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1182b8c86e6bb404b0d40d2cdcdcaf4347c5aad464143625307b362caff690`  
		Last Modified: Wed, 14 Jul 2021 00:44:02 GMT  
		Size: 16.0 MB (16033076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1461af6857aed41d09a8ce6e2447ad52c9cdf1e6fe2f19ddaa2ab35d21aa1b`  
		Last Modified: Wed, 14 Jul 2021 00:50:41 GMT  
		Size: 44.4 MB (44382137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b538d86edfd8bb98ca5958e79321f730b01a2adc10244bd8ff7abf2aea9b8d8`  
		Last Modified: Wed, 14 Jul 2021 00:50:36 GMT  
		Size: 4.1 MB (4134048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f289b9688849f2751466d4c24cc0ff90b3064d8ab25868671628829902cbf1d`  
		Last Modified: Wed, 14 Jul 2021 04:27:35 GMT  
		Size: 14.1 MB (14087084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bf925863e963d52a59aca1d42c1e75c75b02689d267a56ecb716c53300efbd`  
		Last Modified: Wed, 14 Jul 2021 04:27:31 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a294d7a7685d83363812d4d061e907766fe5eaa462a9c38e60ecb9f933574ca`  
		Last Modified: Wed, 14 Jul 2021 04:27:31 GMT  
		Size: 9.6 KB (9552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dfa9f9e49bd150d5fa52e6c91fed6ccbbe3b20b0d91972618d87fc513b86758`  
		Last Modified: Wed, 14 Jul 2021 04:27:31 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da039d2151be24f85d90e6a6c2038bd3cbd2511b0d2762c3ef3571bea640b35e`  
		Last Modified: Wed, 14 Jul 2021 04:27:31 GMT  
		Size: 10.5 KB (10536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95339fd4836ffd77fe4dee0c06ad8ca6eb46d11c66359346d5fc240789be9e03`  
		Last Modified: Wed, 14 Jul 2021 04:27:32 GMT  
		Size: 2.5 MB (2477910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.3-kernel-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:ddb955f0e10897c5897815d4374acf44c69801c0eaf5cb44b65e6b91caedad37
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.4 MB (115435943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5999f12c108d361e237c9dfc34d104ef3a3ab5460e668056ac35eef0bb736e`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 01:29:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 01:31:53 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:41:26 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Fri, 18 Jun 2021 01:43:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 01:43:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 01:43:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 18 Jun 2021 01:44:39 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 09 Jul 2021 12:06:18 GMT
ARG VERBOSE=false
# Fri, 09 Jul 2021 12:06:22 GMT
ARG OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:42:07 GMT
ARG EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f
# Fri, 09 Jul 2021 12:42:15 GMT
ARG NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8
# Fri, 09 Jul 2021 12:42:19 GMT
ARG NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075
# Fri, 09 Jul 2021 12:42:22 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.3 org.opencontainers.image.revision=cl210320210309-1101 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 09 Jul 2021 12:42:25 GMT
ENV LIBERTY_VERSION=21.0.0_03
# Fri, 09 Jul 2021 12:42:29 GMT
ARG LIBERTY_URL
# Fri, 09 Jul 2021 12:42:34 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 09 Jul 2021 12:43:09 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Jul 2021 12:43:14 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Jul 2021 12:43:17 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.3 BuildLabel=cl210320210309-1101
# Fri, 09 Jul 2021 12:43:19 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:43:30 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 09 Jul 2021 12:43:32 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Fri, 09 Jul 2021 12:43:35 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 09 Jul 2021 12:43:49 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 09 Jul 2021 12:44:09 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 09 Jul 2021 12:44:14 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 09 Jul 2021 12:44:22 GMT
USER 1001
# Fri, 09 Jul 2021 12:44:26 GMT
EXPOSE 9080 9443
# Fri, 09 Jul 2021 12:44:29 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 09 Jul 2021 12:44:32 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b268950217e490e209e0491ae6fbd3af12b4642aefad9c0039daf7b3ea0371`  
		Last Modified: Fri, 18 Jun 2021 01:52:43 GMT  
		Size: 17.2 MB (17208433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74aa12681d5d14a96459a14094fd9b08f1379e61fa1e8979b311b55b0561dead`  
		Last Modified: Fri, 18 Jun 2021 01:57:43 GMT  
		Size: 45.1 MB (45104807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee28cff75d70e071001e265878f54c811f52ab2cf95d0cc9daa0085c8e1465d`  
		Last Modified: Fri, 18 Jun 2021 01:57:35 GMT  
		Size: 3.3 MB (3284426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8934a68406748539cbf4551dd9d89c6dd83c8049d25254d23b5e9e71549796d6`  
		Last Modified: Fri, 09 Jul 2021 13:00:25 GMT  
		Size: 14.1 MB (14088106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74cb765629f5b79b860201e16fc9679609d61ecd5352b224fda39e8b75306fb8`  
		Last Modified: Fri, 09 Jul 2021 13:00:19 GMT  
		Size: 691.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3611916086aa01fff230caa7d6eaff9d395282448609309a45e3254f74a9624`  
		Last Modified: Fri, 09 Jul 2021 13:00:19 GMT  
		Size: 9.6 KB (9552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a033803b23b91de2f3d1b82c31f0924f1ed573c0f588f870d87213b2b8058d`  
		Last Modified: Fri, 09 Jul 2021 13:00:19 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa019c53c1dc63a01b9a94250393a989f17bb8c8ffcafe66356891316deda4d`  
		Last Modified: Fri, 09 Jul 2021 13:00:19 GMT  
		Size: 10.5 KB (10541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfbb2936eb2c30638645c0cc0e459731004310f03bc7ec16f4cf3951270cee2`  
		Last Modified: Fri, 09 Jul 2021 13:00:19 GMT  
		Size: 2.5 MB (2450872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.3-kernel-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:4b2bcb85e5d0a3c5067beec96244d971d33493e020fd93a3cab129b54b607021
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107089352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5760f7b54aaaedc04ec9ff26695a6aa35cbfbfce57c251f8763648d3e581f54c`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:34 GMT
ADD file:ae5354f89d91eedd0614e3e97ee59fd6e23254923062c288d775e19b137dfd1c in / 
# Tue, 13 Jul 2021 22:53:36 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:18:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Jul 2021 23:18:55 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:23:22 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Tue, 13 Jul 2021 23:24:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 13 Jul 2021 23:24:37 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jul 2021 23:24:37 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 13 Jul 2021 23:25:12 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 14 Jul 2021 00:26:14 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 00:26:15 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:50:36 GMT
ARG EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f
# Wed, 14 Jul 2021 00:50:36 GMT
ARG NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8
# Wed, 14 Jul 2021 00:50:37 GMT
ARG NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075
# Wed, 14 Jul 2021 00:50:37 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.3 org.opencontainers.image.revision=cl210320210309-1101 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 00:50:37 GMT
ENV LIBERTY_VERSION=21.0.0_03
# Wed, 14 Jul 2021 00:50:37 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 00:50:38 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 00:50:46 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:50:46 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 00:50:47 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.3 BuildLabel=cl210320210309-1101
# Wed, 14 Jul 2021 00:50:47 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:50:48 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 00:50:48 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 00:50:48 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 00:50:49 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 00:50:55 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 00:50:55 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 14 Jul 2021 00:50:55 GMT
USER 1001
# Wed, 14 Jul 2021 00:50:56 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 00:50:56 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 00:50:56 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:761fa758059faa0c80b0b90fcbcc192fc7f573da055460d5b3f019e0faceeb7a`  
		Last Modified: Tue, 13 Jul 2021 22:55:47 GMT  
		Size: 27.1 MB (27149318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0237838e148d45cea54b0d86c053131b4152f4928836cbb3a0c83ba79b538728`  
		Last Modified: Tue, 13 Jul 2021 23:32:23 GMT  
		Size: 15.7 MB (15741695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454768ac3fd4bd9b5536afd4e03c6c369d7eae1ee6b240b461dace5364b911f5`  
		Last Modified: Tue, 13 Jul 2021 23:36:09 GMT  
		Size: 43.8 MB (43840969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add6cc1d828e7c42608c4398d9d18baceea2e5104c4ff50d96eba8015aa4a896`  
		Last Modified: Tue, 13 Jul 2021 23:36:03 GMT  
		Size: 3.8 MB (3845109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53fe2ec5661d485ebb553e33cda7a75124d3d3326c46d78213cb174cc96167c`  
		Last Modified: Wed, 14 Jul 2021 01:02:18 GMT  
		Size: 14.1 MB (14087271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5bc84b15bc784178893508bc8b5b06692b70b227e0b63ddf51f048db8c0511`  
		Last Modified: Wed, 14 Jul 2021 01:02:15 GMT  
		Size: 690.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e366c33bb2a97777af7ed55c843d087a71d5ab3757e2f7e0a045518fb2d74182`  
		Last Modified: Wed, 14 Jul 2021 01:02:15 GMT  
		Size: 9.6 KB (9554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc02acc0088e74a2310df1f647646139f169f60b4434ae4e06574679ff6bc8d`  
		Last Modified: Wed, 14 Jul 2021 01:02:15 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31128c991901bd973dbe86c9c8dda73f01fc3f0bb2a867957560ed83bcd660db`  
		Last Modified: Wed, 14 Jul 2021 01:02:15 GMT  
		Size: 10.5 KB (10535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd07e9a6d1403fa04e2aef9855016844412f4982f78ae5999eb7a5edb34c449`  
		Last Modified: Wed, 14 Jul 2021 01:02:15 GMT  
		Size: 2.4 MB (2403939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:21.0.0.3-kernel-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:69edf41267fbe46ee9cc7d0721d9c034f8d4c34a1ef2a15bccbf754b074d860b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:21.0.0.3-kernel-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:1c24107703537e1b07dda8a80adada33abe57fd564a3a2d82aa577455ac73580
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178858654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc74226f2670692d4fa3278ef78b453213127e2b8a425fa5a533d1261f5eef9`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:19:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:19:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:19:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:19:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:19:52 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 14 Jul 2021 03:57:10 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 03:57:10 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 04:15:33 GMT
ARG EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f
# Wed, 14 Jul 2021 04:15:33 GMT
ARG NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8
# Wed, 14 Jul 2021 04:15:33 GMT
ARG NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075
# Wed, 14 Jul 2021 04:15:34 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.3 org.opencontainers.image.revision=cl210320210309-1101 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 04:15:34 GMT
ENV LIBERTY_VERSION=21.0.0_03
# Wed, 14 Jul 2021 04:15:34 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 04:15:34 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 04:15:44 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:15:44 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 04:15:45 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.3 BuildLabel=cl210320210309-1101
# Wed, 14 Jul 2021 04:15:45 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 04:15:46 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 04:15:47 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 04:15:47 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 04:15:48 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 04:15:58 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 04:15:58 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 14 Jul 2021 04:15:58 GMT
USER 1001
# Wed, 14 Jul 2021 04:15:58 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 04:15:58 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 04:15:59 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22821a14390caaab5b1f7ca9feb8e54ce64d3d81ca1fa64c6f1eee32ae92da5b`  
		Last Modified: Tue, 13 Jul 2021 23:23:03 GMT  
		Size: 3.0 MB (2959004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4403b30ef5ef8f7b37c65fc3d0a0e0d7e0fca7451dd9b42a43bee1de1f389c09`  
		Last Modified: Tue, 13 Jul 2021 23:23:13 GMT  
		Size: 129.5 MB (129536228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10d72199745009b56f78f418f97a9095a454904bad394f993393f7f1feecfd5`  
		Last Modified: Wed, 14 Jul 2021 04:27:23 GMT  
		Size: 14.0 MB (13988948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b518013c5cc1badd31dae723dbdcde785d271e7419238daf4ee93e6ac8a53187`  
		Last Modified: Wed, 14 Jul 2021 04:27:19 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea73ce22784ac15b48d7129d677b0d883e3ebb13a3c8bf0fa532f3d2541fddc`  
		Last Modified: Wed, 14 Jul 2021 04:27:19 GMT  
		Size: 9.6 KB (9553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afca36b12789fe4a6126946fb176e685863cdc7c9b588a344d7c332c9ecf7933`  
		Last Modified: Wed, 14 Jul 2021 04:27:19 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f08301c4eea896a7850e76947d8c0e3d2cfaac499f62df4e0ecf8dd366b148`  
		Last Modified: Wed, 14 Jul 2021 04:27:19 GMT  
		Size: 10.5 KB (10535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66221921700b8697ef17a84450f187b06790bd1ee1011fce836f6ac5160ffaa9`  
		Last Modified: Wed, 14 Jul 2021 04:27:20 GMT  
		Size: 5.6 MB (5647276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.3-kernel-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:c3ee622ab35a7c0330832577aec3ad3a06aeeb832aad8d1ec9cff50c63a8f2f0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.8 MB (181819411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0636f07c1d54f045962b179eaf425c878db701ee2395455c4bf32c64fb77ae`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 17 Jun 2021 23:24:58 GMT
ADD file:33bc9edd94d5731da919e83ed38bd4aa7daffcb5f629d93bbde112a795c79d48 in / 
# Thu, 17 Jun 2021 23:25:03 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:01:35 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 18 Jun 2021 02:02:36 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:02:42 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Fri, 18 Jun 2021 02:03:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 18 Jun 2021 02:04:05 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 09 Jul 2021 12:02:21 GMT
ARG VERBOSE=false
# Fri, 09 Jul 2021 12:02:27 GMT
ARG OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:38:38 GMT
ARG EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f
# Fri, 09 Jul 2021 12:38:42 GMT
ARG NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8
# Fri, 09 Jul 2021 12:38:45 GMT
ARG NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075
# Fri, 09 Jul 2021 12:38:49 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.3 org.opencontainers.image.revision=cl210320210309-1101 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 09 Jul 2021 12:38:54 GMT
ENV LIBERTY_VERSION=21.0.0_03
# Fri, 09 Jul 2021 12:39:00 GMT
ARG LIBERTY_URL
# Fri, 09 Jul 2021 12:39:11 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 09 Jul 2021 12:40:19 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Jul 2021 12:40:26 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Jul 2021 12:40:30 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.3 BuildLabel=cl210320210309-1101
# Fri, 09 Jul 2021 12:40:33 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:40:44 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 09 Jul 2021 12:40:45 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Fri, 09 Jul 2021 12:40:47 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 09 Jul 2021 12:41:11 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 09 Jul 2021 12:41:30 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 09 Jul 2021 12:41:33 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Fri, 09 Jul 2021 12:41:38 GMT
USER 1001
# Fri, 09 Jul 2021 12:41:42 GMT
EXPOSE 9080 9443
# Fri, 09 Jul 2021 12:41:45 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 09 Jul 2021 12:41:48 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:4e37c2419ee7d7e826be5c6ee69243351aaf456d6527714660cf7e7015491051`  
		Last Modified: Thu, 17 Jun 2021 23:28:22 GMT  
		Size: 30.4 MB (30425356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8d177e4917900437a3445272639bed389b718cc65a87346ba94f6d99327f34`  
		Last Modified: Fri, 18 Jun 2021 02:07:44 GMT  
		Size: 3.1 MB (3082963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09af03e0818b00fa01f51019b91f996a958b5ffb6b7dcd23e88d4d0df759f391`  
		Last Modified: Fri, 18 Jun 2021 02:07:59 GMT  
		Size: 129.1 MB (129059791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c73ab0e009309ce6891ae8bb263b6aebd59105c1eb9179d42976e3b93c2099`  
		Last Modified: Fri, 09 Jul 2021 13:00:09 GMT  
		Size: 14.0 MB (13989397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48db10faa5d6301afba460ec5343c9d17672aacf2d5d74384f76ffe4ef38cc07`  
		Last Modified: Fri, 09 Jul 2021 13:00:04 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51767e8a50e913466e46c80f96d48d88fb454c9ec7a3048552bd9132f998571`  
		Last Modified: Fri, 09 Jul 2021 13:00:03 GMT  
		Size: 9.6 KB (9557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c2c208d08e4e5682c6c9e5af0e840de4b302a43926d712d0e24c860fe736e7`  
		Last Modified: Fri, 09 Jul 2021 13:00:03 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2c1b85c34fe4c104929c4b3dcaaeabfff39b4d723c1a327a7fa006c75c21ef`  
		Last Modified: Fri, 09 Jul 2021 13:00:04 GMT  
		Size: 10.5 KB (10548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa00e1f22f20345c00e9b83e59795ccede28e9d2fc3a478ceda6d0e0a2b5cfde`  
		Last Modified: Fri, 09 Jul 2021 13:00:04 GMT  
		Size: 5.2 MB (5240830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.3-kernel-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:e9aa5875c032c6920289b2640a029975b3bb978808b5c2ae8b8e10eb9ec48e2a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174569943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:388b78f3941d0c0a40901de4bab9fd39a82359b254e4f15f34b4a5c378413bdb`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:22 GMT
ADD file:9e621b1dfa735f1a89553f154f2a2a6f669ff610236d92d6ebf37d1f378d8ec0 in / 
# Tue, 13 Jul 2021 22:53:24 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:12:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:12:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:12:20 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:13:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:13:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 14 Jul 2021 00:25:32 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 00:25:32 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:50:04 GMT
ARG EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f
# Wed, 14 Jul 2021 00:50:04 GMT
ARG NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8
# Wed, 14 Jul 2021 00:50:05 GMT
ARG NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075
# Wed, 14 Jul 2021 00:50:05 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.3 org.opencontainers.image.revision=cl210320210309-1101 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 00:50:05 GMT
ENV LIBERTY_VERSION=21.0.0_03
# Wed, 14 Jul 2021 00:50:05 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 00:50:05 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 00:50:16 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:50:16 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 00:50:16 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.3 BuildLabel=cl210320210309-1101
# Wed, 14 Jul 2021 00:50:17 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:50:18 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 00:50:18 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 00:50:18 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 00:50:19 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 00:50:27 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 00:50:28 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Wed, 14 Jul 2021 00:50:28 GMT
USER 1001
# Wed, 14 Jul 2021 00:50:28 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 00:50:28 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 00:50:29 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:3287e09e36098b10234ccc1f8db0b48e2027ca7caa353a362d65f9b017ab802e`  
		Last Modified: Tue, 13 Jul 2021 22:55:34 GMT  
		Size: 25.4 MB (25365649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6fe4e2b151f33398a6ef48bbb5d9ace538aa5ecf3fab9182babc3a85b9166b`  
		Last Modified: Tue, 13 Jul 2021 23:16:59 GMT  
		Size: 2.7 MB (2676828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b436dddc9b46f3b9e70224bb7eab52e58419d071c07f16f9ce63c77c81e5e24`  
		Last Modified: Tue, 13 Jul 2021 23:17:08 GMT  
		Size: 126.7 MB (126676530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1998064bd8d8ea7ff4e9a8365c04a9f64b6710120fd5ddc59249584f99af2be1`  
		Last Modified: Wed, 14 Jul 2021 01:02:09 GMT  
		Size: 14.0 MB (13988617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9fc4be8562cd0c12bde799f87024d3f07d07e24b45c8c6f7b3b41825b150587`  
		Last Modified: Wed, 14 Jul 2021 01:02:06 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c647ec4aa35a0e55a99d40254aafcf8e578a6be6fcddcf52f9b66f105fdf89`  
		Last Modified: Wed, 14 Jul 2021 01:02:06 GMT  
		Size: 9.6 KB (9555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dca87ec5945d5239dee8c6f64c27da567269daece09afdf1accc33fe0807487`  
		Last Modified: Wed, 14 Jul 2021 01:02:06 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8201e76ed533104079b785b672c2bcb501df13efb6fb9b26d47b56f430190812`  
		Last Modified: Wed, 14 Jul 2021 01:02:06 GMT  
		Size: 10.5 KB (10537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec9f2ba4cb485906aeae84a935931a97c8b30779a7b08af65bbdee9e9ec2f5c`  
		Last Modified: Wed, 14 Jul 2021 01:02:07 GMT  
		Size: 5.8 MB (5841259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:21.0.0.6-full-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:4b95510780e4c73013e0018502b108090fdcb7f07f4911098e8548bdf62c1aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:21.0.0.6-full-java11-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:320aebbf606620cf7ebb2cc47974896a55adb442465ea15fee5e8480261f9fe4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.8 MB (331821041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea111e6f780b4e4c6c2fd961fe7fa5c5eb2096b5eeec4dbfd388b144b42296df`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:29:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 14 Jul 2021 00:30:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:33:59 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Wed, 14 Jul 2021 00:35:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 14 Jul 2021 00:35:04 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 00:35:04 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 14 Jul 2021 00:35:41 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 14 Jul 2021 03:57:41 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 03:57:41 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 04:06:59 GMT
ARG EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27
# Wed, 14 Jul 2021 04:07:00 GMT
ARG NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c
# Wed, 14 Jul 2021 04:07:00 GMT
ARG NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499
# Wed, 14 Jul 2021 04:07:00 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.6 org.opencontainers.image.revision=cl210620210527-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 04:07:00 GMT
ENV LIBERTY_VERSION=21.0.0_06
# Wed, 14 Jul 2021 04:07:00 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 04:07:01 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 04:07:09 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:07:10 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 04:07:10 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.6 BuildLabel=cl210620210527-1900
# Wed, 14 Jul 2021 04:07:10 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 04:07:11 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 04:07:11 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 04:07:12 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 04:07:13 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 04:07:21 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 04:07:21 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 14 Jul 2021 04:07:21 GMT
USER 1001
# Wed, 14 Jul 2021 04:07:21 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 04:07:21 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 04:07:22 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 14 Jul 2021 04:11:36 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 04:11:37 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 14 Jul 2021 04:14:43 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Wed, 14 Jul 2021 04:14:44 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 14 Jul 2021 04:15:19 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1182b8c86e6bb404b0d40d2cdcdcaf4347c5aad464143625307b362caff690`  
		Last Modified: Wed, 14 Jul 2021 00:44:02 GMT  
		Size: 16.0 MB (16033076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1461af6857aed41d09a8ce6e2447ad52c9cdf1e6fe2f19ddaa2ab35d21aa1b`  
		Last Modified: Wed, 14 Jul 2021 00:50:41 GMT  
		Size: 44.4 MB (44382137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b538d86edfd8bb98ca5958e79321f730b01a2adc10244bd8ff7abf2aea9b8d8`  
		Last Modified: Wed, 14 Jul 2021 00:50:36 GMT  
		Size: 4.1 MB (4134048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef0bbfeea758c476384e9605ab5888ce1aa955d14beea7d6b59689de0420a1d`  
		Last Modified: Wed, 14 Jul 2021 04:26:21 GMT  
		Size: 14.2 MB (14170206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1949edf6dfd720cbe3b4db4b69144cc9a47ed957227f5916c818da63f5fbab0f`  
		Last Modified: Wed, 14 Jul 2021 04:26:17 GMT  
		Size: 692.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e28b451a06c3b3420295c4d524f6e217e0992a3809e028e759f8961bb448053`  
		Last Modified: Wed, 14 Jul 2021 04:26:16 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bb87ccb54565ba00adcdfeac59ac41a02432d089efb72aacc2583ceb4658a3`  
		Last Modified: Wed, 14 Jul 2021 04:26:16 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9e1223c0f1c9d3f4e73d02025c6a102631ca797479be488ef7a1df5399feee`  
		Last Modified: Wed, 14 Jul 2021 04:26:16 GMT  
		Size: 10.7 KB (10653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c676078c1f2104917c9c73a0559974c6fdfb41180a14f6d5472a4043a74bf7ab`  
		Last Modified: Wed, 14 Jul 2021 04:26:17 GMT  
		Size: 2.5 MB (2485456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0cb408c53240611f47c83c4fb9cb6b04002c8daa842ebc8800198121cb0efc`  
		Last Modified: Wed, 14 Jul 2021 04:27:11 GMT  
		Size: 207.8 MB (207777145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8f430f0af1da1c85468e1b862276b6d74daeb5c8355c08f5c147d09618963c`  
		Last Modified: Wed, 14 Jul 2021 04:26:58 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b97663a3f46d7e4e992983170c42f79786b63d31610a2945069ffc9e4ead208`  
		Last Modified: Wed, 14 Jul 2021 04:27:01 GMT  
		Size: 14.3 MB (14250879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.6-full-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:c76f6374a9cbc74379f6ab44acdeb634ac4c004cfc5cfe5425b183a3c4d7c087
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.7 MB (335714137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98ed3c1b4ae56fae9ee0b92bdff97777bb467cfa6b01a3ec2614786d953c911`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 01:29:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 01:31:53 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:41:26 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Fri, 18 Jun 2021 01:43:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 01:43:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 01:43:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 18 Jun 2021 01:44:39 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 09 Jul 2021 12:06:18 GMT
ARG VERBOSE=false
# Fri, 09 Jul 2021 12:06:22 GMT
ARG OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:24:14 GMT
ARG EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27
# Fri, 09 Jul 2021 12:24:18 GMT
ARG NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c
# Fri, 09 Jul 2021 12:24:26 GMT
ARG NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499
# Fri, 09 Jul 2021 12:24:29 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.6 org.opencontainers.image.revision=cl210620210527-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 09 Jul 2021 12:24:33 GMT
ENV LIBERTY_VERSION=21.0.0_06
# Fri, 09 Jul 2021 12:24:35 GMT
ARG LIBERTY_URL
# Fri, 09 Jul 2021 12:24:40 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 09 Jul 2021 12:25:27 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Jul 2021 12:25:38 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Jul 2021 12:25:44 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.6 BuildLabel=cl210620210527-1900
# Fri, 09 Jul 2021 12:25:47 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:25:56 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 09 Jul 2021 12:25:57 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Fri, 09 Jul 2021 12:25:59 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 09 Jul 2021 12:26:12 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 09 Jul 2021 12:26:34 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 09 Jul 2021 12:26:40 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 09 Jul 2021 12:26:44 GMT
USER 1001
# Fri, 09 Jul 2021 12:26:47 GMT
EXPOSE 9080 9443
# Fri, 09 Jul 2021 12:26:52 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 09 Jul 2021 12:26:57 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 09 Jul 2021 12:32:26 GMT
ARG VERBOSE=false
# Fri, 09 Jul 2021 12:32:29 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 09 Jul 2021 12:37:00 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Fri, 09 Jul 2021 12:37:03 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 09 Jul 2021 12:38:16 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b268950217e490e209e0491ae6fbd3af12b4642aefad9c0039daf7b3ea0371`  
		Last Modified: Fri, 18 Jun 2021 01:52:43 GMT  
		Size: 17.2 MB (17208433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74aa12681d5d14a96459a14094fd9b08f1379e61fa1e8979b311b55b0561dead`  
		Last Modified: Fri, 18 Jun 2021 01:57:43 GMT  
		Size: 45.1 MB (45104807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee28cff75d70e071001e265878f54c811f52ab2cf95d0cc9daa0085c8e1465d`  
		Last Modified: Fri, 18 Jun 2021 01:57:35 GMT  
		Size: 3.3 MB (3284426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8bc0a64b2ab3278cdb9ab339783bb0cceaa701a7ce33da27f707ceaa008ce1`  
		Last Modified: Fri, 09 Jul 2021 12:58:50 GMT  
		Size: 14.2 MB (14171103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2c4f44ccce02a2525ee43a5efcf3e05abce2df913b365acfeebae8fb73084f`  
		Last Modified: Fri, 09 Jul 2021 12:58:45 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f325ef08d4de94642f048d7dea29eaeeab3efb1b593c7e8bde31199de14141b5`  
		Last Modified: Fri, 09 Jul 2021 12:58:45 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a874b9b19c9958221409a23916f91e1de0961b28a6a052ca34f062ab73b0a47c`  
		Last Modified: Fri, 09 Jul 2021 12:58:44 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41458d6be3c66f6faeb01bd128cbeb0c574d909fb02069ef57f6114b88a0a3e4`  
		Last Modified: Fri, 09 Jul 2021 12:58:44 GMT  
		Size: 10.7 KB (10663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93f402e5fea825689ca243ac3a9b193f0745ae31a1c0490c2bdc36748330352`  
		Last Modified: Fri, 09 Jul 2021 12:58:45 GMT  
		Size: 2.5 MB (2466657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0352954fa3ad68112fb78af2d665d8dd512ce8fcee6c03447e11336b43cab0`  
		Last Modified: Fri, 09 Jul 2021 12:59:54 GMT  
		Size: 207.8 MB (207777818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7eda9c8c1c5a0cf2bcc5edae2864b4a3e6542812c58bb18b52ca2bd5560aa6a`  
		Last Modified: Fri, 09 Jul 2021 12:59:30 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab136454b407f54cd5951cc2ec7f1246fb79d8e5beb7c40344e4ebc822c198bf`  
		Last Modified: Fri, 09 Jul 2021 12:59:34 GMT  
		Size: 12.4 MB (12400400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.6-full-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:53af3683933e80252a1d1a48da08c8d976779e4ff2f71486312b8cada9824be6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.7 MB (437726433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d41552212980fc36f3ce2961e7134878ad256dc4a5d5dd52a908e5d01439ebd`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:34 GMT
ADD file:ae5354f89d91eedd0614e3e97ee59fd6e23254923062c288d775e19b137dfd1c in / 
# Tue, 13 Jul 2021 22:53:36 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:18:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Jul 2021 23:18:55 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:23:22 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Tue, 13 Jul 2021 23:24:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 13 Jul 2021 23:24:37 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jul 2021 23:24:37 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 13 Jul 2021 23:25:12 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 14 Jul 2021 00:26:14 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 00:26:15 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:39:15 GMT
ARG EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27
# Wed, 14 Jul 2021 00:39:17 GMT
ARG NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c
# Wed, 14 Jul 2021 00:39:17 GMT
ARG NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499
# Wed, 14 Jul 2021 00:39:19 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.6 org.opencontainers.image.revision=cl210620210527-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 00:39:22 GMT
ENV LIBERTY_VERSION=21.0.0_06
# Wed, 14 Jul 2021 00:39:25 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 00:39:27 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 00:39:39 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:39:40 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 00:39:44 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.6 BuildLabel=cl210620210527-1900
# Wed, 14 Jul 2021 00:39:49 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:39:56 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 00:40:05 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 00:40:09 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 00:40:16 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 00:40:31 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 00:40:34 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 14 Jul 2021 00:40:36 GMT
USER 1001
# Wed, 14 Jul 2021 00:40:38 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 00:40:40 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 00:40:41 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 14 Jul 2021 00:45:41 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 00:45:42 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 14 Jul 2021 00:48:57 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Wed, 14 Jul 2021 00:49:00 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 14 Jul 2021 00:49:36 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:761fa758059faa0c80b0b90fcbcc192fc7f573da055460d5b3f019e0faceeb7a`  
		Last Modified: Tue, 13 Jul 2021 22:55:47 GMT  
		Size: 27.1 MB (27149318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0237838e148d45cea54b0d86c053131b4152f4928836cbb3a0c83ba79b538728`  
		Last Modified: Tue, 13 Jul 2021 23:32:23 GMT  
		Size: 15.7 MB (15741695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454768ac3fd4bd9b5536afd4e03c6c369d7eae1ee6b240b461dace5364b911f5`  
		Last Modified: Tue, 13 Jul 2021 23:36:09 GMT  
		Size: 43.8 MB (43840969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add6cc1d828e7c42608c4398d9d18baceea2e5104c4ff50d96eba8015aa4a896`  
		Last Modified: Tue, 13 Jul 2021 23:36:03 GMT  
		Size: 3.8 MB (3845109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac3c9edbf35b0fd0a98fd6fbf8733b14c64ec733db29fbc66237c96152675aa`  
		Last Modified: Wed, 14 Jul 2021 01:01:03 GMT  
		Size: 14.2 MB (14170211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a6f9c27ddf5042924151c4163db1d8c77d5e27815c6dd4ab6ac44ca4359ca9`  
		Last Modified: Wed, 14 Jul 2021 01:01:00 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d2155ef21ae68a5433eb02ce485c2846126483d0c16493ccd7957609dee300`  
		Last Modified: Wed, 14 Jul 2021 01:01:00 GMT  
		Size: 9.7 KB (9671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d250bdeb35966d93fe63d5db07ed72f480b22788fb024b0db509336916670a`  
		Last Modified: Wed, 14 Jul 2021 01:01:00 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6267d136ac6f15d5e07083f359200b352cfe64dd46f91d63dbb2f17a368ba1f`  
		Last Modified: Wed, 14 Jul 2021 01:01:00 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ede16eb2950611c95a8ac88bde8aeca3b97581e05e64a4c1fd876c1775f34b`  
		Last Modified: Wed, 14 Jul 2021 01:01:00 GMT  
		Size: 2.4 MB (2442032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bd8f162c95ef51641a0784a22b409e6a6a34e0df0a2eaa838acc39ec114cfd`  
		Last Modified: Wed, 14 Jul 2021 01:01:45 GMT  
		Size: 207.8 MB (207777848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ce9b715e549c57564afaeec98691705c9acde4206251da3a91de09972b1139`  
		Last Modified: Wed, 14 Jul 2021 01:01:35 GMT  
		Size: 944.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d2d1b68276ba212f978ea9dd960e5544fa273a1c0d9e3e47d9c502bca53198`  
		Last Modified: Wed, 14 Jul 2021 01:01:59 GMT  
		Size: 122.7 MB (122737018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:21.0.0.6-full-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:1bccc2a81422664256048bf924d72ec1e3a447b0cdb594b84272b928d55878ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:21.0.0.6-full-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:c852435d7a046a91e0793a6f2727371a264c82598e10ba821cfe995e76a041df
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.4 MB (402436308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61763dbcba40e11bfae07823e14ac8711c62a0151251b12d37cead6f26dde1a`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:19:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:19:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:19:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:19:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:19:52 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 14 Jul 2021 03:57:10 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 03:57:10 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 04:06:29 GMT
ARG EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27
# Wed, 14 Jul 2021 04:06:29 GMT
ARG NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c
# Wed, 14 Jul 2021 04:06:30 GMT
ARG NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499
# Wed, 14 Jul 2021 04:06:30 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.6 org.opencontainers.image.revision=cl210620210527-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 04:06:30 GMT
ENV LIBERTY_VERSION=21.0.0_06
# Wed, 14 Jul 2021 04:06:30 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 04:06:30 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 04:06:43 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:06:43 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 04:06:43 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.6 BuildLabel=cl210620210527-1900
# Wed, 14 Jul 2021 04:06:44 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 04:06:45 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 04:06:45 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 04:06:45 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 04:06:46 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 04:06:55 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 04:06:56 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 14 Jul 2021 04:06:56 GMT
USER 1001
# Wed, 14 Jul 2021 04:06:56 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 04:06:56 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 04:06:56 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 14 Jul 2021 04:07:25 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 04:07:25 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 14 Jul 2021 04:10:49 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Wed, 14 Jul 2021 04:10:50 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 14 Jul 2021 04:11:26 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22821a14390caaab5b1f7ca9feb8e54ce64d3d81ca1fa64c6f1eee32ae92da5b`  
		Last Modified: Tue, 13 Jul 2021 23:23:03 GMT  
		Size: 3.0 MB (2959004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4403b30ef5ef8f7b37c65fc3d0a0e0d7e0fca7451dd9b42a43bee1de1f389c09`  
		Last Modified: Tue, 13 Jul 2021 23:23:13 GMT  
		Size: 129.5 MB (129536228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745de4a9e38ea590f2768cf0e66717a76350c9b6d688e5b83d9ed54bf0431f00`  
		Last Modified: Wed, 14 Jul 2021 04:26:08 GMT  
		Size: 14.1 MB (14073365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3ebf216280a903a6659252558177cdc90c1ddd6a1c8103512d78bc2b25319c`  
		Last Modified: Wed, 14 Jul 2021 04:26:04 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d15611894f8e05f294b6acfcc612247f1d05e0a6ab05dc8b572360b7b315a65`  
		Last Modified: Wed, 14 Jul 2021 04:26:04 GMT  
		Size: 9.7 KB (9674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a407bfecf93a5cb88bf86146a7e1c56d02b511a41a44a691f95c437dcc963a`  
		Last Modified: Wed, 14 Jul 2021 04:26:04 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe5ee71fcca93adfda57e9f302b9d6fd150cb033f117515d45efedf131ac0ed`  
		Last Modified: Wed, 14 Jul 2021 04:26:04 GMT  
		Size: 10.7 KB (10664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe599905aac100721484ffd10a0f8bbdd6a2c9343fcb7161c0a9ac6369af6dd3`  
		Last Modified: Wed, 14 Jul 2021 04:26:05 GMT  
		Size: 5.7 MB (5726690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5acb1fac0663b004bd7e7a49c1e9d7086938920dba7909a8b1ad2d1f8778111f`  
		Last Modified: Wed, 14 Jul 2021 04:26:45 GMT  
		Size: 207.8 MB (207778198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83e3a990ff627a5a795525d1cf2f3e653f79edfb61628742830577061ba51fa`  
		Last Modified: Wed, 14 Jul 2021 04:26:28 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ab8ca85094f247013df0f85ac3288475c52587eac2c6f7e2b5c569eb4fdd05`  
		Last Modified: Wed, 14 Jul 2021 04:26:31 GMT  
		Size: 15.6 MB (15634420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.6-full-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:03e3c655e16fce6517dbd46d9ee3e05e1ad7bc1b0814f52a0100424c8ee3b50f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.5 MB (403549432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85f58598db32623fc8600ebaacfb2a0955ff2d4eed3f363515968898f100a32`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 17 Jun 2021 23:24:58 GMT
ADD file:33bc9edd94d5731da919e83ed38bd4aa7daffcb5f629d93bbde112a795c79d48 in / 
# Thu, 17 Jun 2021 23:25:03 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:01:35 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 18 Jun 2021 02:02:36 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:02:42 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Fri, 18 Jun 2021 02:03:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 18 Jun 2021 02:04:05 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 09 Jul 2021 12:02:21 GMT
ARG VERBOSE=false
# Fri, 09 Jul 2021 12:02:27 GMT
ARG OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:21:33 GMT
ARG EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27
# Fri, 09 Jul 2021 12:21:40 GMT
ARG NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c
# Fri, 09 Jul 2021 12:21:44 GMT
ARG NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499
# Fri, 09 Jul 2021 12:21:47 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.6 org.opencontainers.image.revision=cl210620210527-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 09 Jul 2021 12:21:54 GMT
ENV LIBERTY_VERSION=21.0.0_06
# Fri, 09 Jul 2021 12:21:58 GMT
ARG LIBERTY_URL
# Fri, 09 Jul 2021 12:22:03 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 09 Jul 2021 12:22:39 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Jul 2021 12:22:44 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Jul 2021 12:22:47 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.6 BuildLabel=cl210620210527-1900
# Fri, 09 Jul 2021 12:22:53 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:23:03 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 09 Jul 2021 12:23:05 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Fri, 09 Jul 2021 12:23:06 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 09 Jul 2021 12:23:16 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 09 Jul 2021 12:23:43 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 09 Jul 2021 12:23:50 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 09 Jul 2021 12:23:54 GMT
USER 1001
# Fri, 09 Jul 2021 12:23:58 GMT
EXPOSE 9080 9443
# Fri, 09 Jul 2021 12:24:00 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 09 Jul 2021 12:24:04 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 09 Jul 2021 12:27:12 GMT
ARG VERBOSE=false
# Fri, 09 Jul 2021 12:27:20 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 09 Jul 2021 12:31:08 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Fri, 09 Jul 2021 12:31:14 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 09 Jul 2021 12:32:16 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:4e37c2419ee7d7e826be5c6ee69243351aaf456d6527714660cf7e7015491051`  
		Last Modified: Thu, 17 Jun 2021 23:28:22 GMT  
		Size: 30.4 MB (30425356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8d177e4917900437a3445272639bed389b718cc65a87346ba94f6d99327f34`  
		Last Modified: Fri, 18 Jun 2021 02:07:44 GMT  
		Size: 3.1 MB (3082963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09af03e0818b00fa01f51019b91f996a958b5ffb6b7dcd23e88d4d0df759f391`  
		Last Modified: Fri, 18 Jun 2021 02:07:59 GMT  
		Size: 129.1 MB (129059791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536fb275e646e87309efba2eb8113774342a74c4f2b949fc7e909bb27004030c`  
		Last Modified: Fri, 09 Jul 2021 12:58:34 GMT  
		Size: 14.1 MB (14073843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5eafe574ddb128ae4db89d490193ba5c1a26931b2ce1ec0f24b06097b5d2c5b`  
		Last Modified: Fri, 09 Jul 2021 12:58:29 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6d80b7905b8314e4632cc1f48c49edbf326f84d542e91698352947b9806bf5`  
		Last Modified: Fri, 09 Jul 2021 12:58:29 GMT  
		Size: 9.7 KB (9681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb948fb1402a87be7940a0930b5cfcca70800f13789188c19ec43ad79859a10`  
		Last Modified: Fri, 09 Jul 2021 12:58:29 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1c42006812bf0ce103b4fd1e747abbf28bae45fb5564c58d9f988426490eea`  
		Last Modified: Fri, 09 Jul 2021 12:58:29 GMT  
		Size: 10.7 KB (10670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0f4897d0f19c3d1e110234d55b6e4eac589923968ae5cb1a35798136e31c73`  
		Last Modified: Fri, 09 Jul 2021 12:58:30 GMT  
		Size: 5.3 MB (5309152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e630f39b90f0eaff2c7a418e2504a9126881c63b7305d17eb0f061022bc37ead`  
		Last Modified: Fri, 09 Jul 2021 12:59:20 GMT  
		Size: 207.8 MB (207778042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50eb87e9ba1d1d51bc13ca9f0bfb1903cacbf862c31631c3a4fbdd2741cdaa27`  
		Last Modified: Fri, 09 Jul 2021 12:58:59 GMT  
		Size: 953.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81c80969dc9b69a1ecf1c70fad8c45d71b34d791d555fb5e4511176355d0b55`  
		Last Modified: Fri, 09 Jul 2021 12:59:02 GMT  
		Size: 13.8 MB (13798008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.6-full-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:84146edf62194ab463ed5445e452b63f8624ca181bdd9c719563923dd00e948e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.0 MB (397991048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a992d78c72ce5d26acdf06c854136891e5d93698b31d201e19deed13a7bfa83`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:22 GMT
ADD file:9e621b1dfa735f1a89553f154f2a2a6f669ff610236d92d6ebf37d1f378d8ec0 in / 
# Tue, 13 Jul 2021 22:53:24 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:12:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:12:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:12:20 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:13:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:13:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 14 Jul 2021 00:25:32 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 00:25:32 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:37:29 GMT
ARG EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27
# Wed, 14 Jul 2021 00:37:34 GMT
ARG NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c
# Wed, 14 Jul 2021 00:37:39 GMT
ARG NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499
# Wed, 14 Jul 2021 00:37:42 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.6 org.opencontainers.image.revision=cl210620210527-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 00:37:48 GMT
ENV LIBERTY_VERSION=21.0.0_06
# Wed, 14 Jul 2021 00:37:57 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 00:38:01 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 00:38:22 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:38:26 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 00:38:27 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.6 BuildLabel=cl210620210527-1900
# Wed, 14 Jul 2021 00:38:28 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:38:29 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 00:38:30 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 00:38:30 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 00:38:32 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 00:38:45 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 00:38:46 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 14 Jul 2021 00:38:46 GMT
USER 1001
# Wed, 14 Jul 2021 00:38:46 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 00:38:47 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 00:38:49 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 14 Jul 2021 00:41:06 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 00:41:07 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 14 Jul 2021 00:44:48 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Wed, 14 Jul 2021 00:44:54 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 14 Jul 2021 00:45:30 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:3287e09e36098b10234ccc1f8db0b48e2027ca7caa353a362d65f9b017ab802e`  
		Last Modified: Tue, 13 Jul 2021 22:55:34 GMT  
		Size: 25.4 MB (25365649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6fe4e2b151f33398a6ef48bbb5d9ace538aa5ecf3fab9182babc3a85b9166b`  
		Last Modified: Tue, 13 Jul 2021 23:16:59 GMT  
		Size: 2.7 MB (2676828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b436dddc9b46f3b9e70224bb7eab52e58419d071c07f16f9ce63c77c81e5e24`  
		Last Modified: Tue, 13 Jul 2021 23:17:08 GMT  
		Size: 126.7 MB (126676530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d4bf323f1bc7511736e3431f3336ad04db6d605a39fa8d4c7d832d7675d801`  
		Last Modified: Wed, 14 Jul 2021 01:00:54 GMT  
		Size: 14.1 MB (14073138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f699a8b7ec1db46f7ca1fbf9e81ec3ee6339f7759a5e0decf32d085243e8a9f8`  
		Last Modified: Wed, 14 Jul 2021 01:00:51 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719ce25bb19c404c9005bf6c2e1f252b500259db40d1f35e0acc30aafa077ec3`  
		Last Modified: Wed, 14 Jul 2021 01:00:51 GMT  
		Size: 9.7 KB (9679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d63e66b32162554ff5618c32cd2d0a852600e9d52219f202da933a59d53160`  
		Last Modified: Wed, 14 Jul 2021 01:00:51 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d30abebb191b25f681cd178757cfe196a6ee8675b0855ecf6707d0bbd87c20a`  
		Last Modified: Wed, 14 Jul 2021 01:00:51 GMT  
		Size: 10.7 KB (10660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2408f21dad9a358a1da63043e23b2a4477cb714947b648e025c7d6d6c80f16fa`  
		Last Modified: Wed, 14 Jul 2021 01:00:52 GMT  
		Size: 6.0 MB (5966756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531733965d8136953d564ea1e7eabd98287b6b0ca74ff2810b8e7762ee409185`  
		Last Modified: Wed, 14 Jul 2021 01:01:24 GMT  
		Size: 207.8 MB (207778183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6880cb66cf1981e5ae8ab2cb3f2c5670a046fbdf3d14cc24b272e43eaaca9caf`  
		Last Modified: Wed, 14 Jul 2021 01:01:09 GMT  
		Size: 943.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2a76fcc29578453f188a1ee25487996ea110e698d4371c757b75ad4b97fa7d`  
		Last Modified: Wed, 14 Jul 2021 01:01:11 GMT  
		Size: 15.4 MB (15431706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:21.0.0.6-kernel-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:1967f7411d753579f9b0ff24ef45bb39fb2085d53c45bc27d250924590009b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:21.0.0.6-kernel-java11-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:94034578857be2e3413aa66d33f59e6a528382ebf1b42e5c4a138a0dd41ae0b3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109792075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb3bdf86468ee5b738730bf6173f974a0ceeda62a2f38a5573fe396983d551e`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:29:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 14 Jul 2021 00:30:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:33:59 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Wed, 14 Jul 2021 00:35:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 14 Jul 2021 00:35:04 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 00:35:04 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 14 Jul 2021 00:35:41 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 14 Jul 2021 03:57:41 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 03:57:41 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 04:06:59 GMT
ARG EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27
# Wed, 14 Jul 2021 04:07:00 GMT
ARG NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c
# Wed, 14 Jul 2021 04:07:00 GMT
ARG NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499
# Wed, 14 Jul 2021 04:07:00 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.6 org.opencontainers.image.revision=cl210620210527-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 04:07:00 GMT
ENV LIBERTY_VERSION=21.0.0_06
# Wed, 14 Jul 2021 04:07:00 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 04:07:01 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 04:07:09 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:07:10 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 04:07:10 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.6 BuildLabel=cl210620210527-1900
# Wed, 14 Jul 2021 04:07:10 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 04:07:11 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 04:07:11 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 04:07:12 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 04:07:13 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 04:07:21 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 04:07:21 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 14 Jul 2021 04:07:21 GMT
USER 1001
# Wed, 14 Jul 2021 04:07:21 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 04:07:21 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 04:07:22 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1182b8c86e6bb404b0d40d2cdcdcaf4347c5aad464143625307b362caff690`  
		Last Modified: Wed, 14 Jul 2021 00:44:02 GMT  
		Size: 16.0 MB (16033076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1461af6857aed41d09a8ce6e2447ad52c9cdf1e6fe2f19ddaa2ab35d21aa1b`  
		Last Modified: Wed, 14 Jul 2021 00:50:41 GMT  
		Size: 44.4 MB (44382137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b538d86edfd8bb98ca5958e79321f730b01a2adc10244bd8ff7abf2aea9b8d8`  
		Last Modified: Wed, 14 Jul 2021 00:50:36 GMT  
		Size: 4.1 MB (4134048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef0bbfeea758c476384e9605ab5888ce1aa955d14beea7d6b59689de0420a1d`  
		Last Modified: Wed, 14 Jul 2021 04:26:21 GMT  
		Size: 14.2 MB (14170206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1949edf6dfd720cbe3b4db4b69144cc9a47ed957227f5916c818da63f5fbab0f`  
		Last Modified: Wed, 14 Jul 2021 04:26:17 GMT  
		Size: 692.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e28b451a06c3b3420295c4d524f6e217e0992a3809e028e759f8961bb448053`  
		Last Modified: Wed, 14 Jul 2021 04:26:16 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bb87ccb54565ba00adcdfeac59ac41a02432d089efb72aacc2583ceb4658a3`  
		Last Modified: Wed, 14 Jul 2021 04:26:16 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9e1223c0f1c9d3f4e73d02025c6a102631ca797479be488ef7a1df5399feee`  
		Last Modified: Wed, 14 Jul 2021 04:26:16 GMT  
		Size: 10.7 KB (10653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c676078c1f2104917c9c73a0559974c6fdfb41180a14f6d5472a4043a74bf7ab`  
		Last Modified: Wed, 14 Jul 2021 04:26:17 GMT  
		Size: 2.5 MB (2485456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.6-kernel-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:eb1c2f30122b36a632ea530f30e0824986d7ffbc70ebb4464eb7057cfa9d2e6e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115534973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5776a1caf8b719fd502fe428d99d14b7a23dbf09719dd60bbf7cf9ab773496`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 01:29:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 01:31:53 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:41:26 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Fri, 18 Jun 2021 01:43:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 01:43:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 01:43:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 18 Jun 2021 01:44:39 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 09 Jul 2021 12:06:18 GMT
ARG VERBOSE=false
# Fri, 09 Jul 2021 12:06:22 GMT
ARG OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:24:14 GMT
ARG EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27
# Fri, 09 Jul 2021 12:24:18 GMT
ARG NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c
# Fri, 09 Jul 2021 12:24:26 GMT
ARG NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499
# Fri, 09 Jul 2021 12:24:29 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.6 org.opencontainers.image.revision=cl210620210527-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 09 Jul 2021 12:24:33 GMT
ENV LIBERTY_VERSION=21.0.0_06
# Fri, 09 Jul 2021 12:24:35 GMT
ARG LIBERTY_URL
# Fri, 09 Jul 2021 12:24:40 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 09 Jul 2021 12:25:27 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Jul 2021 12:25:38 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Jul 2021 12:25:44 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.6 BuildLabel=cl210620210527-1900
# Fri, 09 Jul 2021 12:25:47 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:25:56 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 09 Jul 2021 12:25:57 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Fri, 09 Jul 2021 12:25:59 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 09 Jul 2021 12:26:12 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 09 Jul 2021 12:26:34 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 09 Jul 2021 12:26:40 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 09 Jul 2021 12:26:44 GMT
USER 1001
# Fri, 09 Jul 2021 12:26:47 GMT
EXPOSE 9080 9443
# Fri, 09 Jul 2021 12:26:52 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 09 Jul 2021 12:26:57 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b268950217e490e209e0491ae6fbd3af12b4642aefad9c0039daf7b3ea0371`  
		Last Modified: Fri, 18 Jun 2021 01:52:43 GMT  
		Size: 17.2 MB (17208433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74aa12681d5d14a96459a14094fd9b08f1379e61fa1e8979b311b55b0561dead`  
		Last Modified: Fri, 18 Jun 2021 01:57:43 GMT  
		Size: 45.1 MB (45104807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee28cff75d70e071001e265878f54c811f52ab2cf95d0cc9daa0085c8e1465d`  
		Last Modified: Fri, 18 Jun 2021 01:57:35 GMT  
		Size: 3.3 MB (3284426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8bc0a64b2ab3278cdb9ab339783bb0cceaa701a7ce33da27f707ceaa008ce1`  
		Last Modified: Fri, 09 Jul 2021 12:58:50 GMT  
		Size: 14.2 MB (14171103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2c4f44ccce02a2525ee43a5efcf3e05abce2df913b365acfeebae8fb73084f`  
		Last Modified: Fri, 09 Jul 2021 12:58:45 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f325ef08d4de94642f048d7dea29eaeeab3efb1b593c7e8bde31199de14141b5`  
		Last Modified: Fri, 09 Jul 2021 12:58:45 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a874b9b19c9958221409a23916f91e1de0961b28a6a052ca34f062ab73b0a47c`  
		Last Modified: Fri, 09 Jul 2021 12:58:44 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41458d6be3c66f6faeb01bd128cbeb0c574d909fb02069ef57f6114b88a0a3e4`  
		Last Modified: Fri, 09 Jul 2021 12:58:44 GMT  
		Size: 10.7 KB (10663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93f402e5fea825689ca243ac3a9b193f0745ae31a1c0490c2bdc36748330352`  
		Last Modified: Fri, 09 Jul 2021 12:58:45 GMT  
		Size: 2.5 MB (2466657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.6-kernel-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:86dd4c903489b6277d800546e4026b185471df4e489ad47489ee5cb638cf77cc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107210623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e12ff17e9199c2e14c6098b23e5e2ea1d4a9cfc92a23b113ebdbf8b173689962`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:34 GMT
ADD file:ae5354f89d91eedd0614e3e97ee59fd6e23254923062c288d775e19b137dfd1c in / 
# Tue, 13 Jul 2021 22:53:36 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:18:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Jul 2021 23:18:55 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:23:22 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Tue, 13 Jul 2021 23:24:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 13 Jul 2021 23:24:37 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jul 2021 23:24:37 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 13 Jul 2021 23:25:12 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 14 Jul 2021 00:26:14 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 00:26:15 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:39:15 GMT
ARG EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27
# Wed, 14 Jul 2021 00:39:17 GMT
ARG NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c
# Wed, 14 Jul 2021 00:39:17 GMT
ARG NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499
# Wed, 14 Jul 2021 00:39:19 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.6 org.opencontainers.image.revision=cl210620210527-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 00:39:22 GMT
ENV LIBERTY_VERSION=21.0.0_06
# Wed, 14 Jul 2021 00:39:25 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 00:39:27 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 00:39:39 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:39:40 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 00:39:44 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.6 BuildLabel=cl210620210527-1900
# Wed, 14 Jul 2021 00:39:49 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:39:56 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 00:40:05 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 00:40:09 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 00:40:16 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 00:40:31 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 00:40:34 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 14 Jul 2021 00:40:36 GMT
USER 1001
# Wed, 14 Jul 2021 00:40:38 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 00:40:40 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 00:40:41 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:761fa758059faa0c80b0b90fcbcc192fc7f573da055460d5b3f019e0faceeb7a`  
		Last Modified: Tue, 13 Jul 2021 22:55:47 GMT  
		Size: 27.1 MB (27149318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0237838e148d45cea54b0d86c053131b4152f4928836cbb3a0c83ba79b538728`  
		Last Modified: Tue, 13 Jul 2021 23:32:23 GMT  
		Size: 15.7 MB (15741695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454768ac3fd4bd9b5536afd4e03c6c369d7eae1ee6b240b461dace5364b911f5`  
		Last Modified: Tue, 13 Jul 2021 23:36:09 GMT  
		Size: 43.8 MB (43840969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add6cc1d828e7c42608c4398d9d18baceea2e5104c4ff50d96eba8015aa4a896`  
		Last Modified: Tue, 13 Jul 2021 23:36:03 GMT  
		Size: 3.8 MB (3845109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac3c9edbf35b0fd0a98fd6fbf8733b14c64ec733db29fbc66237c96152675aa`  
		Last Modified: Wed, 14 Jul 2021 01:01:03 GMT  
		Size: 14.2 MB (14170211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a6f9c27ddf5042924151c4163db1d8c77d5e27815c6dd4ab6ac44ca4359ca9`  
		Last Modified: Wed, 14 Jul 2021 01:01:00 GMT  
		Size: 688.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d2155ef21ae68a5433eb02ce485c2846126483d0c16493ccd7957609dee300`  
		Last Modified: Wed, 14 Jul 2021 01:01:00 GMT  
		Size: 9.7 KB (9671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d250bdeb35966d93fe63d5db07ed72f480b22788fb024b0db509336916670a`  
		Last Modified: Wed, 14 Jul 2021 01:01:00 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6267d136ac6f15d5e07083f359200b352cfe64dd46f91d63dbb2f17a368ba1f`  
		Last Modified: Wed, 14 Jul 2021 01:01:00 GMT  
		Size: 10.7 KB (10658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ede16eb2950611c95a8ac88bde8aeca3b97581e05e64a4c1fd876c1775f34b`  
		Last Modified: Wed, 14 Jul 2021 01:01:00 GMT  
		Size: 2.4 MB (2442032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:21.0.0.6-kernel-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:ecd0719dbcc7940793ec0832af4541748d707941858dc4c25c99263722cfe602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:21.0.0.6-kernel-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:0ec7d975e21c45668d3ee3938c87da4c1e9bbb4df679e6c3e9e99b52d406ffa9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (179022742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd63c09c642ef53da6f7847c4dcf60af881727f0a625eb28acb35ee01b3eb55`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:19:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:19:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:19:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:19:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:19:52 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 14 Jul 2021 03:57:10 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 03:57:10 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 04:06:29 GMT
ARG EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27
# Wed, 14 Jul 2021 04:06:29 GMT
ARG NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c
# Wed, 14 Jul 2021 04:06:30 GMT
ARG NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499
# Wed, 14 Jul 2021 04:06:30 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.6 org.opencontainers.image.revision=cl210620210527-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 04:06:30 GMT
ENV LIBERTY_VERSION=21.0.0_06
# Wed, 14 Jul 2021 04:06:30 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 04:06:30 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 04:06:43 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:06:43 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 04:06:43 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.6 BuildLabel=cl210620210527-1900
# Wed, 14 Jul 2021 04:06:44 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 04:06:45 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 04:06:45 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 04:06:45 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 04:06:46 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 04:06:55 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 04:06:56 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 14 Jul 2021 04:06:56 GMT
USER 1001
# Wed, 14 Jul 2021 04:06:56 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 04:06:56 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 04:06:56 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22821a14390caaab5b1f7ca9feb8e54ce64d3d81ca1fa64c6f1eee32ae92da5b`  
		Last Modified: Tue, 13 Jul 2021 23:23:03 GMT  
		Size: 3.0 MB (2959004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4403b30ef5ef8f7b37c65fc3d0a0e0d7e0fca7451dd9b42a43bee1de1f389c09`  
		Last Modified: Tue, 13 Jul 2021 23:23:13 GMT  
		Size: 129.5 MB (129536228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745de4a9e38ea590f2768cf0e66717a76350c9b6d688e5b83d9ed54bf0431f00`  
		Last Modified: Wed, 14 Jul 2021 04:26:08 GMT  
		Size: 14.1 MB (14073365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3ebf216280a903a6659252558177cdc90c1ddd6a1c8103512d78bc2b25319c`  
		Last Modified: Wed, 14 Jul 2021 04:26:04 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d15611894f8e05f294b6acfcc612247f1d05e0a6ab05dc8b572360b7b315a65`  
		Last Modified: Wed, 14 Jul 2021 04:26:04 GMT  
		Size: 9.7 KB (9674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a407bfecf93a5cb88bf86146a7e1c56d02b511a41a44a691f95c437dcc963a`  
		Last Modified: Wed, 14 Jul 2021 04:26:04 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe5ee71fcca93adfda57e9f302b9d6fd150cb033f117515d45efedf131ac0ed`  
		Last Modified: Wed, 14 Jul 2021 04:26:04 GMT  
		Size: 10.7 KB (10664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe599905aac100721484ffd10a0f8bbdd6a2c9343fcb7161c0a9ac6369af6dd3`  
		Last Modified: Wed, 14 Jul 2021 04:26:05 GMT  
		Size: 5.7 MB (5726690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.6-kernel-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:3ed2bbb861a5eb50e7774a551509f1c51f56eef2a591587c7abd9ce4efacc490
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (181972429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a936cd8cef5b21e90018d71465bea9466ffee2ca1acde013dd63035d5aca0b3`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 17 Jun 2021 23:24:58 GMT
ADD file:33bc9edd94d5731da919e83ed38bd4aa7daffcb5f629d93bbde112a795c79d48 in / 
# Thu, 17 Jun 2021 23:25:03 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:01:35 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 18 Jun 2021 02:02:36 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:02:42 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Fri, 18 Jun 2021 02:03:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 18 Jun 2021 02:04:05 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 09 Jul 2021 12:02:21 GMT
ARG VERBOSE=false
# Fri, 09 Jul 2021 12:02:27 GMT
ARG OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:21:33 GMT
ARG EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27
# Fri, 09 Jul 2021 12:21:40 GMT
ARG NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c
# Fri, 09 Jul 2021 12:21:44 GMT
ARG NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499
# Fri, 09 Jul 2021 12:21:47 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.6 org.opencontainers.image.revision=cl210620210527-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 09 Jul 2021 12:21:54 GMT
ENV LIBERTY_VERSION=21.0.0_06
# Fri, 09 Jul 2021 12:21:58 GMT
ARG LIBERTY_URL
# Fri, 09 Jul 2021 12:22:03 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 09 Jul 2021 12:22:39 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Jul 2021 12:22:44 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Jul 2021 12:22:47 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.6 BuildLabel=cl210620210527-1900
# Fri, 09 Jul 2021 12:22:53 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:23:03 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 09 Jul 2021 12:23:05 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Fri, 09 Jul 2021 12:23:06 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 09 Jul 2021 12:23:16 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 09 Jul 2021 12:23:43 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 09 Jul 2021 12:23:50 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 09 Jul 2021 12:23:54 GMT
USER 1001
# Fri, 09 Jul 2021 12:23:58 GMT
EXPOSE 9080 9443
# Fri, 09 Jul 2021 12:24:00 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 09 Jul 2021 12:24:04 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:4e37c2419ee7d7e826be5c6ee69243351aaf456d6527714660cf7e7015491051`  
		Last Modified: Thu, 17 Jun 2021 23:28:22 GMT  
		Size: 30.4 MB (30425356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8d177e4917900437a3445272639bed389b718cc65a87346ba94f6d99327f34`  
		Last Modified: Fri, 18 Jun 2021 02:07:44 GMT  
		Size: 3.1 MB (3082963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09af03e0818b00fa01f51019b91f996a958b5ffb6b7dcd23e88d4d0df759f391`  
		Last Modified: Fri, 18 Jun 2021 02:07:59 GMT  
		Size: 129.1 MB (129059791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536fb275e646e87309efba2eb8113774342a74c4f2b949fc7e909bb27004030c`  
		Last Modified: Fri, 09 Jul 2021 12:58:34 GMT  
		Size: 14.1 MB (14073843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5eafe574ddb128ae4db89d490193ba5c1a26931b2ce1ec0f24b06097b5d2c5b`  
		Last Modified: Fri, 09 Jul 2021 12:58:29 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6d80b7905b8314e4632cc1f48c49edbf326f84d542e91698352947b9806bf5`  
		Last Modified: Fri, 09 Jul 2021 12:58:29 GMT  
		Size: 9.7 KB (9681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb948fb1402a87be7940a0930b5cfcca70800f13789188c19ec43ad79859a10`  
		Last Modified: Fri, 09 Jul 2021 12:58:29 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1c42006812bf0ce103b4fd1e747abbf28bae45fb5564c58d9f988426490eea`  
		Last Modified: Fri, 09 Jul 2021 12:58:29 GMT  
		Size: 10.7 KB (10670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0f4897d0f19c3d1e110234d55b6e4eac589923968ae5cb1a35798136e31c73`  
		Last Modified: Fri, 09 Jul 2021 12:58:30 GMT  
		Size: 5.3 MB (5309152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.6-kernel-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:c75e2eac3d75ccc2005985d8d469a30cc0cd7fcd07586965b570cb662c24fb9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174780216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8300ab87b0303716e149a4009cf50ed0fc1172fb241da8f1270af7aa1e14b894`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:22 GMT
ADD file:9e621b1dfa735f1a89553f154f2a2a6f669ff610236d92d6ebf37d1f378d8ec0 in / 
# Tue, 13 Jul 2021 22:53:24 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:12:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:12:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:12:20 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:13:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:13:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 14 Jul 2021 00:25:32 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 00:25:32 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:37:29 GMT
ARG EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27
# Wed, 14 Jul 2021 00:37:34 GMT
ARG NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c
# Wed, 14 Jul 2021 00:37:39 GMT
ARG NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499
# Wed, 14 Jul 2021 00:37:42 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.6 org.opencontainers.image.revision=cl210620210527-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 00:37:48 GMT
ENV LIBERTY_VERSION=21.0.0_06
# Wed, 14 Jul 2021 00:37:57 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 00:38:01 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 00:38:22 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:38:26 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 00:38:27 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.6 BuildLabel=cl210620210527-1900
# Wed, 14 Jul 2021 00:38:28 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:38:29 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 00:38:30 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 00:38:30 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 00:38:32 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 00:38:45 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=c84028a2f075be3750c35ff2c384599c3d72f32f37ee77421a5a13650955bb27 NON_IBM_SHA=f67ddaaa8eb1aaeb68ca0ade04954a97dc5f9b18b4993f5be1181bae6639ac7c NOTICES_SHA=aa4d385fe77ad7c36447eb8e3c1318498bc5277f1a25ac7a3ccb3d9d47558499 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 00:38:46 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 14 Jul 2021 00:38:46 GMT
USER 1001
# Wed, 14 Jul 2021 00:38:46 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 00:38:47 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 00:38:49 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:3287e09e36098b10234ccc1f8db0b48e2027ca7caa353a362d65f9b017ab802e`  
		Last Modified: Tue, 13 Jul 2021 22:55:34 GMT  
		Size: 25.4 MB (25365649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6fe4e2b151f33398a6ef48bbb5d9ace538aa5ecf3fab9182babc3a85b9166b`  
		Last Modified: Tue, 13 Jul 2021 23:16:59 GMT  
		Size: 2.7 MB (2676828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b436dddc9b46f3b9e70224bb7eab52e58419d071c07f16f9ce63c77c81e5e24`  
		Last Modified: Tue, 13 Jul 2021 23:17:08 GMT  
		Size: 126.7 MB (126676530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d4bf323f1bc7511736e3431f3336ad04db6d605a39fa8d4c7d832d7675d801`  
		Last Modified: Wed, 14 Jul 2021 01:00:54 GMT  
		Size: 14.1 MB (14073138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f699a8b7ec1db46f7ca1fbf9e81ec3ee6339f7759a5e0decf32d085243e8a9f8`  
		Last Modified: Wed, 14 Jul 2021 01:00:51 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719ce25bb19c404c9005bf6c2e1f252b500259db40d1f35e0acc30aafa077ec3`  
		Last Modified: Wed, 14 Jul 2021 01:00:51 GMT  
		Size: 9.7 KB (9679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d63e66b32162554ff5618c32cd2d0a852600e9d52219f202da933a59d53160`  
		Last Modified: Wed, 14 Jul 2021 01:00:51 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d30abebb191b25f681cd178757cfe196a6ee8675b0855ecf6707d0bbd87c20a`  
		Last Modified: Wed, 14 Jul 2021 01:00:51 GMT  
		Size: 10.7 KB (10660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2408f21dad9a358a1da63043e23b2a4477cb714947b648e025c7d6d6c80f16fa`  
		Last Modified: Wed, 14 Jul 2021 01:00:52 GMT  
		Size: 6.0 MB (5966756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:21.0.0.7-full-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:c0b24a9ceae5a69e70450ed1f2bf44b728bc0e82881ca34ed3ecec5f57bdea25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:21.0.0.7-full-java11-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:1607c542f71b2f5ccef563b8d06cd80ff5680045ad2870bcd103cb648cbd31b6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.9 MB (331946982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62d781949b689aa65fd1a31820767e9ffe5f41ab8708950a00263da8e72220b`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:29:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 14 Jul 2021 00:30:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:33:59 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Wed, 14 Jul 2021 00:35:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 14 Jul 2021 00:35:04 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 00:35:04 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 14 Jul 2021 00:35:41 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 14 Jul 2021 03:57:41 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 03:57:41 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 03:57:41 GMT
ARG EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448
# Wed, 14 Jul 2021 03:57:41 GMT
ARG NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365
# Wed, 14 Jul 2021 03:57:41 GMT
ARG NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc
# Wed, 14 Jul 2021 03:57:42 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.7 org.opencontainers.image.revision=cl210720210629-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 03:57:42 GMT
ENV LIBERTY_VERSION=21.0.0_07
# Wed, 14 Jul 2021 03:57:42 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 03:57:42 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 03:57:52 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 03:57:52 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 03:57:52 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.7 BuildLabel=cl210720210629-1900
# Wed, 14 Jul 2021 03:57:52 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 03:57:54 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 03:57:54 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 03:57:55 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 03:57:56 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 03:58:03 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 03:58:04 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 14 Jul 2021 03:58:04 GMT
USER 1001
# Wed, 14 Jul 2021 03:58:04 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 03:58:04 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 03:58:04 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 14 Jul 2021 04:02:22 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 04:02:23 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 14 Jul 2021 04:05:29 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Wed, 14 Jul 2021 04:05:30 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 14 Jul 2021 04:06:04 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1182b8c86e6bb404b0d40d2cdcdcaf4347c5aad464143625307b362caff690`  
		Last Modified: Wed, 14 Jul 2021 00:44:02 GMT  
		Size: 16.0 MB (16033076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1461af6857aed41d09a8ce6e2447ad52c9cdf1e6fe2f19ddaa2ab35d21aa1b`  
		Last Modified: Wed, 14 Jul 2021 00:50:41 GMT  
		Size: 44.4 MB (44382137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b538d86edfd8bb98ca5958e79321f730b01a2adc10244bd8ff7abf2aea9b8d8`  
		Last Modified: Wed, 14 Jul 2021 00:50:36 GMT  
		Size: 4.1 MB (4134048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a532adad204607676dccc5605c883856d719bc1eccc9197565f94f999ca6bf0a`  
		Last Modified: Wed, 14 Jul 2021 04:25:00 GMT  
		Size: 14.2 MB (14180546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bba4c8d4ae12b71c54ff9d090380b6ce40d98fcc357144ec5feaa9563dfa52b`  
		Last Modified: Wed, 14 Jul 2021 04:24:56 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5adbe7df68ffe9638f162021e06ead203a57226067210dd2b2fc8aafcbc8834e`  
		Last Modified: Wed, 14 Jul 2021 04:24:56 GMT  
		Size: 9.7 KB (9671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87cc611f3f91d20de349776f088cccc8cbfee6155ce83bee4dc0b2334e4d998`  
		Last Modified: Wed, 14 Jul 2021 04:24:56 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b31847e7e303752ed571f3af6ab967cb238f28af8751b50f7f8e544d697032b`  
		Last Modified: Wed, 14 Jul 2021 04:24:56 GMT  
		Size: 10.7 KB (10665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d5797f6cdf5b45d44deeed85d1698445e0cba043586c1c26cf5e0fc909a998`  
		Last Modified: Wed, 14 Jul 2021 04:24:56 GMT  
		Size: 2.5 MB (2468349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233938e6ffc02206885d22169230d199b4b36b54553521886d91184752e3daaa`  
		Last Modified: Wed, 14 Jul 2021 04:25:44 GMT  
		Size: 207.9 MB (207908038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90ef723b8a21c8cbbf581194e4e42068eacb9843ba3c0dc711c7848bdfdf7ad`  
		Last Modified: Wed, 14 Jul 2021 04:25:32 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8454d223bb998d37808fe994446cbadf77700813c85d535e25576b0291684827`  
		Last Modified: Wed, 14 Jul 2021 04:25:35 GMT  
		Size: 14.3 MB (14252672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.7-full-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:8cafec99a4314343a03fa7d874f636af661cbe6e52f1c5c859c3f124e3ef0059
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.9 MB (335861298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c09e44e2896ed63922f55ca03045a2bcaeca22760bae153406098e092d46f83`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 01:29:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 01:31:53 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:41:26 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Fri, 18 Jun 2021 01:43:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 01:43:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 01:43:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 18 Jun 2021 01:44:39 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 09 Jul 2021 12:06:18 GMT
ARG VERBOSE=false
# Fri, 09 Jul 2021 12:06:22 GMT
ARG OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:06:28 GMT
ARG EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448
# Fri, 09 Jul 2021 12:06:37 GMT
ARG NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365
# Fri, 09 Jul 2021 12:06:42 GMT
ARG NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc
# Fri, 09 Jul 2021 12:06:49 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.7 org.opencontainers.image.revision=cl210720210629-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 09 Jul 2021 12:06:56 GMT
ENV LIBERTY_VERSION=21.0.0_07
# Fri, 09 Jul 2021 12:07:00 GMT
ARG LIBERTY_URL
# Fri, 09 Jul 2021 12:07:10 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 09 Jul 2021 12:07:56 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Jul 2021 12:08:05 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Jul 2021 12:08:11 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.7 BuildLabel=cl210720210629-1900
# Fri, 09 Jul 2021 12:08:20 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:08:35 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 09 Jul 2021 12:08:37 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Fri, 09 Jul 2021 12:08:40 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 09 Jul 2021 12:08:57 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 09 Jul 2021 12:09:15 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 09 Jul 2021 12:09:20 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 09 Jul 2021 12:09:25 GMT
USER 1001
# Fri, 09 Jul 2021 12:09:30 GMT
EXPOSE 9080 9443
# Fri, 09 Jul 2021 12:09:33 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 09 Jul 2021 12:09:40 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 09 Jul 2021 12:15:43 GMT
ARG VERBOSE=false
# Fri, 09 Jul 2021 12:15:49 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 09 Jul 2021 12:19:40 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Fri, 09 Jul 2021 12:19:50 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 09 Jul 2021 12:20:53 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b268950217e490e209e0491ae6fbd3af12b4642aefad9c0039daf7b3ea0371`  
		Last Modified: Fri, 18 Jun 2021 01:52:43 GMT  
		Size: 17.2 MB (17208433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74aa12681d5d14a96459a14094fd9b08f1379e61fa1e8979b311b55b0561dead`  
		Last Modified: Fri, 18 Jun 2021 01:57:43 GMT  
		Size: 45.1 MB (45104807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee28cff75d70e071001e265878f54c811f52ab2cf95d0cc9daa0085c8e1465d`  
		Last Modified: Fri, 18 Jun 2021 01:57:35 GMT  
		Size: 3.3 MB (3284426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d645b89a4dd25a5d864e0eee16fad18b47003f9afbc03fcbb0d0dd722dc67fc8`  
		Last Modified: Fri, 09 Jul 2021 12:57:02 GMT  
		Size: 14.2 MB (14181551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4da63aa53ce2f86286610b335d47c205209123f3b10468f1fbd732174572770`  
		Last Modified: Fri, 09 Jul 2021 12:56:57 GMT  
		Size: 692.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85cdabb46ca79b2b6ab7a933df344ee131c49e7f28758e95f0563be56d88830`  
		Last Modified: Fri, 09 Jul 2021 12:56:57 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee96f4cf06004c656da5e448f035060f82ec53f290430a9869e4387fce1d59a`  
		Last Modified: Fri, 09 Jul 2021 12:56:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c088ac6df31e5b351ce2912eadc32bd7d67f7dc02c903d844f4527504ecfba`  
		Last Modified: Fri, 09 Jul 2021 12:56:58 GMT  
		Size: 10.7 KB (10662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3be9bc98dfc99235b8a23c99b39f927cca9fab5b980ed63f0cc3af7db1ff88`  
		Last Modified: Fri, 09 Jul 2021 12:56:58 GMT  
		Size: 2.5 MB (2470788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3cfa0388ed805bea8ccb8c5f29a0b03a9f2a3862fab969e62f4a0abd6c88775`  
		Last Modified: Fri, 09 Jul 2021 12:58:05 GMT  
		Size: 207.9 MB (207908223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdbe2e74bb76632286d5ef23c2b89cca3c2efc67ca72536dae6363ccb2c2ce6`  
		Last Modified: Fri, 09 Jul 2021 12:57:45 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f426bfa2fd56befb95dd5105bcc4654ef746edb442b2f15785812129669d507`  
		Last Modified: Fri, 09 Jul 2021 12:57:48 GMT  
		Size: 12.4 MB (12402580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.7-full-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:649732a70fc7bf2f172717342cb159e7ed4d8eb9b486d1707f5270cafa134725
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.8 MB (328834951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5776437add2a6dea68145518bf675bc88e7ea3b5d3caeb22528b634a4663aedb`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:34 GMT
ADD file:ae5354f89d91eedd0614e3e97ee59fd6e23254923062c288d775e19b137dfd1c in / 
# Tue, 13 Jul 2021 22:53:36 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:18:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Jul 2021 23:18:55 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:23:22 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Tue, 13 Jul 2021 23:24:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 13 Jul 2021 23:24:37 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jul 2021 23:24:37 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 13 Jul 2021 23:25:12 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 14 Jul 2021 00:26:14 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 00:26:15 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:26:15 GMT
ARG EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448
# Wed, 14 Jul 2021 00:26:16 GMT
ARG NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365
# Wed, 14 Jul 2021 00:26:16 GMT
ARG NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc
# Wed, 14 Jul 2021 00:26:16 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.7 org.opencontainers.image.revision=cl210720210629-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 00:26:17 GMT
ENV LIBERTY_VERSION=21.0.0_07
# Wed, 14 Jul 2021 00:26:17 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 00:26:18 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 00:26:29 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:26:30 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 00:26:31 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.7 BuildLabel=cl210720210629-1900
# Wed, 14 Jul 2021 00:26:31 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:26:32 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 00:26:33 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 00:26:33 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 00:26:35 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 00:26:44 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 00:26:45 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 14 Jul 2021 00:26:46 GMT
USER 1001
# Wed, 14 Jul 2021 00:26:46 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 00:26:47 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 00:26:47 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 14 Jul 2021 00:31:36 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 00:31:37 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 14 Jul 2021 00:35:09 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Wed, 14 Jul 2021 00:35:17 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 14 Jul 2021 00:35:58 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:761fa758059faa0c80b0b90fcbcc192fc7f573da055460d5b3f019e0faceeb7a`  
		Last Modified: Tue, 13 Jul 2021 22:55:47 GMT  
		Size: 27.1 MB (27149318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0237838e148d45cea54b0d86c053131b4152f4928836cbb3a0c83ba79b538728`  
		Last Modified: Tue, 13 Jul 2021 23:32:23 GMT  
		Size: 15.7 MB (15741695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454768ac3fd4bd9b5536afd4e03c6c369d7eae1ee6b240b461dace5364b911f5`  
		Last Modified: Tue, 13 Jul 2021 23:36:09 GMT  
		Size: 43.8 MB (43840969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add6cc1d828e7c42608c4398d9d18baceea2e5104c4ff50d96eba8015aa4a896`  
		Last Modified: Tue, 13 Jul 2021 23:36:03 GMT  
		Size: 3.8 MB (3845109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8db25e8b8b8c38fe38441c03961e2239699ec7d60c2535ee7e3f32b5d9408e`  
		Last Modified: Wed, 14 Jul 2021 00:59:54 GMT  
		Size: 14.2 MB (14180686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2f25fb8653dcf183e4697f3c91aac2b7f2b52ce9b29ddad16203148334326c`  
		Last Modified: Wed, 14 Jul 2021 00:59:51 GMT  
		Size: 691.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5899b27fbac50a6a5dc63dea77388554c0a30d19d49c0fede69dc55b139aaf9d`  
		Last Modified: Wed, 14 Jul 2021 00:59:51 GMT  
		Size: 9.7 KB (9668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e909c0ea2090f66e195b6a98342c9481ac3c8ca4424dee2a56e9510339fc74d2`  
		Last Modified: Wed, 14 Jul 2021 00:59:51 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0725387dcb18203fe63c473bed29ea62c4967f1aa7cd4875bf595e119b67ce98`  
		Last Modified: Wed, 14 Jul 2021 00:59:51 GMT  
		Size: 10.7 KB (10657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0dca61c9477b822a385de7b1018700d87fa9b82c75df3ce7f8ff1d897b5ae27`  
		Last Modified: Wed, 14 Jul 2021 00:59:53 GMT  
		Size: 2.5 MB (2471680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f00e32e1d90d64971a74357199a5c0acaa27cf39d5469135e2d09d3862bbb2`  
		Last Modified: Wed, 14 Jul 2021 01:00:34 GMT  
		Size: 207.9 MB (207908299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f66031a5f5dcccabe1352d2b7c68e45215f20afb38a0b5b81ece512fc359ef1`  
		Last Modified: Wed, 14 Jul 2021 01:00:19 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2ed70fc141f537c65280ed5b10e55b6bac20472e876a135f8723c10208b013`  
		Last Modified: Wed, 14 Jul 2021 01:00:21 GMT  
		Size: 13.7 MB (13674963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:21.0.0.7-full-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:fec4f13f5e933d058d58e97a33c772ec353572e7288445ee1e31040c78801493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:21.0.0.7-full-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:593621830dcf7ed862f01c7b59dbf0c52ac38031f5d4a9e4238c21978417c3ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.8 MB (402767961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32dfa93cd1b2e8518ca9ca11addf6364d0e93655b8fa5c76b8caca2bb92ac7a2`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:19:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:19:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:19:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:19:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:19:52 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 14 Jul 2021 03:57:10 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 03:57:10 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 03:57:10 GMT
ARG EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448
# Wed, 14 Jul 2021 03:57:11 GMT
ARG NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365
# Wed, 14 Jul 2021 03:57:11 GMT
ARG NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc
# Wed, 14 Jul 2021 03:57:11 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.7 org.opencontainers.image.revision=cl210720210629-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 03:57:11 GMT
ENV LIBERTY_VERSION=21.0.0_07
# Wed, 14 Jul 2021 03:57:11 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 03:57:12 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 03:57:23 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 03:57:23 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 03:57:23 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.7 BuildLabel=cl210720210629-1900
# Wed, 14 Jul 2021 03:57:23 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 03:57:25 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 03:57:25 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 03:57:26 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 03:57:27 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 03:57:37 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 03:57:37 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 14 Jul 2021 03:57:37 GMT
USER 1001
# Wed, 14 Jul 2021 03:57:37 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 03:57:37 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 03:57:38 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 14 Jul 2021 03:58:11 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 03:58:11 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 14 Jul 2021 04:01:40 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Wed, 14 Jul 2021 04:01:41 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 14 Jul 2021 04:02:17 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22821a14390caaab5b1f7ca9feb8e54ce64d3d81ca1fa64c6f1eee32ae92da5b`  
		Last Modified: Tue, 13 Jul 2021 23:23:03 GMT  
		Size: 3.0 MB (2959004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4403b30ef5ef8f7b37c65fc3d0a0e0d7e0fca7451dd9b42a43bee1de1f389c09`  
		Last Modified: Tue, 13 Jul 2021 23:23:13 GMT  
		Size: 129.5 MB (129536228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2229a5b48fafe35e4b36d1919ccb99f32d1692b2bec7c9fea77733becb84530c`  
		Last Modified: Wed, 14 Jul 2021 04:24:48 GMT  
		Size: 14.1 MB (14082341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0508db572632c638c6182a39308e5731bfcbd4b598bfc908f0a6c4db23ac0db`  
		Last Modified: Wed, 14 Jul 2021 04:24:43 GMT  
		Size: 692.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5845fe90cc54b2ed48af7b145887feaa37656b8c9d799f40dabf84831e141087`  
		Last Modified: Wed, 14 Jul 2021 04:24:43 GMT  
		Size: 9.7 KB (9673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ea30f4f8482cb87d0f69111edc0a66bc10b6f55dc9431070743dde095a76c7`  
		Last Modified: Wed, 14 Jul 2021 04:24:43 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32852fe819a654da3298d6bb5d00119b56e444c4ff75a5fe4f961145af4cde0`  
		Last Modified: Wed, 14 Jul 2021 04:24:43 GMT  
		Size: 10.7 KB (10659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe8a18351bbc592654b68f132ba3b2d4f542c9013876ef7df5be2e3b67f935e`  
		Last Modified: Wed, 14 Jul 2021 04:24:45 GMT  
		Size: 5.7 MB (5688752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0302e7744226a971fe896e471720ff2db67b7146cdec0050817f45d6b09a04`  
		Last Modified: Wed, 14 Jul 2021 04:25:21 GMT  
		Size: 207.9 MB (207908003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e46e41ead606c0ff89f626961bf1e848fd9710f66ba1036b6f33f388675358`  
		Last Modified: Wed, 14 Jul 2021 04:25:09 GMT  
		Size: 944.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1bdc8179339ab3fcfbe904d27833d22d74c5ea380c667dcdf9e8ba63b9e8300`  
		Last Modified: Wed, 14 Jul 2021 04:25:12 GMT  
		Size: 15.9 MB (15865245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.7-full-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:afb93aa6c7922a3f90dd7096fe10c5d03eaa555892eaabe424d869169285f8e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.4 MB (403364706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c6deacd67107f6a602891b5d74b510d28a8cb9931c19909ac9c1fd01abbe1a`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 17 Jun 2021 23:24:58 GMT
ADD file:33bc9edd94d5731da919e83ed38bd4aa7daffcb5f629d93bbde112a795c79d48 in / 
# Thu, 17 Jun 2021 23:25:03 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:01:35 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 18 Jun 2021 02:02:36 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:02:42 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Fri, 18 Jun 2021 02:03:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 18 Jun 2021 02:04:05 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 09 Jul 2021 12:02:21 GMT
ARG VERBOSE=false
# Fri, 09 Jul 2021 12:02:27 GMT
ARG OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:02:34 GMT
ARG EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448
# Fri, 09 Jul 2021 12:02:38 GMT
ARG NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365
# Fri, 09 Jul 2021 12:02:44 GMT
ARG NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc
# Fri, 09 Jul 2021 12:02:51 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.7 org.opencontainers.image.revision=cl210720210629-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 09 Jul 2021 12:03:01 GMT
ENV LIBERTY_VERSION=21.0.0_07
# Fri, 09 Jul 2021 12:03:07 GMT
ARG LIBERTY_URL
# Fri, 09 Jul 2021 12:03:15 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 09 Jul 2021 12:04:20 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Jul 2021 12:04:26 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Jul 2021 12:04:33 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.7 BuildLabel=cl210720210629-1900
# Fri, 09 Jul 2021 12:04:40 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:04:53 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 09 Jul 2021 12:04:55 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Fri, 09 Jul 2021 12:04:56 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 09 Jul 2021 12:05:06 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 09 Jul 2021 12:05:38 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 09 Jul 2021 12:05:41 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 09 Jul 2021 12:05:45 GMT
USER 1001
# Fri, 09 Jul 2021 12:05:50 GMT
EXPOSE 9080 9443
# Fri, 09 Jul 2021 12:05:56 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 09 Jul 2021 12:06:02 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 09 Jul 2021 12:09:58 GMT
ARG VERBOSE=false
# Fri, 09 Jul 2021 12:10:00 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 09 Jul 2021 12:14:03 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Fri, 09 Jul 2021 12:14:14 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 09 Jul 2021 12:15:29 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:4e37c2419ee7d7e826be5c6ee69243351aaf456d6527714660cf7e7015491051`  
		Last Modified: Thu, 17 Jun 2021 23:28:22 GMT  
		Size: 30.4 MB (30425356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8d177e4917900437a3445272639bed389b718cc65a87346ba94f6d99327f34`  
		Last Modified: Fri, 18 Jun 2021 02:07:44 GMT  
		Size: 3.1 MB (3082963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09af03e0818b00fa01f51019b91f996a958b5ffb6b7dcd23e88d4d0df759f391`  
		Last Modified: Fri, 18 Jun 2021 02:07:59 GMT  
		Size: 129.1 MB (129059791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e575d1b794a99b9e4326e5406abd771cab007d8e4496378d443e133aecd6fc`  
		Last Modified: Fri, 09 Jul 2021 12:56:48 GMT  
		Size: 14.1 MB (14082768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446edb557b83d18920bc3d64ad18bbc793493f18eac5610ae1ad819a37c1b5c8`  
		Last Modified: Fri, 09 Jul 2021 12:56:42 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92aca0eb7db57552a319340ea766bee3e176bb7d52bf238c98bfd7bf1edc62e8`  
		Last Modified: Fri, 09 Jul 2021 12:56:41 GMT  
		Size: 9.7 KB (9676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c68662de813b880c2fe01caa04a35528660efb50af580891a93b24b63ce4273`  
		Last Modified: Fri, 09 Jul 2021 12:56:41 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436ecaaacdb2e6ae26659e31d3c0b911a07a8cfe2e46922e0fe3377f753d6879`  
		Last Modified: Fri, 09 Jul 2021 12:56:42 GMT  
		Size: 10.7 KB (10676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb47456c330b967df85a4df66778e4b5762a52080a7ff7a89c042822a5d0841`  
		Last Modified: Fri, 09 Jul 2021 12:56:43 GMT  
		Size: 5.4 MB (5354019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d889510935916732b2718d9a7f5adffc222f87f6f0ad7c7036c320afe43a1d8e`  
		Last Modified: Fri, 09 Jul 2021 12:57:31 GMT  
		Size: 207.9 MB (207908499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a254bd0d60b4e9fef14d2e8f2ca322cf2da3a90df1cfa3930b64c3cc95d113`  
		Last Modified: Fri, 09 Jul 2021 12:57:12 GMT  
		Size: 952.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a8372af7fe68d759c42eb1c1105eb84743e9e40ba7caf5490c68817776fea4`  
		Last Modified: Fri, 09 Jul 2021 12:57:15 GMT  
		Size: 13.4 MB (13429029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.7-full-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:feccab75dd49b9eacc3dec41d6c9fc662ce921e51dde3fa8868c6968d2b2a570
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.2 MB (398216420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c531ce10ac925f59e00e218ed78df32aab4514ad3a8758dae3b032ec637546b0`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:22 GMT
ADD file:9e621b1dfa735f1a89553f154f2a2a6f669ff610236d92d6ebf37d1f378d8ec0 in / 
# Tue, 13 Jul 2021 22:53:24 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:12:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:12:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:12:20 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:13:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:13:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 14 Jul 2021 00:25:32 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 00:25:32 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:25:32 GMT
ARG EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448
# Wed, 14 Jul 2021 00:25:32 GMT
ARG NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365
# Wed, 14 Jul 2021 00:25:33 GMT
ARG NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc
# Wed, 14 Jul 2021 00:25:33 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.7 org.opencontainers.image.revision=cl210720210629-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 00:25:34 GMT
ENV LIBERTY_VERSION=21.0.0_07
# Wed, 14 Jul 2021 00:25:34 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 00:25:34 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 00:25:46 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:25:47 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 00:25:47 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.7 BuildLabel=cl210720210629-1900
# Wed, 14 Jul 2021 00:25:47 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:25:49 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 00:25:50 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 00:25:50 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 00:25:51 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 00:26:01 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 00:26:02 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 14 Jul 2021 00:26:03 GMT
USER 1001
# Wed, 14 Jul 2021 00:26:04 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 00:26:04 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 00:26:04 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 14 Jul 2021 00:26:59 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 00:27:00 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 14 Jul 2021 00:30:33 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Wed, 14 Jul 2021 00:30:39 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 14 Jul 2021 00:31:15 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:3287e09e36098b10234ccc1f8db0b48e2027ca7caa353a362d65f9b017ab802e`  
		Last Modified: Tue, 13 Jul 2021 22:55:34 GMT  
		Size: 25.4 MB (25365649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6fe4e2b151f33398a6ef48bbb5d9ace538aa5ecf3fab9182babc3a85b9166b`  
		Last Modified: Tue, 13 Jul 2021 23:16:59 GMT  
		Size: 2.7 MB (2676828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b436dddc9b46f3b9e70224bb7eab52e58419d071c07f16f9ce63c77c81e5e24`  
		Last Modified: Tue, 13 Jul 2021 23:17:08 GMT  
		Size: 126.7 MB (126676530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfeb84cc8b0669c7b9e77df6ef93a9af10143ddecdf7cbab90eb2541ea6dae9f`  
		Last Modified: Wed, 14 Jul 2021 00:59:46 GMT  
		Size: 14.1 MB (14082055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc5188d927b29c1e6ec8a352cb13ab32af8ed150ee5c1abb928fef7ec7d2a15`  
		Last Modified: Wed, 14 Jul 2021 00:59:43 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c09c4ee0bf95890e60c06b29e00402b7ca7fbbe3f9b31bbf00426c75b84aaa`  
		Last Modified: Wed, 14 Jul 2021 00:59:43 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7b8bba08a70c5ffca0778748f3e75b2ee3c4d131b3bf31b9e7dfd735c9ec4b`  
		Last Modified: Wed, 14 Jul 2021 00:59:43 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe12bbaa95b8b804b7e6752881f522078004b8355c33d3363e49e5d4c438c2cd`  
		Last Modified: Wed, 14 Jul 2021 00:59:43 GMT  
		Size: 10.7 KB (10664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7dea27e762888900b197a8656b67c7943b619a99797e6b2fcdee52af376627`  
		Last Modified: Wed, 14 Jul 2021 00:59:44 GMT  
		Size: 5.9 MB (5941251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7dda827d3b54d7e48c6470c19206b3547c368b168c59c5946383a1217c8e2d0`  
		Last Modified: Wed, 14 Jul 2021 01:00:10 GMT  
		Size: 207.9 MB (207910341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358ded070ceaa1f2c8acb8b7172deb3fa6884c261e423c03b2585a8d2bbb042c`  
		Last Modified: Wed, 14 Jul 2021 00:59:59 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69694bdedf8776b29d158ed194e88e78c47e8365b5360ad768020dd3a3b22f3`  
		Last Modified: Wed, 14 Jul 2021 01:00:01 GMT  
		Size: 15.5 MB (15541515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:21.0.0.7-kernel-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:111787cfced37823534628c27c610369644c673a44a89b6ca609e4cd815c7c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:21.0.0.7-kernel-java11-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:986dd4e771035ddaa951cf408e8fa0e5ccc5b74e55074464ec3547e9b14f817a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109785326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24cab24d5750e08af9f84ba2908decd6369917ebfca8eb7277d836f12c968e22`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:29:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 14 Jul 2021 00:30:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:33:59 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Wed, 14 Jul 2021 00:35:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 14 Jul 2021 00:35:04 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 00:35:04 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 14 Jul 2021 00:35:41 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 14 Jul 2021 03:57:41 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 03:57:41 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 03:57:41 GMT
ARG EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448
# Wed, 14 Jul 2021 03:57:41 GMT
ARG NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365
# Wed, 14 Jul 2021 03:57:41 GMT
ARG NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc
# Wed, 14 Jul 2021 03:57:42 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.7 org.opencontainers.image.revision=cl210720210629-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 03:57:42 GMT
ENV LIBERTY_VERSION=21.0.0_07
# Wed, 14 Jul 2021 03:57:42 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 03:57:42 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 03:57:52 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 03:57:52 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 03:57:52 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.7 BuildLabel=cl210720210629-1900
# Wed, 14 Jul 2021 03:57:52 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 03:57:54 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 03:57:54 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 03:57:55 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 03:57:56 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 03:58:03 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 03:58:04 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 14 Jul 2021 03:58:04 GMT
USER 1001
# Wed, 14 Jul 2021 03:58:04 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 03:58:04 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 03:58:04 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1182b8c86e6bb404b0d40d2cdcdcaf4347c5aad464143625307b362caff690`  
		Last Modified: Wed, 14 Jul 2021 00:44:02 GMT  
		Size: 16.0 MB (16033076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1461af6857aed41d09a8ce6e2447ad52c9cdf1e6fe2f19ddaa2ab35d21aa1b`  
		Last Modified: Wed, 14 Jul 2021 00:50:41 GMT  
		Size: 44.4 MB (44382137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b538d86edfd8bb98ca5958e79321f730b01a2adc10244bd8ff7abf2aea9b8d8`  
		Last Modified: Wed, 14 Jul 2021 00:50:36 GMT  
		Size: 4.1 MB (4134048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a532adad204607676dccc5605c883856d719bc1eccc9197565f94f999ca6bf0a`  
		Last Modified: Wed, 14 Jul 2021 04:25:00 GMT  
		Size: 14.2 MB (14180546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bba4c8d4ae12b71c54ff9d090380b6ce40d98fcc357144ec5feaa9563dfa52b`  
		Last Modified: Wed, 14 Jul 2021 04:24:56 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5adbe7df68ffe9638f162021e06ead203a57226067210dd2b2fc8aafcbc8834e`  
		Last Modified: Wed, 14 Jul 2021 04:24:56 GMT  
		Size: 9.7 KB (9671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87cc611f3f91d20de349776f088cccc8cbfee6155ce83bee4dc0b2334e4d998`  
		Last Modified: Wed, 14 Jul 2021 04:24:56 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b31847e7e303752ed571f3af6ab967cb238f28af8751b50f7f8e544d697032b`  
		Last Modified: Wed, 14 Jul 2021 04:24:56 GMT  
		Size: 10.7 KB (10665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d5797f6cdf5b45d44deeed85d1698445e0cba043586c1c26cf5e0fc909a998`  
		Last Modified: Wed, 14 Jul 2021 04:24:56 GMT  
		Size: 2.5 MB (2468349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.7-kernel-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:5730494867e297dccd2f78f9acfbfd7c413e7d1c71da4080e1d9a6d87a59ae91
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115549549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1130bdc576a6414c5449d479c4ae27633bcc940b1d9a1a9f1f5862936787757b`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 01:29:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 01:31:53 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:41:26 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Fri, 18 Jun 2021 01:43:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 01:43:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 01:43:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 18 Jun 2021 01:44:39 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 09 Jul 2021 12:06:18 GMT
ARG VERBOSE=false
# Fri, 09 Jul 2021 12:06:22 GMT
ARG OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:06:28 GMT
ARG EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448
# Fri, 09 Jul 2021 12:06:37 GMT
ARG NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365
# Fri, 09 Jul 2021 12:06:42 GMT
ARG NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc
# Fri, 09 Jul 2021 12:06:49 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.7 org.opencontainers.image.revision=cl210720210629-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 09 Jul 2021 12:06:56 GMT
ENV LIBERTY_VERSION=21.0.0_07
# Fri, 09 Jul 2021 12:07:00 GMT
ARG LIBERTY_URL
# Fri, 09 Jul 2021 12:07:10 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 09 Jul 2021 12:07:56 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Jul 2021 12:08:05 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Jul 2021 12:08:11 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.7 BuildLabel=cl210720210629-1900
# Fri, 09 Jul 2021 12:08:20 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:08:35 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 09 Jul 2021 12:08:37 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Fri, 09 Jul 2021 12:08:40 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 09 Jul 2021 12:08:57 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 09 Jul 2021 12:09:15 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 09 Jul 2021 12:09:20 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 09 Jul 2021 12:09:25 GMT
USER 1001
# Fri, 09 Jul 2021 12:09:30 GMT
EXPOSE 9080 9443
# Fri, 09 Jul 2021 12:09:33 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 09 Jul 2021 12:09:40 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b268950217e490e209e0491ae6fbd3af12b4642aefad9c0039daf7b3ea0371`  
		Last Modified: Fri, 18 Jun 2021 01:52:43 GMT  
		Size: 17.2 MB (17208433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74aa12681d5d14a96459a14094fd9b08f1379e61fa1e8979b311b55b0561dead`  
		Last Modified: Fri, 18 Jun 2021 01:57:43 GMT  
		Size: 45.1 MB (45104807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee28cff75d70e071001e265878f54c811f52ab2cf95d0cc9daa0085c8e1465d`  
		Last Modified: Fri, 18 Jun 2021 01:57:35 GMT  
		Size: 3.3 MB (3284426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d645b89a4dd25a5d864e0eee16fad18b47003f9afbc03fcbb0d0dd722dc67fc8`  
		Last Modified: Fri, 09 Jul 2021 12:57:02 GMT  
		Size: 14.2 MB (14181551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4da63aa53ce2f86286610b335d47c205209123f3b10468f1fbd732174572770`  
		Last Modified: Fri, 09 Jul 2021 12:56:57 GMT  
		Size: 692.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85cdabb46ca79b2b6ab7a933df344ee131c49e7f28758e95f0563be56d88830`  
		Last Modified: Fri, 09 Jul 2021 12:56:57 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee96f4cf06004c656da5e448f035060f82ec53f290430a9869e4387fce1d59a`  
		Last Modified: Fri, 09 Jul 2021 12:56:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c088ac6df31e5b351ce2912eadc32bd7d67f7dc02c903d844f4527504ecfba`  
		Last Modified: Fri, 09 Jul 2021 12:56:58 GMT  
		Size: 10.7 KB (10662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3be9bc98dfc99235b8a23c99b39f927cca9fab5b980ed63f0cc3af7db1ff88`  
		Last Modified: Fri, 09 Jul 2021 12:56:58 GMT  
		Size: 2.5 MB (2470788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.7-kernel-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:cc097653826372eefa2b06f16af009a4db47ad681936fcdebfe34d17cde65101
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107250743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f375777082aad70eba3068caf709bab79c6e79a61ce0b60f98815bb69df9f7c7`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:34 GMT
ADD file:ae5354f89d91eedd0614e3e97ee59fd6e23254923062c288d775e19b137dfd1c in / 
# Tue, 13 Jul 2021 22:53:36 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:18:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Jul 2021 23:18:55 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:23:22 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Tue, 13 Jul 2021 23:24:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 13 Jul 2021 23:24:37 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jul 2021 23:24:37 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 13 Jul 2021 23:25:12 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 14 Jul 2021 00:26:14 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 00:26:15 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:26:15 GMT
ARG EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448
# Wed, 14 Jul 2021 00:26:16 GMT
ARG NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365
# Wed, 14 Jul 2021 00:26:16 GMT
ARG NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc
# Wed, 14 Jul 2021 00:26:16 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.7 org.opencontainers.image.revision=cl210720210629-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 00:26:17 GMT
ENV LIBERTY_VERSION=21.0.0_07
# Wed, 14 Jul 2021 00:26:17 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 00:26:18 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 00:26:29 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:26:30 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 00:26:31 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.7 BuildLabel=cl210720210629-1900
# Wed, 14 Jul 2021 00:26:31 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:26:32 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 00:26:33 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 00:26:33 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 00:26:35 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 00:26:44 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 00:26:45 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 14 Jul 2021 00:26:46 GMT
USER 1001
# Wed, 14 Jul 2021 00:26:46 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 00:26:47 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 00:26:47 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:761fa758059faa0c80b0b90fcbcc192fc7f573da055460d5b3f019e0faceeb7a`  
		Last Modified: Tue, 13 Jul 2021 22:55:47 GMT  
		Size: 27.1 MB (27149318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0237838e148d45cea54b0d86c053131b4152f4928836cbb3a0c83ba79b538728`  
		Last Modified: Tue, 13 Jul 2021 23:32:23 GMT  
		Size: 15.7 MB (15741695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454768ac3fd4bd9b5536afd4e03c6c369d7eae1ee6b240b461dace5364b911f5`  
		Last Modified: Tue, 13 Jul 2021 23:36:09 GMT  
		Size: 43.8 MB (43840969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add6cc1d828e7c42608c4398d9d18baceea2e5104c4ff50d96eba8015aa4a896`  
		Last Modified: Tue, 13 Jul 2021 23:36:03 GMT  
		Size: 3.8 MB (3845109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8db25e8b8b8c38fe38441c03961e2239699ec7d60c2535ee7e3f32b5d9408e`  
		Last Modified: Wed, 14 Jul 2021 00:59:54 GMT  
		Size: 14.2 MB (14180686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2f25fb8653dcf183e4697f3c91aac2b7f2b52ce9b29ddad16203148334326c`  
		Last Modified: Wed, 14 Jul 2021 00:59:51 GMT  
		Size: 691.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5899b27fbac50a6a5dc63dea77388554c0a30d19d49c0fede69dc55b139aaf9d`  
		Last Modified: Wed, 14 Jul 2021 00:59:51 GMT  
		Size: 9.7 KB (9668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e909c0ea2090f66e195b6a98342c9481ac3c8ca4424dee2a56e9510339fc74d2`  
		Last Modified: Wed, 14 Jul 2021 00:59:51 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0725387dcb18203fe63c473bed29ea62c4967f1aa7cd4875bf595e119b67ce98`  
		Last Modified: Wed, 14 Jul 2021 00:59:51 GMT  
		Size: 10.7 KB (10657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0dca61c9477b822a385de7b1018700d87fa9b82c75df3ce7f8ff1d897b5ae27`  
		Last Modified: Wed, 14 Jul 2021 00:59:53 GMT  
		Size: 2.5 MB (2471680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:21.0.0.7-kernel-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:6aa85252d65e5bb3ebbd9d5c68651eaef4806f92a2f6b1f62d376dca6e1f0f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:21.0.0.7-kernel-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:508840046c1a01e61a610495f4f0220e90127fa32ffc287c877d4d75aa77e33e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (178993769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ca11b94f5e93af4ddd5d167ebc64cb6ef4c8ecacfe47cec39b23a7966dbb80`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:19:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:19:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:19:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:19:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:19:52 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 14 Jul 2021 03:57:10 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 03:57:10 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 03:57:10 GMT
ARG EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448
# Wed, 14 Jul 2021 03:57:11 GMT
ARG NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365
# Wed, 14 Jul 2021 03:57:11 GMT
ARG NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc
# Wed, 14 Jul 2021 03:57:11 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.7 org.opencontainers.image.revision=cl210720210629-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 03:57:11 GMT
ENV LIBERTY_VERSION=21.0.0_07
# Wed, 14 Jul 2021 03:57:11 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 03:57:12 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 03:57:23 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 03:57:23 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 03:57:23 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.7 BuildLabel=cl210720210629-1900
# Wed, 14 Jul 2021 03:57:23 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 03:57:25 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 03:57:25 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 03:57:26 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 03:57:27 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 03:57:37 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 03:57:37 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 14 Jul 2021 03:57:37 GMT
USER 1001
# Wed, 14 Jul 2021 03:57:37 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 03:57:37 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 03:57:38 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22821a14390caaab5b1f7ca9feb8e54ce64d3d81ca1fa64c6f1eee32ae92da5b`  
		Last Modified: Tue, 13 Jul 2021 23:23:03 GMT  
		Size: 3.0 MB (2959004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4403b30ef5ef8f7b37c65fc3d0a0e0d7e0fca7451dd9b42a43bee1de1f389c09`  
		Last Modified: Tue, 13 Jul 2021 23:23:13 GMT  
		Size: 129.5 MB (129536228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2229a5b48fafe35e4b36d1919ccb99f32d1692b2bec7c9fea77733becb84530c`  
		Last Modified: Wed, 14 Jul 2021 04:24:48 GMT  
		Size: 14.1 MB (14082341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0508db572632c638c6182a39308e5731bfcbd4b598bfc908f0a6c4db23ac0db`  
		Last Modified: Wed, 14 Jul 2021 04:24:43 GMT  
		Size: 692.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5845fe90cc54b2ed48af7b145887feaa37656b8c9d799f40dabf84831e141087`  
		Last Modified: Wed, 14 Jul 2021 04:24:43 GMT  
		Size: 9.7 KB (9673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ea30f4f8482cb87d0f69111edc0a66bc10b6f55dc9431070743dde095a76c7`  
		Last Modified: Wed, 14 Jul 2021 04:24:43 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32852fe819a654da3298d6bb5d00119b56e444c4ff75a5fe4f961145af4cde0`  
		Last Modified: Wed, 14 Jul 2021 04:24:43 GMT  
		Size: 10.7 KB (10659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe8a18351bbc592654b68f132ba3b2d4f542c9013876ef7df5be2e3b67f935e`  
		Last Modified: Wed, 14 Jul 2021 04:24:45 GMT  
		Size: 5.7 MB (5688752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.7-kernel-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:64715ffdad873a0fbd8df331a4a0617c85f6f4dcb7aa2cf0eca67616f391fb0d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (182026226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77888c40392dd2c7c05beb7b29a1ac8f72684772469335e9a72bec8f8143ac8`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 17 Jun 2021 23:24:58 GMT
ADD file:33bc9edd94d5731da919e83ed38bd4aa7daffcb5f629d93bbde112a795c79d48 in / 
# Thu, 17 Jun 2021 23:25:03 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:01:35 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 18 Jun 2021 02:02:36 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:02:42 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Fri, 18 Jun 2021 02:03:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 18 Jun 2021 02:04:05 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 09 Jul 2021 12:02:21 GMT
ARG VERBOSE=false
# Fri, 09 Jul 2021 12:02:27 GMT
ARG OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:02:34 GMT
ARG EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448
# Fri, 09 Jul 2021 12:02:38 GMT
ARG NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365
# Fri, 09 Jul 2021 12:02:44 GMT
ARG NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc
# Fri, 09 Jul 2021 12:02:51 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.7 org.opencontainers.image.revision=cl210720210629-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 09 Jul 2021 12:03:01 GMT
ENV LIBERTY_VERSION=21.0.0_07
# Fri, 09 Jul 2021 12:03:07 GMT
ARG LIBERTY_URL
# Fri, 09 Jul 2021 12:03:15 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 09 Jul 2021 12:04:20 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Jul 2021 12:04:26 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Jul 2021 12:04:33 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.7 BuildLabel=cl210720210629-1900
# Fri, 09 Jul 2021 12:04:40 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:04:53 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 09 Jul 2021 12:04:55 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Fri, 09 Jul 2021 12:04:56 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 09 Jul 2021 12:05:06 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 09 Jul 2021 12:05:38 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 09 Jul 2021 12:05:41 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 09 Jul 2021 12:05:45 GMT
USER 1001
# Fri, 09 Jul 2021 12:05:50 GMT
EXPOSE 9080 9443
# Fri, 09 Jul 2021 12:05:56 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 09 Jul 2021 12:06:02 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:4e37c2419ee7d7e826be5c6ee69243351aaf456d6527714660cf7e7015491051`  
		Last Modified: Thu, 17 Jun 2021 23:28:22 GMT  
		Size: 30.4 MB (30425356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8d177e4917900437a3445272639bed389b718cc65a87346ba94f6d99327f34`  
		Last Modified: Fri, 18 Jun 2021 02:07:44 GMT  
		Size: 3.1 MB (3082963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09af03e0818b00fa01f51019b91f996a958b5ffb6b7dcd23e88d4d0df759f391`  
		Last Modified: Fri, 18 Jun 2021 02:07:59 GMT  
		Size: 129.1 MB (129059791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e575d1b794a99b9e4326e5406abd771cab007d8e4496378d443e133aecd6fc`  
		Last Modified: Fri, 09 Jul 2021 12:56:48 GMT  
		Size: 14.1 MB (14082768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446edb557b83d18920bc3d64ad18bbc793493f18eac5610ae1ad819a37c1b5c8`  
		Last Modified: Fri, 09 Jul 2021 12:56:42 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92aca0eb7db57552a319340ea766bee3e176bb7d52bf238c98bfd7bf1edc62e8`  
		Last Modified: Fri, 09 Jul 2021 12:56:41 GMT  
		Size: 9.7 KB (9676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c68662de813b880c2fe01caa04a35528660efb50af580891a93b24b63ce4273`  
		Last Modified: Fri, 09 Jul 2021 12:56:41 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436ecaaacdb2e6ae26659e31d3c0b911a07a8cfe2e46922e0fe3377f753d6879`  
		Last Modified: Fri, 09 Jul 2021 12:56:42 GMT  
		Size: 10.7 KB (10676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb47456c330b967df85a4df66778e4b5762a52080a7ff7a89c042822a5d0841`  
		Last Modified: Fri, 09 Jul 2021 12:56:43 GMT  
		Size: 5.4 MB (5354019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.7-kernel-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:55856b2476daee17153b81ce345dffaa4083176bd759c79956bfba5c02509501
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174763616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff421b8cea6bcbbc11b070bb151010c392420c2bb198bfc328d4982b7e240b55`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:22 GMT
ADD file:9e621b1dfa735f1a89553f154f2a2a6f669ff610236d92d6ebf37d1f378d8ec0 in / 
# Tue, 13 Jul 2021 22:53:24 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:12:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:12:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:12:20 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:13:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:13:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 14 Jul 2021 00:25:32 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 00:25:32 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:25:32 GMT
ARG EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448
# Wed, 14 Jul 2021 00:25:32 GMT
ARG NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365
# Wed, 14 Jul 2021 00:25:33 GMT
ARG NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc
# Wed, 14 Jul 2021 00:25:33 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.7 org.opencontainers.image.revision=cl210720210629-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 00:25:34 GMT
ENV LIBERTY_VERSION=21.0.0_07
# Wed, 14 Jul 2021 00:25:34 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 00:25:34 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 00:25:46 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:25:47 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 00:25:47 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.7 BuildLabel=cl210720210629-1900
# Wed, 14 Jul 2021 00:25:47 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:25:49 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 00:25:50 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 00:25:50 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 00:25:51 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 00:26:01 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 00:26:02 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 14 Jul 2021 00:26:03 GMT
USER 1001
# Wed, 14 Jul 2021 00:26:04 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 00:26:04 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 00:26:04 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:3287e09e36098b10234ccc1f8db0b48e2027ca7caa353a362d65f9b017ab802e`  
		Last Modified: Tue, 13 Jul 2021 22:55:34 GMT  
		Size: 25.4 MB (25365649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6fe4e2b151f33398a6ef48bbb5d9ace538aa5ecf3fab9182babc3a85b9166b`  
		Last Modified: Tue, 13 Jul 2021 23:16:59 GMT  
		Size: 2.7 MB (2676828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b436dddc9b46f3b9e70224bb7eab52e58419d071c07f16f9ce63c77c81e5e24`  
		Last Modified: Tue, 13 Jul 2021 23:17:08 GMT  
		Size: 126.7 MB (126676530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfeb84cc8b0669c7b9e77df6ef93a9af10143ddecdf7cbab90eb2541ea6dae9f`  
		Last Modified: Wed, 14 Jul 2021 00:59:46 GMT  
		Size: 14.1 MB (14082055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc5188d927b29c1e6ec8a352cb13ab32af8ed150ee5c1abb928fef7ec7d2a15`  
		Last Modified: Wed, 14 Jul 2021 00:59:43 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c09c4ee0bf95890e60c06b29e00402b7ca7fbbe3f9b31bbf00426c75b84aaa`  
		Last Modified: Wed, 14 Jul 2021 00:59:43 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7b8bba08a70c5ffca0778748f3e75b2ee3c4d131b3bf31b9e7dfd735c9ec4b`  
		Last Modified: Wed, 14 Jul 2021 00:59:43 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe12bbaa95b8b804b7e6752881f522078004b8355c33d3363e49e5d4c438c2cd`  
		Last Modified: Wed, 14 Jul 2021 00:59:43 GMT  
		Size: 10.7 KB (10664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7dea27e762888900b197a8656b67c7943b619a99797e6b2fcdee52af376627`  
		Last Modified: Wed, 14 Jul 2021 00:59:44 GMT  
		Size: 5.9 MB (5941251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:full`

```console
$ docker pull websphere-liberty@sha256:27080236fe8c5aa85459d37ec18b450a792074c7c500649aacdeb1ea5697c749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:full` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:593621830dcf7ed862f01c7b59dbf0c52ac38031f5d4a9e4238c21978417c3ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.8 MB (402767961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32dfa93cd1b2e8518ca9ca11addf6364d0e93655b8fa5c76b8caca2bb92ac7a2`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:19:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:19:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:19:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:19:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:19:52 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 14 Jul 2021 03:57:10 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 03:57:10 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 03:57:10 GMT
ARG EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448
# Wed, 14 Jul 2021 03:57:11 GMT
ARG NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365
# Wed, 14 Jul 2021 03:57:11 GMT
ARG NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc
# Wed, 14 Jul 2021 03:57:11 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.7 org.opencontainers.image.revision=cl210720210629-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 03:57:11 GMT
ENV LIBERTY_VERSION=21.0.0_07
# Wed, 14 Jul 2021 03:57:11 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 03:57:12 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 03:57:23 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 03:57:23 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 03:57:23 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.7 BuildLabel=cl210720210629-1900
# Wed, 14 Jul 2021 03:57:23 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 03:57:25 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 03:57:25 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 03:57:26 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 03:57:27 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 03:57:37 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 03:57:37 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 14 Jul 2021 03:57:37 GMT
USER 1001
# Wed, 14 Jul 2021 03:57:37 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 03:57:37 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 03:57:38 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 14 Jul 2021 03:58:11 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 03:58:11 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 14 Jul 2021 04:01:40 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Wed, 14 Jul 2021 04:01:41 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 14 Jul 2021 04:02:17 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22821a14390caaab5b1f7ca9feb8e54ce64d3d81ca1fa64c6f1eee32ae92da5b`  
		Last Modified: Tue, 13 Jul 2021 23:23:03 GMT  
		Size: 3.0 MB (2959004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4403b30ef5ef8f7b37c65fc3d0a0e0d7e0fca7451dd9b42a43bee1de1f389c09`  
		Last Modified: Tue, 13 Jul 2021 23:23:13 GMT  
		Size: 129.5 MB (129536228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2229a5b48fafe35e4b36d1919ccb99f32d1692b2bec7c9fea77733becb84530c`  
		Last Modified: Wed, 14 Jul 2021 04:24:48 GMT  
		Size: 14.1 MB (14082341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0508db572632c638c6182a39308e5731bfcbd4b598bfc908f0a6c4db23ac0db`  
		Last Modified: Wed, 14 Jul 2021 04:24:43 GMT  
		Size: 692.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5845fe90cc54b2ed48af7b145887feaa37656b8c9d799f40dabf84831e141087`  
		Last Modified: Wed, 14 Jul 2021 04:24:43 GMT  
		Size: 9.7 KB (9673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ea30f4f8482cb87d0f69111edc0a66bc10b6f55dc9431070743dde095a76c7`  
		Last Modified: Wed, 14 Jul 2021 04:24:43 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32852fe819a654da3298d6bb5d00119b56e444c4ff75a5fe4f961145af4cde0`  
		Last Modified: Wed, 14 Jul 2021 04:24:43 GMT  
		Size: 10.7 KB (10659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe8a18351bbc592654b68f132ba3b2d4f542c9013876ef7df5be2e3b67f935e`  
		Last Modified: Wed, 14 Jul 2021 04:24:45 GMT  
		Size: 5.7 MB (5688752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0302e7744226a971fe896e471720ff2db67b7146cdec0050817f45d6b09a04`  
		Last Modified: Wed, 14 Jul 2021 04:25:21 GMT  
		Size: 207.9 MB (207908003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e46e41ead606c0ff89f626961bf1e848fd9710f66ba1036b6f33f388675358`  
		Last Modified: Wed, 14 Jul 2021 04:25:09 GMT  
		Size: 944.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1bdc8179339ab3fcfbe904d27833d22d74c5ea380c667dcdf9e8ba63b9e8300`  
		Last Modified: Wed, 14 Jul 2021 04:25:12 GMT  
		Size: 15.9 MB (15865245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full` - linux; 386

```console
$ docker pull websphere-liberty@sha256:c847143995aec30ca5d4526544d7c41ca7a42a8baf8195848864d0128e96ecf3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.2 MB (349209019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d2c9374be56a63d6e35820fec8676f2d4ed2b9bdaf09a49c8545b039479bb7`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 20 Mar 2020 18:38:55 GMT
ADD file:d859d389e38b7ac70fd56f97e38d52a77b58e72b96237a4302d1984cdd912a55 in / 
# Fri, 20 Mar 2020 18:38:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 18:38:57 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 18:38:58 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 18:38:58 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 19:06:34 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 20 Mar 2020 19:06:41 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:06:42 GMT
ENV JAVA_VERSION=1.8.0_sr6fp6
# Fri, 20 Mar 2020 19:07:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='87f9d45b7e1fa65ec018479f3ca7da69a03b52b0da10b8d1555142eec8ab0093';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='b5f825047c9bb5d360fb83694f12e17b1a5a15abf94ac82cd0a3aea32c9a361c';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f3c04cd07ef269c24373840eae6f59c7db7a16d2e206d393ba93efa6dbb8d74f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2bbefda96f7d1a5f1694893961e92ccc59dfa50375ae5450675d7a4213d5812e';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d5b0508d53d1c7382c06f5bc1daf3d57c19c70d851e86e6b1162bcd93f616f7e';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 20 Mar 2020 19:07:26 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 20 Mar 2020 19:31:53 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.3 org.opencontainers.image.revision=cl200320200305-1433
# Fri, 20 Mar 2020 19:31:53 GMT
ENV LIBERTY_VERSION=20.0.0_03
# Fri, 20 Mar 2020 19:31:53 GMT
ARG LIBERTY_URL
# Fri, 20 Mar 2020 19:31:53 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 20 Mar 2020 19:32:02 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:32:03 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2020 19:32:03 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.3 BuildLabel=cl200320200305-1433
# Fri, 20 Mar 2020 19:32:03 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Fri, 20 Mar 2020 19:32:04 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 20 Mar 2020 19:32:04 GMT
COPY dir:0d0cedab2fbb7208b9d81afa78e9f15b12b71232224a2fe9753c00b7b72bd72e in /opt/ibm/helpers/ 
# Fri, 20 Mar 2020 19:32:05 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 20 Mar 2020 19:32:05 GMT
COPY dir:9277507d983008afcf8df6e0bfe2735bd4e92717515dbb3a7e268c830f213489 in /licenses/ 
# Fri, 20 Mar 2020 19:32:06 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 20 Mar 2020 19:32:06 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Fri, 20 Mar 2020 19:32:06 GMT
USER 1001
# Fri, 20 Mar 2020 19:32:06 GMT
EXPOSE 9080 9443
# Fri, 20 Mar 2020 19:32:07 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 20 Mar 2020 19:32:07 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 20 Mar 2020 19:32:10 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 20 Mar 2020 19:35:01 GMT
# ARGS: REPOSITORIES_PROPERTIES=
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Fri, 20 Mar 2020 19:35:01 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
```

-	Layers:
	-	`sha256:765ce743592771b94ad8ff27e281e66c13f6039962c7dde4dbe47123081e015b`  
		Last Modified: Mon, 16 Mar 2020 15:38:41 GMT  
		Size: 27.1 MB (27122453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59dc9c4739090a3d2f7265f1f8184b1cbd8ae133b863f8aa93ec5cf1761ee7a5`  
		Last Modified: Fri, 20 Mar 2020 18:39:35 GMT  
		Size: 34.6 KB (34625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a5b698281c077f48fc598e698f0619e4d00a2fedc1832fc95e9cf281408f63`  
		Last Modified: Fri, 20 Mar 2020 18:39:34 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaebe599891b1e1befc10d752a117cc5615ec2dd3913d399fd66e26e0cace3e5`  
		Last Modified: Fri, 20 Mar 2020 18:39:34 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f829150bc8a53a37ac17eb34838fa33c990881a4031bc650a9dae26b3f7880e`  
		Last Modified: Fri, 20 Mar 2020 19:09:23 GMT  
		Size: 3.0 MB (2992132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17b9ccc4baf3a1ffa517a03c7c3d01900136b128b36a83558c67c42e6c1cbaa`  
		Last Modified: Fri, 20 Mar 2020 19:09:35 GMT  
		Size: 118.8 MB (118756706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5011972f1876d464fb62206211a5b5e162ba2603bf20fc4cd0f2b4ffd311cd9`  
		Last Modified: Fri, 20 Mar 2020 19:39:16 GMT  
		Size: 13.6 MB (13600436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5395b713d5baa0917182ca82077b6fa2a0c51789907f96cbb12455586d9fa9b`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389324a3d9489b2fbcd5946f9d24285c0171c3218470e4a5e2d45c731cefc522`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 3.5 KB (3515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38ea596499e1f23ce426826250984869e92da50aec5845a6233a76d7764bfd1`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea3197b55235384f836e31a605c460f6cb7196f68dc29c65640738d8aa50188`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 57.4 KB (57426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683f76bf565cdb9e59c325f24357eb6b164555ed8629a4b8383448239608966d`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 4.4 KB (4358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cd2560c76831311d13d197b4784e0826f6ffae62e3b9a22d2fa5675b9b71a2`  
		Last Modified: Fri, 20 Mar 2020 19:39:42 GMT  
		Size: 186.6 MB (186634496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9891aa2b3e904f8f514677372187983ac12c98c209c433ab5bf0862e09d6f4ef`  
		Last Modified: Fri, 20 Mar 2020 19:39:20 GMT  
		Size: 943.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:afb93aa6c7922a3f90dd7096fe10c5d03eaa555892eaabe424d869169285f8e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.4 MB (403364706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c6deacd67107f6a602891b5d74b510d28a8cb9931c19909ac9c1fd01abbe1a`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 17 Jun 2021 23:24:58 GMT
ADD file:33bc9edd94d5731da919e83ed38bd4aa7daffcb5f629d93bbde112a795c79d48 in / 
# Thu, 17 Jun 2021 23:25:03 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:01:35 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 18 Jun 2021 02:02:36 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:02:42 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Fri, 18 Jun 2021 02:03:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 18 Jun 2021 02:04:05 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 09 Jul 2021 12:02:21 GMT
ARG VERBOSE=false
# Fri, 09 Jul 2021 12:02:27 GMT
ARG OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:02:34 GMT
ARG EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448
# Fri, 09 Jul 2021 12:02:38 GMT
ARG NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365
# Fri, 09 Jul 2021 12:02:44 GMT
ARG NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc
# Fri, 09 Jul 2021 12:02:51 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.7 org.opencontainers.image.revision=cl210720210629-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 09 Jul 2021 12:03:01 GMT
ENV LIBERTY_VERSION=21.0.0_07
# Fri, 09 Jul 2021 12:03:07 GMT
ARG LIBERTY_URL
# Fri, 09 Jul 2021 12:03:15 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 09 Jul 2021 12:04:20 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Jul 2021 12:04:26 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Jul 2021 12:04:33 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.7 BuildLabel=cl210720210629-1900
# Fri, 09 Jul 2021 12:04:40 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:04:53 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 09 Jul 2021 12:04:55 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Fri, 09 Jul 2021 12:04:56 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 09 Jul 2021 12:05:06 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 09 Jul 2021 12:05:38 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 09 Jul 2021 12:05:41 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 09 Jul 2021 12:05:45 GMT
USER 1001
# Fri, 09 Jul 2021 12:05:50 GMT
EXPOSE 9080 9443
# Fri, 09 Jul 2021 12:05:56 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 09 Jul 2021 12:06:02 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 09 Jul 2021 12:09:58 GMT
ARG VERBOSE=false
# Fri, 09 Jul 2021 12:10:00 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 09 Jul 2021 12:14:03 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Fri, 09 Jul 2021 12:14:14 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 09 Jul 2021 12:15:29 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:4e37c2419ee7d7e826be5c6ee69243351aaf456d6527714660cf7e7015491051`  
		Last Modified: Thu, 17 Jun 2021 23:28:22 GMT  
		Size: 30.4 MB (30425356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8d177e4917900437a3445272639bed389b718cc65a87346ba94f6d99327f34`  
		Last Modified: Fri, 18 Jun 2021 02:07:44 GMT  
		Size: 3.1 MB (3082963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09af03e0818b00fa01f51019b91f996a958b5ffb6b7dcd23e88d4d0df759f391`  
		Last Modified: Fri, 18 Jun 2021 02:07:59 GMT  
		Size: 129.1 MB (129059791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e575d1b794a99b9e4326e5406abd771cab007d8e4496378d443e133aecd6fc`  
		Last Modified: Fri, 09 Jul 2021 12:56:48 GMT  
		Size: 14.1 MB (14082768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446edb557b83d18920bc3d64ad18bbc793493f18eac5610ae1ad819a37c1b5c8`  
		Last Modified: Fri, 09 Jul 2021 12:56:42 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92aca0eb7db57552a319340ea766bee3e176bb7d52bf238c98bfd7bf1edc62e8`  
		Last Modified: Fri, 09 Jul 2021 12:56:41 GMT  
		Size: 9.7 KB (9676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c68662de813b880c2fe01caa04a35528660efb50af580891a93b24b63ce4273`  
		Last Modified: Fri, 09 Jul 2021 12:56:41 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436ecaaacdb2e6ae26659e31d3c0b911a07a8cfe2e46922e0fe3377f753d6879`  
		Last Modified: Fri, 09 Jul 2021 12:56:42 GMT  
		Size: 10.7 KB (10676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb47456c330b967df85a4df66778e4b5762a52080a7ff7a89c042822a5d0841`  
		Last Modified: Fri, 09 Jul 2021 12:56:43 GMT  
		Size: 5.4 MB (5354019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d889510935916732b2718d9a7f5adffc222f87f6f0ad7c7036c320afe43a1d8e`  
		Last Modified: Fri, 09 Jul 2021 12:57:31 GMT  
		Size: 207.9 MB (207908499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a254bd0d60b4e9fef14d2e8f2ca322cf2da3a90df1cfa3930b64c3cc95d113`  
		Last Modified: Fri, 09 Jul 2021 12:57:12 GMT  
		Size: 952.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a8372af7fe68d759c42eb1c1105eb84743e9e40ba7caf5490c68817776fea4`  
		Last Modified: Fri, 09 Jul 2021 12:57:15 GMT  
		Size: 13.4 MB (13429029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:feccab75dd49b9eacc3dec41d6c9fc662ce921e51dde3fa8868c6968d2b2a570
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.2 MB (398216420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c531ce10ac925f59e00e218ed78df32aab4514ad3a8758dae3b032ec637546b0`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:22 GMT
ADD file:9e621b1dfa735f1a89553f154f2a2a6f669ff610236d92d6ebf37d1f378d8ec0 in / 
# Tue, 13 Jul 2021 22:53:24 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:12:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:12:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:12:20 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:13:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:13:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 14 Jul 2021 00:25:32 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 00:25:32 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:25:32 GMT
ARG EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448
# Wed, 14 Jul 2021 00:25:32 GMT
ARG NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365
# Wed, 14 Jul 2021 00:25:33 GMT
ARG NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc
# Wed, 14 Jul 2021 00:25:33 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.7 org.opencontainers.image.revision=cl210720210629-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 00:25:34 GMT
ENV LIBERTY_VERSION=21.0.0_07
# Wed, 14 Jul 2021 00:25:34 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 00:25:34 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 00:25:46 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:25:47 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 00:25:47 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.7 BuildLabel=cl210720210629-1900
# Wed, 14 Jul 2021 00:25:47 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:25:49 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 00:25:50 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 00:25:50 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 00:25:51 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 00:26:01 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 00:26:02 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 14 Jul 2021 00:26:03 GMT
USER 1001
# Wed, 14 Jul 2021 00:26:04 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 00:26:04 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 00:26:04 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 14 Jul 2021 00:26:59 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 00:27:00 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 14 Jul 2021 00:30:33 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Wed, 14 Jul 2021 00:30:39 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 14 Jul 2021 00:31:15 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:3287e09e36098b10234ccc1f8db0b48e2027ca7caa353a362d65f9b017ab802e`  
		Last Modified: Tue, 13 Jul 2021 22:55:34 GMT  
		Size: 25.4 MB (25365649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6fe4e2b151f33398a6ef48bbb5d9ace538aa5ecf3fab9182babc3a85b9166b`  
		Last Modified: Tue, 13 Jul 2021 23:16:59 GMT  
		Size: 2.7 MB (2676828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b436dddc9b46f3b9e70224bb7eab52e58419d071c07f16f9ce63c77c81e5e24`  
		Last Modified: Tue, 13 Jul 2021 23:17:08 GMT  
		Size: 126.7 MB (126676530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfeb84cc8b0669c7b9e77df6ef93a9af10143ddecdf7cbab90eb2541ea6dae9f`  
		Last Modified: Wed, 14 Jul 2021 00:59:46 GMT  
		Size: 14.1 MB (14082055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc5188d927b29c1e6ec8a352cb13ab32af8ed150ee5c1abb928fef7ec7d2a15`  
		Last Modified: Wed, 14 Jul 2021 00:59:43 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c09c4ee0bf95890e60c06b29e00402b7ca7fbbe3f9b31bbf00426c75b84aaa`  
		Last Modified: Wed, 14 Jul 2021 00:59:43 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7b8bba08a70c5ffca0778748f3e75b2ee3c4d131b3bf31b9e7dfd735c9ec4b`  
		Last Modified: Wed, 14 Jul 2021 00:59:43 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe12bbaa95b8b804b7e6752881f522078004b8355c33d3363e49e5d4c438c2cd`  
		Last Modified: Wed, 14 Jul 2021 00:59:43 GMT  
		Size: 10.7 KB (10664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7dea27e762888900b197a8656b67c7943b619a99797e6b2fcdee52af376627`  
		Last Modified: Wed, 14 Jul 2021 00:59:44 GMT  
		Size: 5.9 MB (5941251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7dda827d3b54d7e48c6470c19206b3547c368b168c59c5946383a1217c8e2d0`  
		Last Modified: Wed, 14 Jul 2021 01:00:10 GMT  
		Size: 207.9 MB (207910341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358ded070ceaa1f2c8acb8b7172deb3fa6884c261e423c03b2585a8d2bbb042c`  
		Last Modified: Wed, 14 Jul 2021 00:59:59 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69694bdedf8776b29d158ed194e88e78c47e8365b5360ad768020dd3a3b22f3`  
		Last Modified: Wed, 14 Jul 2021 01:00:01 GMT  
		Size: 15.5 MB (15541515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:full-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:c0b24a9ceae5a69e70450ed1f2bf44b728bc0e82881ca34ed3ecec5f57bdea25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:full-java11-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:1607c542f71b2f5ccef563b8d06cd80ff5680045ad2870bcd103cb648cbd31b6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.9 MB (331946982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b62d781949b689aa65fd1a31820767e9ffe5f41ab8708950a00263da8e72220b`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:29:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 14 Jul 2021 00:30:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:33:59 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Wed, 14 Jul 2021 00:35:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 14 Jul 2021 00:35:04 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 00:35:04 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 14 Jul 2021 00:35:41 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 14 Jul 2021 03:57:41 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 03:57:41 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 03:57:41 GMT
ARG EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448
# Wed, 14 Jul 2021 03:57:41 GMT
ARG NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365
# Wed, 14 Jul 2021 03:57:41 GMT
ARG NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc
# Wed, 14 Jul 2021 03:57:42 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.7 org.opencontainers.image.revision=cl210720210629-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 03:57:42 GMT
ENV LIBERTY_VERSION=21.0.0_07
# Wed, 14 Jul 2021 03:57:42 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 03:57:42 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 03:57:52 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 03:57:52 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 03:57:52 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.7 BuildLabel=cl210720210629-1900
# Wed, 14 Jul 2021 03:57:52 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 03:57:54 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 03:57:54 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 03:57:55 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 03:57:56 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 03:58:03 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 03:58:04 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 14 Jul 2021 03:58:04 GMT
USER 1001
# Wed, 14 Jul 2021 03:58:04 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 03:58:04 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 03:58:04 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 14 Jul 2021 04:02:22 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 04:02:23 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 14 Jul 2021 04:05:29 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Wed, 14 Jul 2021 04:05:30 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 14 Jul 2021 04:06:04 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1182b8c86e6bb404b0d40d2cdcdcaf4347c5aad464143625307b362caff690`  
		Last Modified: Wed, 14 Jul 2021 00:44:02 GMT  
		Size: 16.0 MB (16033076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1461af6857aed41d09a8ce6e2447ad52c9cdf1e6fe2f19ddaa2ab35d21aa1b`  
		Last Modified: Wed, 14 Jul 2021 00:50:41 GMT  
		Size: 44.4 MB (44382137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b538d86edfd8bb98ca5958e79321f730b01a2adc10244bd8ff7abf2aea9b8d8`  
		Last Modified: Wed, 14 Jul 2021 00:50:36 GMT  
		Size: 4.1 MB (4134048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a532adad204607676dccc5605c883856d719bc1eccc9197565f94f999ca6bf0a`  
		Last Modified: Wed, 14 Jul 2021 04:25:00 GMT  
		Size: 14.2 MB (14180546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bba4c8d4ae12b71c54ff9d090380b6ce40d98fcc357144ec5feaa9563dfa52b`  
		Last Modified: Wed, 14 Jul 2021 04:24:56 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5adbe7df68ffe9638f162021e06ead203a57226067210dd2b2fc8aafcbc8834e`  
		Last Modified: Wed, 14 Jul 2021 04:24:56 GMT  
		Size: 9.7 KB (9671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87cc611f3f91d20de349776f088cccc8cbfee6155ce83bee4dc0b2334e4d998`  
		Last Modified: Wed, 14 Jul 2021 04:24:56 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b31847e7e303752ed571f3af6ab967cb238f28af8751b50f7f8e544d697032b`  
		Last Modified: Wed, 14 Jul 2021 04:24:56 GMT  
		Size: 10.7 KB (10665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d5797f6cdf5b45d44deeed85d1698445e0cba043586c1c26cf5e0fc909a998`  
		Last Modified: Wed, 14 Jul 2021 04:24:56 GMT  
		Size: 2.5 MB (2468349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233938e6ffc02206885d22169230d199b4b36b54553521886d91184752e3daaa`  
		Last Modified: Wed, 14 Jul 2021 04:25:44 GMT  
		Size: 207.9 MB (207908038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90ef723b8a21c8cbbf581194e4e42068eacb9843ba3c0dc711c7848bdfdf7ad`  
		Last Modified: Wed, 14 Jul 2021 04:25:32 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8454d223bb998d37808fe994446cbadf77700813c85d535e25576b0291684827`  
		Last Modified: Wed, 14 Jul 2021 04:25:35 GMT  
		Size: 14.3 MB (14252672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:8cafec99a4314343a03fa7d874f636af661cbe6e52f1c5c859c3f124e3ef0059
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.9 MB (335861298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c09e44e2896ed63922f55ca03045a2bcaeca22760bae153406098e092d46f83`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 01:29:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 01:31:53 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:41:26 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Fri, 18 Jun 2021 01:43:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 01:43:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 01:43:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 18 Jun 2021 01:44:39 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 09 Jul 2021 12:06:18 GMT
ARG VERBOSE=false
# Fri, 09 Jul 2021 12:06:22 GMT
ARG OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:06:28 GMT
ARG EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448
# Fri, 09 Jul 2021 12:06:37 GMT
ARG NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365
# Fri, 09 Jul 2021 12:06:42 GMT
ARG NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc
# Fri, 09 Jul 2021 12:06:49 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.7 org.opencontainers.image.revision=cl210720210629-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 09 Jul 2021 12:06:56 GMT
ENV LIBERTY_VERSION=21.0.0_07
# Fri, 09 Jul 2021 12:07:00 GMT
ARG LIBERTY_URL
# Fri, 09 Jul 2021 12:07:10 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 09 Jul 2021 12:07:56 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Jul 2021 12:08:05 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Jul 2021 12:08:11 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.7 BuildLabel=cl210720210629-1900
# Fri, 09 Jul 2021 12:08:20 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:08:35 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 09 Jul 2021 12:08:37 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Fri, 09 Jul 2021 12:08:40 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 09 Jul 2021 12:08:57 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 09 Jul 2021 12:09:15 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 09 Jul 2021 12:09:20 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 09 Jul 2021 12:09:25 GMT
USER 1001
# Fri, 09 Jul 2021 12:09:30 GMT
EXPOSE 9080 9443
# Fri, 09 Jul 2021 12:09:33 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 09 Jul 2021 12:09:40 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 09 Jul 2021 12:15:43 GMT
ARG VERBOSE=false
# Fri, 09 Jul 2021 12:15:49 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 09 Jul 2021 12:19:40 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Fri, 09 Jul 2021 12:19:50 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 09 Jul 2021 12:20:53 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b268950217e490e209e0491ae6fbd3af12b4642aefad9c0039daf7b3ea0371`  
		Last Modified: Fri, 18 Jun 2021 01:52:43 GMT  
		Size: 17.2 MB (17208433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74aa12681d5d14a96459a14094fd9b08f1379e61fa1e8979b311b55b0561dead`  
		Last Modified: Fri, 18 Jun 2021 01:57:43 GMT  
		Size: 45.1 MB (45104807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee28cff75d70e071001e265878f54c811f52ab2cf95d0cc9daa0085c8e1465d`  
		Last Modified: Fri, 18 Jun 2021 01:57:35 GMT  
		Size: 3.3 MB (3284426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d645b89a4dd25a5d864e0eee16fad18b47003f9afbc03fcbb0d0dd722dc67fc8`  
		Last Modified: Fri, 09 Jul 2021 12:57:02 GMT  
		Size: 14.2 MB (14181551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4da63aa53ce2f86286610b335d47c205209123f3b10468f1fbd732174572770`  
		Last Modified: Fri, 09 Jul 2021 12:56:57 GMT  
		Size: 692.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85cdabb46ca79b2b6ab7a933df344ee131c49e7f28758e95f0563be56d88830`  
		Last Modified: Fri, 09 Jul 2021 12:56:57 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee96f4cf06004c656da5e448f035060f82ec53f290430a9869e4387fce1d59a`  
		Last Modified: Fri, 09 Jul 2021 12:56:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c088ac6df31e5b351ce2912eadc32bd7d67f7dc02c903d844f4527504ecfba`  
		Last Modified: Fri, 09 Jul 2021 12:56:58 GMT  
		Size: 10.7 KB (10662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3be9bc98dfc99235b8a23c99b39f927cca9fab5b980ed63f0cc3af7db1ff88`  
		Last Modified: Fri, 09 Jul 2021 12:56:58 GMT  
		Size: 2.5 MB (2470788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3cfa0388ed805bea8ccb8c5f29a0b03a9f2a3862fab969e62f4a0abd6c88775`  
		Last Modified: Fri, 09 Jul 2021 12:58:05 GMT  
		Size: 207.9 MB (207908223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bdbe2e74bb76632286d5ef23c2b89cca3c2efc67ca72536dae6363ccb2c2ce6`  
		Last Modified: Fri, 09 Jul 2021 12:57:45 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f426bfa2fd56befb95dd5105bcc4654ef746edb442b2f15785812129669d507`  
		Last Modified: Fri, 09 Jul 2021 12:57:48 GMT  
		Size: 12.4 MB (12402580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:649732a70fc7bf2f172717342cb159e7ed4d8eb9b486d1707f5270cafa134725
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.8 MB (328834951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5776437add2a6dea68145518bf675bc88e7ea3b5d3caeb22528b634a4663aedb`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:34 GMT
ADD file:ae5354f89d91eedd0614e3e97ee59fd6e23254923062c288d775e19b137dfd1c in / 
# Tue, 13 Jul 2021 22:53:36 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:18:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Jul 2021 23:18:55 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:23:22 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Tue, 13 Jul 2021 23:24:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 13 Jul 2021 23:24:37 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jul 2021 23:24:37 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 13 Jul 2021 23:25:12 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 14 Jul 2021 00:26:14 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 00:26:15 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:26:15 GMT
ARG EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448
# Wed, 14 Jul 2021 00:26:16 GMT
ARG NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365
# Wed, 14 Jul 2021 00:26:16 GMT
ARG NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc
# Wed, 14 Jul 2021 00:26:16 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.7 org.opencontainers.image.revision=cl210720210629-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 00:26:17 GMT
ENV LIBERTY_VERSION=21.0.0_07
# Wed, 14 Jul 2021 00:26:17 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 00:26:18 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 00:26:29 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:26:30 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 00:26:31 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.7 BuildLabel=cl210720210629-1900
# Wed, 14 Jul 2021 00:26:31 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:26:32 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 00:26:33 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 00:26:33 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 00:26:35 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 00:26:44 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 00:26:45 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 14 Jul 2021 00:26:46 GMT
USER 1001
# Wed, 14 Jul 2021 00:26:46 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 00:26:47 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 00:26:47 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 14 Jul 2021 00:31:36 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 00:31:37 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 14 Jul 2021 00:35:09 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Wed, 14 Jul 2021 00:35:17 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 14 Jul 2021 00:35:58 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:761fa758059faa0c80b0b90fcbcc192fc7f573da055460d5b3f019e0faceeb7a`  
		Last Modified: Tue, 13 Jul 2021 22:55:47 GMT  
		Size: 27.1 MB (27149318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0237838e148d45cea54b0d86c053131b4152f4928836cbb3a0c83ba79b538728`  
		Last Modified: Tue, 13 Jul 2021 23:32:23 GMT  
		Size: 15.7 MB (15741695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454768ac3fd4bd9b5536afd4e03c6c369d7eae1ee6b240b461dace5364b911f5`  
		Last Modified: Tue, 13 Jul 2021 23:36:09 GMT  
		Size: 43.8 MB (43840969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add6cc1d828e7c42608c4398d9d18baceea2e5104c4ff50d96eba8015aa4a896`  
		Last Modified: Tue, 13 Jul 2021 23:36:03 GMT  
		Size: 3.8 MB (3845109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8db25e8b8b8c38fe38441c03961e2239699ec7d60c2535ee7e3f32b5d9408e`  
		Last Modified: Wed, 14 Jul 2021 00:59:54 GMT  
		Size: 14.2 MB (14180686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2f25fb8653dcf183e4697f3c91aac2b7f2b52ce9b29ddad16203148334326c`  
		Last Modified: Wed, 14 Jul 2021 00:59:51 GMT  
		Size: 691.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5899b27fbac50a6a5dc63dea77388554c0a30d19d49c0fede69dc55b139aaf9d`  
		Last Modified: Wed, 14 Jul 2021 00:59:51 GMT  
		Size: 9.7 KB (9668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e909c0ea2090f66e195b6a98342c9481ac3c8ca4424dee2a56e9510339fc74d2`  
		Last Modified: Wed, 14 Jul 2021 00:59:51 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0725387dcb18203fe63c473bed29ea62c4967f1aa7cd4875bf595e119b67ce98`  
		Last Modified: Wed, 14 Jul 2021 00:59:51 GMT  
		Size: 10.7 KB (10657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0dca61c9477b822a385de7b1018700d87fa9b82c75df3ce7f8ff1d897b5ae27`  
		Last Modified: Wed, 14 Jul 2021 00:59:53 GMT  
		Size: 2.5 MB (2471680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f00e32e1d90d64971a74357199a5c0acaa27cf39d5469135e2d09d3862bbb2`  
		Last Modified: Wed, 14 Jul 2021 01:00:34 GMT  
		Size: 207.9 MB (207908299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f66031a5f5dcccabe1352d2b7c68e45215f20afb38a0b5b81ece512fc359ef1`  
		Last Modified: Wed, 14 Jul 2021 01:00:19 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2ed70fc141f537c65280ed5b10e55b6bac20472e876a135f8723c10208b013`  
		Last Modified: Wed, 14 Jul 2021 01:00:21 GMT  
		Size: 13.7 MB (13674963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:kernel`

```console
$ docker pull websphere-liberty@sha256:887f92b492185a808d8720cfbf4ff3dbfa17f64fde0c7dcf18bd9ebe0ef7f927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:kernel` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:508840046c1a01e61a610495f4f0220e90127fa32ffc287c877d4d75aa77e33e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.0 MB (178993769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58ca11b94f5e93af4ddd5d167ebc64cb6ef4c8ecacfe47cec39b23a7966dbb80`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:19:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:19:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:19:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:19:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:19:52 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 14 Jul 2021 03:57:10 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 03:57:10 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 03:57:10 GMT
ARG EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448
# Wed, 14 Jul 2021 03:57:11 GMT
ARG NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365
# Wed, 14 Jul 2021 03:57:11 GMT
ARG NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc
# Wed, 14 Jul 2021 03:57:11 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.7 org.opencontainers.image.revision=cl210720210629-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 03:57:11 GMT
ENV LIBERTY_VERSION=21.0.0_07
# Wed, 14 Jul 2021 03:57:11 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 03:57:12 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 03:57:23 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 03:57:23 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 03:57:23 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.7 BuildLabel=cl210720210629-1900
# Wed, 14 Jul 2021 03:57:23 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 03:57:25 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 03:57:25 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 03:57:26 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 03:57:27 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 03:57:37 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 03:57:37 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 14 Jul 2021 03:57:37 GMT
USER 1001
# Wed, 14 Jul 2021 03:57:37 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 03:57:37 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 03:57:38 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22821a14390caaab5b1f7ca9feb8e54ce64d3d81ca1fa64c6f1eee32ae92da5b`  
		Last Modified: Tue, 13 Jul 2021 23:23:03 GMT  
		Size: 3.0 MB (2959004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4403b30ef5ef8f7b37c65fc3d0a0e0d7e0fca7451dd9b42a43bee1de1f389c09`  
		Last Modified: Tue, 13 Jul 2021 23:23:13 GMT  
		Size: 129.5 MB (129536228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2229a5b48fafe35e4b36d1919ccb99f32d1692b2bec7c9fea77733becb84530c`  
		Last Modified: Wed, 14 Jul 2021 04:24:48 GMT  
		Size: 14.1 MB (14082341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0508db572632c638c6182a39308e5731bfcbd4b598bfc908f0a6c4db23ac0db`  
		Last Modified: Wed, 14 Jul 2021 04:24:43 GMT  
		Size: 692.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5845fe90cc54b2ed48af7b145887feaa37656b8c9d799f40dabf84831e141087`  
		Last Modified: Wed, 14 Jul 2021 04:24:43 GMT  
		Size: 9.7 KB (9673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ea30f4f8482cb87d0f69111edc0a66bc10b6f55dc9431070743dde095a76c7`  
		Last Modified: Wed, 14 Jul 2021 04:24:43 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32852fe819a654da3298d6bb5d00119b56e444c4ff75a5fe4f961145af4cde0`  
		Last Modified: Wed, 14 Jul 2021 04:24:43 GMT  
		Size: 10.7 KB (10659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe8a18351bbc592654b68f132ba3b2d4f542c9013876ef7df5be2e3b67f935e`  
		Last Modified: Wed, 14 Jul 2021 04:24:45 GMT  
		Size: 5.7 MB (5688752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel` - linux; 386

```console
$ docker pull websphere-liberty@sha256:21c2835a021b91c09268f12dc8f3c61f590c1b34d7669aeacf3792d83a7ef016
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162573580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e89243446a76e85ea4bf274dd0ad9e6fd0e763e50ced541577b62bee7dfcb74`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 20 Mar 2020 18:38:55 GMT
ADD file:d859d389e38b7ac70fd56f97e38d52a77b58e72b96237a4302d1984cdd912a55 in / 
# Fri, 20 Mar 2020 18:38:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 18:38:57 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 18:38:58 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 18:38:58 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 19:06:34 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 20 Mar 2020 19:06:41 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:06:42 GMT
ENV JAVA_VERSION=1.8.0_sr6fp6
# Fri, 20 Mar 2020 19:07:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='87f9d45b7e1fa65ec018479f3ca7da69a03b52b0da10b8d1555142eec8ab0093';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='b5f825047c9bb5d360fb83694f12e17b1a5a15abf94ac82cd0a3aea32c9a361c';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f3c04cd07ef269c24373840eae6f59c7db7a16d2e206d393ba93efa6dbb8d74f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2bbefda96f7d1a5f1694893961e92ccc59dfa50375ae5450675d7a4213d5812e';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d5b0508d53d1c7382c06f5bc1daf3d57c19c70d851e86e6b1162bcd93f616f7e';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 20 Mar 2020 19:07:26 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 20 Mar 2020 19:31:53 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.3 org.opencontainers.image.revision=cl200320200305-1433
# Fri, 20 Mar 2020 19:31:53 GMT
ENV LIBERTY_VERSION=20.0.0_03
# Fri, 20 Mar 2020 19:31:53 GMT
ARG LIBERTY_URL
# Fri, 20 Mar 2020 19:31:53 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 20 Mar 2020 19:32:02 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:32:03 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2020 19:32:03 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.3 BuildLabel=cl200320200305-1433
# Fri, 20 Mar 2020 19:32:03 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Fri, 20 Mar 2020 19:32:04 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 20 Mar 2020 19:32:04 GMT
COPY dir:0d0cedab2fbb7208b9d81afa78e9f15b12b71232224a2fe9753c00b7b72bd72e in /opt/ibm/helpers/ 
# Fri, 20 Mar 2020 19:32:05 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 20 Mar 2020 19:32:05 GMT
COPY dir:9277507d983008afcf8df6e0bfe2735bd4e92717515dbb3a7e268c830f213489 in /licenses/ 
# Fri, 20 Mar 2020 19:32:06 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 20 Mar 2020 19:32:06 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Fri, 20 Mar 2020 19:32:06 GMT
USER 1001
# Fri, 20 Mar 2020 19:32:06 GMT
EXPOSE 9080 9443
# Fri, 20 Mar 2020 19:32:07 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 20 Mar 2020 19:32:07 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:765ce743592771b94ad8ff27e281e66c13f6039962c7dde4dbe47123081e015b`  
		Last Modified: Mon, 16 Mar 2020 15:38:41 GMT  
		Size: 27.1 MB (27122453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59dc9c4739090a3d2f7265f1f8184b1cbd8ae133b863f8aa93ec5cf1761ee7a5`  
		Last Modified: Fri, 20 Mar 2020 18:39:35 GMT  
		Size: 34.6 KB (34625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a5b698281c077f48fc598e698f0619e4d00a2fedc1832fc95e9cf281408f63`  
		Last Modified: Fri, 20 Mar 2020 18:39:34 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaebe599891b1e1befc10d752a117cc5615ec2dd3913d399fd66e26e0cace3e5`  
		Last Modified: Fri, 20 Mar 2020 18:39:34 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f829150bc8a53a37ac17eb34838fa33c990881a4031bc650a9dae26b3f7880e`  
		Last Modified: Fri, 20 Mar 2020 19:09:23 GMT  
		Size: 3.0 MB (2992132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17b9ccc4baf3a1ffa517a03c7c3d01900136b128b36a83558c67c42e6c1cbaa`  
		Last Modified: Fri, 20 Mar 2020 19:09:35 GMT  
		Size: 118.8 MB (118756706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5011972f1876d464fb62206211a5b5e162ba2603bf20fc4cd0f2b4ffd311cd9`  
		Last Modified: Fri, 20 Mar 2020 19:39:16 GMT  
		Size: 13.6 MB (13600436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5395b713d5baa0917182ca82077b6fa2a0c51789907f96cbb12455586d9fa9b`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389324a3d9489b2fbcd5946f9d24285c0171c3218470e4a5e2d45c731cefc522`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 3.5 KB (3515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38ea596499e1f23ce426826250984869e92da50aec5845a6233a76d7764bfd1`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea3197b55235384f836e31a605c460f6cb7196f68dc29c65640738d8aa50188`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 57.4 KB (57426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683f76bf565cdb9e59c325f24357eb6b164555ed8629a4b8383448239608966d`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 4.4 KB (4358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:64715ffdad873a0fbd8df331a4a0617c85f6f4dcb7aa2cf0eca67616f391fb0d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (182026226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77888c40392dd2c7c05beb7b29a1ac8f72684772469335e9a72bec8f8143ac8`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 17 Jun 2021 23:24:58 GMT
ADD file:33bc9edd94d5731da919e83ed38bd4aa7daffcb5f629d93bbde112a795c79d48 in / 
# Thu, 17 Jun 2021 23:25:03 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:01:35 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 18 Jun 2021 02:02:36 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:02:42 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Fri, 18 Jun 2021 02:03:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 18 Jun 2021 02:04:05 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 09 Jul 2021 12:02:21 GMT
ARG VERBOSE=false
# Fri, 09 Jul 2021 12:02:27 GMT
ARG OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:02:34 GMT
ARG EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448
# Fri, 09 Jul 2021 12:02:38 GMT
ARG NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365
# Fri, 09 Jul 2021 12:02:44 GMT
ARG NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc
# Fri, 09 Jul 2021 12:02:51 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.7 org.opencontainers.image.revision=cl210720210629-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 09 Jul 2021 12:03:01 GMT
ENV LIBERTY_VERSION=21.0.0_07
# Fri, 09 Jul 2021 12:03:07 GMT
ARG LIBERTY_URL
# Fri, 09 Jul 2021 12:03:15 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 09 Jul 2021 12:04:20 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Jul 2021 12:04:26 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Jul 2021 12:04:33 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.7 BuildLabel=cl210720210629-1900
# Fri, 09 Jul 2021 12:04:40 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:04:53 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 09 Jul 2021 12:04:55 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Fri, 09 Jul 2021 12:04:56 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 09 Jul 2021 12:05:06 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 09 Jul 2021 12:05:38 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 09 Jul 2021 12:05:41 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 09 Jul 2021 12:05:45 GMT
USER 1001
# Fri, 09 Jul 2021 12:05:50 GMT
EXPOSE 9080 9443
# Fri, 09 Jul 2021 12:05:56 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 09 Jul 2021 12:06:02 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:4e37c2419ee7d7e826be5c6ee69243351aaf456d6527714660cf7e7015491051`  
		Last Modified: Thu, 17 Jun 2021 23:28:22 GMT  
		Size: 30.4 MB (30425356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8d177e4917900437a3445272639bed389b718cc65a87346ba94f6d99327f34`  
		Last Modified: Fri, 18 Jun 2021 02:07:44 GMT  
		Size: 3.1 MB (3082963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09af03e0818b00fa01f51019b91f996a958b5ffb6b7dcd23e88d4d0df759f391`  
		Last Modified: Fri, 18 Jun 2021 02:07:59 GMT  
		Size: 129.1 MB (129059791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e575d1b794a99b9e4326e5406abd771cab007d8e4496378d443e133aecd6fc`  
		Last Modified: Fri, 09 Jul 2021 12:56:48 GMT  
		Size: 14.1 MB (14082768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446edb557b83d18920bc3d64ad18bbc793493f18eac5610ae1ad819a37c1b5c8`  
		Last Modified: Fri, 09 Jul 2021 12:56:42 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92aca0eb7db57552a319340ea766bee3e176bb7d52bf238c98bfd7bf1edc62e8`  
		Last Modified: Fri, 09 Jul 2021 12:56:41 GMT  
		Size: 9.7 KB (9676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c68662de813b880c2fe01caa04a35528660efb50af580891a93b24b63ce4273`  
		Last Modified: Fri, 09 Jul 2021 12:56:41 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436ecaaacdb2e6ae26659e31d3c0b911a07a8cfe2e46922e0fe3377f753d6879`  
		Last Modified: Fri, 09 Jul 2021 12:56:42 GMT  
		Size: 10.7 KB (10676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb47456c330b967df85a4df66778e4b5762a52080a7ff7a89c042822a5d0841`  
		Last Modified: Fri, 09 Jul 2021 12:56:43 GMT  
		Size: 5.4 MB (5354019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:55856b2476daee17153b81ce345dffaa4083176bd759c79956bfba5c02509501
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174763616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff421b8cea6bcbbc11b070bb151010c392420c2bb198bfc328d4982b7e240b55`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:22 GMT
ADD file:9e621b1dfa735f1a89553f154f2a2a6f669ff610236d92d6ebf37d1f378d8ec0 in / 
# Tue, 13 Jul 2021 22:53:24 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:12:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:12:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:12:20 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:13:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:13:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 14 Jul 2021 00:25:32 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 00:25:32 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:25:32 GMT
ARG EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448
# Wed, 14 Jul 2021 00:25:32 GMT
ARG NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365
# Wed, 14 Jul 2021 00:25:33 GMT
ARG NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc
# Wed, 14 Jul 2021 00:25:33 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.7 org.opencontainers.image.revision=cl210720210629-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 00:25:34 GMT
ENV LIBERTY_VERSION=21.0.0_07
# Wed, 14 Jul 2021 00:25:34 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 00:25:34 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 00:25:46 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:25:47 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 00:25:47 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.7 BuildLabel=cl210720210629-1900
# Wed, 14 Jul 2021 00:25:47 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:25:49 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 00:25:50 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 00:25:50 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 00:25:51 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 00:26:01 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 00:26:02 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 14 Jul 2021 00:26:03 GMT
USER 1001
# Wed, 14 Jul 2021 00:26:04 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 00:26:04 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 00:26:04 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:3287e09e36098b10234ccc1f8db0b48e2027ca7caa353a362d65f9b017ab802e`  
		Last Modified: Tue, 13 Jul 2021 22:55:34 GMT  
		Size: 25.4 MB (25365649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6fe4e2b151f33398a6ef48bbb5d9ace538aa5ecf3fab9182babc3a85b9166b`  
		Last Modified: Tue, 13 Jul 2021 23:16:59 GMT  
		Size: 2.7 MB (2676828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b436dddc9b46f3b9e70224bb7eab52e58419d071c07f16f9ce63c77c81e5e24`  
		Last Modified: Tue, 13 Jul 2021 23:17:08 GMT  
		Size: 126.7 MB (126676530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfeb84cc8b0669c7b9e77df6ef93a9af10143ddecdf7cbab90eb2541ea6dae9f`  
		Last Modified: Wed, 14 Jul 2021 00:59:46 GMT  
		Size: 14.1 MB (14082055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc5188d927b29c1e6ec8a352cb13ab32af8ed150ee5c1abb928fef7ec7d2a15`  
		Last Modified: Wed, 14 Jul 2021 00:59:43 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c09c4ee0bf95890e60c06b29e00402b7ca7fbbe3f9b31bbf00426c75b84aaa`  
		Last Modified: Wed, 14 Jul 2021 00:59:43 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7b8bba08a70c5ffca0778748f3e75b2ee3c4d131b3bf31b9e7dfd735c9ec4b`  
		Last Modified: Wed, 14 Jul 2021 00:59:43 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe12bbaa95b8b804b7e6752881f522078004b8355c33d3363e49e5d4c438c2cd`  
		Last Modified: Wed, 14 Jul 2021 00:59:43 GMT  
		Size: 10.7 KB (10664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7dea27e762888900b197a8656b67c7943b619a99797e6b2fcdee52af376627`  
		Last Modified: Wed, 14 Jul 2021 00:59:44 GMT  
		Size: 5.9 MB (5941251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:kernel-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:111787cfced37823534628c27c610369644c673a44a89b6ca609e4cd815c7c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:kernel-java11-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:986dd4e771035ddaa951cf408e8fa0e5ccc5b74e55074464ec3547e9b14f817a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.8 MB (109785326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24cab24d5750e08af9f84ba2908decd6369917ebfca8eb7277d836f12c968e22`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:29:50 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 14 Jul 2021 00:30:19 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:33:59 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Wed, 14 Jul 2021 00:35:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 14 Jul 2021 00:35:04 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 00:35:04 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 14 Jul 2021 00:35:41 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 14 Jul 2021 03:57:41 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 03:57:41 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 03:57:41 GMT
ARG EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448
# Wed, 14 Jul 2021 03:57:41 GMT
ARG NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365
# Wed, 14 Jul 2021 03:57:41 GMT
ARG NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc
# Wed, 14 Jul 2021 03:57:42 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.7 org.opencontainers.image.revision=cl210720210629-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 03:57:42 GMT
ENV LIBERTY_VERSION=21.0.0_07
# Wed, 14 Jul 2021 03:57:42 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 03:57:42 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 03:57:52 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 03:57:52 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 03:57:52 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.7 BuildLabel=cl210720210629-1900
# Wed, 14 Jul 2021 03:57:52 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 03:57:54 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 03:57:54 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 03:57:55 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 03:57:56 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 03:58:03 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 03:58:04 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 14 Jul 2021 03:58:04 GMT
USER 1001
# Wed, 14 Jul 2021 03:58:04 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 03:58:04 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 03:58:04 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1182b8c86e6bb404b0d40d2cdcdcaf4347c5aad464143625307b362caff690`  
		Last Modified: Wed, 14 Jul 2021 00:44:02 GMT  
		Size: 16.0 MB (16033076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1461af6857aed41d09a8ce6e2447ad52c9cdf1e6fe2f19ddaa2ab35d21aa1b`  
		Last Modified: Wed, 14 Jul 2021 00:50:41 GMT  
		Size: 44.4 MB (44382137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b538d86edfd8bb98ca5958e79321f730b01a2adc10244bd8ff7abf2aea9b8d8`  
		Last Modified: Wed, 14 Jul 2021 00:50:36 GMT  
		Size: 4.1 MB (4134048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a532adad204607676dccc5605c883856d719bc1eccc9197565f94f999ca6bf0a`  
		Last Modified: Wed, 14 Jul 2021 04:25:00 GMT  
		Size: 14.2 MB (14180546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bba4c8d4ae12b71c54ff9d090380b6ce40d98fcc357144ec5feaa9563dfa52b`  
		Last Modified: Wed, 14 Jul 2021 04:24:56 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5adbe7df68ffe9638f162021e06ead203a57226067210dd2b2fc8aafcbc8834e`  
		Last Modified: Wed, 14 Jul 2021 04:24:56 GMT  
		Size: 9.7 KB (9671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87cc611f3f91d20de349776f088cccc8cbfee6155ce83bee4dc0b2334e4d998`  
		Last Modified: Wed, 14 Jul 2021 04:24:56 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b31847e7e303752ed571f3af6ab967cb238f28af8751b50f7f8e544d697032b`  
		Last Modified: Wed, 14 Jul 2021 04:24:56 GMT  
		Size: 10.7 KB (10665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d5797f6cdf5b45d44deeed85d1698445e0cba043586c1c26cf5e0fc909a998`  
		Last Modified: Wed, 14 Jul 2021 04:24:56 GMT  
		Size: 2.5 MB (2468349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:5730494867e297dccd2f78f9acfbfd7c413e7d1c71da4080e1d9a6d87a59ae91
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.5 MB (115549549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1130bdc576a6414c5449d479c4ae27633bcc940b1d9a1a9f1f5862936787757b`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 17 Jun 2021 23:25:15 GMT
ADD file:8bcc5606b1ba5ed52b8c7ede7afc0f1a2303865b9f9c1a268f8893b2772d227b in / 
# Thu, 17 Jun 2021 23:25:21 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 01:29:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 18 Jun 2021 01:31:53 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 01:41:26 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Fri, 18 Jun 2021 01:43:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 18 Jun 2021 01:43:45 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Jun 2021 01:43:55 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 18 Jun 2021 01:44:39 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 09 Jul 2021 12:06:18 GMT
ARG VERBOSE=false
# Fri, 09 Jul 2021 12:06:22 GMT
ARG OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:06:28 GMT
ARG EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448
# Fri, 09 Jul 2021 12:06:37 GMT
ARG NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365
# Fri, 09 Jul 2021 12:06:42 GMT
ARG NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc
# Fri, 09 Jul 2021 12:06:49 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.7 org.opencontainers.image.revision=cl210720210629-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 09 Jul 2021 12:06:56 GMT
ENV LIBERTY_VERSION=21.0.0_07
# Fri, 09 Jul 2021 12:07:00 GMT
ARG LIBERTY_URL
# Fri, 09 Jul 2021 12:07:10 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 09 Jul 2021 12:07:56 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Jul 2021 12:08:05 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Jul 2021 12:08:11 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.7 BuildLabel=cl210720210629-1900
# Fri, 09 Jul 2021 12:08:20 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:08:35 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 09 Jul 2021 12:08:37 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Fri, 09 Jul 2021 12:08:40 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 09 Jul 2021 12:08:57 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 09 Jul 2021 12:09:15 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 09 Jul 2021 12:09:20 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 09 Jul 2021 12:09:25 GMT
USER 1001
# Fri, 09 Jul 2021 12:09:30 GMT
EXPOSE 9080 9443
# Fri, 09 Jul 2021 12:09:33 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 09 Jul 2021 12:09:40 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:830138a32e2b9cb850f077b06d89ea5d26428556430bf886f193115b2527779a`  
		Last Modified: Thu, 17 Jun 2021 23:28:41 GMT  
		Size: 33.3 MB (33278245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b268950217e490e209e0491ae6fbd3af12b4642aefad9c0039daf7b3ea0371`  
		Last Modified: Fri, 18 Jun 2021 01:52:43 GMT  
		Size: 17.2 MB (17208433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74aa12681d5d14a96459a14094fd9b08f1379e61fa1e8979b311b55b0561dead`  
		Last Modified: Fri, 18 Jun 2021 01:57:43 GMT  
		Size: 45.1 MB (45104807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee28cff75d70e071001e265878f54c811f52ab2cf95d0cc9daa0085c8e1465d`  
		Last Modified: Fri, 18 Jun 2021 01:57:35 GMT  
		Size: 3.3 MB (3284426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d645b89a4dd25a5d864e0eee16fad18b47003f9afbc03fcbb0d0dd722dc67fc8`  
		Last Modified: Fri, 09 Jul 2021 12:57:02 GMT  
		Size: 14.2 MB (14181551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4da63aa53ce2f86286610b335d47c205209123f3b10468f1fbd732174572770`  
		Last Modified: Fri, 09 Jul 2021 12:56:57 GMT  
		Size: 692.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85cdabb46ca79b2b6ab7a933df344ee131c49e7f28758e95f0563be56d88830`  
		Last Modified: Fri, 09 Jul 2021 12:56:57 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee96f4cf06004c656da5e448f035060f82ec53f290430a9869e4387fce1d59a`  
		Last Modified: Fri, 09 Jul 2021 12:56:57 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c088ac6df31e5b351ce2912eadc32bd7d67f7dc02c903d844f4527504ecfba`  
		Last Modified: Fri, 09 Jul 2021 12:56:58 GMT  
		Size: 10.7 KB (10662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3be9bc98dfc99235b8a23c99b39f927cca9fab5b980ed63f0cc3af7db1ff88`  
		Last Modified: Fri, 09 Jul 2021 12:56:58 GMT  
		Size: 2.5 MB (2470788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:cc097653826372eefa2b06f16af009a4db47ad681936fcdebfe34d17cde65101
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107250743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f375777082aad70eba3068caf709bab79c6e79a61ce0b60f98815bb69df9f7c7`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:34 GMT
ADD file:ae5354f89d91eedd0614e3e97ee59fd6e23254923062c288d775e19b137dfd1c in / 
# Tue, 13 Jul 2021 22:53:36 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:18:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 13 Jul 2021 23:18:55 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:23:22 GMT
ENV JAVA_VERSION=jdk-11.0.11+9_openj9-0.26.0
# Tue, 13 Jul 2021 23:24:35 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='f11ae15da7f2809caeeca70a7cf3b9e7f943848869f498f1b73efc10ef7170f0';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        s390x)          ESUM='2d746296f743bdca55e3c391ddd5529c819e3b5193782085441c0078e1471406';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        amd64|x86_64)          ESUM='152bf992d965ed018e9e1c3c2eb2c1771f92e0b6485b9a1f2c6d84d282117715';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.11%2B9_openj9-0.26.0/OpenJDK11U-jre_x64_linux_openj9_11.0.11_9_openj9-0.26.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 13 Jul 2021 23:24:37 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jul 2021 23:24:37 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 13 Jul 2021 23:25:12 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 14 Jul 2021 00:26:14 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 00:26:15 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:26:15 GMT
ARG EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448
# Wed, 14 Jul 2021 00:26:16 GMT
ARG NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365
# Wed, 14 Jul 2021 00:26:16 GMT
ARG NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc
# Wed, 14 Jul 2021 00:26:16 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.7 org.opencontainers.image.revision=cl210720210629-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 00:26:17 GMT
ENV LIBERTY_VERSION=21.0.0_07
# Wed, 14 Jul 2021 00:26:17 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 00:26:18 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 00:26:29 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:26:30 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 00:26:31 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.7 BuildLabel=cl210720210629-1900
# Wed, 14 Jul 2021 00:26:31 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:26:32 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 00:26:33 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 00:26:33 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 00:26:35 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 00:26:44 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 00:26:45 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Wed, 14 Jul 2021 00:26:46 GMT
USER 1001
# Wed, 14 Jul 2021 00:26:46 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 00:26:47 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 00:26:47 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:761fa758059faa0c80b0b90fcbcc192fc7f573da055460d5b3f019e0faceeb7a`  
		Last Modified: Tue, 13 Jul 2021 22:55:47 GMT  
		Size: 27.1 MB (27149318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0237838e148d45cea54b0d86c053131b4152f4928836cbb3a0c83ba79b538728`  
		Last Modified: Tue, 13 Jul 2021 23:32:23 GMT  
		Size: 15.7 MB (15741695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454768ac3fd4bd9b5536afd4e03c6c369d7eae1ee6b240b461dace5364b911f5`  
		Last Modified: Tue, 13 Jul 2021 23:36:09 GMT  
		Size: 43.8 MB (43840969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add6cc1d828e7c42608c4398d9d18baceea2e5104c4ff50d96eba8015aa4a896`  
		Last Modified: Tue, 13 Jul 2021 23:36:03 GMT  
		Size: 3.8 MB (3845109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8db25e8b8b8c38fe38441c03961e2239699ec7d60c2535ee7e3f32b5d9408e`  
		Last Modified: Wed, 14 Jul 2021 00:59:54 GMT  
		Size: 14.2 MB (14180686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2f25fb8653dcf183e4697f3c91aac2b7f2b52ce9b29ddad16203148334326c`  
		Last Modified: Wed, 14 Jul 2021 00:59:51 GMT  
		Size: 691.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5899b27fbac50a6a5dc63dea77388554c0a30d19d49c0fede69dc55b139aaf9d`  
		Last Modified: Wed, 14 Jul 2021 00:59:51 GMT  
		Size: 9.7 KB (9668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e909c0ea2090f66e195b6a98342c9481ac3c8ca4424dee2a56e9510339fc74d2`  
		Last Modified: Wed, 14 Jul 2021 00:59:51 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0725387dcb18203fe63c473bed29ea62c4967f1aa7cd4875bf595e119b67ce98`  
		Last Modified: Wed, 14 Jul 2021 00:59:51 GMT  
		Size: 10.7 KB (10657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0dca61c9477b822a385de7b1018700d87fa9b82c75df3ce7f8ff1d897b5ae27`  
		Last Modified: Wed, 14 Jul 2021 00:59:53 GMT  
		Size: 2.5 MB (2471680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:latest`

```console
$ docker pull websphere-liberty@sha256:27080236fe8c5aa85459d37ec18b450a792074c7c500649aacdeb1ea5697c749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:latest` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:593621830dcf7ed862f01c7b59dbf0c52ac38031f5d4a9e4238c21978417c3ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.8 MB (402767961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32dfa93cd1b2e8518ca9ca11addf6364d0e93655b8fa5c76b8caca2bb92ac7a2`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:19:05 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:19:13 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:19:14 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:19:52 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:19:52 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 14 Jul 2021 03:57:10 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 03:57:10 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 03:57:10 GMT
ARG EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448
# Wed, 14 Jul 2021 03:57:11 GMT
ARG NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365
# Wed, 14 Jul 2021 03:57:11 GMT
ARG NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc
# Wed, 14 Jul 2021 03:57:11 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.7 org.opencontainers.image.revision=cl210720210629-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 03:57:11 GMT
ENV LIBERTY_VERSION=21.0.0_07
# Wed, 14 Jul 2021 03:57:11 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 03:57:12 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 03:57:23 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 03:57:23 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 03:57:23 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.7 BuildLabel=cl210720210629-1900
# Wed, 14 Jul 2021 03:57:23 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 03:57:25 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 03:57:25 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 03:57:26 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 03:57:27 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 03:57:37 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 03:57:37 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 14 Jul 2021 03:57:37 GMT
USER 1001
# Wed, 14 Jul 2021 03:57:37 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 03:57:37 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 03:57:38 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 14 Jul 2021 03:58:11 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 03:58:11 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 14 Jul 2021 04:01:40 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Wed, 14 Jul 2021 04:01:41 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 14 Jul 2021 04:02:17 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22821a14390caaab5b1f7ca9feb8e54ce64d3d81ca1fa64c6f1eee32ae92da5b`  
		Last Modified: Tue, 13 Jul 2021 23:23:03 GMT  
		Size: 3.0 MB (2959004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4403b30ef5ef8f7b37c65fc3d0a0e0d7e0fca7451dd9b42a43bee1de1f389c09`  
		Last Modified: Tue, 13 Jul 2021 23:23:13 GMT  
		Size: 129.5 MB (129536228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2229a5b48fafe35e4b36d1919ccb99f32d1692b2bec7c9fea77733becb84530c`  
		Last Modified: Wed, 14 Jul 2021 04:24:48 GMT  
		Size: 14.1 MB (14082341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0508db572632c638c6182a39308e5731bfcbd4b598bfc908f0a6c4db23ac0db`  
		Last Modified: Wed, 14 Jul 2021 04:24:43 GMT  
		Size: 692.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5845fe90cc54b2ed48af7b145887feaa37656b8c9d799f40dabf84831e141087`  
		Last Modified: Wed, 14 Jul 2021 04:24:43 GMT  
		Size: 9.7 KB (9673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ea30f4f8482cb87d0f69111edc0a66bc10b6f55dc9431070743dde095a76c7`  
		Last Modified: Wed, 14 Jul 2021 04:24:43 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32852fe819a654da3298d6bb5d00119b56e444c4ff75a5fe4f961145af4cde0`  
		Last Modified: Wed, 14 Jul 2021 04:24:43 GMT  
		Size: 10.7 KB (10659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe8a18351bbc592654b68f132ba3b2d4f542c9013876ef7df5be2e3b67f935e`  
		Last Modified: Wed, 14 Jul 2021 04:24:45 GMT  
		Size: 5.7 MB (5688752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0302e7744226a971fe896e471720ff2db67b7146cdec0050817f45d6b09a04`  
		Last Modified: Wed, 14 Jul 2021 04:25:21 GMT  
		Size: 207.9 MB (207908003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e46e41ead606c0ff89f626961bf1e848fd9710f66ba1036b6f33f388675358`  
		Last Modified: Wed, 14 Jul 2021 04:25:09 GMT  
		Size: 944.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1bdc8179339ab3fcfbe904d27833d22d74c5ea380c667dcdf9e8ba63b9e8300`  
		Last Modified: Wed, 14 Jul 2021 04:25:12 GMT  
		Size: 15.9 MB (15865245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:latest` - linux; 386

```console
$ docker pull websphere-liberty@sha256:c847143995aec30ca5d4526544d7c41ca7a42a8baf8195848864d0128e96ecf3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.2 MB (349209019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d2c9374be56a63d6e35820fec8676f2d4ed2b9bdaf09a49c8545b039479bb7`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 20 Mar 2020 18:38:55 GMT
ADD file:d859d389e38b7ac70fd56f97e38d52a77b58e72b96237a4302d1984cdd912a55 in / 
# Fri, 20 Mar 2020 18:38:56 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 20 Mar 2020 18:38:57 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 20 Mar 2020 18:38:58 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 20 Mar 2020 18:38:58 GMT
CMD ["/bin/bash"]
# Fri, 20 Mar 2020 19:06:34 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 20 Mar 2020 19:06:41 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:06:42 GMT
ENV JAVA_VERSION=1.8.0_sr6fp6
# Fri, 20 Mar 2020 19:07:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='87f9d45b7e1fa65ec018479f3ca7da69a03b52b0da10b8d1555142eec8ab0093';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='b5f825047c9bb5d360fb83694f12e17b1a5a15abf94ac82cd0a3aea32c9a361c';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='f3c04cd07ef269c24373840eae6f59c7db7a16d2e206d393ba93efa6dbb8d74f';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2bbefda96f7d1a5f1694893961e92ccc59dfa50375ae5450675d7a4213d5812e';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='d5b0508d53d1c7382c06f5bc1daf3d57c19c70d851e86e6b1162bcd93f616f7e';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 20 Mar 2020 19:07:26 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 20 Mar 2020 19:31:53 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.3 org.opencontainers.image.revision=cl200320200305-1433
# Fri, 20 Mar 2020 19:31:53 GMT
ENV LIBERTY_VERSION=20.0.0_03
# Fri, 20 Mar 2020 19:31:53 GMT
ARG LIBERTY_URL
# Fri, 20 Mar 2020 19:31:53 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 20 Mar 2020 19:32:02 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 20 Mar 2020 19:32:03 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2020 19:32:03 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.3 BuildLabel=cl200320200305-1433
# Fri, 20 Mar 2020 19:32:03 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output
# Fri, 20 Mar 2020 19:32:04 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 20 Mar 2020 19:32:04 GMT
COPY dir:0d0cedab2fbb7208b9d81afa78e9f15b12b71232224a2fe9753c00b7b72bd72e in /opt/ibm/helpers/ 
# Fri, 20 Mar 2020 19:32:05 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 20 Mar 2020 19:32:05 GMT
COPY dir:9277507d983008afcf8df6e0bfe2735bd4e92717515dbb3a7e268c830f213489 in /licenses/ 
# Fri, 20 Mar 2020 19:32:06 GMT
# ARGS: DOWNLOAD_OPTIONS=
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 20 Mar 2020 19:32:06 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Fri, 20 Mar 2020 19:32:06 GMT
USER 1001
# Fri, 20 Mar 2020 19:32:06 GMT
EXPOSE 9080 9443
# Fri, 20 Mar 2020 19:32:07 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 20 Mar 2020 19:32:07 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 20 Mar 2020 19:32:10 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 20 Mar 2020 19:35:01 GMT
# ARGS: REPOSITORIES_PROPERTIES=
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Fri, 20 Mar 2020 19:35:01 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
```

-	Layers:
	-	`sha256:765ce743592771b94ad8ff27e281e66c13f6039962c7dde4dbe47123081e015b`  
		Last Modified: Mon, 16 Mar 2020 15:38:41 GMT  
		Size: 27.1 MB (27122453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59dc9c4739090a3d2f7265f1f8184b1cbd8ae133b863f8aa93ec5cf1761ee7a5`  
		Last Modified: Fri, 20 Mar 2020 18:39:35 GMT  
		Size: 34.6 KB (34625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a5b698281c077f48fc598e698f0619e4d00a2fedc1832fc95e9cf281408f63`  
		Last Modified: Fri, 20 Mar 2020 18:39:34 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaebe599891b1e1befc10d752a117cc5615ec2dd3913d399fd66e26e0cace3e5`  
		Last Modified: Fri, 20 Mar 2020 18:39:34 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f829150bc8a53a37ac17eb34838fa33c990881a4031bc650a9dae26b3f7880e`  
		Last Modified: Fri, 20 Mar 2020 19:09:23 GMT  
		Size: 3.0 MB (2992132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17b9ccc4baf3a1ffa517a03c7c3d01900136b128b36a83558c67c42e6c1cbaa`  
		Last Modified: Fri, 20 Mar 2020 19:09:35 GMT  
		Size: 118.8 MB (118756706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5011972f1876d464fb62206211a5b5e162ba2603bf20fc4cd0f2b4ffd311cd9`  
		Last Modified: Fri, 20 Mar 2020 19:39:16 GMT  
		Size: 13.6 MB (13600436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5395b713d5baa0917182ca82077b6fa2a0c51789907f96cbb12455586d9fa9b`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 672.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389324a3d9489b2fbcd5946f9d24285c0171c3218470e4a5e2d45c731cefc522`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 3.5 KB (3515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38ea596499e1f23ce426826250984869e92da50aec5845a6233a76d7764bfd1`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea3197b55235384f836e31a605c460f6cb7196f68dc29c65640738d8aa50188`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 57.4 KB (57426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683f76bf565cdb9e59c325f24357eb6b164555ed8629a4b8383448239608966d`  
		Last Modified: Fri, 20 Mar 2020 19:39:13 GMT  
		Size: 4.4 KB (4358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cd2560c76831311d13d197b4784e0826f6ffae62e3b9a22d2fa5675b9b71a2`  
		Last Modified: Fri, 20 Mar 2020 19:39:42 GMT  
		Size: 186.6 MB (186634496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9891aa2b3e904f8f514677372187983ac12c98c209c433ab5bf0862e09d6f4ef`  
		Last Modified: Fri, 20 Mar 2020 19:39:20 GMT  
		Size: 943.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:latest` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:afb93aa6c7922a3f90dd7096fe10c5d03eaa555892eaabe424d869169285f8e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.4 MB (403364706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c6deacd67107f6a602891b5d74b510d28a8cb9931c19909ac9c1fd01abbe1a`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 17 Jun 2021 23:24:58 GMT
ADD file:33bc9edd94d5731da919e83ed38bd4aa7daffcb5f629d93bbde112a795c79d48 in / 
# Thu, 17 Jun 2021 23:25:03 GMT
CMD ["bash"]
# Fri, 18 Jun 2021 02:01:35 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 18 Jun 2021 02:02:36 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Jun 2021 02:02:42 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Fri, 18 Jun 2021 02:03:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 18 Jun 2021 02:04:05 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 09 Jul 2021 12:02:21 GMT
ARG VERBOSE=false
# Fri, 09 Jul 2021 12:02:27 GMT
ARG OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:02:34 GMT
ARG EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448
# Fri, 09 Jul 2021 12:02:38 GMT
ARG NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365
# Fri, 09 Jul 2021 12:02:44 GMT
ARG NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc
# Fri, 09 Jul 2021 12:02:51 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.7 org.opencontainers.image.revision=cl210720210629-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 09 Jul 2021 12:03:01 GMT
ENV LIBERTY_VERSION=21.0.0_07
# Fri, 09 Jul 2021 12:03:07 GMT
ARG LIBERTY_URL
# Fri, 09 Jul 2021 12:03:15 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 09 Jul 2021 12:04:20 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Jul 2021 12:04:26 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Jul 2021 12:04:33 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.7 BuildLabel=cl210720210629-1900
# Fri, 09 Jul 2021 12:04:40 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 09 Jul 2021 12:04:53 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 09 Jul 2021 12:04:55 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Fri, 09 Jul 2021 12:04:56 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 09 Jul 2021 12:05:06 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 09 Jul 2021 12:05:38 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 09 Jul 2021 12:05:41 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 09 Jul 2021 12:05:45 GMT
USER 1001
# Fri, 09 Jul 2021 12:05:50 GMT
EXPOSE 9080 9443
# Fri, 09 Jul 2021 12:05:56 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 09 Jul 2021 12:06:02 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 09 Jul 2021 12:09:58 GMT
ARG VERBOSE=false
# Fri, 09 Jul 2021 12:10:00 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 09 Jul 2021 12:14:03 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Fri, 09 Jul 2021 12:14:14 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 09 Jul 2021 12:15:29 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:4e37c2419ee7d7e826be5c6ee69243351aaf456d6527714660cf7e7015491051`  
		Last Modified: Thu, 17 Jun 2021 23:28:22 GMT  
		Size: 30.4 MB (30425356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8d177e4917900437a3445272639bed389b718cc65a87346ba94f6d99327f34`  
		Last Modified: Fri, 18 Jun 2021 02:07:44 GMT  
		Size: 3.1 MB (3082963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09af03e0818b00fa01f51019b91f996a958b5ffb6b7dcd23e88d4d0df759f391`  
		Last Modified: Fri, 18 Jun 2021 02:07:59 GMT  
		Size: 129.1 MB (129059791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e575d1b794a99b9e4326e5406abd771cab007d8e4496378d443e133aecd6fc`  
		Last Modified: Fri, 09 Jul 2021 12:56:48 GMT  
		Size: 14.1 MB (14082768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446edb557b83d18920bc3d64ad18bbc793493f18eac5610ae1ad819a37c1b5c8`  
		Last Modified: Fri, 09 Jul 2021 12:56:42 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92aca0eb7db57552a319340ea766bee3e176bb7d52bf238c98bfd7bf1edc62e8`  
		Last Modified: Fri, 09 Jul 2021 12:56:41 GMT  
		Size: 9.7 KB (9676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c68662de813b880c2fe01caa04a35528660efb50af580891a93b24b63ce4273`  
		Last Modified: Fri, 09 Jul 2021 12:56:41 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:436ecaaacdb2e6ae26659e31d3c0b911a07a8cfe2e46922e0fe3377f753d6879`  
		Last Modified: Fri, 09 Jul 2021 12:56:42 GMT  
		Size: 10.7 KB (10676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb47456c330b967df85a4df66778e4b5762a52080a7ff7a89c042822a5d0841`  
		Last Modified: Fri, 09 Jul 2021 12:56:43 GMT  
		Size: 5.4 MB (5354019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d889510935916732b2718d9a7f5adffc222f87f6f0ad7c7036c320afe43a1d8e`  
		Last Modified: Fri, 09 Jul 2021 12:57:31 GMT  
		Size: 207.9 MB (207908499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a254bd0d60b4e9fef14d2e8f2ca322cf2da3a90df1cfa3930b64c3cc95d113`  
		Last Modified: Fri, 09 Jul 2021 12:57:12 GMT  
		Size: 952.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a8372af7fe68d759c42eb1c1105eb84743e9e40ba7caf5490c68817776fea4`  
		Last Modified: Fri, 09 Jul 2021 12:57:15 GMT  
		Size: 13.4 MB (13429029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:latest` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:feccab75dd49b9eacc3dec41d6c9fc662ce921e51dde3fa8868c6968d2b2a570
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.2 MB (398216420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c531ce10ac925f59e00e218ed78df32aab4514ad3a8758dae3b032ec637546b0`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:22 GMT
ADD file:9e621b1dfa735f1a89553f154f2a2a6f669ff610236d92d6ebf37d1f378d8ec0 in / 
# Tue, 13 Jul 2021 22:53:24 GMT
CMD ["bash"]
# Tue, 13 Jul 2021 23:12:13 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 13 Jul 2021 23:12:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:12:20 GMT
ENV JAVA_VERSION=1.8.0_sr6fp31
# Tue, 13 Jul 2021 23:13:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ed09900a0219b40ddfa06098118a701b8633dcf12588e13ff8b7d810ef2769dc';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='95bf8be233306b046150b949d2a8b9ce604eb6f4a090aaa7bf54152181fcdc06';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='b6a57eff545b75f6fe164c0e96eab56d1a889ae7574e205230f84175b50f6c03';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='2b2b73eef781996e570670a2dec541778647a2afb37b516c9a750e7857fc90aa';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='70da4d42a8181e7a13ca63320acf856315b993f35222e34fa50032a270d472d4';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 13 Jul 2021 23:13:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 14 Jul 2021 00:25:32 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 00:25:32 GMT
ARG OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:25:32 GMT
ARG EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448
# Wed, 14 Jul 2021 00:25:32 GMT
ARG NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365
# Wed, 14 Jul 2021 00:25:33 GMT
ARG NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc
# Wed, 14 Jul 2021 00:25:33 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.7 org.opencontainers.image.revision=cl210720210629-1900 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Wed, 14 Jul 2021 00:25:34 GMT
ENV LIBERTY_VERSION=21.0.0_07
# Wed, 14 Jul 2021 00:25:34 GMT
ARG LIBERTY_URL
# Wed, 14 Jul 2021 00:25:34 GMT
ARG DOWNLOAD_OPTIONS=
# Wed, 14 Jul 2021 00:25:46 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:25:47 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jul 2021 00:25:47 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.7 BuildLabel=cl210720210629-1900
# Wed, 14 Jul 2021 00:25:47 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Wed, 14 Jul 2021 00:25:49 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Wed, 14 Jul 2021 00:25:50 GMT
COPY dir:489212918c9117d43d99cf93a14feddea56ce0482c252c77c33827f9d0160cb8 in /opt/ibm/helpers/ 
# Wed, 14 Jul 2021 00:25:50 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Wed, 14 Jul 2021 00:25:51 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Wed, 14 Jul 2021 00:26:01 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=425d8d4f51c093246f74f5e8b7a320258cd0651a3b6c3667c643b0c88cb3d448 NON_IBM_SHA=532029e6b4f490ffdf97773d57477e01921b1d10d50b5add77c5d2259dd9e365 NOTICES_SHA=569a42319a082ef6a4350df05be88a344c8d2a38345f8d8dd39ae9ff433f1fbc VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Wed, 14 Jul 2021 00:26:02 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,readonly,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Wed, 14 Jul 2021 00:26:03 GMT
USER 1001
# Wed, 14 Jul 2021 00:26:04 GMT
EXPOSE 9080 9443
# Wed, 14 Jul 2021 00:26:04 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Wed, 14 Jul 2021 00:26:04 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Wed, 14 Jul 2021 00:26:59 GMT
ARG VERBOSE=false
# Wed, 14 Jul 2021 00:27:00 GMT
ARG REPOSITORIES_PROPERTIES=
# Wed, 14 Jul 2021 00:30:33 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && find /opt/ibm/wlp ! -perm -g=rw -print0 | xargs -r -0 chmod g+rw
# Wed, 14 Jul 2021 00:30:39 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Wed, 14 Jul 2021 00:31:15 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && find /opt/ibm/wlp/output ! -path "*.classCache*" ! -perm -g=rwx -print0 | xargs -0 -r chmod g+rwx
```

-	Layers:
	-	`sha256:3287e09e36098b10234ccc1f8db0b48e2027ca7caa353a362d65f9b017ab802e`  
		Last Modified: Tue, 13 Jul 2021 22:55:34 GMT  
		Size: 25.4 MB (25365649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6fe4e2b151f33398a6ef48bbb5d9ace538aa5ecf3fab9182babc3a85b9166b`  
		Last Modified: Tue, 13 Jul 2021 23:16:59 GMT  
		Size: 2.7 MB (2676828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b436dddc9b46f3b9e70224bb7eab52e58419d071c07f16f9ce63c77c81e5e24`  
		Last Modified: Tue, 13 Jul 2021 23:17:08 GMT  
		Size: 126.7 MB (126676530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfeb84cc8b0669c7b9e77df6ef93a9af10143ddecdf7cbab90eb2541ea6dae9f`  
		Last Modified: Wed, 14 Jul 2021 00:59:46 GMT  
		Size: 14.1 MB (14082055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc5188d927b29c1e6ec8a352cb13ab32af8ed150ee5c1abb928fef7ec7d2a15`  
		Last Modified: Wed, 14 Jul 2021 00:59:43 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c09c4ee0bf95890e60c06b29e00402b7ca7fbbe3f9b31bbf00426c75b84aaa`  
		Last Modified: Wed, 14 Jul 2021 00:59:43 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7b8bba08a70c5ffca0778748f3e75b2ee3c4d131b3bf31b9e7dfd735c9ec4b`  
		Last Modified: Wed, 14 Jul 2021 00:59:43 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe12bbaa95b8b804b7e6752881f522078004b8355c33d3363e49e5d4c438c2cd`  
		Last Modified: Wed, 14 Jul 2021 00:59:43 GMT  
		Size: 10.7 KB (10664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7dea27e762888900b197a8656b67c7943b619a99797e6b2fcdee52af376627`  
		Last Modified: Wed, 14 Jul 2021 00:59:44 GMT  
		Size: 5.9 MB (5941251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7dda827d3b54d7e48c6470c19206b3547c368b168c59c5946383a1217c8e2d0`  
		Last Modified: Wed, 14 Jul 2021 01:00:10 GMT  
		Size: 207.9 MB (207910341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358ded070ceaa1f2c8acb8b7172deb3fa6884c261e423c03b2585a8d2bbb042c`  
		Last Modified: Wed, 14 Jul 2021 00:59:59 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69694bdedf8776b29d158ed194e88e78c47e8365b5360ad768020dd3a3b22f3`  
		Last Modified: Wed, 14 Jul 2021 01:00:01 GMT  
		Size: 15.5 MB (15541515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

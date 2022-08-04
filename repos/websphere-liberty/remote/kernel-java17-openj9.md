## `websphere-liberty:kernel-java17-openj9`

```console
$ docker pull websphere-liberty@sha256:30969b1a40b4b43f6c0ee85e4816fbd44d82c1290cc201184d5ce7083fe7fd99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:kernel-java17-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:12a9df990b58802276bdd4a175d4296ddeeb45011e02efd76d6f7758899c42df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.9 MB (113913580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f1234bd9a63c2dd3a7bd0bddbe2ab6e7020ab96441b87e61dd7e843d96a8462`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 02 Aug 2022 01:30:49 GMT
ADD file:af4cf77e6818016b697a1491101b40c71d06529ced65f36107749f099d6d4bdc in / 
# Tue, 02 Aug 2022 01:30:49 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 19:04:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Aug 2022 19:05:01 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 20:00:47 GMT
ENV JAVA_VERSION=jdk-17.0.3+7_openj9-0.32.0
# Tue, 02 Aug 2022 20:02:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f899948ea0c5dc80a66f801db585939a25a4ae7e1f21a9a8f3bf3749c3baa87f';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.3%2B7_openj9-0.32.0/ibm-semeru-open-jre_aarch64_linux_17.0.3_7_openj9-0.32.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='9c54166490ac55a6bd26249b57eae5df4531635f4871e6642e7979affc894875';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.3%2B7_openj9-0.32.0/ibm-semeru-open-jre_ppc64le_linux_17.0.3_7_openj9-0.32.0.tar.gz';          ;;        amd64|x86_64)          ESUM='dad35fec82047e3a82c6e2dda8b53ee763b55aaedaed13b7b130856f4a3ffd35';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.3%2B7_openj9-0.32.0/ibm-semeru-open-jre_x64_linux_17.0.3_7_openj9-0.32.0.tar.gz';          ;;        s390x)          ESUM='4e2f631ad18c288e419db5c35295829dd7e83f4cd1be95252db06eb622b23090';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.3%2B7_openj9-0.32.0/ibm-semeru-open-jre_s390x_linux_17.0.3_7_openj9-0.32.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 02 Aug 2022 20:02:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 20:02:05 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 02 Aug 2022 20:02:40 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 03 Aug 2022 13:23:34 GMT
ARG VERBOSE=false
# Wed, 03 Aug 2022 13:23:34 GMT
ARG OPENJ9_SCC=true
# Thu, 04 Aug 2022 00:39:53 GMT
ARG EN_SHA=1558244d39947a6f608f757be932356607a9f2be6c4d6ab7def29e54512d70d0
# Thu, 04 Aug 2022 00:39:53 GMT
ARG NON_IBM_SHA=c5edb6e93c6ac1f3ee6b74780a7b265efaaaaed625efccdd6f8597b844469a50
# Thu, 04 Aug 2022 00:39:53 GMT
ARG NOTICES_SHA=8f92b2e9c7dff626fb7f4cc360e29be26e3497bcc626aca216144589bf3f9715
# Thu, 04 Aug 2022 00:39:53 GMT
LABEL org.opencontainers.image.authors=Chris Potter, Christy Jesuraj, Melissa Lee org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.8 org.opencontainers.image.revision=cl220820220719-1056 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 04 Aug 2022 00:39:54 GMT
ENV LIBERTY_VERSION=22.0.0_08
# Thu, 04 Aug 2022 00:39:54 GMT
ARG LIBERTY_URL
# Thu, 04 Aug 2022 00:39:54 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 04 Aug 2022 00:40:08 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1558244d39947a6f608f757be932356607a9f2be6c4d6ab7def29e54512d70d0 NON_IBM_SHA=c5edb6e93c6ac1f3ee6b74780a7b265efaaaaed625efccdd6f8597b844469a50 NOTICES_SHA=8f92b2e9c7dff626fb7f4cc360e29be26e3497bcc626aca216144589bf3f9715 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 00:40:08 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Aug 2022 00:40:08 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.8 BuildLabel=cl220820220719-1056
# Thu, 04 Aug 2022 00:40:08 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 04 Aug 2022 00:40:09 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1558244d39947a6f608f757be932356607a9f2be6c4d6ab7def29e54512d70d0 NON_IBM_SHA=c5edb6e93c6ac1f3ee6b74780a7b265efaaaaed625efccdd6f8597b844469a50 NOTICES_SHA=8f92b2e9c7dff626fb7f4cc360e29be26e3497bcc626aca216144589bf3f9715 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 04 Aug 2022 00:40:09 GMT
COPY dir:8bf844c49178cf63745af9ec643f57d70bd92c28166fabfad188dfc250d88353 in /opt/ibm/helpers/ 
# Thu, 04 Aug 2022 00:40:09 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 04 Aug 2022 00:40:10 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1558244d39947a6f608f757be932356607a9f2be6c4d6ab7def29e54512d70d0 NON_IBM_SHA=c5edb6e93c6ac1f3ee6b74780a7b265efaaaaed625efccdd6f8597b844469a50 NOTICES_SHA=8f92b2e9c7dff626fb7f4cc360e29be26e3497bcc626aca216144589bf3f9715 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 04 Aug 2022 00:40:17 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1558244d39947a6f608f757be932356607a9f2be6c4d6ab7def29e54512d70d0 NON_IBM_SHA=c5edb6e93c6ac1f3ee6b74780a7b265efaaaaed625efccdd6f8597b844469a50 NOTICES_SHA=8f92b2e9c7dff626fb7f4cc360e29be26e3497bcc626aca216144589bf3f9715 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 04 Aug 2022 00:40:17 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 04 Aug 2022 00:40:17 GMT
USER 1001
# Thu, 04 Aug 2022 00:40:18 GMT
EXPOSE 9080 9443
# Thu, 04 Aug 2022 00:40:18 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 04 Aug 2022 00:40:18 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:3b65ec22a9e96affe680712973e88355927506aa3f792ff03330f3a3eb601a98`  
		Last Modified: Tue, 02 Aug 2022 01:31:59 GMT  
		Size: 28.6 MB (28572596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398d776e32fac0ec8c2698a6d7bc5d81c5d35de32a68fb2d7882e0f46b73fd37`  
		Last Modified: Tue, 02 Aug 2022 19:13:20 GMT  
		Size: 16.0 MB (16029939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6279e9931cb0efc3b60659be8fd46c95156f958f00818850fba3ac0ecd0616`  
		Last Modified: Tue, 02 Aug 2022 20:08:11 GMT  
		Size: 47.8 MB (47754438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e834be70bdf636e5c875d9e2badbf281d32ff675b9eb7db8768a2da9dbdf5e`  
		Last Modified: Tue, 02 Aug 2022 20:08:05 GMT  
		Size: 4.7 MB (4744099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b576137a2256116992627bd3da2373004fb013a2b166d5d0f4b4d1323cdcd3e`  
		Last Modified: Thu, 04 Aug 2022 01:07:41 GMT  
		Size: 14.2 MB (14201858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75032a5c637d1df3f3def608ca2cb1c7ef1ab0213d69c922b291ea1e47480ed0`  
		Last Modified: Thu, 04 Aug 2022 01:07:38 GMT  
		Size: 698.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4adc9aa029be97e74fe8569a3afcec3c944ec76ca957b61b468d0cda59fe966a`  
		Last Modified: Thu, 04 Aug 2022 01:07:38 GMT  
		Size: 9.8 KB (9754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01aa7af585d1b13690521dd64fc16a6c45a23f531a7a656d38162ba06f23a6b0`  
		Last Modified: Thu, 04 Aug 2022 01:07:38 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d2d779ef6a0e3cd502ebb1fd3f2eef668841d616c0361068020daab0235a87e`  
		Last Modified: Thu, 04 Aug 2022 01:07:38 GMT  
		Size: 10.7 KB (10730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5eb48aa6e51176a8cbfed996c69ce524bd388bf4463231a6efd69a88c443dff`  
		Last Modified: Thu, 04 Aug 2022 01:07:38 GMT  
		Size: 2.6 MB (2589196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel-java17-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:e07434f05a0ce037deb7160f615fd2c70ac87cd34fe541dfb1376ab0c729e822
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.4 MB (119366206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22291564784ba272c1f2bc0584e564e4bf1b4d7e1a1f88c7d48c94972dc2b219`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 07 Jun 2022 05:46:02 GMT
ADD file:86506a94b834ba2b6f10dc0d1955bee539be1cf565e4ccc2c4bc074e0375f115 in / 
# Tue, 07 Jun 2022 05:46:06 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 07:16:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 07:18:13 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 09:52:39 GMT
ENV JAVA_VERSION=jdk-17.0.3+7_openj9-0.32.0
# Tue, 07 Jun 2022 09:54:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f899948ea0c5dc80a66f801db585939a25a4ae7e1f21a9a8f3bf3749c3baa87f';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.3%2B7_openj9-0.32.0/ibm-semeru-open-jre_aarch64_linux_17.0.3_7_openj9-0.32.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='9c54166490ac55a6bd26249b57eae5df4531635f4871e6642e7979affc894875';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.3%2B7_openj9-0.32.0/ibm-semeru-open-jre_ppc64le_linux_17.0.3_7_openj9-0.32.0.tar.gz';          ;;        amd64|x86_64)          ESUM='dad35fec82047e3a82c6e2dda8b53ee763b55aaedaed13b7b130856f4a3ffd35';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.3%2B7_openj9-0.32.0/ibm-semeru-open-jre_x64_linux_17.0.3_7_openj9-0.32.0.tar.gz';          ;;        s390x)          ESUM='4e2f631ad18c288e419db5c35295829dd7e83f4cd1be95252db06eb622b23090';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.3%2B7_openj9-0.32.0/ibm-semeru-open-jre_s390x_linux_17.0.3_7_openj9-0.32.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 09:54:20 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 09:54:22 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 07 Jun 2022 09:55:03 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Tue, 07 Jun 2022 11:31:51 GMT
ARG VERBOSE=false
# Tue, 07 Jun 2022 11:31:54 GMT
ARG OPENJ9_SCC=true
# Mon, 27 Jun 2022 19:08:20 GMT
ARG EN_SHA=6d76dc1906ca448927abb8238487de96089a1b1591286c7339cba94976261abf
# Mon, 27 Jun 2022 19:08:23 GMT
ARG NON_IBM_SHA=412ee94517773939d86d1ac9aa013c8bdff481de4d8ef58c84c997b4d612fef1
# Mon, 27 Jun 2022 19:08:26 GMT
ARG NOTICES_SHA=ca3ea01852554c9f84c907754677a18b6d9e39707469f7af93808fd1c1d42a09
# Mon, 27 Jun 2022 19:08:29 GMT
LABEL org.opencontainers.image.authors=Chris Potter, Christy Jesuraj, Melissa Lee org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.6 org.opencontainers.image.revision=cl220620220523-1607 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Mon, 27 Jun 2022 19:08:32 GMT
ENV LIBERTY_VERSION=22.0.0_06
# Mon, 27 Jun 2022 19:08:33 GMT
ARG LIBERTY_URL
# Mon, 27 Jun 2022 19:08:37 GMT
ARG DOWNLOAD_OPTIONS=
# Mon, 27 Jun 2022 19:09:23 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=6d76dc1906ca448927abb8238487de96089a1b1591286c7339cba94976261abf NON_IBM_SHA=412ee94517773939d86d1ac9aa013c8bdff481de4d8ef58c84c997b4d612fef1 NOTICES_SHA=ca3ea01852554c9f84c907754677a18b6d9e39707469f7af93808fd1c1d42a09 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Mon, 27 Jun 2022 19:09:29 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 27 Jun 2022 19:09:31 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.6 BuildLabel=cl220620220523-1607
# Mon, 27 Jun 2022 19:09:32 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Mon, 27 Jun 2022 19:09:40 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=6d76dc1906ca448927abb8238487de96089a1b1591286c7339cba94976261abf NON_IBM_SHA=412ee94517773939d86d1ac9aa013c8bdff481de4d8ef58c84c997b4d612fef1 NOTICES_SHA=ca3ea01852554c9f84c907754677a18b6d9e39707469f7af93808fd1c1d42a09 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Mon, 27 Jun 2022 19:09:42 GMT
COPY dir:8bf844c49178cf63745af9ec643f57d70bd92c28166fabfad188dfc250d88353 in /opt/ibm/helpers/ 
# Mon, 27 Jun 2022 19:09:43 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Mon, 27 Jun 2022 19:09:52 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=6d76dc1906ca448927abb8238487de96089a1b1591286c7339cba94976261abf NON_IBM_SHA=412ee94517773939d86d1ac9aa013c8bdff481de4d8ef58c84c997b4d612fef1 NOTICES_SHA=ca3ea01852554c9f84c907754677a18b6d9e39707469f7af93808fd1c1d42a09 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Mon, 27 Jun 2022 19:10:09 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=6d76dc1906ca448927abb8238487de96089a1b1591286c7339cba94976261abf NON_IBM_SHA=412ee94517773939d86d1ac9aa013c8bdff481de4d8ef58c84c997b4d612fef1 NOTICES_SHA=ca3ea01852554c9f84c907754677a18b6d9e39707469f7af93808fd1c1d42a09 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Mon, 27 Jun 2022 19:10:11 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Mon, 27 Jun 2022 19:10:14 GMT
USER 1001
# Mon, 27 Jun 2022 19:10:17 GMT
EXPOSE 9080 9443
# Mon, 27 Jun 2022 19:10:18 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Mon, 27 Jun 2022 19:10:23 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:3f52d061d2d3fdde0d3a099bbeae64080476c9650e9f3ba05de898d5bb5f03e8`  
		Last Modified: Tue, 07 Jun 2022 05:49:10 GMT  
		Size: 33.3 MB (33294345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6c621e52fdf1e59e073b1c51c52e2e5a829be92510ef56949c609a03af2492`  
		Last Modified: Tue, 07 Jun 2022 07:30:19 GMT  
		Size: 17.2 MB (17203633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:643e82d1f37eb2778986afcd7aa289e4f42b3c21d19b6dc2b50320f2836d580e`  
		Last Modified: Tue, 07 Jun 2022 10:03:59 GMT  
		Size: 48.1 MB (48115319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe972a29b91980b448bef8b1d66c53f248a582f57eb8476283dad120863f562`  
		Last Modified: Tue, 07 Jun 2022 10:03:52 GMT  
		Size: 3.7 MB (3691417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c056cb98358395a411cf5384fbbdbec5ccfd5f81859801ac0c85148bbb98a4`  
		Last Modified: Mon, 27 Jun 2022 20:22:00 GMT  
		Size: 14.5 MB (14515851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd06b09fbbdc503b03e823a42d86309633c6d84767fa73330825bc907e14df3`  
		Last Modified: Mon, 27 Jun 2022 20:21:51 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbb19c1ede5ad19ca10791cc60a2f22dd80c54475f408a0e73abdccbca16792`  
		Last Modified: Mon, 27 Jun 2022 20:21:51 GMT  
		Size: 9.8 KB (9753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948cca84307d534dd3b66a3ccd42411c24283967d6c73d87983819647f564e0c`  
		Last Modified: Mon, 27 Jun 2022 20:21:51 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39dcdc56c341ef84605200c2bc492ee7ebd2d7d6c088f9188b4b724f2316504`  
		Last Modified: Mon, 27 Jun 2022 20:21:51 GMT  
		Size: 10.7 KB (10740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdde75f3ce0ceab51ecdf4a88f513912d5744afccff705acaa98d4d96a9399d1`  
		Last Modified: Mon, 27 Jun 2022 20:21:52 GMT  
		Size: 2.5 MB (2524189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel-java17-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:5908ba3aaa373af2bf178346dfca3d2fd49847f08e1416f6ed6efed3a8134653
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.7 MB (110745257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cdcf331028526e4b752481e64edfac02cd9fde10652094a5915b2717a8eac61`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Tue, 02 Aug 2022 01:02:06 GMT
ADD file:409a01624b482522ab1ba2da28ff57bceb3bf89ff2f3cae5c9ea6068f6993355 in / 
# Tue, 02 Aug 2022 01:02:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 12:41:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Aug 2022 12:41:50 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 12:47:17 GMT
ENV JAVA_VERSION=jdk-17.0.3+7_openj9-0.32.0
# Tue, 02 Aug 2022 12:48:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f899948ea0c5dc80a66f801db585939a25a4ae7e1f21a9a8f3bf3749c3baa87f';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.3%2B7_openj9-0.32.0/ibm-semeru-open-jre_aarch64_linux_17.0.3_7_openj9-0.32.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='9c54166490ac55a6bd26249b57eae5df4531635f4871e6642e7979affc894875';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.3%2B7_openj9-0.32.0/ibm-semeru-open-jre_ppc64le_linux_17.0.3_7_openj9-0.32.0.tar.gz';          ;;        amd64|x86_64)          ESUM='dad35fec82047e3a82c6e2dda8b53ee763b55aaedaed13b7b130856f4a3ffd35';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.3%2B7_openj9-0.32.0/ibm-semeru-open-jre_x64_linux_17.0.3_7_openj9-0.32.0.tar.gz';          ;;        s390x)          ESUM='4e2f631ad18c288e419db5c35295829dd7e83f4cd1be95252db06eb622b23090';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.3%2B7_openj9-0.32.0/ibm-semeru-open-jre_s390x_linux_17.0.3_7_openj9-0.32.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 02 Aug 2022 12:48:20 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 12:48:20 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 02 Aug 2022 12:48:53 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 03 Aug 2022 00:31:56 GMT
ARG VERBOSE=false
# Wed, 03 Aug 2022 00:31:56 GMT
ARG OPENJ9_SCC=true
# Thu, 04 Aug 2022 00:57:27 GMT
ARG EN_SHA=1558244d39947a6f608f757be932356607a9f2be6c4d6ab7def29e54512d70d0
# Thu, 04 Aug 2022 00:57:27 GMT
ARG NON_IBM_SHA=c5edb6e93c6ac1f3ee6b74780a7b265efaaaaed625efccdd6f8597b844469a50
# Thu, 04 Aug 2022 00:57:27 GMT
ARG NOTICES_SHA=8f92b2e9c7dff626fb7f4cc360e29be26e3497bcc626aca216144589bf3f9715
# Thu, 04 Aug 2022 00:57:27 GMT
LABEL org.opencontainers.image.authors=Chris Potter, Christy Jesuraj, Melissa Lee org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=22.0.0.8 org.opencontainers.image.revision=cl220820220719-1056 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM Semeru Runtime Open Edition OpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 04 Aug 2022 00:57:27 GMT
ENV LIBERTY_VERSION=22.0.0_08
# Thu, 04 Aug 2022 00:57:27 GMT
ARG LIBERTY_URL
# Thu, 04 Aug 2022 00:57:27 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 04 Aug 2022 00:57:37 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1558244d39947a6f608f757be932356607a9f2be6c4d6ab7def29e54512d70d0 NON_IBM_SHA=c5edb6e93c6ac1f3ee6b74780a7b265efaaaaed625efccdd6f8597b844469a50 NOTICES_SHA=8f92b2e9c7dff626fb7f4cc360e29be26e3497bcc626aca216144589bf3f9715 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir -p /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 04 Aug 2022 00:57:37 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Aug 2022 00:57:37 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=22.0.0.8 BuildLabel=cl220820220719-1056
# Thu, 04 Aug 2022 00:57:37 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 04 Aug 2022 00:57:38 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1558244d39947a6f608f757be932356607a9f2be6c4d6ab7def29e54512d70d0 NON_IBM_SHA=c5edb6e93c6ac1f3ee6b74780a7b265efaaaaed625efccdd6f8597b844469a50 NOTICES_SHA=8f92b2e9c7dff626fb7f4cc360e29be26e3497bcc626aca216144589bf3f9715 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 04 Aug 2022 00:57:38 GMT
COPY dir:8bf844c49178cf63745af9ec643f57d70bd92c28166fabfad188dfc250d88353 in /opt/ibm/helpers/ 
# Thu, 04 Aug 2022 00:57:38 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 04 Aug 2022 00:57:39 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1558244d39947a6f608f757be932356607a9f2be6c4d6ab7def29e54512d70d0 NON_IBM_SHA=c5edb6e93c6ac1f3ee6b74780a7b265efaaaaed625efccdd6f8597b844469a50 NOTICES_SHA=8f92b2e9c7dff626fb7f4cc360e29be26e3497bcc626aca216144589bf3f9715 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 04 Aug 2022 00:57:44 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1558244d39947a6f608f757be932356607a9f2be6c4d6ab7def29e54512d70d0 NON_IBM_SHA=c5edb6e93c6ac1f3ee6b74780a7b265efaaaaed625efccdd6f8597b844469a50 NOTICES_SHA=8f92b2e9c7dff626fb7f4cc360e29be26e3497bcc626aca216144589bf3f9715 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 04 Aug 2022 00:57:44 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 04 Aug 2022 00:57:45 GMT
USER 1001
# Thu, 04 Aug 2022 00:57:45 GMT
EXPOSE 9080 9443
# Thu, 04 Aug 2022 00:57:45 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 04 Aug 2022 00:57:45 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:d522b75fb69271e75617d2e7bbeede1210f48bffdc57121ee39534eea94e2815`  
		Last Modified: Tue, 02 Aug 2022 01:03:38 GMT  
		Size: 27.0 MB (27045363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:204f6f9c0aa5d9c3e1300660817d3dd41177073448243d9ccc18a39c3f14083a`  
		Last Modified: Tue, 02 Aug 2022 12:52:19 GMT  
		Size: 15.7 MB (15730128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8366f0be07eee724257935ccff074ac6069837c38e228be50a0b6f2e058ab16c`  
		Last Modified: Tue, 02 Aug 2022 12:54:24 GMT  
		Size: 46.2 MB (46241889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc471632f4e136d4fa45d0a7216573974cc332f3e9fa969846cb74f259e5e9cc`  
		Last Modified: Tue, 02 Aug 2022 12:54:19 GMT  
		Size: 4.9 MB (4939140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdc9afc8efc1309595eafa5adfd624bc22c5d84667a0c89cf57d1cde692e67c`  
		Last Modified: Thu, 04 Aug 2022 01:23:01 GMT  
		Size: 14.2 MB (14201993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e66b2b6dfc8750fee1bbaba474e4e0f7e2bf789226713771c8b8d1380675897`  
		Last Modified: Thu, 04 Aug 2022 01:22:59 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff18a7d4adfb8b62896d859c6d1b34ff9b5b7959fc5631ac782fd36e852f33b`  
		Last Modified: Thu, 04 Aug 2022 01:22:59 GMT  
		Size: 9.8 KB (9753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac767a48c47b1a0268a2b0e739712d2a74a2f8bb154bdf994a76295e5c0a8d2f`  
		Last Modified: Thu, 04 Aug 2022 01:22:59 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd713308939c792ac53c95605c01d82c9de766ad9c050df0032112407ef7f3d`  
		Last Modified: Thu, 04 Aug 2022 01:22:59 GMT  
		Size: 10.7 KB (10733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7bc158a3121e6b2ef4f86e2f2f575fc45c49ab28500bc0e6e50c8218bb136b`  
		Last Modified: Thu, 04 Aug 2022 01:22:59 GMT  
		Size: 2.6 MB (2565293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

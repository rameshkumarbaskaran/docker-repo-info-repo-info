<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `websphere-liberty`

-	[`websphere-liberty:20.0.0.12-full-java11-openj9`](#websphere-liberty200012-full-java11-openj9)
-	[`websphere-liberty:20.0.0.12-full-java8-ibmjava`](#websphere-liberty200012-full-java8-ibmjava)
-	[`websphere-liberty:20.0.0.12-kernel-java11-openj9`](#websphere-liberty200012-kernel-java11-openj9)
-	[`websphere-liberty:20.0.0.12-kernel-java8-ibmjava`](#websphere-liberty200012-kernel-java8-ibmjava)
-	[`websphere-liberty:21.0.0.3-full-java11-openj9`](#websphere-liberty21003-full-java11-openj9)
-	[`websphere-liberty:21.0.0.3-full-java8-ibmjava`](#websphere-liberty21003-full-java8-ibmjava)
-	[`websphere-liberty:21.0.0.3-kernel-java11-openj9`](#websphere-liberty21003-kernel-java11-openj9)
-	[`websphere-liberty:21.0.0.3-kernel-java8-ibmjava`](#websphere-liberty21003-kernel-java8-ibmjava)
-	[`websphere-liberty:21.0.0.4-full-java11-openj9`](#websphere-liberty21004-full-java11-openj9)
-	[`websphere-liberty:21.0.0.4-full-java8-ibmjava`](#websphere-liberty21004-full-java8-ibmjava)
-	[`websphere-liberty:21.0.0.4-kernel-java11-openj9`](#websphere-liberty21004-kernel-java11-openj9)
-	[`websphere-liberty:21.0.0.4-kernel-java8-ibmjava`](#websphere-liberty21004-kernel-java8-ibmjava)
-	[`websphere-liberty:full`](#websphere-libertyfull)
-	[`websphere-liberty:full-java11-openj9`](#websphere-libertyfull-java11-openj9)
-	[`websphere-liberty:kernel`](#websphere-libertykernel)
-	[`websphere-liberty:kernel-java11-openj9`](#websphere-libertykernel-java11-openj9)
-	[`websphere-liberty:latest`](#websphere-libertylatest)

## `websphere-liberty:20.0.0.12-full-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:0cb2795484dce3f8a515fd535003b8e4f68bf917a46c6c3a9f67ce9adddffbe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:20.0.0.12-full-java11-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:49aa464afb2c2d7e3af705fa95df60d73e4e2a8920eb168b32286e534d155d66
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.3 MB (316279108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85ddf0ea4cc63b052194e75c8fb196a9dcdcef4fca959000a5194793d2a8ca72`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 03 Apr 2021 00:53:06 GMT
ADD file:27277aee655dd263ee698d1f2fe17f0b1dbba740615bcac8642723a6ac0d62be in / 
# Sat, 03 Apr 2021 00:53:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 03 Apr 2021 00:53:08 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Sat, 03 Apr 2021 00:53:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 03 Apr 2021 00:53:09 GMT
CMD ["/bin/bash"]
# Sat, 03 Apr 2021 01:29:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 03 Apr 2021 01:29:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 03 Apr 2021 01:32:52 GMT
ENV JAVA_VERSION=jdk-11.0.10+9_openj9-0.24.0
# Mon, 19 Apr 2021 18:22:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='5d2b2939637f999a1910d5cc0fb3d96756125941e5f8b9e3003635aa863664b5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        s390x)          ESUM='2ff9f50d6ffc345434703c43a1d67ac6d3d054b5d4925b4b73a3ce51b02940e5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7e5f97071f8b86c22c36ddfd7f821c3e8ec531c1128e2e6c931b2e64118a517a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 19 Apr 2021 18:22:34 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Apr 2021 18:22:34 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 19 Apr 2021 18:23:10 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 22 Apr 2021 21:40:48 GMT
ARG VERBOSE=false
# Thu, 22 Apr 2021 21:40:48 GMT
ARG OPENJ9_SCC=true
# Thu, 22 Apr 2021 21:52:45 GMT
ARG EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95
# Thu, 22 Apr 2021 21:52:45 GMT
ARG NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b
# Thu, 22 Apr 2021 21:52:45 GMT
ARG NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e
# Thu, 22 Apr 2021 21:52:46 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.12 org.opencontainers.image.revision=cl201220201111-0736 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 22 Apr 2021 21:52:46 GMT
ENV LIBERTY_VERSION=20.0.0_12
# Thu, 22 Apr 2021 21:52:46 GMT
ARG LIBERTY_URL
# Thu, 22 Apr 2021 21:52:46 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 22 Apr 2021 21:52:54 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Apr 2021 21:52:54 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Apr 2021 21:52:54 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.12 BuildLabel=cl201220201111-0736
# Thu, 22 Apr 2021 21:52:55 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 22 Apr 2021 21:52:56 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Apr 2021 21:52:56 GMT
COPY dir:87fb88e41281cc95d67404db807cebd05ba85ea3f246dace99de7f445dc641b1 in /opt/ibm/helpers/ 
# Thu, 22 Apr 2021 21:52:56 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Apr 2021 21:52:57 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Apr 2021 21:53:05 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Apr 2021 21:53:05 GMT
ENV RANDFILE=/tmp/.rnd
# Thu, 22 Apr 2021 21:53:05 GMT
USER 1001
# Thu, 22 Apr 2021 21:53:05 GMT
EXPOSE 9080 9443
# Thu, 22 Apr 2021 21:53:05 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Apr 2021 21:53:06 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 22 Apr 2021 21:53:13 GMT
ARG VERBOSE=false
# Thu, 22 Apr 2021 21:53:13 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 22 Apr 2021 21:55:54 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Thu, 22 Apr 2021 21:55:55 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 22 Apr 2021 21:56:29 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:a70d879fa5984474288d52009479054b8bb2993de2a1859f43b5480600cecb24`  
		Last Modified: Thu, 01 Apr 2021 15:20:06 GMT  
		Size: 28.6 MB (28569016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4394a92d1f8760cf7d17fee0bcee732c94c5b858dd8d19c7ff02beecf3b4e83`  
		Last Modified: Sat, 03 Apr 2021 00:54:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e6159c56c084c858f5de2416454ac0a49ddda47b764e4379c5d5a147c9bf5f`  
		Last Modified: Sat, 03 Apr 2021 00:54:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04b772c31f76720583412a2507c5c53889985db45169a85f0d3cd7f842e041a`  
		Last Modified: Sat, 03 Apr 2021 01:39:30 GMT  
		Size: 16.0 MB (16032891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf71362343a962febc8c6ce8c4fd12d961c5712407993471f60ac0e5d43415e`  
		Last Modified: Mon, 19 Apr 2021 18:30:17 GMT  
		Size: 42.4 MB (42440313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9163852ff25e45c3b95c7b759a719b91afa29724136e68d1cf7f822c034c4df`  
		Last Modified: Mon, 19 Apr 2021 18:30:04 GMT  
		Size: 4.0 MB (4025359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf4544075da5a2c6e7e1b2994b4e7636ccfe9b195b9bb20633733c96ec9a4f9`  
		Last Modified: Thu, 22 Apr 2021 21:59:06 GMT  
		Size: 14.1 MB (14073296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc613cdafc1c7638c8e6e19a98b47464b53ed0758b32961a8ac7780be065560`  
		Last Modified: Thu, 22 Apr 2021 21:59:01 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1783f70e1fa5a4b6784678ac26ee301431e1fd49ab67ec6d1c5670bf1f3fbb16`  
		Last Modified: Thu, 22 Apr 2021 21:59:01 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774ae461e99f7b8733efbb61a4690422357faa1c019ba98c32119eebd94a8e52`  
		Last Modified: Thu, 22 Apr 2021 21:59:01 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a0fcd773f7170f8b6ecd93b521d77d68777a7041eebbf8ce5d6d7b3fd5318c`  
		Last Modified: Thu, 22 Apr 2021 21:59:01 GMT  
		Size: 10.5 KB (10528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7315afa7e7544b7a663e1baa7146a4cd1bb0d2b26e6bf855b9d7a18fe3dfbf`  
		Last Modified: Thu, 22 Apr 2021 21:59:02 GMT  
		Size: 2.5 MB (2488744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc49043520d0ff26d0907a5bba87aed2572f3f24eb8e540be369d54aef6eb62a`  
		Last Modified: Thu, 22 Apr 2021 21:59:30 GMT  
		Size: 194.6 MB (194615911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cdde7a1ddc9aa91231ca742449789475ca92bb7fb964ca5ac7e6f42157c0ee1`  
		Last Modified: Thu, 22 Apr 2021 21:59:15 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3edd9c6c0a9893eaab32a11827fef2579d405fadf7a13469f099c9d6df369b5`  
		Last Modified: Thu, 22 Apr 2021 21:59:17 GMT  
		Size: 14.0 MB (14010556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:20.0.0.12-full-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:adfe8c0e9a2be8f949612e251eff89b99ea0a8cd30934cc62ad069b701dd8a9b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.9 MB (320885059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faec97d6b085a5f2ff54d72c4c7bd5b8304108e36e4b0f4ee3cac459447ce890`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:16:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 24 Apr 2021 01:19:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:28:36 GMT
ENV JAVA_VERSION=jdk-11.0.10+9_openj9-0.24.0
# Sat, 24 Apr 2021 01:30:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='5d2b2939637f999a1910d5cc0fb3d96756125941e5f8b9e3003635aa863664b5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        s390x)          ESUM='2ff9f50d6ffc345434703c43a1d67ac6d3d054b5d4925b4b73a3ce51b02940e5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7e5f97071f8b86c22c36ddfd7f821c3e8ec531c1128e2e6c931b2e64118a517a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 24 Apr 2021 01:30:48 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 24 Apr 2021 01:30:53 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Sat, 24 Apr 2021 01:31:37 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Sat, 24 Apr 2021 03:09:49 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 03:09:52 GMT
ARG OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:43:37 GMT
ARG EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95
# Sat, 24 Apr 2021 03:43:40 GMT
ARG NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b
# Sat, 24 Apr 2021 03:43:42 GMT
ARG NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e
# Sat, 24 Apr 2021 03:43:48 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.12 org.opencontainers.image.revision=cl201220201111-0736 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Sat, 24 Apr 2021 03:43:50 GMT
ENV LIBERTY_VERSION=20.0.0_12
# Sat, 24 Apr 2021 03:43:57 GMT
ARG LIBERTY_URL
# Sat, 24 Apr 2021 03:44:00 GMT
ARG DOWNLOAD_OPTIONS=
# Sat, 24 Apr 2021 03:44:45 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 03:44:54 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 24 Apr 2021 03:45:02 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.12 BuildLabel=cl201220201111-0736
# Sat, 24 Apr 2021 03:45:09 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:45:24 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Sat, 24 Apr 2021 03:45:26 GMT
COPY dir:87fb88e41281cc95d67404db807cebd05ba85ea3f246dace99de7f445dc641b1 in /opt/ibm/helpers/ 
# Sat, 24 Apr 2021 03:45:28 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Sat, 24 Apr 2021 03:45:43 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Sat, 24 Apr 2021 03:46:10 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Sat, 24 Apr 2021 03:46:12 GMT
ENV RANDFILE=/tmp/.rnd
# Sat, 24 Apr 2021 03:46:15 GMT
USER 1001
# Sat, 24 Apr 2021 03:46:18 GMT
EXPOSE 9080 9443
# Sat, 24 Apr 2021 03:46:22 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Sat, 24 Apr 2021 03:46:27 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Sat, 24 Apr 2021 03:51:58 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 03:52:04 GMT
ARG REPOSITORIES_PROPERTIES=
# Sat, 24 Apr 2021 03:55:25 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Sat, 24 Apr 2021 03:55:32 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Sat, 24 Apr 2021 03:56:35 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da07529aeac8fe5c90c5bb8c4f516c9d6fd248cc1daa5fecd137c809bce39bb6`  
		Last Modified: Sat, 24 Apr 2021 01:40:58 GMT  
		Size: 17.2 MB (17209103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53f9612e78ec5df6fbbbab4098deb40150ceef63be58aec6c2dd4df6af9f634`  
		Last Modified: Sat, 24 Apr 2021 01:46:21 GMT  
		Size: 43.3 MB (43277570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec133c54d62c9541f8b987c7353d67bd5d58ea39050f8cd947bf150d5ce8bb7a`  
		Last Modified: Sat, 24 Apr 2021 01:46:15 GMT  
		Size: 3.3 MB (3289250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc394ddf4e34a090a199321258a21dfecfcf1ab44974ab8b4a36662ef5287ed5`  
		Last Modified: Sat, 24 Apr 2021 04:00:57 GMT  
		Size: 14.1 MB (14074578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b11004119d5d190e5164dc96ce5220189cc627326713ac4bbce2e96f88bfd1c`  
		Last Modified: Sat, 24 Apr 2021 04:00:51 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d7cd2480a852fef8c64bcd9ff7b4c757ef6229c4e21e2b2170a326f36ec550`  
		Last Modified: Sat, 24 Apr 2021 04:00:51 GMT  
		Size: 9.5 KB (9549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2808ea8be40d8b0ffae1ee4c07b5ebbfa183d5df84c84416829b8f45ad31a9b`  
		Last Modified: Sat, 24 Apr 2021 04:00:52 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c158e0bf410648b3c8d9e8d211f242606d8e90a07db1db5e209412c559827a`  
		Last Modified: Sat, 24 Apr 2021 04:00:51 GMT  
		Size: 10.5 KB (10543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66491e8e215274e92107b8d888d7544390984679b322aba9530bbfba4b8366e`  
		Last Modified: Sat, 24 Apr 2021 04:00:52 GMT  
		Size: 2.4 MB (2429469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c15d0312f71d0f0c908d43f666e0d862a2895aed4fef1b1e20249090f3de53a`  
		Last Modified: Sat, 24 Apr 2021 04:02:03 GMT  
		Size: 194.6 MB (194615967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00af4d9ade8de1a3a20f35b7fb1e1f67867bb684fec937609466637d4f8c90c8`  
		Last Modified: Sat, 24 Apr 2021 04:01:40 GMT  
		Size: 947.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a738c839fed142f7c74ca904d2f7a244785e431697de95c4f0cdf72728ad620`  
		Last Modified: Sat, 24 Apr 2021 04:01:44 GMT  
		Size: 12.7 MB (12710692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:20.0.0.12-full-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:f823274b222c18aa9bc7e19f53b27251773c4f6d57c76558c63991f39b71ce69
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.4 MB (313435528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30485c3ca716f34affb573b50fc116333177044889fe27adc418d63879b3ece9`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 21:45:20 GMT
ADD file:282d950116f923276efabd13c7dc17b942821edb14ffac4b89b9a50bcdf99e17 in / 
# Fri, 23 Apr 2021 21:45:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 21:45:27 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 21:45:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 21:45:29 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 22:03:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Apr 2021 22:04:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:10:11 GMT
ENV JAVA_VERSION=jdk-11.0.10+9_openj9-0.24.0
# Fri, 23 Apr 2021 22:11:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='5d2b2939637f999a1910d5cc0fb3d96756125941e5f8b9e3003635aa863664b5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        s390x)          ESUM='2ff9f50d6ffc345434703c43a1d67ac6d3d054b5d4925b4b73a3ce51b02940e5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7e5f97071f8b86c22c36ddfd7f821c3e8ec531c1128e2e6c931b2e64118a517a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 23 Apr 2021 22:11:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Apr 2021 22:11:44 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 23 Apr 2021 22:12:20 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 23 Apr 2021 23:17:55 GMT
ARG VERBOSE=false
# Fri, 23 Apr 2021 23:17:56 GMT
ARG OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:42:47 GMT
ARG EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95
# Fri, 23 Apr 2021 23:42:48 GMT
ARG NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b
# Fri, 23 Apr 2021 23:42:48 GMT
ARG NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e
# Fri, 23 Apr 2021 23:42:49 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.12 org.opencontainers.image.revision=cl201220201111-0736 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 23 Apr 2021 23:42:49 GMT
ENV LIBERTY_VERSION=20.0.0_12
# Fri, 23 Apr 2021 23:42:50 GMT
ARG LIBERTY_URL
# Fri, 23 Apr 2021 23:42:50 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 23 Apr 2021 23:43:05 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:43:07 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Apr 2021 23:43:07 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.12 BuildLabel=cl201220201111-0736
# Fri, 23 Apr 2021 23:43:08 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:43:10 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 23 Apr 2021 23:43:10 GMT
COPY dir:87fb88e41281cc95d67404db807cebd05ba85ea3f246dace99de7f445dc641b1 in /opt/ibm/helpers/ 
# Fri, 23 Apr 2021 23:43:11 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 23 Apr 2021 23:43:13 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 23 Apr 2021 23:43:24 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 23 Apr 2021 23:43:25 GMT
ENV RANDFILE=/tmp/.rnd
# Fri, 23 Apr 2021 23:43:26 GMT
USER 1001
# Fri, 23 Apr 2021 23:43:27 GMT
EXPOSE 9080 9443
# Fri, 23 Apr 2021 23:43:27 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 23 Apr 2021 23:43:28 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 23 Apr 2021 23:48:29 GMT
ARG VERBOSE=false
# Fri, 23 Apr 2021 23:48:29 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 23 Apr 2021 23:52:12 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Fri, 23 Apr 2021 23:52:21 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 23 Apr 2021 23:53:03 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:de53239ada2db01e7972c3f6eddcf6729f7cf3102be78e0b41363125ce7c2425`  
		Last Modified: Fri, 23 Apr 2021 21:47:14 GMT  
		Size: 27.1 MB (27136362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12932016d0f51acb5c5e5ba5b420a369401a7df47a219f24680bbc05ffde7e11`  
		Last Modified: Fri, 23 Apr 2021 21:47:10 GMT  
		Size: 840.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46997f76c5876e3274170b667463b3d88475cd696ccbc735d2f63965668673ad`  
		Last Modified: Fri, 23 Apr 2021 21:47:10 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bab416938acf6dd045c9fc9097e5768c61b5899b07d110ab3844f447e12b113`  
		Last Modified: Fri, 23 Apr 2021 22:19:05 GMT  
		Size: 15.7 MB (15741779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0273d3bc7cd55960a36b00d19e8d51f8bbeed03d24fd8d551c957fc19ef079b`  
		Last Modified: Fri, 23 Apr 2021 22:22:19 GMT  
		Size: 42.0 MB (41951613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95422aa686364d2877a279281f6eb1157805fa8516aa976b06ce8889dc9f932`  
		Last Modified: Fri, 23 Apr 2021 22:22:13 GMT  
		Size: 3.8 MB (3836026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14990fd09b16cce85a67e70a4e36d5d7ef545bc5829d4dc06518ea0903f4358`  
		Last Modified: Fri, 23 Apr 2021 23:56:06 GMT  
		Size: 14.1 MB (14073762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38aa8db5d764898076adcec4d5fcb6d26084791113dbda57be0b413f0ac4ea5a`  
		Last Modified: Fri, 23 Apr 2021 23:56:03 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7e6711cc2aa475abf04587896ab39969dc660ddb9421d972c056ef7b5c5dc2`  
		Last Modified: Fri, 23 Apr 2021 23:56:03 GMT  
		Size: 9.5 KB (9547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe14ed65b3cf26bd582e4bd1eb693e3f71699e9e92311a838656193a9e2477b`  
		Last Modified: Fri, 23 Apr 2021 23:56:03 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73018234e80a68db6be5395e2a277fff7a9f1af426031715465df02238c7249e`  
		Last Modified: Fri, 23 Apr 2021 23:56:03 GMT  
		Size: 10.5 KB (10539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ce511ea4a40133df08b1bc9befe2d7e56b51ab317b52c4a1aa57e2a1b0347`  
		Last Modified: Fri, 23 Apr 2021 23:56:03 GMT  
		Size: 2.5 MB (2456182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65f16c41028a74817e6ad6bfcbc77333a5352ac0b213f3ec5ae985b4adc6863`  
		Last Modified: Fri, 23 Apr 2021 23:56:40 GMT  
		Size: 194.6 MB (194616382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53733f5dce7b155495e96e49df8e86a805c2643b277d79f4ea121fbc946b872`  
		Last Modified: Fri, 23 Apr 2021 23:56:32 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727cc458a6da1a2cd1ccfedd3fe7d36bf0a6ccd5e0e97de73f0bfcaa63aed45a`  
		Last Modified: Fri, 23 Apr 2021 23:56:33 GMT  
		Size: 13.6 MB (13600394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:20.0.0.12-full-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:1a402efa5f5122d51171f50766ed2490fb6f77e697b48789339679d7c817e9ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:20.0.0.12-full-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:e288402fbc22c5f5c3807a168770e277288ba2059e61492d6c5eee110d60aafb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.5 MB (401499441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde0be4d6aa814b6c1137b0da28d2b72f44dade75a07845f52455802144033a2`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 09:30:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 26 Mar 2021 09:31:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 09:31:04 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 26 Mar 2021 09:31:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Mar 2021 09:31:42 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 26 Mar 2021 21:31:17 GMT
ARG VERBOSE=false
# Fri, 26 Mar 2021 21:31:18 GMT
ARG OPENJ9_SCC=true
# Fri, 26 Mar 2021 21:40:32 GMT
ARG EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95
# Fri, 26 Mar 2021 21:40:33 GMT
ARG NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b
# Fri, 26 Mar 2021 21:40:33 GMT
ARG NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e
# Fri, 26 Mar 2021 21:40:33 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.12 org.opencontainers.image.revision=cl201220201111-0736 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 26 Mar 2021 21:40:33 GMT
ENV LIBERTY_VERSION=20.0.0_12
# Fri, 26 Mar 2021 21:40:33 GMT
ARG LIBERTY_URL
# Fri, 26 Mar 2021 21:40:34 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 26 Mar 2021 21:40:45 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 21:40:45 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Mar 2021 21:40:46 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.12 BuildLabel=cl201220201111-0736
# Fri, 26 Mar 2021 21:40:46 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 26 Mar 2021 21:40:48 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 26 Mar 2021 21:40:48 GMT
COPY dir:87fb88e41281cc95d67404db807cebd05ba85ea3f246dace99de7f445dc641b1 in /opt/ibm/helpers/ 
# Fri, 26 Mar 2021 21:40:48 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 26 Mar 2021 21:40:49 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 26 Mar 2021 21:41:03 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 26 Mar 2021 21:41:04 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Fri, 26 Mar 2021 21:41:04 GMT
USER 1001
# Fri, 26 Mar 2021 21:41:04 GMT
EXPOSE 9080 9443
# Fri, 26 Mar 2021 21:41:04 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 26 Mar 2021 21:41:05 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 26 Mar 2021 21:41:38 GMT
ARG VERBOSE=false
# Fri, 26 Mar 2021 21:41:38 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 26 Mar 2021 21:44:24 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Fri, 26 Mar 2021 21:44:24 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 26 Mar 2021 21:45:06 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4764ed71d2900c9874838108e377eb8821088502d5504fadeb080e5dd1a3e65d`  
		Last Modified: Fri, 26 Mar 2021 09:35:47 GMT  
		Size: 3.0 MB (2958415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf5000c541da177b7cfe59bf3ff8cb271529f443ee224bf88989910e9a2abb1`  
		Last Modified: Fri, 26 Mar 2021 09:36:01 GMT  
		Size: 130.8 MB (130805802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40ee7d487dafaadac6979a031a0ebf6012f22c16e40fbe1bd8f10efce0b9c65`  
		Last Modified: Fri, 26 Mar 2021 21:50:42 GMT  
		Size: 14.0 MB (13974218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d7271e1d74576aed28a2bd8d9d204d8710a6ae9b56d7272219c22df6d1ffc8`  
		Last Modified: Fri, 26 Mar 2021 21:50:39 GMT  
		Size: 695.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be684063c168c2aff35e4fb23280fe43601dee7593e3505b7da6739babcda15f`  
		Last Modified: Fri, 26 Mar 2021 21:50:38 GMT  
		Size: 9.5 KB (9549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcee88b6cd6ee2df9893637c15b1e02d9553045adb73c9012fa79da341939115`  
		Last Modified: Fri, 26 Mar 2021 21:50:40 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07e52523e231c16607e11a295f6532f04c620e6d8a35cb21b692316bbf009ef`  
		Last Modified: Fri, 26 Mar 2021 21:50:38 GMT  
		Size: 10.5 KB (10534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda582494cd506b03886741b406ca50a1f5f2b64a906e71ba036f4f85ba18d9e`  
		Last Modified: Fri, 26 Mar 2021 21:50:40 GMT  
		Size: 5.6 MB (5626186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25dff5c8795a4876ec943dedb0967b151bd8d9be7224b5677531162811efac0f`  
		Last Modified: Fri, 26 Mar 2021 21:51:20 GMT  
		Size: 200.2 MB (200202832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eec289478ec51c113035877e59e023aaed08605aedaa036a3d648933cf6f128`  
		Last Modified: Fri, 26 Mar 2021 21:51:05 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce67a12bea5a210d5c3a06156c50e006c0d9ca021cdc1a26f5013c5a730756a`  
		Last Modified: Fri, 26 Mar 2021 21:51:12 GMT  
		Size: 21.2 MB (21198171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:20.0.0.12-full-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:f071c3de874f9d7146711232277cab8ad3b5907c324548c8fb1ef13d1501ac31
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.5 MB (401530884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1fdcc0f38330a433c3ab56e3964e73b9081b882476f67546efaa28f0924d68`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 22:30:25 GMT
ADD file:818f810cd30ef74fd4690c6265d80265647ba3353880cf8323500df6d2c48b69 in / 
# Fri, 23 Apr 2021 22:30:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:31:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:31:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:31:32 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:16:58 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 23 Apr 2021 23:17:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:17:43 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 23 Apr 2021 23:18:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 23 Apr 2021 23:19:03 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Sat, 24 Apr 2021 03:07:07 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 03:07:12 GMT
ARG OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:40:58 GMT
ARG EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95
# Sat, 24 Apr 2021 03:41:01 GMT
ARG NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b
# Sat, 24 Apr 2021 03:41:04 GMT
ARG NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e
# Sat, 24 Apr 2021 03:41:10 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.12 org.opencontainers.image.revision=cl201220201111-0736 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Sat, 24 Apr 2021 03:41:11 GMT
ENV LIBERTY_VERSION=20.0.0_12
# Sat, 24 Apr 2021 03:41:17 GMT
ARG LIBERTY_URL
# Sat, 24 Apr 2021 03:41:24 GMT
ARG DOWNLOAD_OPTIONS=
# Sat, 24 Apr 2021 03:42:03 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 03:42:08 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 24 Apr 2021 03:42:10 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.12 BuildLabel=cl201220201111-0736
# Sat, 24 Apr 2021 03:42:14 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:42:25 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Sat, 24 Apr 2021 03:42:26 GMT
COPY dir:87fb88e41281cc95d67404db807cebd05ba85ea3f246dace99de7f445dc641b1 in /opt/ibm/helpers/ 
# Sat, 24 Apr 2021 03:42:27 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Sat, 24 Apr 2021 03:42:39 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Sat, 24 Apr 2021 03:42:59 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Sat, 24 Apr 2021 03:43:03 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Sat, 24 Apr 2021 03:43:07 GMT
USER 1001
# Sat, 24 Apr 2021 03:43:11 GMT
EXPOSE 9080 9443
# Sat, 24 Apr 2021 03:43:17 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Sat, 24 Apr 2021 03:43:22 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Sat, 24 Apr 2021 03:46:46 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 03:46:52 GMT
ARG REPOSITORIES_PROPERTIES=
# Sat, 24 Apr 2021 03:50:25 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Sat, 24 Apr 2021 03:50:32 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Sat, 24 Apr 2021 03:51:35 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:bb3095714506c08a64a49e29ab001d7000d94957d52e05db35361fd4a54c460c`  
		Last Modified: Fri, 23 Apr 2021 22:36:52 GMT  
		Size: 30.4 MB (30407300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd29acc6f7bfef8034eaca0bfb069f0d66e50351c84b062e224d6eae710afa79`  
		Last Modified: Fri, 23 Apr 2021 22:36:46 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7645fc50c9e70df51732b36ef7f8b21ebacd148c3bee4f1b29ca6dcba1bbb949`  
		Last Modified: Fri, 23 Apr 2021 22:36:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab6dc42492fe0eca98f1e563f3e8dabb70f122b45b752264bacb4ea14f59354`  
		Last Modified: Fri, 23 Apr 2021 23:22:26 GMT  
		Size: 3.1 MB (3082775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510992b332e039a7852bef411702a4b667a17ae9ef201c9118477ccc53172fa8`  
		Last Modified: Fri, 23 Apr 2021 23:22:40 GMT  
		Size: 130.4 MB (130406625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2e0effe70284b9aaa34e20248a8d553b2eca8d4a13ba8c93fa4bd1271e5010`  
		Last Modified: Sat, 24 Apr 2021 04:00:40 GMT  
		Size: 14.0 MB (13975149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8e08d2f933b715233d01bd3e35d4f175e0a0d2984b5af3a10ea10cba1ec886`  
		Last Modified: Sat, 24 Apr 2021 04:00:35 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d6f2bbd86f77d68a9f5fbc39009d8fb953e3a98cfa5b99be7ac425492b29506`  
		Last Modified: Sat, 24 Apr 2021 04:00:35 GMT  
		Size: 9.6 KB (9551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f6784f1f468a3b7e5818e3817fa058c2d6627026d35766f8e3d9a3c0e8b125`  
		Last Modified: Sat, 24 Apr 2021 04:00:35 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41dadc8108b94ff940095ded5ad7a9f8a6c33ab4ed3890cbc19f228b7a8d38c4`  
		Last Modified: Sat, 24 Apr 2021 04:00:35 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f115418b905857fcb014ab4ed2c33207a3991f94a65f8670934831ec68eaa435`  
		Last Modified: Sat, 24 Apr 2021 04:00:36 GMT  
		Size: 5.2 MB (5157234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8148eb87a14826269394746ac257b7935a6b7eb2e92e5990f41c5f064e62976`  
		Last Modified: Sat, 24 Apr 2021 04:01:27 GMT  
		Size: 199.7 MB (199735551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc029e2c19f14f14a4ee3752d20208253ada649ae6e6f2db9d4f3397218443a`  
		Last Modified: Sat, 24 Apr 2021 04:01:07 GMT  
		Size: 950.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14b4cd159cc03571e68c271dedf205f06b4591ea93ecbcf5c28f486360233d9`  
		Last Modified: Sat, 24 Apr 2021 04:01:12 GMT  
		Size: 18.7 MB (18743188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:20.0.0.12-full-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:c3ba620ffcffe507805150be6db3dbe7bb2673b1690875bd8c1ccdec87ecab4d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.8 MB (397786781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aab8e79b4cda357d7d5e110a6f7962ed7af1c62c8c64dadbc2b124b8115f6c2`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 21:45:00 GMT
ADD file:5e61a5300d520d61a2130623465ba2e46da8e80dc2afa042473a42cbcd8d88d2 in / 
# Fri, 23 Apr 2021 21:45:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 21:45:05 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 21:45:07 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 21:45:07 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 22:25:02 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 23 Apr 2021 22:25:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:25:17 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 23 Apr 2021 22:26:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 23 Apr 2021 22:26:15 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 23 Apr 2021 23:16:58 GMT
ARG VERBOSE=false
# Fri, 23 Apr 2021 23:16:58 GMT
ARG OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:41:58 GMT
ARG EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95
# Fri, 23 Apr 2021 23:41:59 GMT
ARG NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b
# Fri, 23 Apr 2021 23:42:00 GMT
ARG NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e
# Fri, 23 Apr 2021 23:42:00 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.12 org.opencontainers.image.revision=cl201220201111-0736 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 23 Apr 2021 23:42:01 GMT
ENV LIBERTY_VERSION=20.0.0_12
# Fri, 23 Apr 2021 23:42:01 GMT
ARG LIBERTY_URL
# Fri, 23 Apr 2021 23:42:02 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 23 Apr 2021 23:42:17 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:42:18 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Apr 2021 23:42:18 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.12 BuildLabel=cl201220201111-0736
# Fri, 23 Apr 2021 23:42:19 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:42:21 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 23 Apr 2021 23:42:21 GMT
COPY dir:87fb88e41281cc95d67404db807cebd05ba85ea3f246dace99de7f445dc641b1 in /opt/ibm/helpers/ 
# Fri, 23 Apr 2021 23:42:22 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 23 Apr 2021 23:42:24 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 23 Apr 2021 23:42:37 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 23 Apr 2021 23:42:39 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Fri, 23 Apr 2021 23:42:39 GMT
USER 1001
# Fri, 23 Apr 2021 23:42:40 GMT
EXPOSE 9080 9443
# Fri, 23 Apr 2021 23:42:40 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 23 Apr 2021 23:42:41 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 23 Apr 2021 23:43:36 GMT
ARG VERBOSE=false
# Fri, 23 Apr 2021 23:43:37 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 23 Apr 2021 23:47:22 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Fri, 23 Apr 2021 23:47:35 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 23 Apr 2021 23:48:18 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:33ddddc4572ffe1f294f9f599ed989cc41eee5da4cdcf7db12d10700aa8c894e`  
		Last Modified: Fri, 23 Apr 2021 21:47:03 GMT  
		Size: 25.4 MB (25352756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4395f372a786db91b2f50dc8e43d8b7c3533eb4bd86f6728eb2a0c7108c077d2`  
		Last Modified: Fri, 23 Apr 2021 21:46:59 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e39753730df188282ca8193f14bbbb8cbe0b76ec02b34283a28449b1e41c05`  
		Last Modified: Fri, 23 Apr 2021 21:47:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e93b87da546ac7aa6705cd2f20bfe70cf04793ac73561e5dd8c579af88754aec`  
		Last Modified: Fri, 23 Apr 2021 22:28:41 GMT  
		Size: 2.7 MB (2676643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268462fc02d2bd9da227784f5f243759923a14cefb3648739ca02e8fa7d63ee7`  
		Last Modified: Fri, 23 Apr 2021 22:28:50 GMT  
		Size: 128.1 MB (128065984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4df10ec61b2e9901491d4f07888d6c128dfbc89ae81370abc047a85d361b573`  
		Last Modified: Fri, 23 Apr 2021 23:55:57 GMT  
		Size: 14.0 MB (13974414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b6dcfa2ac20b90dbdc5c0eca9e30f63ba290ecb24d0a2a7161dfd1698eb9dc`  
		Last Modified: Fri, 23 Apr 2021 23:55:52 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b8e5538da3fede30dc5d6f993e2d935e513e68b67eec3bf34b49992e0c0a28`  
		Last Modified: Fri, 23 Apr 2021 23:55:55 GMT  
		Size: 9.5 KB (9548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986f755a30bd8e1dce1334bec46b1614c36821840b84ef826782f1ff8d8fd247`  
		Last Modified: Fri, 23 Apr 2021 23:55:52 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c4c1e123eb0af1079650d1d318286fe5e4df814ada15c45d58dc31a274cd54`  
		Last Modified: Fri, 23 Apr 2021 23:55:55 GMT  
		Size: 10.5 KB (10534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503e041448d0e036d4d18f56f75d491f9a4492e94731e354db7370afc652015f`  
		Last Modified: Fri, 23 Apr 2021 23:55:53 GMT  
		Size: 5.8 MB (5776530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cca07b4da726863086c9e80efa52bcf0498db17ec4c66510543a8e83ff33ae`  
		Last Modified: Fri, 23 Apr 2021 23:56:23 GMT  
		Size: 200.4 MB (200355463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bf9b5980ecfadb96f1fcf3bcc6967e8e930fcf1e0950628514511ee7e4622a`  
		Last Modified: Fri, 23 Apr 2021 23:56:10 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48303b42988be9dab5c39442053d70969976646d4444669017e816b857e28656`  
		Last Modified: Fri, 23 Apr 2021 23:56:13 GMT  
		Size: 21.6 MB (21561952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:20.0.0.12-kernel-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:cc401f8cee4b8048b12d21fb1f110d1f4918c1f66d1c86f01e1deae58599d7df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:20.0.0.12-kernel-java11-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:517bb85cf121708889127e989c208693965377616ceeeb03ff4f2b1415a7ffa2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107651695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868de794a5c32cd1f825e1c673450c6f48b44e3db6f6953e2fb4257d04323a34`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 03 Apr 2021 00:53:06 GMT
ADD file:27277aee655dd263ee698d1f2fe17f0b1dbba740615bcac8642723a6ac0d62be in / 
# Sat, 03 Apr 2021 00:53:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 03 Apr 2021 00:53:08 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Sat, 03 Apr 2021 00:53:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 03 Apr 2021 00:53:09 GMT
CMD ["/bin/bash"]
# Sat, 03 Apr 2021 01:29:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 03 Apr 2021 01:29:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 03 Apr 2021 01:32:52 GMT
ENV JAVA_VERSION=jdk-11.0.10+9_openj9-0.24.0
# Mon, 19 Apr 2021 18:22:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='5d2b2939637f999a1910d5cc0fb3d96756125941e5f8b9e3003635aa863664b5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        s390x)          ESUM='2ff9f50d6ffc345434703c43a1d67ac6d3d054b5d4925b4b73a3ce51b02940e5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7e5f97071f8b86c22c36ddfd7f821c3e8ec531c1128e2e6c931b2e64118a517a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 19 Apr 2021 18:22:34 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Apr 2021 18:22:34 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 19 Apr 2021 18:23:10 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 22 Apr 2021 21:40:48 GMT
ARG VERBOSE=false
# Thu, 22 Apr 2021 21:40:48 GMT
ARG OPENJ9_SCC=true
# Thu, 22 Apr 2021 21:52:45 GMT
ARG EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95
# Thu, 22 Apr 2021 21:52:45 GMT
ARG NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b
# Thu, 22 Apr 2021 21:52:45 GMT
ARG NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e
# Thu, 22 Apr 2021 21:52:46 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.12 org.opencontainers.image.revision=cl201220201111-0736 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 22 Apr 2021 21:52:46 GMT
ENV LIBERTY_VERSION=20.0.0_12
# Thu, 22 Apr 2021 21:52:46 GMT
ARG LIBERTY_URL
# Thu, 22 Apr 2021 21:52:46 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 22 Apr 2021 21:52:54 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Apr 2021 21:52:54 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Apr 2021 21:52:54 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.12 BuildLabel=cl201220201111-0736
# Thu, 22 Apr 2021 21:52:55 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 22 Apr 2021 21:52:56 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Apr 2021 21:52:56 GMT
COPY dir:87fb88e41281cc95d67404db807cebd05ba85ea3f246dace99de7f445dc641b1 in /opt/ibm/helpers/ 
# Thu, 22 Apr 2021 21:52:56 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Apr 2021 21:52:57 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Apr 2021 21:53:05 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Apr 2021 21:53:05 GMT
ENV RANDFILE=/tmp/.rnd
# Thu, 22 Apr 2021 21:53:05 GMT
USER 1001
# Thu, 22 Apr 2021 21:53:05 GMT
EXPOSE 9080 9443
# Thu, 22 Apr 2021 21:53:05 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Apr 2021 21:53:06 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:a70d879fa5984474288d52009479054b8bb2993de2a1859f43b5480600cecb24`  
		Last Modified: Thu, 01 Apr 2021 15:20:06 GMT  
		Size: 28.6 MB (28569016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4394a92d1f8760cf7d17fee0bcee732c94c5b858dd8d19c7ff02beecf3b4e83`  
		Last Modified: Sat, 03 Apr 2021 00:54:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e6159c56c084c858f5de2416454ac0a49ddda47b764e4379c5d5a147c9bf5f`  
		Last Modified: Sat, 03 Apr 2021 00:54:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04b772c31f76720583412a2507c5c53889985db45169a85f0d3cd7f842e041a`  
		Last Modified: Sat, 03 Apr 2021 01:39:30 GMT  
		Size: 16.0 MB (16032891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf71362343a962febc8c6ce8c4fd12d961c5712407993471f60ac0e5d43415e`  
		Last Modified: Mon, 19 Apr 2021 18:30:17 GMT  
		Size: 42.4 MB (42440313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9163852ff25e45c3b95c7b759a719b91afa29724136e68d1cf7f822c034c4df`  
		Last Modified: Mon, 19 Apr 2021 18:30:04 GMT  
		Size: 4.0 MB (4025359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf4544075da5a2c6e7e1b2994b4e7636ccfe9b195b9bb20633733c96ec9a4f9`  
		Last Modified: Thu, 22 Apr 2021 21:59:06 GMT  
		Size: 14.1 MB (14073296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc613cdafc1c7638c8e6e19a98b47464b53ed0758b32961a8ac7780be065560`  
		Last Modified: Thu, 22 Apr 2021 21:59:01 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1783f70e1fa5a4b6784678ac26ee301431e1fd49ab67ec6d1c5670bf1f3fbb16`  
		Last Modified: Thu, 22 Apr 2021 21:59:01 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774ae461e99f7b8733efbb61a4690422357faa1c019ba98c32119eebd94a8e52`  
		Last Modified: Thu, 22 Apr 2021 21:59:01 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a0fcd773f7170f8b6ecd93b521d77d68777a7041eebbf8ce5d6d7b3fd5318c`  
		Last Modified: Thu, 22 Apr 2021 21:59:01 GMT  
		Size: 10.5 KB (10528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7315afa7e7544b7a663e1baa7146a4cd1bb0d2b26e6bf855b9d7a18fe3dfbf`  
		Last Modified: Thu, 22 Apr 2021 21:59:02 GMT  
		Size: 2.5 MB (2488744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:20.0.0.12-kernel-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:4fe26604b5cf343c117e9b279a7fe7f968bdf03d2aaa82a639a06dfcaa972308
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.6 MB (113557453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771b8ed8c8bbb1e9c961ccd1fe3b23deb9b72d0082c9d47c9f53ecd2394e6ca7`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:16:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 24 Apr 2021 01:19:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:28:36 GMT
ENV JAVA_VERSION=jdk-11.0.10+9_openj9-0.24.0
# Sat, 24 Apr 2021 01:30:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='5d2b2939637f999a1910d5cc0fb3d96756125941e5f8b9e3003635aa863664b5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        s390x)          ESUM='2ff9f50d6ffc345434703c43a1d67ac6d3d054b5d4925b4b73a3ce51b02940e5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7e5f97071f8b86c22c36ddfd7f821c3e8ec531c1128e2e6c931b2e64118a517a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 24 Apr 2021 01:30:48 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 24 Apr 2021 01:30:53 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Sat, 24 Apr 2021 01:31:37 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Sat, 24 Apr 2021 03:09:49 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 03:09:52 GMT
ARG OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:43:37 GMT
ARG EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95
# Sat, 24 Apr 2021 03:43:40 GMT
ARG NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b
# Sat, 24 Apr 2021 03:43:42 GMT
ARG NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e
# Sat, 24 Apr 2021 03:43:48 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.12 org.opencontainers.image.revision=cl201220201111-0736 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Sat, 24 Apr 2021 03:43:50 GMT
ENV LIBERTY_VERSION=20.0.0_12
# Sat, 24 Apr 2021 03:43:57 GMT
ARG LIBERTY_URL
# Sat, 24 Apr 2021 03:44:00 GMT
ARG DOWNLOAD_OPTIONS=
# Sat, 24 Apr 2021 03:44:45 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 03:44:54 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 24 Apr 2021 03:45:02 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.12 BuildLabel=cl201220201111-0736
# Sat, 24 Apr 2021 03:45:09 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:45:24 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Sat, 24 Apr 2021 03:45:26 GMT
COPY dir:87fb88e41281cc95d67404db807cebd05ba85ea3f246dace99de7f445dc641b1 in /opt/ibm/helpers/ 
# Sat, 24 Apr 2021 03:45:28 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Sat, 24 Apr 2021 03:45:43 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Sat, 24 Apr 2021 03:46:10 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Sat, 24 Apr 2021 03:46:12 GMT
ENV RANDFILE=/tmp/.rnd
# Sat, 24 Apr 2021 03:46:15 GMT
USER 1001
# Sat, 24 Apr 2021 03:46:18 GMT
EXPOSE 9080 9443
# Sat, 24 Apr 2021 03:46:22 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Sat, 24 Apr 2021 03:46:27 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da07529aeac8fe5c90c5bb8c4f516c9d6fd248cc1daa5fecd137c809bce39bb6`  
		Last Modified: Sat, 24 Apr 2021 01:40:58 GMT  
		Size: 17.2 MB (17209103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53f9612e78ec5df6fbbbab4098deb40150ceef63be58aec6c2dd4df6af9f634`  
		Last Modified: Sat, 24 Apr 2021 01:46:21 GMT  
		Size: 43.3 MB (43277570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec133c54d62c9541f8b987c7353d67bd5d58ea39050f8cd947bf150d5ce8bb7a`  
		Last Modified: Sat, 24 Apr 2021 01:46:15 GMT  
		Size: 3.3 MB (3289250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc394ddf4e34a090a199321258a21dfecfcf1ab44974ab8b4a36662ef5287ed5`  
		Last Modified: Sat, 24 Apr 2021 04:00:57 GMT  
		Size: 14.1 MB (14074578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b11004119d5d190e5164dc96ce5220189cc627326713ac4bbce2e96f88bfd1c`  
		Last Modified: Sat, 24 Apr 2021 04:00:51 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91d7cd2480a852fef8c64bcd9ff7b4c757ef6229c4e21e2b2170a326f36ec550`  
		Last Modified: Sat, 24 Apr 2021 04:00:51 GMT  
		Size: 9.5 KB (9549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2808ea8be40d8b0ffae1ee4c07b5ebbfa183d5df84c84416829b8f45ad31a9b`  
		Last Modified: Sat, 24 Apr 2021 04:00:52 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c158e0bf410648b3c8d9e8d211f242606d8e90a07db1db5e209412c559827a`  
		Last Modified: Sat, 24 Apr 2021 04:00:51 GMT  
		Size: 10.5 KB (10543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66491e8e215274e92107b8d888d7544390984679b322aba9530bbfba4b8366e`  
		Last Modified: Sat, 24 Apr 2021 04:00:52 GMT  
		Size: 2.4 MB (2429469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:20.0.0.12-kernel-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:cf5f49a62545164e7953f96a232cedae4445c2f5fe7308f023abc84620ecfc5c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105217806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:685dcea7a6f0d953adc1be0206a79e39bcf7dfb5b803376cf1dfe9829459fd30`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 21:45:20 GMT
ADD file:282d950116f923276efabd13c7dc17b942821edb14ffac4b89b9a50bcdf99e17 in / 
# Fri, 23 Apr 2021 21:45:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 21:45:27 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 21:45:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 21:45:29 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 22:03:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Apr 2021 22:04:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:10:11 GMT
ENV JAVA_VERSION=jdk-11.0.10+9_openj9-0.24.0
# Fri, 23 Apr 2021 22:11:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='5d2b2939637f999a1910d5cc0fb3d96756125941e5f8b9e3003635aa863664b5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        s390x)          ESUM='2ff9f50d6ffc345434703c43a1d67ac6d3d054b5d4925b4b73a3ce51b02940e5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7e5f97071f8b86c22c36ddfd7f821c3e8ec531c1128e2e6c931b2e64118a517a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 23 Apr 2021 22:11:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Apr 2021 22:11:44 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 23 Apr 2021 22:12:20 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 23 Apr 2021 23:17:55 GMT
ARG VERBOSE=false
# Fri, 23 Apr 2021 23:17:56 GMT
ARG OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:42:47 GMT
ARG EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95
# Fri, 23 Apr 2021 23:42:48 GMT
ARG NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b
# Fri, 23 Apr 2021 23:42:48 GMT
ARG NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e
# Fri, 23 Apr 2021 23:42:49 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.12 org.opencontainers.image.revision=cl201220201111-0736 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 23 Apr 2021 23:42:49 GMT
ENV LIBERTY_VERSION=20.0.0_12
# Fri, 23 Apr 2021 23:42:50 GMT
ARG LIBERTY_URL
# Fri, 23 Apr 2021 23:42:50 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 23 Apr 2021 23:43:05 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:43:07 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Apr 2021 23:43:07 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.12 BuildLabel=cl201220201111-0736
# Fri, 23 Apr 2021 23:43:08 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:43:10 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 23 Apr 2021 23:43:10 GMT
COPY dir:87fb88e41281cc95d67404db807cebd05ba85ea3f246dace99de7f445dc641b1 in /opt/ibm/helpers/ 
# Fri, 23 Apr 2021 23:43:11 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 23 Apr 2021 23:43:13 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 23 Apr 2021 23:43:24 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 23 Apr 2021 23:43:25 GMT
ENV RANDFILE=/tmp/.rnd
# Fri, 23 Apr 2021 23:43:26 GMT
USER 1001
# Fri, 23 Apr 2021 23:43:27 GMT
EXPOSE 9080 9443
# Fri, 23 Apr 2021 23:43:27 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 23 Apr 2021 23:43:28 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:de53239ada2db01e7972c3f6eddcf6729f7cf3102be78e0b41363125ce7c2425`  
		Last Modified: Fri, 23 Apr 2021 21:47:14 GMT  
		Size: 27.1 MB (27136362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12932016d0f51acb5c5e5ba5b420a369401a7df47a219f24680bbc05ffde7e11`  
		Last Modified: Fri, 23 Apr 2021 21:47:10 GMT  
		Size: 840.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46997f76c5876e3274170b667463b3d88475cd696ccbc735d2f63965668673ad`  
		Last Modified: Fri, 23 Apr 2021 21:47:10 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bab416938acf6dd045c9fc9097e5768c61b5899b07d110ab3844f447e12b113`  
		Last Modified: Fri, 23 Apr 2021 22:19:05 GMT  
		Size: 15.7 MB (15741779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0273d3bc7cd55960a36b00d19e8d51f8bbeed03d24fd8d551c957fc19ef079b`  
		Last Modified: Fri, 23 Apr 2021 22:22:19 GMT  
		Size: 42.0 MB (41951613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95422aa686364d2877a279281f6eb1157805fa8516aa976b06ce8889dc9f932`  
		Last Modified: Fri, 23 Apr 2021 22:22:13 GMT  
		Size: 3.8 MB (3836026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14990fd09b16cce85a67e70a4e36d5d7ef545bc5829d4dc06518ea0903f4358`  
		Last Modified: Fri, 23 Apr 2021 23:56:06 GMT  
		Size: 14.1 MB (14073762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38aa8db5d764898076adcec4d5fcb6d26084791113dbda57be0b413f0ac4ea5a`  
		Last Modified: Fri, 23 Apr 2021 23:56:03 GMT  
		Size: 696.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7e6711cc2aa475abf04587896ab39969dc660ddb9421d972c056ef7b5c5dc2`  
		Last Modified: Fri, 23 Apr 2021 23:56:03 GMT  
		Size: 9.5 KB (9547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe14ed65b3cf26bd582e4bd1eb693e3f71699e9e92311a838656193a9e2477b`  
		Last Modified: Fri, 23 Apr 2021 23:56:03 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73018234e80a68db6be5395e2a277fff7a9f1af426031715465df02238c7249e`  
		Last Modified: Fri, 23 Apr 2021 23:56:03 GMT  
		Size: 10.5 KB (10539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6ce511ea4a40133df08b1bc9befe2d7e56b51ab317b52c4a1aa57e2a1b0347`  
		Last Modified: Fri, 23 Apr 2021 23:56:03 GMT  
		Size: 2.5 MB (2456182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:20.0.0.12-kernel-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:9c88b5ad6672adb9876123d53f70a41c03544830f0be72d9a98d50b902fd9416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:20.0.0.12-kernel-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:0d0ae8155a5bb5941362a2c5b9d85a479e540ea08efd26b26fe1c52271bfb1cb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.1 MB (180097492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b68159b13cedee60e6bbcdced790ec517a99868c5ce2e586fbe12982bf9978c`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 09:30:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 26 Mar 2021 09:31:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 09:31:04 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 26 Mar 2021 09:31:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Mar 2021 09:31:42 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 26 Mar 2021 21:31:17 GMT
ARG VERBOSE=false
# Fri, 26 Mar 2021 21:31:18 GMT
ARG OPENJ9_SCC=true
# Fri, 26 Mar 2021 21:40:32 GMT
ARG EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95
# Fri, 26 Mar 2021 21:40:33 GMT
ARG NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b
# Fri, 26 Mar 2021 21:40:33 GMT
ARG NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e
# Fri, 26 Mar 2021 21:40:33 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.12 org.opencontainers.image.revision=cl201220201111-0736 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 26 Mar 2021 21:40:33 GMT
ENV LIBERTY_VERSION=20.0.0_12
# Fri, 26 Mar 2021 21:40:33 GMT
ARG LIBERTY_URL
# Fri, 26 Mar 2021 21:40:34 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 26 Mar 2021 21:40:45 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 21:40:45 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Mar 2021 21:40:46 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.12 BuildLabel=cl201220201111-0736
# Fri, 26 Mar 2021 21:40:46 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 26 Mar 2021 21:40:48 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 26 Mar 2021 21:40:48 GMT
COPY dir:87fb88e41281cc95d67404db807cebd05ba85ea3f246dace99de7f445dc641b1 in /opt/ibm/helpers/ 
# Fri, 26 Mar 2021 21:40:48 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 26 Mar 2021 21:40:49 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 26 Mar 2021 21:41:03 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 26 Mar 2021 21:41:04 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Fri, 26 Mar 2021 21:41:04 GMT
USER 1001
# Fri, 26 Mar 2021 21:41:04 GMT
EXPOSE 9080 9443
# Fri, 26 Mar 2021 21:41:04 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 26 Mar 2021 21:41:05 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4764ed71d2900c9874838108e377eb8821088502d5504fadeb080e5dd1a3e65d`  
		Last Modified: Fri, 26 Mar 2021 09:35:47 GMT  
		Size: 3.0 MB (2958415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf5000c541da177b7cfe59bf3ff8cb271529f443ee224bf88989910e9a2abb1`  
		Last Modified: Fri, 26 Mar 2021 09:36:01 GMT  
		Size: 130.8 MB (130805802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40ee7d487dafaadac6979a031a0ebf6012f22c16e40fbe1bd8f10efce0b9c65`  
		Last Modified: Fri, 26 Mar 2021 21:50:42 GMT  
		Size: 14.0 MB (13974218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d7271e1d74576aed28a2bd8d9d204d8710a6ae9b56d7272219c22df6d1ffc8`  
		Last Modified: Fri, 26 Mar 2021 21:50:39 GMT  
		Size: 695.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be684063c168c2aff35e4fb23280fe43601dee7593e3505b7da6739babcda15f`  
		Last Modified: Fri, 26 Mar 2021 21:50:38 GMT  
		Size: 9.5 KB (9549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcee88b6cd6ee2df9893637c15b1e02d9553045adb73c9012fa79da341939115`  
		Last Modified: Fri, 26 Mar 2021 21:50:40 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07e52523e231c16607e11a295f6532f04c620e6d8a35cb21b692316bbf009ef`  
		Last Modified: Fri, 26 Mar 2021 21:50:38 GMT  
		Size: 10.5 KB (10534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda582494cd506b03886741b406ca50a1f5f2b64a906e71ba036f4f85ba18d9e`  
		Last Modified: Fri, 26 Mar 2021 21:50:40 GMT  
		Size: 5.6 MB (5626186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:20.0.0.12-kernel-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:95c455568517b35b5d99f8d25129f9b68dfbb56da5e597cd0841002333d9beab
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.1 MB (183051195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbafd2af836b048d114959790980db6f7ea46798a0159d2dacb66298be03503`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 22:30:25 GMT
ADD file:818f810cd30ef74fd4690c6265d80265647ba3353880cf8323500df6d2c48b69 in / 
# Fri, 23 Apr 2021 22:30:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:31:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:31:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:31:32 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:16:58 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 23 Apr 2021 23:17:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:17:43 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 23 Apr 2021 23:18:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 23 Apr 2021 23:19:03 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Sat, 24 Apr 2021 03:07:07 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 03:07:12 GMT
ARG OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:40:58 GMT
ARG EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95
# Sat, 24 Apr 2021 03:41:01 GMT
ARG NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b
# Sat, 24 Apr 2021 03:41:04 GMT
ARG NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e
# Sat, 24 Apr 2021 03:41:10 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.12 org.opencontainers.image.revision=cl201220201111-0736 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Sat, 24 Apr 2021 03:41:11 GMT
ENV LIBERTY_VERSION=20.0.0_12
# Sat, 24 Apr 2021 03:41:17 GMT
ARG LIBERTY_URL
# Sat, 24 Apr 2021 03:41:24 GMT
ARG DOWNLOAD_OPTIONS=
# Sat, 24 Apr 2021 03:42:03 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 03:42:08 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 24 Apr 2021 03:42:10 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.12 BuildLabel=cl201220201111-0736
# Sat, 24 Apr 2021 03:42:14 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:42:25 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Sat, 24 Apr 2021 03:42:26 GMT
COPY dir:87fb88e41281cc95d67404db807cebd05ba85ea3f246dace99de7f445dc641b1 in /opt/ibm/helpers/ 
# Sat, 24 Apr 2021 03:42:27 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Sat, 24 Apr 2021 03:42:39 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Sat, 24 Apr 2021 03:42:59 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Sat, 24 Apr 2021 03:43:03 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Sat, 24 Apr 2021 03:43:07 GMT
USER 1001
# Sat, 24 Apr 2021 03:43:11 GMT
EXPOSE 9080 9443
# Sat, 24 Apr 2021 03:43:17 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Sat, 24 Apr 2021 03:43:22 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:bb3095714506c08a64a49e29ab001d7000d94957d52e05db35361fd4a54c460c`  
		Last Modified: Fri, 23 Apr 2021 22:36:52 GMT  
		Size: 30.4 MB (30407300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd29acc6f7bfef8034eaca0bfb069f0d66e50351c84b062e224d6eae710afa79`  
		Last Modified: Fri, 23 Apr 2021 22:36:46 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7645fc50c9e70df51732b36ef7f8b21ebacd148c3bee4f1b29ca6dcba1bbb949`  
		Last Modified: Fri, 23 Apr 2021 22:36:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab6dc42492fe0eca98f1e563f3e8dabb70f122b45b752264bacb4ea14f59354`  
		Last Modified: Fri, 23 Apr 2021 23:22:26 GMT  
		Size: 3.1 MB (3082775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510992b332e039a7852bef411702a4b667a17ae9ef201c9118477ccc53172fa8`  
		Last Modified: Fri, 23 Apr 2021 23:22:40 GMT  
		Size: 130.4 MB (130406625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2e0effe70284b9aaa34e20248a8d553b2eca8d4a13ba8c93fa4bd1271e5010`  
		Last Modified: Sat, 24 Apr 2021 04:00:40 GMT  
		Size: 14.0 MB (13975149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8e08d2f933b715233d01bd3e35d4f175e0a0d2984b5af3a10ea10cba1ec886`  
		Last Modified: Sat, 24 Apr 2021 04:00:35 GMT  
		Size: 704.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d6f2bbd86f77d68a9f5fbc39009d8fb953e3a98cfa5b99be7ac425492b29506`  
		Last Modified: Sat, 24 Apr 2021 04:00:35 GMT  
		Size: 9.6 KB (9551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f6784f1f468a3b7e5818e3817fa058c2d6627026d35766f8e3d9a3c0e8b125`  
		Last Modified: Sat, 24 Apr 2021 04:00:35 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41dadc8108b94ff940095ded5ad7a9f8a6c33ab4ed3890cbc19f228b7a8d38c4`  
		Last Modified: Sat, 24 Apr 2021 04:00:35 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f115418b905857fcb014ab4ed2c33207a3991f94a65f8670934831ec68eaa435`  
		Last Modified: Sat, 24 Apr 2021 04:00:36 GMT  
		Size: 5.2 MB (5157234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:20.0.0.12-kernel-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:b1c099564582a14945574a91b48a32161989b6895b9f3b8efc0eb67a50b7f143
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.9 MB (175868418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a7aa9e39c1e1480f526d98393b7bf1d7d6d37d0204861b8c2280590daae1fa`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 21:45:00 GMT
ADD file:5e61a5300d520d61a2130623465ba2e46da8e80dc2afa042473a42cbcd8d88d2 in / 
# Fri, 23 Apr 2021 21:45:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 21:45:05 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 21:45:07 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 21:45:07 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 22:25:02 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 23 Apr 2021 22:25:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:25:17 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 23 Apr 2021 22:26:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 23 Apr 2021 22:26:15 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 23 Apr 2021 23:16:58 GMT
ARG VERBOSE=false
# Fri, 23 Apr 2021 23:16:58 GMT
ARG OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:41:58 GMT
ARG EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95
# Fri, 23 Apr 2021 23:41:59 GMT
ARG NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b
# Fri, 23 Apr 2021 23:42:00 GMT
ARG NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e
# Fri, 23 Apr 2021 23:42:00 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=20.0.0.12 org.opencontainers.image.revision=cl201220201111-0736 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 23 Apr 2021 23:42:01 GMT
ENV LIBERTY_VERSION=20.0.0_12
# Fri, 23 Apr 2021 23:42:01 GMT
ARG LIBERTY_URL
# Fri, 23 Apr 2021 23:42:02 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 23 Apr 2021 23:42:17 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:42:18 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Apr 2021 23:42:18 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=20.0.0.12 BuildLabel=cl201220201111-0736
# Fri, 23 Apr 2021 23:42:19 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:42:21 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 23 Apr 2021 23:42:21 GMT
COPY dir:87fb88e41281cc95d67404db807cebd05ba85ea3f246dace99de7f445dc641b1 in /opt/ibm/helpers/ 
# Fri, 23 Apr 2021 23:42:22 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 23 Apr 2021 23:42:24 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 23 Apr 2021 23:42:37 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=58eed6f817b4ecc5b464f355b0641938c83b95ac22d29b4f657378f887ff4d95 NON_IBM_SHA=454dca0329ea492fc2ddbc03b19031a7eb7a71b45f9e13c89c9fef0f5f51517b NOTICES_SHA=498313e3f283eada744d1fbfd7626473d989d2df58be714f0df0ad561498520e VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 23 Apr 2021 23:42:39 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Fri, 23 Apr 2021 23:42:39 GMT
USER 1001
# Fri, 23 Apr 2021 23:42:40 GMT
EXPOSE 9080 9443
# Fri, 23 Apr 2021 23:42:40 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 23 Apr 2021 23:42:41 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:33ddddc4572ffe1f294f9f599ed989cc41eee5da4cdcf7db12d10700aa8c894e`  
		Last Modified: Fri, 23 Apr 2021 21:47:03 GMT  
		Size: 25.4 MB (25352756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4395f372a786db91b2f50dc8e43d8b7c3533eb4bd86f6728eb2a0c7108c077d2`  
		Last Modified: Fri, 23 Apr 2021 21:46:59 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e39753730df188282ca8193f14bbbb8cbe0b76ec02b34283a28449b1e41c05`  
		Last Modified: Fri, 23 Apr 2021 21:47:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e93b87da546ac7aa6705cd2f20bfe70cf04793ac73561e5dd8c579af88754aec`  
		Last Modified: Fri, 23 Apr 2021 22:28:41 GMT  
		Size: 2.7 MB (2676643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268462fc02d2bd9da227784f5f243759923a14cefb3648739ca02e8fa7d63ee7`  
		Last Modified: Fri, 23 Apr 2021 22:28:50 GMT  
		Size: 128.1 MB (128065984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4df10ec61b2e9901491d4f07888d6c128dfbc89ae81370abc047a85d361b573`  
		Last Modified: Fri, 23 Apr 2021 23:55:57 GMT  
		Size: 14.0 MB (13974414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b6dcfa2ac20b90dbdc5c0eca9e30f63ba290ecb24d0a2a7161dfd1698eb9dc`  
		Last Modified: Fri, 23 Apr 2021 23:55:52 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b8e5538da3fede30dc5d6f993e2d935e513e68b67eec3bf34b49992e0c0a28`  
		Last Modified: Fri, 23 Apr 2021 23:55:55 GMT  
		Size: 9.5 KB (9548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986f755a30bd8e1dce1334bec46b1614c36821840b84ef826782f1ff8d8fd247`  
		Last Modified: Fri, 23 Apr 2021 23:55:52 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c4c1e123eb0af1079650d1d318286fe5e4df814ada15c45d58dc31a274cd54`  
		Last Modified: Fri, 23 Apr 2021 23:55:55 GMT  
		Size: 10.5 KB (10534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503e041448d0e036d4d18f56f75d491f9a4492e94731e354db7370afc652015f`  
		Last Modified: Fri, 23 Apr 2021 23:55:53 GMT  
		Size: 5.8 MB (5776530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:21.0.0.3-full-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:036d18486a11355e421eb633432716e021115ae7708b9750ec5f0e78ee352d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:21.0.0.3-full-java11-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:2f19a41174f8c2c45730c99b71042dfbfef0e96e74815cf702814aa2096638b3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.1 MB (329145880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f609fe19aab6f7cd7ef0d88ac12bdecdfc6f55f5b03185ebaec997588ff25b4`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 03 Apr 2021 00:53:06 GMT
ADD file:27277aee655dd263ee698d1f2fe17f0b1dbba740615bcac8642723a6ac0d62be in / 
# Sat, 03 Apr 2021 00:53:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 03 Apr 2021 00:53:08 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Sat, 03 Apr 2021 00:53:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 03 Apr 2021 00:53:09 GMT
CMD ["/bin/bash"]
# Sat, 03 Apr 2021 01:29:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 03 Apr 2021 01:29:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 03 Apr 2021 01:32:52 GMT
ENV JAVA_VERSION=jdk-11.0.10+9_openj9-0.24.0
# Mon, 19 Apr 2021 18:22:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='5d2b2939637f999a1910d5cc0fb3d96756125941e5f8b9e3003635aa863664b5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        s390x)          ESUM='2ff9f50d6ffc345434703c43a1d67ac6d3d054b5d4925b4b73a3ce51b02940e5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7e5f97071f8b86c22c36ddfd7f821c3e8ec531c1128e2e6c931b2e64118a517a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 19 Apr 2021 18:22:34 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Apr 2021 18:22:34 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 19 Apr 2021 18:23:10 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 22 Apr 2021 21:40:48 GMT
ARG VERBOSE=false
# Thu, 22 Apr 2021 21:40:48 GMT
ARG OPENJ9_SCC=true
# Thu, 22 Apr 2021 21:48:33 GMT
ARG EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f
# Thu, 22 Apr 2021 21:48:34 GMT
ARG NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8
# Thu, 22 Apr 2021 21:48:34 GMT
ARG NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075
# Thu, 22 Apr 2021 21:48:34 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.3 org.opencontainers.image.revision=cl210320210309-1101 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 22 Apr 2021 21:48:34 GMT
ENV LIBERTY_VERSION=21.0.0_03
# Thu, 22 Apr 2021 21:48:34 GMT
ARG LIBERTY_URL
# Thu, 22 Apr 2021 21:48:34 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 22 Apr 2021 21:48:42 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Apr 2021 21:48:42 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Apr 2021 21:48:42 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.3 BuildLabel=cl210320210309-1101
# Thu, 22 Apr 2021 21:48:43 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 22 Apr 2021 21:48:44 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Apr 2021 21:48:44 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Thu, 22 Apr 2021 21:48:44 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Apr 2021 21:48:45 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Apr 2021 21:48:53 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Apr 2021 21:48:53 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 22 Apr 2021 21:48:53 GMT
USER 1001
# Thu, 22 Apr 2021 21:48:53 GMT
EXPOSE 9080 9443
# Thu, 22 Apr 2021 21:48:53 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Apr 2021 21:48:54 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 22 Apr 2021 21:49:01 GMT
ARG VERBOSE=false
# Thu, 22 Apr 2021 21:49:01 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 22 Apr 2021 21:51:53 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Thu, 22 Apr 2021 21:51:54 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 22 Apr 2021 21:52:28 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:a70d879fa5984474288d52009479054b8bb2993de2a1859f43b5480600cecb24`  
		Last Modified: Thu, 01 Apr 2021 15:20:06 GMT  
		Size: 28.6 MB (28569016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4394a92d1f8760cf7d17fee0bcee732c94c5b858dd8d19c7ff02beecf3b4e83`  
		Last Modified: Sat, 03 Apr 2021 00:54:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e6159c56c084c858f5de2416454ac0a49ddda47b764e4379c5d5a147c9bf5f`  
		Last Modified: Sat, 03 Apr 2021 00:54:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04b772c31f76720583412a2507c5c53889985db45169a85f0d3cd7f842e041a`  
		Last Modified: Sat, 03 Apr 2021 01:39:30 GMT  
		Size: 16.0 MB (16032891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf71362343a962febc8c6ce8c4fd12d961c5712407993471f60ac0e5d43415e`  
		Last Modified: Mon, 19 Apr 2021 18:30:17 GMT  
		Size: 42.4 MB (42440313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9163852ff25e45c3b95c7b759a719b91afa29724136e68d1cf7f822c034c4df`  
		Last Modified: Mon, 19 Apr 2021 18:30:04 GMT  
		Size: 4.0 MB (4025359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27124d51bbcd34a7b9c5ca77307857ac8826a5df7ce13344b52d08235bba7934`  
		Last Modified: Thu, 22 Apr 2021 21:58:30 GMT  
		Size: 14.1 MB (14086702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66b15db611395228cd150cf79924843344bd047b6c5692257ac61c370fb78bb`  
		Last Modified: Thu, 22 Apr 2021 21:58:27 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f642892e4176b386da852ba7c8ca979b999d1d646d4b70d97c47b14748f74cb`  
		Last Modified: Thu, 22 Apr 2021 21:58:26 GMT  
		Size: 9.6 KB (9552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aca56f0e23052c96ef1a40fdadf3c7745e6a10b4a886dd1b56043e2ef85fec8`  
		Last Modified: Thu, 22 Apr 2021 21:58:26 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626b91e4928db98bd94286caa519f81552ea1f50b114fd2ab51d9c483e9f1623`  
		Last Modified: Thu, 22 Apr 2021 21:58:26 GMT  
		Size: 10.5 KB (10538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18d0b3c58eef5da06cf3322879d39897408847806b395cfd01b8f80a705a723`  
		Last Modified: Thu, 22 Apr 2021 21:58:26 GMT  
		Size: 2.5 MB (2502138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce80311ac261dcb41a0304bd9d8d10c3b99c9d5435fc94894a877f605341855`  
		Last Modified: Thu, 22 Apr 2021 21:58:52 GMT  
		Size: 207.2 MB (207198736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8675b05603d8b247f99cff034e07c405dbd0a2e12f2a0c1f95393d906c226b12`  
		Last Modified: Thu, 22 Apr 2021 21:58:38 GMT  
		Size: 943.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb3af4c9512944dad516500de58fe33876c3610552cb4a71a42db58bfaff644`  
		Last Modified: Thu, 22 Apr 2021 21:58:41 GMT  
		Size: 14.3 MB (14267694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.3-full-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:a334927897c779225dba945f824c3c008673d66e98a64d700e1f7b976412d848
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.9 MB (333854612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b52931da68f9a8ba20288f348d8748fa1f5df4a12c3e19e0cf773d97a0950b7`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:16:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 24 Apr 2021 01:19:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:28:36 GMT
ENV JAVA_VERSION=jdk-11.0.10+9_openj9-0.24.0
# Sat, 24 Apr 2021 01:30:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='5d2b2939637f999a1910d5cc0fb3d96756125941e5f8b9e3003635aa863664b5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        s390x)          ESUM='2ff9f50d6ffc345434703c43a1d67ac6d3d054b5d4925b4b73a3ce51b02940e5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7e5f97071f8b86c22c36ddfd7f821c3e8ec531c1128e2e6c931b2e64118a517a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 24 Apr 2021 01:30:48 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 24 Apr 2021 01:30:53 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Sat, 24 Apr 2021 01:31:37 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Sat, 24 Apr 2021 03:09:49 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 03:09:52 GMT
ARG OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:27:49 GMT
ARG EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f
# Sat, 24 Apr 2021 03:27:54 GMT
ARG NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8
# Sat, 24 Apr 2021 03:27:57 GMT
ARG NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075
# Sat, 24 Apr 2021 03:28:02 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.3 org.opencontainers.image.revision=cl210320210309-1101 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Sat, 24 Apr 2021 03:28:07 GMT
ENV LIBERTY_VERSION=21.0.0_03
# Sat, 24 Apr 2021 03:28:11 GMT
ARG LIBERTY_URL
# Sat, 24 Apr 2021 03:28:13 GMT
ARG DOWNLOAD_OPTIONS=
# Sat, 24 Apr 2021 03:28:53 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 03:28:58 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 24 Apr 2021 03:29:02 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.3 BuildLabel=cl210320210309-1101
# Sat, 24 Apr 2021 03:29:07 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:29:16 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Sat, 24 Apr 2021 03:29:17 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Sat, 24 Apr 2021 03:29:18 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Sat, 24 Apr 2021 03:29:31 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Sat, 24 Apr 2021 03:29:51 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Sat, 24 Apr 2021 03:29:54 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Sat, 24 Apr 2021 03:29:56 GMT
USER 1001
# Sat, 24 Apr 2021 03:30:01 GMT
EXPOSE 9080 9443
# Sat, 24 Apr 2021 03:30:06 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Sat, 24 Apr 2021 03:30:11 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Sat, 24 Apr 2021 03:35:59 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 03:36:02 GMT
ARG REPOSITORIES_PROPERTIES=
# Sat, 24 Apr 2021 03:39:20 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Sat, 24 Apr 2021 03:39:35 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Sat, 24 Apr 2021 03:40:34 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da07529aeac8fe5c90c5bb8c4f516c9d6fd248cc1daa5fecd137c809bce39bb6`  
		Last Modified: Sat, 24 Apr 2021 01:40:58 GMT  
		Size: 17.2 MB (17209103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53f9612e78ec5df6fbbbab4098deb40150ceef63be58aec6c2dd4df6af9f634`  
		Last Modified: Sat, 24 Apr 2021 01:46:21 GMT  
		Size: 43.3 MB (43277570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec133c54d62c9541f8b987c7353d67bd5d58ea39050f8cd947bf150d5ce8bb7a`  
		Last Modified: Sat, 24 Apr 2021 01:46:15 GMT  
		Size: 3.3 MB (3289250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe1eca1711268c3ebb66b11ccecc7f8139d17df782d1bb9f888b9446636567c`  
		Last Modified: Sat, 24 Apr 2021 03:59:26 GMT  
		Size: 14.1 MB (14087998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692696f6f89667bb21e2e255737c8ca3b49f4a0345897ce817812793b056be65`  
		Last Modified: Sat, 24 Apr 2021 03:59:22 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51cd3682323985f658899f90475eea4aad600131abbfbe700724cd047a1310bb`  
		Last Modified: Sat, 24 Apr 2021 03:59:22 GMT  
		Size: 9.6 KB (9552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4180195fec5952068c43e145c7a7d1c7d83bce6cd3b88bc275cfc7f06563d5fe`  
		Last Modified: Sat, 24 Apr 2021 03:59:22 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f9e516179d708b4986d3b8d632841814f9101a04e2096ed39bfdc72070f23a`  
		Last Modified: Sat, 24 Apr 2021 03:59:22 GMT  
		Size: 10.5 KB (10538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d120b9f44a36570563ad6172c7aff79a3fba5521ab9c78f1ae07b76d58f8fbc`  
		Last Modified: Sat, 24 Apr 2021 03:59:23 GMT  
		Size: 2.4 MB (2438743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fd2962792f12ce87b4436bb7c5099250ba596b81aa485c6d5f9dc9f2f1442d`  
		Last Modified: Sat, 24 Apr 2021 04:00:24 GMT  
		Size: 207.2 MB (207198480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be1bb6201fa0d9b8358ed7f5bf22e9c119ff2abb47f69335c5782ccc3fa81c31`  
		Last Modified: Sat, 24 Apr 2021 04:00:07 GMT  
		Size: 945.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a433422f420bae20ecb71b0d6f530e1937b57e5db09ec272fd1c2287edbf539`  
		Last Modified: Sat, 24 Apr 2021 04:00:08 GMT  
		Size: 13.1 MB (13075049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.3-full-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:94e3bd056686fd88e274f1d0866bf9fa1ea394166f5471d5539f64922e42f0b3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.1 MB (326083570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35a6985d189c29379befcdd8b0c2f1806ffdbd5fbb6037931a26c4dea10f053`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 21:45:20 GMT
ADD file:282d950116f923276efabd13c7dc17b942821edb14ffac4b89b9a50bcdf99e17 in / 
# Fri, 23 Apr 2021 21:45:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 21:45:27 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 21:45:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 21:45:29 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 22:03:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Apr 2021 22:04:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:10:11 GMT
ENV JAVA_VERSION=jdk-11.0.10+9_openj9-0.24.0
# Fri, 23 Apr 2021 22:11:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='5d2b2939637f999a1910d5cc0fb3d96756125941e5f8b9e3003635aa863664b5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        s390x)          ESUM='2ff9f50d6ffc345434703c43a1d67ac6d3d054b5d4925b4b73a3ce51b02940e5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7e5f97071f8b86c22c36ddfd7f821c3e8ec531c1128e2e6c931b2e64118a517a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 23 Apr 2021 22:11:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Apr 2021 22:11:44 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 23 Apr 2021 22:12:20 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 23 Apr 2021 23:17:55 GMT
ARG VERBOSE=false
# Fri, 23 Apr 2021 23:17:56 GMT
ARG OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:30:46 GMT
ARG EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f
# Fri, 23 Apr 2021 23:30:46 GMT
ARG NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8
# Fri, 23 Apr 2021 23:30:47 GMT
ARG NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075
# Fri, 23 Apr 2021 23:30:48 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.3 org.opencontainers.image.revision=cl210320210309-1101 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 23 Apr 2021 23:30:48 GMT
ENV LIBERTY_VERSION=21.0.0_03
# Fri, 23 Apr 2021 23:30:49 GMT
ARG LIBERTY_URL
# Fri, 23 Apr 2021 23:30:50 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 23 Apr 2021 23:31:05 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:31:07 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Apr 2021 23:31:07 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.3 BuildLabel=cl210320210309-1101
# Fri, 23 Apr 2021 23:31:08 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:31:10 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 23 Apr 2021 23:31:10 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Fri, 23 Apr 2021 23:31:11 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 23 Apr 2021 23:31:14 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 23 Apr 2021 23:31:26 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 23 Apr 2021 23:31:27 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 23 Apr 2021 23:31:28 GMT
USER 1001
# Fri, 23 Apr 2021 23:31:28 GMT
EXPOSE 9080 9443
# Fri, 23 Apr 2021 23:31:29 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 23 Apr 2021 23:31:29 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 23 Apr 2021 23:36:50 GMT
ARG VERBOSE=false
# Fri, 23 Apr 2021 23:36:50 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 23 Apr 2021 23:40:47 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Fri, 23 Apr 2021 23:40:59 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 23 Apr 2021 23:41:41 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:de53239ada2db01e7972c3f6eddcf6729f7cf3102be78e0b41363125ce7c2425`  
		Last Modified: Fri, 23 Apr 2021 21:47:14 GMT  
		Size: 27.1 MB (27136362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12932016d0f51acb5c5e5ba5b420a369401a7df47a219f24680bbc05ffde7e11`  
		Last Modified: Fri, 23 Apr 2021 21:47:10 GMT  
		Size: 840.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46997f76c5876e3274170b667463b3d88475cd696ccbc735d2f63965668673ad`  
		Last Modified: Fri, 23 Apr 2021 21:47:10 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bab416938acf6dd045c9fc9097e5768c61b5899b07d110ab3844f447e12b113`  
		Last Modified: Fri, 23 Apr 2021 22:19:05 GMT  
		Size: 15.7 MB (15741779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0273d3bc7cd55960a36b00d19e8d51f8bbeed03d24fd8d551c957fc19ef079b`  
		Last Modified: Fri, 23 Apr 2021 22:22:19 GMT  
		Size: 42.0 MB (41951613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95422aa686364d2877a279281f6eb1157805fa8516aa976b06ce8889dc9f932`  
		Last Modified: Fri, 23 Apr 2021 22:22:13 GMT  
		Size: 3.8 MB (3836026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f4fac1a8aceea217c7fe53bbfc322b60fbc9aa714e55650ace47a05de81069`  
		Last Modified: Fri, 23 Apr 2021 23:54:57 GMT  
		Size: 14.1 MB (14087190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756fea3647fb5e2b8750dbb5e4c2fcf03f89f52b7e5cb55b7606924b2389ca81`  
		Last Modified: Fri, 23 Apr 2021 23:54:54 GMT  
		Size: 691.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8fa9033e59f89cbb013c7d832613bab3a656300357cc70b7eade006a8edefce`  
		Last Modified: Fri, 23 Apr 2021 23:54:54 GMT  
		Size: 9.6 KB (9554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f62d4b9f7c9f91f8d9c689ebf626986dd4c2efd6d86ff851bd15bc6183dded0`  
		Last Modified: Fri, 23 Apr 2021 23:54:54 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491f6056574f25428a41b45fd180908c3bcb491ed462310db1dda218415df01c`  
		Last Modified: Fri, 23 Apr 2021 23:54:54 GMT  
		Size: 10.5 KB (10537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df697bb1f00968be2197f2465a5306f2873b7d22664eeb96b49f2a15ce43654d`  
		Last Modified: Fri, 23 Apr 2021 23:54:54 GMT  
		Size: 2.5 MB (2489469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59753a091e4624a995faf14a9f9ff0afcb986c686a48635b1697d46125128b14`  
		Last Modified: Fri, 23 Apr 2021 23:55:42 GMT  
		Size: 207.2 MB (207198908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d5f5c0b23fd673685a77862a45ffd6f44f6f97f9d801c7938c09aa77a3c6b7`  
		Last Modified: Fri, 23 Apr 2021 23:55:29 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7a099266c968226b8409c4aa7536ccc7546b900ff860ebef4cb27010323e18`  
		Last Modified: Fri, 23 Apr 2021 23:55:30 GMT  
		Size: 13.6 MB (13619199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:21.0.0.3-full-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:fe54deeaf018a2806129d3b10b583b4ab8b64b40e2e18f81322b80fc7c0f6e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:21.0.0.3-full-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:18902eb4619a6c3c50377fd1d4efaa9a4b9d3ec75ff475b1195e60b2b50d2d5c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.5 MB (414462047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f29f7bd268928d680dcec8c1ad8666555fcb0ab86c3812f8b5f0765cdf6c8d`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 09:30:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 26 Mar 2021 09:31:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 09:31:04 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 26 Mar 2021 09:31:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Mar 2021 09:31:42 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 26 Mar 2021 21:31:17 GMT
ARG VERBOSE=false
# Fri, 26 Mar 2021 21:31:18 GMT
ARG OPENJ9_SCC=true
# Fri, 26 Mar 2021 21:31:18 GMT
ARG EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f
# Fri, 26 Mar 2021 21:31:18 GMT
ARG NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8
# Fri, 26 Mar 2021 21:31:18 GMT
ARG NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075
# Fri, 26 Mar 2021 21:31:18 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.3 org.opencontainers.image.revision=cl210320210309-1101 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 26 Mar 2021 21:31:19 GMT
ENV LIBERTY_VERSION=21.0.0_03
# Fri, 26 Mar 2021 21:31:19 GMT
ARG LIBERTY_URL
# Fri, 26 Mar 2021 21:31:19 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 26 Mar 2021 21:31:33 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 21:31:33 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Mar 2021 21:31:33 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.3 BuildLabel=cl210320210309-1101
# Fri, 26 Mar 2021 21:31:33 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 26 Mar 2021 21:31:35 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 26 Mar 2021 21:31:35 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Fri, 26 Mar 2021 21:31:35 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 26 Mar 2021 21:31:37 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 26 Mar 2021 21:31:48 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 26 Mar 2021 21:31:49 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Fri, 26 Mar 2021 21:31:49 GMT
USER 1001
# Fri, 26 Mar 2021 21:31:49 GMT
EXPOSE 9080 9443
# Fri, 26 Mar 2021 21:31:49 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 26 Mar 2021 21:31:49 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 26 Mar 2021 21:32:29 GMT
ARG VERBOSE=false
# Fri, 26 Mar 2021 21:32:30 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 26 Mar 2021 21:35:38 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Fri, 26 Mar 2021 21:35:39 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 26 Mar 2021 21:36:24 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4764ed71d2900c9874838108e377eb8821088502d5504fadeb080e5dd1a3e65d`  
		Last Modified: Fri, 26 Mar 2021 09:35:47 GMT  
		Size: 3.0 MB (2958415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf5000c541da177b7cfe59bf3ff8cb271529f443ee224bf88989910e9a2abb1`  
		Last Modified: Fri, 26 Mar 2021 09:36:01 GMT  
		Size: 130.8 MB (130805802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f62ff9f46b7fe8abf21ca3992ddfdba43c9a869ab05da497fd0c961b82bcc8`  
		Last Modified: Fri, 26 Mar 2021 21:49:10 GMT  
		Size: 14.0 MB (13988287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade44e6f5f910e4171dbe956b6f82444a1a0cf77cbb628a3cd3a4e02b91e4a75`  
		Last Modified: Fri, 26 Mar 2021 21:49:06 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e194224da53e4dca0cfb2e746e2dc2780faf558e27fbea8a051bbb1e645412a`  
		Last Modified: Fri, 26 Mar 2021 21:49:05 GMT  
		Size: 9.6 KB (9555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee645bef2bf69d54e107e8f571dd29a3a04a4bc4b3dc86db1e83a1cc15f0be9`  
		Last Modified: Fri, 26 Mar 2021 21:49:05 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7592107637fd3c10cd009e854a974a81b2a2bb14bbfc045924a369d59d3098`  
		Last Modified: Fri, 26 Mar 2021 21:49:05 GMT  
		Size: 10.5 KB (10545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11fedbbde6cf647ecb2604ada8a232f0040986bc0bab990ba49c28482ddc35f4`  
		Last Modified: Fri, 26 Mar 2021 21:49:07 GMT  
		Size: 5.7 MB (5661783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c44f60c1c5e6897a6c8ab173b4552e16708e2bbf180aab829a6e2045fdd2206`  
		Last Modified: Fri, 26 Mar 2021 21:49:44 GMT  
		Size: 212.8 MB (212822107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1023c04b596fcb951bc35f6638adf41d8ba07d1252a26495c71f95cfd17878`  
		Last Modified: Fri, 26 Mar 2021 21:49:30 GMT  
		Size: 947.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4831ae3a88bfff0d766ba60d4f176b42097c5b1d0821d32427611ff49389f89`  
		Last Modified: Fri, 26 Mar 2021 21:49:34 GMT  
		Size: 21.5 MB (21491809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.3-full-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:e7cc1beaf45ca555931fbd4071d18e7696f70d896672dd12456f1e518c703290
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.6 MB (414628193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1242d258b0247306e10a663b7819d4439f9229da3525a1c765294640f3f2679`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 22:30:25 GMT
ADD file:818f810cd30ef74fd4690c6265d80265647ba3353880cf8323500df6d2c48b69 in / 
# Fri, 23 Apr 2021 22:30:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:31:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:31:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:31:32 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:16:58 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 23 Apr 2021 23:17:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:17:43 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 23 Apr 2021 23:18:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 23 Apr 2021 23:19:03 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Sat, 24 Apr 2021 03:07:07 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 03:07:12 GMT
ARG OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:24:41 GMT
ARG EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f
# Sat, 24 Apr 2021 03:24:46 GMT
ARG NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8
# Sat, 24 Apr 2021 03:24:50 GMT
ARG NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075
# Sat, 24 Apr 2021 03:24:56 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.3 org.opencontainers.image.revision=cl210320210309-1101 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Sat, 24 Apr 2021 03:24:59 GMT
ENV LIBERTY_VERSION=21.0.0_03
# Sat, 24 Apr 2021 03:25:02 GMT
ARG LIBERTY_URL
# Sat, 24 Apr 2021 03:25:03 GMT
ARG DOWNLOAD_OPTIONS=
# Sat, 24 Apr 2021 03:25:46 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 03:25:51 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 24 Apr 2021 03:26:00 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.3 BuildLabel=cl210320210309-1101
# Sat, 24 Apr 2021 03:26:05 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:26:29 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Sat, 24 Apr 2021 03:26:30 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Sat, 24 Apr 2021 03:26:32 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Sat, 24 Apr 2021 03:26:48 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Sat, 24 Apr 2021 03:27:19 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Sat, 24 Apr 2021 03:27:25 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Sat, 24 Apr 2021 03:27:28 GMT
USER 1001
# Sat, 24 Apr 2021 03:27:34 GMT
EXPOSE 9080 9443
# Sat, 24 Apr 2021 03:27:39 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Sat, 24 Apr 2021 03:27:42 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Sat, 24 Apr 2021 03:30:34 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 03:30:38 GMT
ARG REPOSITORIES_PROPERTIES=
# Sat, 24 Apr 2021 03:34:26 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Sat, 24 Apr 2021 03:34:36 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Sat, 24 Apr 2021 03:35:46 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:bb3095714506c08a64a49e29ab001d7000d94957d52e05db35361fd4a54c460c`  
		Last Modified: Fri, 23 Apr 2021 22:36:52 GMT  
		Size: 30.4 MB (30407300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd29acc6f7bfef8034eaca0bfb069f0d66e50351c84b062e224d6eae710afa79`  
		Last Modified: Fri, 23 Apr 2021 22:36:46 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7645fc50c9e70df51732b36ef7f8b21ebacd148c3bee4f1b29ca6dcba1bbb949`  
		Last Modified: Fri, 23 Apr 2021 22:36:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab6dc42492fe0eca98f1e563f3e8dabb70f122b45b752264bacb4ea14f59354`  
		Last Modified: Fri, 23 Apr 2021 23:22:26 GMT  
		Size: 3.1 MB (3082775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510992b332e039a7852bef411702a4b667a17ae9ef201c9118477ccc53172fa8`  
		Last Modified: Fri, 23 Apr 2021 23:22:40 GMT  
		Size: 130.4 MB (130406625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd31b308db951c2fb01269a9a47650d67aaae73f5c6391a9e67f4921c403ba57`  
		Last Modified: Sat, 24 Apr 2021 03:59:14 GMT  
		Size: 14.0 MB (13989164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c2633c82a8a8e5896d9c9a12bc8523f99077e522a939a3c059e50497336f01`  
		Last Modified: Sat, 24 Apr 2021 03:59:09 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e942e16565d6f821eebf25a9305f3c221094a1070938264d7d26d2cf1519c8df`  
		Last Modified: Sat, 24 Apr 2021 03:59:09 GMT  
		Size: 9.6 KB (9553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172808243e1a52ecbdd1265e24f73e00a81bb41124082378f10ad90ab850598b`  
		Last Modified: Sat, 24 Apr 2021 03:59:09 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d017355bc45360b9c74a42eff93dd089db63c696cdea8222f3d6c4c78e5c073`  
		Last Modified: Sat, 24 Apr 2021 03:59:09 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf6a0067da138767867fa18d60edb2ba9c2b106b3d78329d1ee3c76b65d04d2`  
		Last Modified: Sat, 24 Apr 2021 03:59:10 GMT  
		Size: 5.3 MB (5253005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ad83ddd5df2486140bcd140b9ec52e4249428686bc9a5c265a01e43aa37dfb`  
		Last Modified: Sat, 24 Apr 2021 03:59:56 GMT  
		Size: 212.4 MB (212413876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63cca15cf2c1d62b42cd3d6e99ddf436d28492e7e46192b300aaeb77c2ad122`  
		Last Modified: Sat, 24 Apr 2021 03:59:34 GMT  
		Size: 951.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0203c6ceb4e0f4429d4310921f52bd86b3972671d775a66feae98accb8a7c971`  
		Last Modified: Sat, 24 Apr 2021 03:59:39 GMT  
		Size: 19.1 MB (19052388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.3-full-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:ec03093309c98603a416d3ecb6845f4d54dddb5208ca14a9e3ddc233f8960e77
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.7 MB (410660108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a055c4d5a8b3680d7928b4c804e24d859318e386ac4ec10fe03fc3d124a7f53`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 21:45:00 GMT
ADD file:5e61a5300d520d61a2130623465ba2e46da8e80dc2afa042473a42cbcd8d88d2 in / 
# Fri, 23 Apr 2021 21:45:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 21:45:05 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 21:45:07 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 21:45:07 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 22:25:02 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 23 Apr 2021 22:25:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:25:17 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 23 Apr 2021 22:26:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 23 Apr 2021 22:26:15 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 23 Apr 2021 23:16:58 GMT
ARG VERBOSE=false
# Fri, 23 Apr 2021 23:16:58 GMT
ARG OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:29:48 GMT
ARG EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f
# Fri, 23 Apr 2021 23:29:49 GMT
ARG NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8
# Fri, 23 Apr 2021 23:29:50 GMT
ARG NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075
# Fri, 23 Apr 2021 23:29:50 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.3 org.opencontainers.image.revision=cl210320210309-1101 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 23 Apr 2021 23:29:51 GMT
ENV LIBERTY_VERSION=21.0.0_03
# Fri, 23 Apr 2021 23:29:52 GMT
ARG LIBERTY_URL
# Fri, 23 Apr 2021 23:29:52 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 23 Apr 2021 23:30:08 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:30:10 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Apr 2021 23:30:11 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.3 BuildLabel=cl210320210309-1101
# Fri, 23 Apr 2021 23:30:11 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:30:14 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 23 Apr 2021 23:30:15 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Fri, 23 Apr 2021 23:30:15 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 23 Apr 2021 23:30:17 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 23 Apr 2021 23:30:31 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 23 Apr 2021 23:30:32 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Fri, 23 Apr 2021 23:30:33 GMT
USER 1001
# Fri, 23 Apr 2021 23:30:33 GMT
EXPOSE 9080 9443
# Fri, 23 Apr 2021 23:30:34 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 23 Apr 2021 23:30:34 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 23 Apr 2021 23:31:42 GMT
ARG VERBOSE=false
# Fri, 23 Apr 2021 23:31:43 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 23 Apr 2021 23:35:45 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Fri, 23 Apr 2021 23:36:01 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 23 Apr 2021 23:36:42 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:33ddddc4572ffe1f294f9f599ed989cc41eee5da4cdcf7db12d10700aa8c894e`  
		Last Modified: Fri, 23 Apr 2021 21:47:03 GMT  
		Size: 25.4 MB (25352756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4395f372a786db91b2f50dc8e43d8b7c3533eb4bd86f6728eb2a0c7108c077d2`  
		Last Modified: Fri, 23 Apr 2021 21:46:59 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e39753730df188282ca8193f14bbbb8cbe0b76ec02b34283a28449b1e41c05`  
		Last Modified: Fri, 23 Apr 2021 21:47:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e93b87da546ac7aa6705cd2f20bfe70cf04793ac73561e5dd8c579af88754aec`  
		Last Modified: Fri, 23 Apr 2021 22:28:41 GMT  
		Size: 2.7 MB (2676643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268462fc02d2bd9da227784f5f243759923a14cefb3648739ca02e8fa7d63ee7`  
		Last Modified: Fri, 23 Apr 2021 22:28:50 GMT  
		Size: 128.1 MB (128065984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2e27878ce60350be68bbdb3b8ee9cbfde9b111787d0b974a06b8dffadddcbd`  
		Last Modified: Fri, 23 Apr 2021 23:54:49 GMT  
		Size: 14.0 MB (13988524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c894cb19fa986a022ad70870257b92d2c0c4fb51aabb232cd0284dacada85fe2`  
		Last Modified: Fri, 23 Apr 2021 23:54:46 GMT  
		Size: 695.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08d76891a169b900915649827dc512feb56f753883fe52981be6f04d736b2f6`  
		Last Modified: Fri, 23 Apr 2021 23:54:46 GMT  
		Size: 9.6 KB (9557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34ee5d8f9435c0ed35bd9d1b5ae402ce58f34113d03dd5a315a826c6cd83b36`  
		Last Modified: Fri, 23 Apr 2021 23:54:46 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d300d3fb2439110af45d80a2ddbf132b397feb71fefce3d1f0a596b771fdb90c`  
		Last Modified: Fri, 23 Apr 2021 23:54:47 GMT  
		Size: 10.5 KB (10543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a38e178e857d2811edcaca15881bfc7721e5afa49da3e0557037dfec12a23f`  
		Last Modified: Fri, 23 Apr 2021 23:54:47 GMT  
		Size: 5.8 MB (5848991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b424a8ac9b26bcdac2c714b92bad760cf44182a95956269fb3f0a873be87e547`  
		Last Modified: Fri, 23 Apr 2021 23:55:15 GMT  
		Size: 213.0 MB (213010696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6d93757514d2ad41bbfdd187dc542cb9353de5290ab8d5acda3d7e85435fca`  
		Last Modified: Fri, 23 Apr 2021 23:55:02 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd4875bb40fed31bff06329f774ad259835e6b45dc6c967fed0cdcd164fab27`  
		Last Modified: Fri, 23 Apr 2021 23:55:04 GMT  
		Size: 21.7 MB (21693461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:21.0.0.3-kernel-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:531c91d8c260e5ed0341729405966978b88de8d10329352d12e405d0ff01936f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:21.0.0.3-kernel-java11-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:fc39abe3376b11a33b27b0ea6a93bb4dfa82b2a8c22b61d16b102fd91a396fd8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.7 MB (107678507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd0e8588bf66acce2efe2ec9d8f46bf79a8162e5e496d58646fc734d7763d85`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 03 Apr 2021 00:53:06 GMT
ADD file:27277aee655dd263ee698d1f2fe17f0b1dbba740615bcac8642723a6ac0d62be in / 
# Sat, 03 Apr 2021 00:53:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 03 Apr 2021 00:53:08 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Sat, 03 Apr 2021 00:53:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 03 Apr 2021 00:53:09 GMT
CMD ["/bin/bash"]
# Sat, 03 Apr 2021 01:29:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 03 Apr 2021 01:29:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 03 Apr 2021 01:32:52 GMT
ENV JAVA_VERSION=jdk-11.0.10+9_openj9-0.24.0
# Mon, 19 Apr 2021 18:22:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='5d2b2939637f999a1910d5cc0fb3d96756125941e5f8b9e3003635aa863664b5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        s390x)          ESUM='2ff9f50d6ffc345434703c43a1d67ac6d3d054b5d4925b4b73a3ce51b02940e5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7e5f97071f8b86c22c36ddfd7f821c3e8ec531c1128e2e6c931b2e64118a517a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 19 Apr 2021 18:22:34 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Apr 2021 18:22:34 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 19 Apr 2021 18:23:10 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 22 Apr 2021 21:40:48 GMT
ARG VERBOSE=false
# Thu, 22 Apr 2021 21:40:48 GMT
ARG OPENJ9_SCC=true
# Thu, 22 Apr 2021 21:48:33 GMT
ARG EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f
# Thu, 22 Apr 2021 21:48:34 GMT
ARG NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8
# Thu, 22 Apr 2021 21:48:34 GMT
ARG NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075
# Thu, 22 Apr 2021 21:48:34 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.3 org.opencontainers.image.revision=cl210320210309-1101 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 22 Apr 2021 21:48:34 GMT
ENV LIBERTY_VERSION=21.0.0_03
# Thu, 22 Apr 2021 21:48:34 GMT
ARG LIBERTY_URL
# Thu, 22 Apr 2021 21:48:34 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 22 Apr 2021 21:48:42 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Apr 2021 21:48:42 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Apr 2021 21:48:42 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.3 BuildLabel=cl210320210309-1101
# Thu, 22 Apr 2021 21:48:43 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 22 Apr 2021 21:48:44 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Apr 2021 21:48:44 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Thu, 22 Apr 2021 21:48:44 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Apr 2021 21:48:45 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Apr 2021 21:48:53 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Apr 2021 21:48:53 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 22 Apr 2021 21:48:53 GMT
USER 1001
# Thu, 22 Apr 2021 21:48:53 GMT
EXPOSE 9080 9443
# Thu, 22 Apr 2021 21:48:53 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Apr 2021 21:48:54 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:a70d879fa5984474288d52009479054b8bb2993de2a1859f43b5480600cecb24`  
		Last Modified: Thu, 01 Apr 2021 15:20:06 GMT  
		Size: 28.6 MB (28569016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4394a92d1f8760cf7d17fee0bcee732c94c5b858dd8d19c7ff02beecf3b4e83`  
		Last Modified: Sat, 03 Apr 2021 00:54:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e6159c56c084c858f5de2416454ac0a49ddda47b764e4379c5d5a147c9bf5f`  
		Last Modified: Sat, 03 Apr 2021 00:54:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04b772c31f76720583412a2507c5c53889985db45169a85f0d3cd7f842e041a`  
		Last Modified: Sat, 03 Apr 2021 01:39:30 GMT  
		Size: 16.0 MB (16032891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf71362343a962febc8c6ce8c4fd12d961c5712407993471f60ac0e5d43415e`  
		Last Modified: Mon, 19 Apr 2021 18:30:17 GMT  
		Size: 42.4 MB (42440313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9163852ff25e45c3b95c7b759a719b91afa29724136e68d1cf7f822c034c4df`  
		Last Modified: Mon, 19 Apr 2021 18:30:04 GMT  
		Size: 4.0 MB (4025359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27124d51bbcd34a7b9c5ca77307857ac8826a5df7ce13344b52d08235bba7934`  
		Last Modified: Thu, 22 Apr 2021 21:58:30 GMT  
		Size: 14.1 MB (14086702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66b15db611395228cd150cf79924843344bd047b6c5692257ac61c370fb78bb`  
		Last Modified: Thu, 22 Apr 2021 21:58:27 GMT  
		Size: 694.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f642892e4176b386da852ba7c8ca979b999d1d646d4b70d97c47b14748f74cb`  
		Last Modified: Thu, 22 Apr 2021 21:58:26 GMT  
		Size: 9.6 KB (9552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aca56f0e23052c96ef1a40fdadf3c7745e6a10b4a886dd1b56043e2ef85fec8`  
		Last Modified: Thu, 22 Apr 2021 21:58:26 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626b91e4928db98bd94286caa519f81552ea1f50b114fd2ab51d9c483e9f1623`  
		Last Modified: Thu, 22 Apr 2021 21:58:26 GMT  
		Size: 10.5 KB (10538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18d0b3c58eef5da06cf3322879d39897408847806b395cfd01b8f80a705a723`  
		Last Modified: Thu, 22 Apr 2021 21:58:26 GMT  
		Size: 2.5 MB (2502138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.3-kernel-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:c768482246eb322cf8de3635d4daf1a6c2ce07699cebd378ac14bb1e7e7e3239
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.6 MB (113580138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ae5a7b627eeff12df00e6f1f24ce11e1f56aec4ab0658b85dcb4ad967da97c`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:16:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 24 Apr 2021 01:19:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:28:36 GMT
ENV JAVA_VERSION=jdk-11.0.10+9_openj9-0.24.0
# Sat, 24 Apr 2021 01:30:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='5d2b2939637f999a1910d5cc0fb3d96756125941e5f8b9e3003635aa863664b5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        s390x)          ESUM='2ff9f50d6ffc345434703c43a1d67ac6d3d054b5d4925b4b73a3ce51b02940e5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7e5f97071f8b86c22c36ddfd7f821c3e8ec531c1128e2e6c931b2e64118a517a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 24 Apr 2021 01:30:48 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 24 Apr 2021 01:30:53 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Sat, 24 Apr 2021 01:31:37 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Sat, 24 Apr 2021 03:09:49 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 03:09:52 GMT
ARG OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:27:49 GMT
ARG EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f
# Sat, 24 Apr 2021 03:27:54 GMT
ARG NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8
# Sat, 24 Apr 2021 03:27:57 GMT
ARG NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075
# Sat, 24 Apr 2021 03:28:02 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.3 org.opencontainers.image.revision=cl210320210309-1101 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Sat, 24 Apr 2021 03:28:07 GMT
ENV LIBERTY_VERSION=21.0.0_03
# Sat, 24 Apr 2021 03:28:11 GMT
ARG LIBERTY_URL
# Sat, 24 Apr 2021 03:28:13 GMT
ARG DOWNLOAD_OPTIONS=
# Sat, 24 Apr 2021 03:28:53 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 03:28:58 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 24 Apr 2021 03:29:02 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.3 BuildLabel=cl210320210309-1101
# Sat, 24 Apr 2021 03:29:07 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:29:16 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Sat, 24 Apr 2021 03:29:17 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Sat, 24 Apr 2021 03:29:18 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Sat, 24 Apr 2021 03:29:31 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Sat, 24 Apr 2021 03:29:51 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Sat, 24 Apr 2021 03:29:54 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Sat, 24 Apr 2021 03:29:56 GMT
USER 1001
# Sat, 24 Apr 2021 03:30:01 GMT
EXPOSE 9080 9443
# Sat, 24 Apr 2021 03:30:06 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Sat, 24 Apr 2021 03:30:11 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da07529aeac8fe5c90c5bb8c4f516c9d6fd248cc1daa5fecd137c809bce39bb6`  
		Last Modified: Sat, 24 Apr 2021 01:40:58 GMT  
		Size: 17.2 MB (17209103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53f9612e78ec5df6fbbbab4098deb40150ceef63be58aec6c2dd4df6af9f634`  
		Last Modified: Sat, 24 Apr 2021 01:46:21 GMT  
		Size: 43.3 MB (43277570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec133c54d62c9541f8b987c7353d67bd5d58ea39050f8cd947bf150d5ce8bb7a`  
		Last Modified: Sat, 24 Apr 2021 01:46:15 GMT  
		Size: 3.3 MB (3289250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe1eca1711268c3ebb66b11ccecc7f8139d17df782d1bb9f888b9446636567c`  
		Last Modified: Sat, 24 Apr 2021 03:59:26 GMT  
		Size: 14.1 MB (14087998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692696f6f89667bb21e2e255737c8ca3b49f4a0345897ce817812793b056be65`  
		Last Modified: Sat, 24 Apr 2021 03:59:22 GMT  
		Size: 689.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51cd3682323985f658899f90475eea4aad600131abbfbe700724cd047a1310bb`  
		Last Modified: Sat, 24 Apr 2021 03:59:22 GMT  
		Size: 9.6 KB (9552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4180195fec5952068c43e145c7a7d1c7d83bce6cd3b88bc275cfc7f06563d5fe`  
		Last Modified: Sat, 24 Apr 2021 03:59:22 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f9e516179d708b4986d3b8d632841814f9101a04e2096ed39bfdc72070f23a`  
		Last Modified: Sat, 24 Apr 2021 03:59:22 GMT  
		Size: 10.5 KB (10538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d120b9f44a36570563ad6172c7aff79a3fba5521ab9c78f1ae07b76d58f8fbc`  
		Last Modified: Sat, 24 Apr 2021 03:59:23 GMT  
		Size: 2.4 MB (2438743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.3-kernel-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:0737828b881ffc978313a472df0f167f3230bb616aff887d83285b9835144491
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105264517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b35f835c2859721d78c892a578760dbc2d0d1175ddf1420085542b3855ce38e1`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 21:45:20 GMT
ADD file:282d950116f923276efabd13c7dc17b942821edb14ffac4b89b9a50bcdf99e17 in / 
# Fri, 23 Apr 2021 21:45:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 21:45:27 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 21:45:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 21:45:29 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 22:03:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Apr 2021 22:04:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:10:11 GMT
ENV JAVA_VERSION=jdk-11.0.10+9_openj9-0.24.0
# Fri, 23 Apr 2021 22:11:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='5d2b2939637f999a1910d5cc0fb3d96756125941e5f8b9e3003635aa863664b5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        s390x)          ESUM='2ff9f50d6ffc345434703c43a1d67ac6d3d054b5d4925b4b73a3ce51b02940e5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7e5f97071f8b86c22c36ddfd7f821c3e8ec531c1128e2e6c931b2e64118a517a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 23 Apr 2021 22:11:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Apr 2021 22:11:44 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 23 Apr 2021 22:12:20 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 23 Apr 2021 23:17:55 GMT
ARG VERBOSE=false
# Fri, 23 Apr 2021 23:17:56 GMT
ARG OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:30:46 GMT
ARG EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f
# Fri, 23 Apr 2021 23:30:46 GMT
ARG NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8
# Fri, 23 Apr 2021 23:30:47 GMT
ARG NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075
# Fri, 23 Apr 2021 23:30:48 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.3 org.opencontainers.image.revision=cl210320210309-1101 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 23 Apr 2021 23:30:48 GMT
ENV LIBERTY_VERSION=21.0.0_03
# Fri, 23 Apr 2021 23:30:49 GMT
ARG LIBERTY_URL
# Fri, 23 Apr 2021 23:30:50 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 23 Apr 2021 23:31:05 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:31:07 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Apr 2021 23:31:07 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.3 BuildLabel=cl210320210309-1101
# Fri, 23 Apr 2021 23:31:08 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:31:10 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 23 Apr 2021 23:31:10 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Fri, 23 Apr 2021 23:31:11 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 23 Apr 2021 23:31:14 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 23 Apr 2021 23:31:26 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 23 Apr 2021 23:31:27 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 23 Apr 2021 23:31:28 GMT
USER 1001
# Fri, 23 Apr 2021 23:31:28 GMT
EXPOSE 9080 9443
# Fri, 23 Apr 2021 23:31:29 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 23 Apr 2021 23:31:29 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:de53239ada2db01e7972c3f6eddcf6729f7cf3102be78e0b41363125ce7c2425`  
		Last Modified: Fri, 23 Apr 2021 21:47:14 GMT  
		Size: 27.1 MB (27136362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12932016d0f51acb5c5e5ba5b420a369401a7df47a219f24680bbc05ffde7e11`  
		Last Modified: Fri, 23 Apr 2021 21:47:10 GMT  
		Size: 840.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46997f76c5876e3274170b667463b3d88475cd696ccbc735d2f63965668673ad`  
		Last Modified: Fri, 23 Apr 2021 21:47:10 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bab416938acf6dd045c9fc9097e5768c61b5899b07d110ab3844f447e12b113`  
		Last Modified: Fri, 23 Apr 2021 22:19:05 GMT  
		Size: 15.7 MB (15741779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0273d3bc7cd55960a36b00d19e8d51f8bbeed03d24fd8d551c957fc19ef079b`  
		Last Modified: Fri, 23 Apr 2021 22:22:19 GMT  
		Size: 42.0 MB (41951613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95422aa686364d2877a279281f6eb1157805fa8516aa976b06ce8889dc9f932`  
		Last Modified: Fri, 23 Apr 2021 22:22:13 GMT  
		Size: 3.8 MB (3836026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f4fac1a8aceea217c7fe53bbfc322b60fbc9aa714e55650ace47a05de81069`  
		Last Modified: Fri, 23 Apr 2021 23:54:57 GMT  
		Size: 14.1 MB (14087190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756fea3647fb5e2b8750dbb5e4c2fcf03f89f52b7e5cb55b7606924b2389ca81`  
		Last Modified: Fri, 23 Apr 2021 23:54:54 GMT  
		Size: 691.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8fa9033e59f89cbb013c7d832613bab3a656300357cc70b7eade006a8edefce`  
		Last Modified: Fri, 23 Apr 2021 23:54:54 GMT  
		Size: 9.6 KB (9554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f62d4b9f7c9f91f8d9c689ebf626986dd4c2efd6d86ff851bd15bc6183dded0`  
		Last Modified: Fri, 23 Apr 2021 23:54:54 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491f6056574f25428a41b45fd180908c3bcb491ed462310db1dda218415df01c`  
		Last Modified: Fri, 23 Apr 2021 23:54:54 GMT  
		Size: 10.5 KB (10537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df697bb1f00968be2197f2465a5306f2873b7d22664eeb96b49f2a15ce43654d`  
		Last Modified: Fri, 23 Apr 2021 23:54:54 GMT  
		Size: 2.5 MB (2489469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:21.0.0.3-kernel-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:732d0744cc3d9399d6195f023b48efc50aee4b72893e68432d2eb8f15bc62e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:21.0.0.3-kernel-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:3a4d36916ade30aabf91903a3a99226c23a9f07ff83d4507b8be5f06003da9dd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.1 MB (180147184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559cc09d5d52e1c96eb02fda9d41efea67cd397625dd9cb0d5089aa21bf9ad6a`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 09:30:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 26 Mar 2021 09:31:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 09:31:04 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 26 Mar 2021 09:31:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Mar 2021 09:31:42 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 26 Mar 2021 21:31:17 GMT
ARG VERBOSE=false
# Fri, 26 Mar 2021 21:31:18 GMT
ARG OPENJ9_SCC=true
# Fri, 26 Mar 2021 21:31:18 GMT
ARG EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f
# Fri, 26 Mar 2021 21:31:18 GMT
ARG NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8
# Fri, 26 Mar 2021 21:31:18 GMT
ARG NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075
# Fri, 26 Mar 2021 21:31:18 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.3 org.opencontainers.image.revision=cl210320210309-1101 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 26 Mar 2021 21:31:19 GMT
ENV LIBERTY_VERSION=21.0.0_03
# Fri, 26 Mar 2021 21:31:19 GMT
ARG LIBERTY_URL
# Fri, 26 Mar 2021 21:31:19 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 26 Mar 2021 21:31:33 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 21:31:33 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Mar 2021 21:31:33 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.3 BuildLabel=cl210320210309-1101
# Fri, 26 Mar 2021 21:31:33 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 26 Mar 2021 21:31:35 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 26 Mar 2021 21:31:35 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Fri, 26 Mar 2021 21:31:35 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 26 Mar 2021 21:31:37 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 26 Mar 2021 21:31:48 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 26 Mar 2021 21:31:49 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Fri, 26 Mar 2021 21:31:49 GMT
USER 1001
# Fri, 26 Mar 2021 21:31:49 GMT
EXPOSE 9080 9443
# Fri, 26 Mar 2021 21:31:49 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 26 Mar 2021 21:31:49 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4764ed71d2900c9874838108e377eb8821088502d5504fadeb080e5dd1a3e65d`  
		Last Modified: Fri, 26 Mar 2021 09:35:47 GMT  
		Size: 3.0 MB (2958415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf5000c541da177b7cfe59bf3ff8cb271529f443ee224bf88989910e9a2abb1`  
		Last Modified: Fri, 26 Mar 2021 09:36:01 GMT  
		Size: 130.8 MB (130805802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8f62ff9f46b7fe8abf21ca3992ddfdba43c9a869ab05da497fd0c961b82bcc8`  
		Last Modified: Fri, 26 Mar 2021 21:49:10 GMT  
		Size: 14.0 MB (13988287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade44e6f5f910e4171dbe956b6f82444a1a0cf77cbb628a3cd3a4e02b91e4a75`  
		Last Modified: Fri, 26 Mar 2021 21:49:06 GMT  
		Size: 703.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e194224da53e4dca0cfb2e746e2dc2780faf558e27fbea8a051bbb1e645412a`  
		Last Modified: Fri, 26 Mar 2021 21:49:05 GMT  
		Size: 9.6 KB (9555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee645bef2bf69d54e107e8f571dd29a3a04a4bc4b3dc86db1e83a1cc15f0be9`  
		Last Modified: Fri, 26 Mar 2021 21:49:05 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7592107637fd3c10cd009e854a974a81b2a2bb14bbfc045924a369d59d3098`  
		Last Modified: Fri, 26 Mar 2021 21:49:05 GMT  
		Size: 10.5 KB (10545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11fedbbde6cf647ecb2604ada8a232f0040986bc0bab990ba49c28482ddc35f4`  
		Last Modified: Fri, 26 Mar 2021 21:49:07 GMT  
		Size: 5.7 MB (5661783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.3-kernel-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:6e13cd6d8321c892a92bad1c18c7eac59f81cf159333f4abd6b68f646623568a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183160978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2189d90c2e5eb68ed77ccd518af495f1386ebf9901bd7cf9eb3fd53d65099c61`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 22:30:25 GMT
ADD file:818f810cd30ef74fd4690c6265d80265647ba3353880cf8323500df6d2c48b69 in / 
# Fri, 23 Apr 2021 22:30:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:31:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:31:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:31:32 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:16:58 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 23 Apr 2021 23:17:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:17:43 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 23 Apr 2021 23:18:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 23 Apr 2021 23:19:03 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Sat, 24 Apr 2021 03:07:07 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 03:07:12 GMT
ARG OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:24:41 GMT
ARG EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f
# Sat, 24 Apr 2021 03:24:46 GMT
ARG NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8
# Sat, 24 Apr 2021 03:24:50 GMT
ARG NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075
# Sat, 24 Apr 2021 03:24:56 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.3 org.opencontainers.image.revision=cl210320210309-1101 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Sat, 24 Apr 2021 03:24:59 GMT
ENV LIBERTY_VERSION=21.0.0_03
# Sat, 24 Apr 2021 03:25:02 GMT
ARG LIBERTY_URL
# Sat, 24 Apr 2021 03:25:03 GMT
ARG DOWNLOAD_OPTIONS=
# Sat, 24 Apr 2021 03:25:46 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 03:25:51 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 24 Apr 2021 03:26:00 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.3 BuildLabel=cl210320210309-1101
# Sat, 24 Apr 2021 03:26:05 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:26:29 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Sat, 24 Apr 2021 03:26:30 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Sat, 24 Apr 2021 03:26:32 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Sat, 24 Apr 2021 03:26:48 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Sat, 24 Apr 2021 03:27:19 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Sat, 24 Apr 2021 03:27:25 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Sat, 24 Apr 2021 03:27:28 GMT
USER 1001
# Sat, 24 Apr 2021 03:27:34 GMT
EXPOSE 9080 9443
# Sat, 24 Apr 2021 03:27:39 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Sat, 24 Apr 2021 03:27:42 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:bb3095714506c08a64a49e29ab001d7000d94957d52e05db35361fd4a54c460c`  
		Last Modified: Fri, 23 Apr 2021 22:36:52 GMT  
		Size: 30.4 MB (30407300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd29acc6f7bfef8034eaca0bfb069f0d66e50351c84b062e224d6eae710afa79`  
		Last Modified: Fri, 23 Apr 2021 22:36:46 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7645fc50c9e70df51732b36ef7f8b21ebacd148c3bee4f1b29ca6dcba1bbb949`  
		Last Modified: Fri, 23 Apr 2021 22:36:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab6dc42492fe0eca98f1e563f3e8dabb70f122b45b752264bacb4ea14f59354`  
		Last Modified: Fri, 23 Apr 2021 23:22:26 GMT  
		Size: 3.1 MB (3082775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510992b332e039a7852bef411702a4b667a17ae9ef201c9118477ccc53172fa8`  
		Last Modified: Fri, 23 Apr 2021 23:22:40 GMT  
		Size: 130.4 MB (130406625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd31b308db951c2fb01269a9a47650d67aaae73f5c6391a9e67f4921c403ba57`  
		Last Modified: Sat, 24 Apr 2021 03:59:14 GMT  
		Size: 14.0 MB (13989164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c2633c82a8a8e5896d9c9a12bc8523f99077e522a939a3c059e50497336f01`  
		Last Modified: Sat, 24 Apr 2021 03:59:09 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e942e16565d6f821eebf25a9305f3c221094a1070938264d7d26d2cf1519c8df`  
		Last Modified: Sat, 24 Apr 2021 03:59:09 GMT  
		Size: 9.6 KB (9553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172808243e1a52ecbdd1265e24f73e00a81bb41124082378f10ad90ab850598b`  
		Last Modified: Sat, 24 Apr 2021 03:59:09 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d017355bc45360b9c74a42eff93dd089db63c696cdea8222f3d6c4c78e5c073`  
		Last Modified: Sat, 24 Apr 2021 03:59:09 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf6a0067da138767867fa18d60edb2ba9c2b106b3d78329d1ee3c76b65d04d2`  
		Last Modified: Sat, 24 Apr 2021 03:59:10 GMT  
		Size: 5.3 MB (5253005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.3-kernel-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:7ec7cd651e1f55c59b2ced91a2002ec8589bad439419f68c395622a287dad243
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.0 MB (175955005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bec04b1307de7153f1bd7a3a2cf3022ed3d3f35064bd24ba6e28c45a27b5d1`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 21:45:00 GMT
ADD file:5e61a5300d520d61a2130623465ba2e46da8e80dc2afa042473a42cbcd8d88d2 in / 
# Fri, 23 Apr 2021 21:45:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 21:45:05 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 21:45:07 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 21:45:07 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 22:25:02 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 23 Apr 2021 22:25:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:25:17 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 23 Apr 2021 22:26:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 23 Apr 2021 22:26:15 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 23 Apr 2021 23:16:58 GMT
ARG VERBOSE=false
# Fri, 23 Apr 2021 23:16:58 GMT
ARG OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:29:48 GMT
ARG EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f
# Fri, 23 Apr 2021 23:29:49 GMT
ARG NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8
# Fri, 23 Apr 2021 23:29:50 GMT
ARG NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075
# Fri, 23 Apr 2021 23:29:50 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.3 org.opencontainers.image.revision=cl210320210309-1101 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 23 Apr 2021 23:29:51 GMT
ENV LIBERTY_VERSION=21.0.0_03
# Fri, 23 Apr 2021 23:29:52 GMT
ARG LIBERTY_URL
# Fri, 23 Apr 2021 23:29:52 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 23 Apr 2021 23:30:08 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:30:10 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Apr 2021 23:30:11 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.3 BuildLabel=cl210320210309-1101
# Fri, 23 Apr 2021 23:30:11 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:30:14 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 23 Apr 2021 23:30:15 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Fri, 23 Apr 2021 23:30:15 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 23 Apr 2021 23:30:17 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 23 Apr 2021 23:30:31 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=1ada8dde94633b139876c01b15c2f47011108bbd38e9d498abe73c7f3682b22f NON_IBM_SHA=a495097ac17101fa55a3b763225b4b814c7d2b3019e55922e095f31351790ed8 NOTICES_SHA=c50d7a288214bf29b9e1f01d10f9f43dce85c73829cc2030a7f398ff9bc0b075 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 23 Apr 2021 23:30:32 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -XX:+UseContainerSupport
# Fri, 23 Apr 2021 23:30:33 GMT
USER 1001
# Fri, 23 Apr 2021 23:30:33 GMT
EXPOSE 9080 9443
# Fri, 23 Apr 2021 23:30:34 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 23 Apr 2021 23:30:34 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:33ddddc4572ffe1f294f9f599ed989cc41eee5da4cdcf7db12d10700aa8c894e`  
		Last Modified: Fri, 23 Apr 2021 21:47:03 GMT  
		Size: 25.4 MB (25352756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4395f372a786db91b2f50dc8e43d8b7c3533eb4bd86f6728eb2a0c7108c077d2`  
		Last Modified: Fri, 23 Apr 2021 21:46:59 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e39753730df188282ca8193f14bbbb8cbe0b76ec02b34283a28449b1e41c05`  
		Last Modified: Fri, 23 Apr 2021 21:47:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e93b87da546ac7aa6705cd2f20bfe70cf04793ac73561e5dd8c579af88754aec`  
		Last Modified: Fri, 23 Apr 2021 22:28:41 GMT  
		Size: 2.7 MB (2676643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268462fc02d2bd9da227784f5f243759923a14cefb3648739ca02e8fa7d63ee7`  
		Last Modified: Fri, 23 Apr 2021 22:28:50 GMT  
		Size: 128.1 MB (128065984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2e27878ce60350be68bbdb3b8ee9cbfde9b111787d0b974a06b8dffadddcbd`  
		Last Modified: Fri, 23 Apr 2021 23:54:49 GMT  
		Size: 14.0 MB (13988524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c894cb19fa986a022ad70870257b92d2c0c4fb51aabb232cd0284dacada85fe2`  
		Last Modified: Fri, 23 Apr 2021 23:54:46 GMT  
		Size: 695.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08d76891a169b900915649827dc512feb56f753883fe52981be6f04d736b2f6`  
		Last Modified: Fri, 23 Apr 2021 23:54:46 GMT  
		Size: 9.6 KB (9557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34ee5d8f9435c0ed35bd9d1b5ae402ce58f34113d03dd5a315a826c6cd83b36`  
		Last Modified: Fri, 23 Apr 2021 23:54:46 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d300d3fb2439110af45d80a2ddbf132b397feb71fefce3d1f0a596b771fdb90c`  
		Last Modified: Fri, 23 Apr 2021 23:54:47 GMT  
		Size: 10.5 KB (10543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a38e178e857d2811edcaca15881bfc7721e5afa49da3e0557037dfec12a23f`  
		Last Modified: Fri, 23 Apr 2021 23:54:47 GMT  
		Size: 5.8 MB (5848991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:21.0.0.4-full-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:d92942e9b32f987f620c47fe75f32d533a206a05c775f2856948bac34f6a7fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:21.0.0.4-full-java11-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:35cc2096f3510a3db928f854c16a9bedad246d1252f311c839f1c572d9c73dff
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.6 MB (329563878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a13fac28833e00b5e3a59ae871ccdd0fbdf78ae2ea63171016753dc05b77a32`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 03 Apr 2021 00:53:06 GMT
ADD file:27277aee655dd263ee698d1f2fe17f0b1dbba740615bcac8642723a6ac0d62be in / 
# Sat, 03 Apr 2021 00:53:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 03 Apr 2021 00:53:08 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Sat, 03 Apr 2021 00:53:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 03 Apr 2021 00:53:09 GMT
CMD ["/bin/bash"]
# Sat, 03 Apr 2021 01:29:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 03 Apr 2021 01:29:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 03 Apr 2021 01:32:52 GMT
ENV JAVA_VERSION=jdk-11.0.10+9_openj9-0.24.0
# Mon, 19 Apr 2021 18:22:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='5d2b2939637f999a1910d5cc0fb3d96756125941e5f8b9e3003635aa863664b5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        s390x)          ESUM='2ff9f50d6ffc345434703c43a1d67ac6d3d054b5d4925b4b73a3ce51b02940e5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7e5f97071f8b86c22c36ddfd7f821c3e8ec531c1128e2e6c931b2e64118a517a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 19 Apr 2021 18:22:34 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Apr 2021 18:22:34 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 19 Apr 2021 18:23:10 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 22 Apr 2021 21:40:48 GMT
ARG VERBOSE=false
# Thu, 22 Apr 2021 21:40:48 GMT
ARG OPENJ9_SCC=true
# Thu, 22 Apr 2021 21:40:48 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Thu, 22 Apr 2021 21:40:49 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Thu, 22 Apr 2021 21:40:49 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Thu, 22 Apr 2021 21:40:49 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 22 Apr 2021 21:40:49 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Thu, 22 Apr 2021 21:40:49 GMT
ARG LIBERTY_URL
# Thu, 22 Apr 2021 21:40:49 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 22 Apr 2021 21:40:58 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Apr 2021 21:40:58 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Apr 2021 21:40:58 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Thu, 22 Apr 2021 21:40:58 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 22 Apr 2021 21:41:00 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Apr 2021 21:41:00 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Thu, 22 Apr 2021 21:41:00 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Apr 2021 21:41:01 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Apr 2021 21:41:09 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Apr 2021 21:41:09 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 22 Apr 2021 21:41:09 GMT
USER 1001
# Thu, 22 Apr 2021 21:41:10 GMT
EXPOSE 9080 9443
# Thu, 22 Apr 2021 21:41:10 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Apr 2021 21:41:10 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 22 Apr 2021 21:44:55 GMT
ARG VERBOSE=false
# Thu, 22 Apr 2021 21:44:55 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 22 Apr 2021 21:47:40 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Thu, 22 Apr 2021 21:47:41 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 22 Apr 2021 21:48:15 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:a70d879fa5984474288d52009479054b8bb2993de2a1859f43b5480600cecb24`  
		Last Modified: Thu, 01 Apr 2021 15:20:06 GMT  
		Size: 28.6 MB (28569016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4394a92d1f8760cf7d17fee0bcee732c94c5b858dd8d19c7ff02beecf3b4e83`  
		Last Modified: Sat, 03 Apr 2021 00:54:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e6159c56c084c858f5de2416454ac0a49ddda47b764e4379c5d5a147c9bf5f`  
		Last Modified: Sat, 03 Apr 2021 00:54:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04b772c31f76720583412a2507c5c53889985db45169a85f0d3cd7f842e041a`  
		Last Modified: Sat, 03 Apr 2021 01:39:30 GMT  
		Size: 16.0 MB (16032891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf71362343a962febc8c6ce8c4fd12d961c5712407993471f60ac0e5d43415e`  
		Last Modified: Mon, 19 Apr 2021 18:30:17 GMT  
		Size: 42.4 MB (42440313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9163852ff25e45c3b95c7b759a719b91afa29724136e68d1cf7f822c034c4df`  
		Last Modified: Mon, 19 Apr 2021 18:30:04 GMT  
		Size: 4.0 MB (4025359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a723eb5427857d3e6f939a462cbbaeedb1b248662076fe72f2fab621d9acc3`  
		Last Modified: Thu, 22 Apr 2021 21:57:15 GMT  
		Size: 14.2 MB (14160245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0598dd9101a4447350e39fc9445131bdeb5a9bee7fc233879f0451c08a79fe`  
		Last Modified: Thu, 22 Apr 2021 21:57:12 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf163d48e000642c258afeea2bb09c0cca8829f72fcd792c97840c181f7331f8`  
		Last Modified: Thu, 22 Apr 2021 21:57:12 GMT  
		Size: 9.6 KB (9550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5906189dfc1fa00888b59c4cefad5a2f4aa3085bcc6da5d37e63197585a231c`  
		Last Modified: Thu, 22 Apr 2021 21:57:10 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062608db9cb7d8e8fc2dfa23464525e84b5d5fe1bc979194b937d8b2a4de74a6`  
		Last Modified: Thu, 22 Apr 2021 21:57:11 GMT  
		Size: 10.5 KB (10531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc2d74ce76564c5e8a6dafde72882602b446b3d3d81d620c5b1f08232a5a019`  
		Last Modified: Thu, 22 Apr 2021 21:57:11 GMT  
		Size: 2.6 MB (2555007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2717086accd7d50a5527b2b70f1177f08e904718f5388f702983ce093761304`  
		Last Modified: Thu, 22 Apr 2021 21:58:02 GMT  
		Size: 207.7 MB (207669936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b59e20e338e249cff7c3435973456929f13dfea41138604d3fe1696e479dc61`  
		Last Modified: Thu, 22 Apr 2021 21:57:50 GMT  
		Size: 944.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455eb33d7a0b34ae7cec9f9f41505c10dd6db2bd14f0f792b193a312a1c64b9e`  
		Last Modified: Thu, 22 Apr 2021 21:57:53 GMT  
		Size: 14.1 MB (14088088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.4-full-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:58d2df36fa80fd34c6efd19e002465a236bf9863e4fb5910f188695f8f0c6f0c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.5 MB (334494224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f187bd2be5cc7237467c10fb9155ab68dffc18d8c2e2b99ecd81a3b016a7f9`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:16:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 24 Apr 2021 01:19:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:28:36 GMT
ENV JAVA_VERSION=jdk-11.0.10+9_openj9-0.24.0
# Sat, 24 Apr 2021 01:30:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='5d2b2939637f999a1910d5cc0fb3d96756125941e5f8b9e3003635aa863664b5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        s390x)          ESUM='2ff9f50d6ffc345434703c43a1d67ac6d3d054b5d4925b4b73a3ce51b02940e5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7e5f97071f8b86c22c36ddfd7f821c3e8ec531c1128e2e6c931b2e64118a517a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 24 Apr 2021 01:30:48 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 24 Apr 2021 01:30:53 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Sat, 24 Apr 2021 01:31:37 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Sat, 24 Apr 2021 03:09:49 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 03:09:52 GMT
ARG OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:09:54 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Sat, 24 Apr 2021 03:09:57 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Sat, 24 Apr 2021 03:10:02 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Sat, 24 Apr 2021 03:10:05 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Sat, 24 Apr 2021 03:10:09 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Sat, 24 Apr 2021 03:10:15 GMT
ARG LIBERTY_URL
# Sat, 24 Apr 2021 03:10:19 GMT
ARG DOWNLOAD_OPTIONS=
# Sat, 24 Apr 2021 03:10:59 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 03:11:04 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 24 Apr 2021 03:11:08 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Sat, 24 Apr 2021 03:11:13 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:11:26 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Sat, 24 Apr 2021 03:11:28 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Sat, 24 Apr 2021 03:11:29 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Sat, 24 Apr 2021 03:11:41 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Sat, 24 Apr 2021 03:12:04 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Sat, 24 Apr 2021 03:12:09 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Sat, 24 Apr 2021 03:12:14 GMT
USER 1001
# Sat, 24 Apr 2021 03:12:25 GMT
EXPOSE 9080 9443
# Sat, 24 Apr 2021 03:12:36 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Sat, 24 Apr 2021 03:12:38 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Sat, 24 Apr 2021 03:19:14 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 03:19:16 GMT
ARG REPOSITORIES_PROPERTIES=
# Sat, 24 Apr 2021 03:22:47 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Sat, 24 Apr 2021 03:22:55 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Sat, 24 Apr 2021 03:24:07 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da07529aeac8fe5c90c5bb8c4f516c9d6fd248cc1daa5fecd137c809bce39bb6`  
		Last Modified: Sat, 24 Apr 2021 01:40:58 GMT  
		Size: 17.2 MB (17209103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53f9612e78ec5df6fbbbab4098deb40150ceef63be58aec6c2dd4df6af9f634`  
		Last Modified: Sat, 24 Apr 2021 01:46:21 GMT  
		Size: 43.3 MB (43277570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec133c54d62c9541f8b987c7353d67bd5d58ea39050f8cd947bf150d5ce8bb7a`  
		Last Modified: Sat, 24 Apr 2021 01:46:15 GMT  
		Size: 3.3 MB (3289250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062a0799a977bb2eb37a4a5544f4bd9dcb11b4139484efeb167d51a76dca344a`  
		Last Modified: Sat, 24 Apr 2021 03:57:40 GMT  
		Size: 14.2 MB (14161560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17e6eee9e8f60faaa4a97342c2158cd7796ac7bb6b08f138f711a9005741b36`  
		Last Modified: Sat, 24 Apr 2021 03:57:35 GMT  
		Size: 697.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b718a9fd82bc2a543e1c729118139996c38bc7710b89c7ecc990debf128858a`  
		Last Modified: Sat, 24 Apr 2021 03:57:35 GMT  
		Size: 9.6 KB (9554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f60415893707e5b040738d7e8a87ff3fa04cc21d7b2d5c85562332e2d497ea5`  
		Last Modified: Sat, 24 Apr 2021 03:57:35 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe6a41ec43a7b373422e863b76d451d0137a52c137e44b547ac9ad39fb73de2`  
		Last Modified: Sat, 24 Apr 2021 03:57:35 GMT  
		Size: 10.5 KB (10534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8aebc0ca7b2fb770385f3b4cfd9d7e7bac63d078e6c70044101e080ed32788e`  
		Last Modified: Sat, 24 Apr 2021 03:57:36 GMT  
		Size: 2.4 MB (2447444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b635648abb6c1d815d8bd988b55c7440c3dd8cd34211c0774827f2721c6022`  
		Last Modified: Sat, 24 Apr 2021 03:58:47 GMT  
		Size: 207.7 MB (207669849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52431dbbec59f34a44a99af91356d620b21524fe914b30b4c0dd9080ca5dee05`  
		Last Modified: Sat, 24 Apr 2021 03:58:27 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221e0c907c55b23b136a53cd5ece658f13412cb017e26a7c8b7d236b5ffcdaa9`  
		Last Modified: Sat, 24 Apr 2021 03:58:30 GMT  
		Size: 13.2 MB (13161022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.4-full-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:0d02e361435df46fff35ebc173579ebb1dafbc0713fa6fa5882156f0ac9abb76
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.6 MB (326645376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c382f67d2996379923080d0c01ae3039c6ef3b9f1e0b452d32958d81cd7e7487`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 21:45:20 GMT
ADD file:282d950116f923276efabd13c7dc17b942821edb14ffac4b89b9a50bcdf99e17 in / 
# Fri, 23 Apr 2021 21:45:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 21:45:27 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 21:45:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 21:45:29 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 22:03:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Apr 2021 22:04:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:10:11 GMT
ENV JAVA_VERSION=jdk-11.0.10+9_openj9-0.24.0
# Fri, 23 Apr 2021 22:11:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='5d2b2939637f999a1910d5cc0fb3d96756125941e5f8b9e3003635aa863664b5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        s390x)          ESUM='2ff9f50d6ffc345434703c43a1d67ac6d3d054b5d4925b4b73a3ce51b02940e5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7e5f97071f8b86c22c36ddfd7f821c3e8ec531c1128e2e6c931b2e64118a517a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 23 Apr 2021 22:11:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Apr 2021 22:11:44 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 23 Apr 2021 22:12:20 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 23 Apr 2021 23:17:55 GMT
ARG VERBOSE=false
# Fri, 23 Apr 2021 23:17:56 GMT
ARG OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:17:56 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Fri, 23 Apr 2021 23:17:57 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Fri, 23 Apr 2021 23:17:57 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Fri, 23 Apr 2021 23:17:58 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 23 Apr 2021 23:17:59 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Fri, 23 Apr 2021 23:17:59 GMT
ARG LIBERTY_URL
# Fri, 23 Apr 2021 23:18:00 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 23 Apr 2021 23:18:14 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:18:15 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Apr 2021 23:18:16 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Fri, 23 Apr 2021 23:18:16 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:18:18 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 23 Apr 2021 23:18:19 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Fri, 23 Apr 2021 23:18:19 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 23 Apr 2021 23:18:22 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 23 Apr 2021 23:18:32 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 23 Apr 2021 23:18:33 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 23 Apr 2021 23:18:34 GMT
USER 1001
# Fri, 23 Apr 2021 23:18:35 GMT
EXPOSE 9080 9443
# Fri, 23 Apr 2021 23:18:36 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 23 Apr 2021 23:18:36 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 23 Apr 2021 23:24:07 GMT
ARG VERBOSE=false
# Fri, 23 Apr 2021 23:24:07 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 23 Apr 2021 23:28:09 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Fri, 23 Apr 2021 23:28:21 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 23 Apr 2021 23:29:08 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:de53239ada2db01e7972c3f6eddcf6729f7cf3102be78e0b41363125ce7c2425`  
		Last Modified: Fri, 23 Apr 2021 21:47:14 GMT  
		Size: 27.1 MB (27136362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12932016d0f51acb5c5e5ba5b420a369401a7df47a219f24680bbc05ffde7e11`  
		Last Modified: Fri, 23 Apr 2021 21:47:10 GMT  
		Size: 840.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46997f76c5876e3274170b667463b3d88475cd696ccbc735d2f63965668673ad`  
		Last Modified: Fri, 23 Apr 2021 21:47:10 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bab416938acf6dd045c9fc9097e5768c61b5899b07d110ab3844f447e12b113`  
		Last Modified: Fri, 23 Apr 2021 22:19:05 GMT  
		Size: 15.7 MB (15741779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0273d3bc7cd55960a36b00d19e8d51f8bbeed03d24fd8d551c957fc19ef079b`  
		Last Modified: Fri, 23 Apr 2021 22:22:19 GMT  
		Size: 42.0 MB (41951613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95422aa686364d2877a279281f6eb1157805fa8516aa976b06ce8889dc9f932`  
		Last Modified: Fri, 23 Apr 2021 22:22:13 GMT  
		Size: 3.8 MB (3836026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f024126ee5e04e37dd48573fe2e6aefd2d98012df116b366e0aef9fa63b8ba93`  
		Last Modified: Fri, 23 Apr 2021 23:54:00 GMT  
		Size: 14.2 MB (14160729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a63a9d57fd3b2ed838f0044559d5cfa241eab25d7626378b2fd1c5463947a9`  
		Last Modified: Fri, 23 Apr 2021 23:53:57 GMT  
		Size: 687.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62def58659c4a5a6fd3cde1c4245691f62a7d197ac87536975c7c888e8fd5ff`  
		Last Modified: Fri, 23 Apr 2021 23:53:57 GMT  
		Size: 9.6 KB (9551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288fec31697eb659f1a7285ca37ce8460c07bd8485fdb21628ff246a6661660d`  
		Last Modified: Fri, 23 Apr 2021 23:53:57 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bce08718a41817d4e1e9dd6bb83ac83f3a1c3014753a04447805c257e51a9c3`  
		Last Modified: Fri, 23 Apr 2021 23:53:57 GMT  
		Size: 10.5 KB (10544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3096c60acccc8db5e2ef0df733a4693cf8068658a1fc8af639461c112c1589a`  
		Last Modified: Fri, 23 Apr 2021 23:53:57 GMT  
		Size: 2.5 MB (2491647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d29297ab00722488619fd9526e89b49277ed66bac34206e8f7e2cb0917e1945`  
		Last Modified: Fri, 23 Apr 2021 23:54:35 GMT  
		Size: 207.7 MB (207671747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b7a66a256bd33f418c1622886d5384d5a5abc02e2c3b042d528a7153211728`  
		Last Modified: Fri, 23 Apr 2021 23:54:24 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba111cf88078cf3a5f862c69d813cf4940c21337daefa46d9c6a9818aae58d8e`  
		Last Modified: Fri, 23 Apr 2021 23:54:26 GMT  
		Size: 13.6 MB (13632445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:21.0.0.4-full-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:d1780004f0389b487847ce25dc81722d446d73a340336370e1ddaf71d4e0fe8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:21.0.0.4-full-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:750da2549ddcfbd3e9ae2850b9ae2347adbb712410041faf8a02a81d635d2cde
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.8 MB (414810589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bfd08f9c2afdc6e2530607e9db350908221943ae7b3a387ed47fde3bad081c`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 09:30:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 26 Mar 2021 09:31:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 09:31:04 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 26 Mar 2021 09:31:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Mar 2021 09:31:42 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 26 Mar 2021 21:31:17 GMT
ARG VERBOSE=false
# Fri, 26 Mar 2021 21:31:18 GMT
ARG OPENJ9_SCC=true
# Thu, 22 Apr 2021 21:40:06 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Thu, 22 Apr 2021 21:40:06 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Thu, 22 Apr 2021 21:40:06 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Thu, 22 Apr 2021 21:40:06 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 22 Apr 2021 21:40:06 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Thu, 22 Apr 2021 21:40:07 GMT
ARG LIBERTY_URL
# Thu, 22 Apr 2021 21:40:07 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 22 Apr 2021 21:40:24 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Apr 2021 21:40:24 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Apr 2021 21:40:24 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Thu, 22 Apr 2021 21:40:24 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 22 Apr 2021 21:40:26 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Apr 2021 21:40:26 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Thu, 22 Apr 2021 21:40:26 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Apr 2021 21:40:28 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Apr 2021 21:40:38 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Apr 2021 21:40:38 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 22 Apr 2021 21:40:38 GMT
USER 1001
# Thu, 22 Apr 2021 21:40:39 GMT
EXPOSE 9080 9443
# Thu, 22 Apr 2021 21:40:39 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Apr 2021 21:40:39 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 22 Apr 2021 21:41:13 GMT
ARG VERBOSE=false
# Thu, 22 Apr 2021 21:41:13 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 22 Apr 2021 21:44:16 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Thu, 22 Apr 2021 21:44:16 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 22 Apr 2021 21:44:52 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4764ed71d2900c9874838108e377eb8821088502d5504fadeb080e5dd1a3e65d`  
		Last Modified: Fri, 26 Mar 2021 09:35:47 GMT  
		Size: 3.0 MB (2958415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf5000c541da177b7cfe59bf3ff8cb271529f443ee224bf88989910e9a2abb1`  
		Last Modified: Fri, 26 Mar 2021 09:36:01 GMT  
		Size: 130.8 MB (130805802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33df46370333075337eb25c08aa74c706467351aa5abe9711e870aa5e647baaf`  
		Last Modified: Thu, 22 Apr 2021 21:57:02 GMT  
		Size: 14.1 MB (14061162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d854faca6db468012fcae8e445cd69affeb82c5efbb89ac2b53b719cb4eabd`  
		Last Modified: Thu, 22 Apr 2021 21:56:58 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f56d571437c689e2188bb2653cbbaf3ef56de28093fd63e3229a142d9d87fa`  
		Last Modified: Thu, 22 Apr 2021 21:56:58 GMT  
		Size: 9.6 KB (9556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fde75a052b81ad9ca202510ebedb5083754ed163d499a6f28f1be76b6615ad`  
		Last Modified: Thu, 22 Apr 2021 21:56:58 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610a90e750f1b7eb794e24a2970acb3b9f79a569ed064d70771895e2cf5c4795`  
		Last Modified: Thu, 22 Apr 2021 21:56:58 GMT  
		Size: 10.5 KB (10544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3782c27b14b1eea6ec7f8a3c56182ccbf3a0db0e5a00cb4aad829f8b16f628b1`  
		Last Modified: Thu, 22 Apr 2021 21:56:59 GMT  
		Size: 5.7 MB (5734998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f94a4feba9d432ba504a626d7c726342855fc5baffbda070b24e905aa4d6f2`  
		Last Modified: Thu, 22 Apr 2021 21:57:36 GMT  
		Size: 213.4 MB (213364505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f32f1e0b41195d19cb5b1bc063af6b2ebd037fee723a18c58cee092d68b465`  
		Last Modified: Thu, 22 Apr 2021 21:57:24 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926bbbd582bf41deb09392c6714bc00b03c3a35a16db042c445f171588d03f52`  
		Last Modified: Thu, 22 Apr 2021 21:57:28 GMT  
		Size: 21.2 MB (21151866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.4-full-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:9e6931d099e61e14b50000de09a805e628326d2ca36b7f785fb87afddb5f31b7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.8 MB (414816829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:145832e765296a2c9cf6f91cac745f6fdb49cea3740a2436251f4f16d501ae05`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 22:30:25 GMT
ADD file:818f810cd30ef74fd4690c6265d80265647ba3353880cf8323500df6d2c48b69 in / 
# Fri, 23 Apr 2021 22:30:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:31:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:31:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:31:32 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:16:58 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 23 Apr 2021 23:17:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:17:43 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 23 Apr 2021 23:18:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 23 Apr 2021 23:19:03 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Sat, 24 Apr 2021 03:07:07 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 03:07:12 GMT
ARG OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:07:15 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Sat, 24 Apr 2021 03:07:18 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Sat, 24 Apr 2021 03:07:22 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Sat, 24 Apr 2021 03:07:25 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Sat, 24 Apr 2021 03:07:30 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Sat, 24 Apr 2021 03:07:35 GMT
ARG LIBERTY_URL
# Sat, 24 Apr 2021 03:07:39 GMT
ARG DOWNLOAD_OPTIONS=
# Sat, 24 Apr 2021 03:08:16 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 03:08:18 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 24 Apr 2021 03:08:20 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Sat, 24 Apr 2021 03:08:21 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:08:37 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Sat, 24 Apr 2021 03:08:40 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Sat, 24 Apr 2021 03:08:42 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Sat, 24 Apr 2021 03:08:53 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Sat, 24 Apr 2021 03:09:13 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Sat, 24 Apr 2021 03:09:19 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Sat, 24 Apr 2021 03:09:24 GMT
USER 1001
# Sat, 24 Apr 2021 03:09:27 GMT
EXPOSE 9080 9443
# Sat, 24 Apr 2021 03:09:30 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Sat, 24 Apr 2021 03:09:34 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Sat, 24 Apr 2021 03:12:46 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 03:12:51 GMT
ARG REPOSITORIES_PROPERTIES=
# Sat, 24 Apr 2021 03:17:43 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Sat, 24 Apr 2021 03:17:46 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Sat, 24 Apr 2021 03:18:58 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:bb3095714506c08a64a49e29ab001d7000d94957d52e05db35361fd4a54c460c`  
		Last Modified: Fri, 23 Apr 2021 22:36:52 GMT  
		Size: 30.4 MB (30407300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd29acc6f7bfef8034eaca0bfb069f0d66e50351c84b062e224d6eae710afa79`  
		Last Modified: Fri, 23 Apr 2021 22:36:46 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7645fc50c9e70df51732b36ef7f8b21ebacd148c3bee4f1b29ca6dcba1bbb949`  
		Last Modified: Fri, 23 Apr 2021 22:36:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab6dc42492fe0eca98f1e563f3e8dabb70f122b45b752264bacb4ea14f59354`  
		Last Modified: Fri, 23 Apr 2021 23:22:26 GMT  
		Size: 3.1 MB (3082775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510992b332e039a7852bef411702a4b667a17ae9ef201c9118477ccc53172fa8`  
		Last Modified: Fri, 23 Apr 2021 23:22:40 GMT  
		Size: 130.4 MB (130406625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de545400b0a4b20e99a41bb03dd0464d3f4e6b22326a58a0f8a6f27df35ed53`  
		Last Modified: Sat, 24 Apr 2021 03:57:21 GMT  
		Size: 14.1 MB (14062037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19c270fd954ab1850546a2f1fe907e5812464bb308554d74ff3b77fe4d085a5`  
		Last Modified: Sat, 24 Apr 2021 03:57:16 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b461e2c9230ad6d7e36d9fddcc2d3d04a394954d5b5437473fde9a958d54c05c`  
		Last Modified: Sat, 24 Apr 2021 03:57:15 GMT  
		Size: 9.6 KB (9557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0821ea49c2f2252a0938a998b8388c6f28a42fa11fcea87f34c94c523b2a1e`  
		Last Modified: Sat, 24 Apr 2021 03:57:15 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b875abf5447191fb37fb076a3def6e4623314c82cf9c399a82e81f2d7fbfdd`  
		Last Modified: Sat, 24 Apr 2021 03:57:16 GMT  
		Size: 10.5 KB (10548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1dc37ac444dea5f60b5a444e3fe1cf82f9c846fe2eef1d199c48742f541072e`  
		Last Modified: Sat, 24 Apr 2021 03:57:17 GMT  
		Size: 5.3 MB (5300774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340964737ae2ffbf89a010557d283b9a17b7d52790d89962d818463313818768`  
		Last Modified: Sat, 24 Apr 2021 03:58:11 GMT  
		Size: 212.9 MB (212930880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba214ef51994cf88584d070810d932460f4e7341911cbf935ff7cbe006e467d`  
		Last Modified: Sat, 24 Apr 2021 03:57:49 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c830a72dca5b968adec807675fd7d07de4a08456b2188cbf92acdf09a5132f`  
		Last Modified: Sat, 24 Apr 2021 03:57:53 GMT  
		Size: 18.6 MB (18603368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.4-full-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:1813d2e44e1f79784ab44778359fd80a47b37726d4ded32db082ca08eb72f80f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.0 MB (411023034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1109636c471215912302d8affaad06caa663cedee902a569c14ebc0e70e6a9a`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 21:45:00 GMT
ADD file:5e61a5300d520d61a2130623465ba2e46da8e80dc2afa042473a42cbcd8d88d2 in / 
# Fri, 23 Apr 2021 21:45:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 21:45:05 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 21:45:07 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 21:45:07 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 22:25:02 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 23 Apr 2021 22:25:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:25:17 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 23 Apr 2021 22:26:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 23 Apr 2021 22:26:15 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 23 Apr 2021 23:16:58 GMT
ARG VERBOSE=false
# Fri, 23 Apr 2021 23:16:58 GMT
ARG OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:16:59 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Fri, 23 Apr 2021 23:17:00 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Fri, 23 Apr 2021 23:17:00 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Fri, 23 Apr 2021 23:17:01 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 23 Apr 2021 23:17:02 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Fri, 23 Apr 2021 23:17:02 GMT
ARG LIBERTY_URL
# Fri, 23 Apr 2021 23:17:03 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 23 Apr 2021 23:17:18 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:17:20 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Apr 2021 23:17:21 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Fri, 23 Apr 2021 23:17:21 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:17:23 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 23 Apr 2021 23:17:24 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Fri, 23 Apr 2021 23:17:25 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 23 Apr 2021 23:17:27 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 23 Apr 2021 23:17:40 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 23 Apr 2021 23:17:41 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 23 Apr 2021 23:17:42 GMT
USER 1001
# Fri, 23 Apr 2021 23:17:42 GMT
EXPOSE 9080 9443
# Fri, 23 Apr 2021 23:17:43 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 23 Apr 2021 23:17:43 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 23 Apr 2021 23:18:44 GMT
ARG VERBOSE=false
# Fri, 23 Apr 2021 23:18:45 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 23 Apr 2021 23:22:46 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Fri, 23 Apr 2021 23:23:00 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 23 Apr 2021 23:23:44 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:33ddddc4572ffe1f294f9f599ed989cc41eee5da4cdcf7db12d10700aa8c894e`  
		Last Modified: Fri, 23 Apr 2021 21:47:03 GMT  
		Size: 25.4 MB (25352756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4395f372a786db91b2f50dc8e43d8b7c3533eb4bd86f6728eb2a0c7108c077d2`  
		Last Modified: Fri, 23 Apr 2021 21:46:59 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e39753730df188282ca8193f14bbbb8cbe0b76ec02b34283a28449b1e41c05`  
		Last Modified: Fri, 23 Apr 2021 21:47:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e93b87da546ac7aa6705cd2f20bfe70cf04793ac73561e5dd8c579af88754aec`  
		Last Modified: Fri, 23 Apr 2021 22:28:41 GMT  
		Size: 2.7 MB (2676643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268462fc02d2bd9da227784f5f243759923a14cefb3648739ca02e8fa7d63ee7`  
		Last Modified: Fri, 23 Apr 2021 22:28:50 GMT  
		Size: 128.1 MB (128065984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895091e75a5c1ee863c074a41c334973d986bb55cef3d4ba2f8267a2887f8336`  
		Last Modified: Fri, 23 Apr 2021 23:53:50 GMT  
		Size: 14.1 MB (14061390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26d2145efe41abadeb2694f43164f1a155e500e85bf004da26812cd8532de7f`  
		Last Modified: Fri, 23 Apr 2021 23:53:47 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1dc41aa938b0af86dfd6446147e4484cb5d6bad6e84eb2edb074790b0615a1`  
		Last Modified: Fri, 23 Apr 2021 23:53:47 GMT  
		Size: 9.6 KB (9556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0e2666f7e25fefd1dfbbb522189283388626a78a6993958a175bfe3d453daa`  
		Last Modified: Fri, 23 Apr 2021 23:53:47 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1422da1f78c4ff3f196f908ccd43d884e84e4586193eab1bfe59df39b352b130`  
		Last Modified: Fri, 23 Apr 2021 23:53:47 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6a848b971c7539a51ff9771c57f7df448cc5b960c0be0fa5b3c3b547e8589c`  
		Last Modified: Fri, 23 Apr 2021 23:53:47 GMT  
		Size: 5.9 MB (5924580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a29d9ef14335af914d1a4155de231f338e3649b1e962477e8f3c3007227195`  
		Last Modified: Fri, 23 Apr 2021 23:54:16 GMT  
		Size: 213.6 MB (213555213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85098d48d9a85bbbdc1b5f863692bf7b326b94c5f44d091ff39e53fb34a41cc`  
		Last Modified: Fri, 23 Apr 2021 23:54:05 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1e656c995305a66ce28c668c88b221183600d735978d891b72351644e890c2`  
		Last Modified: Fri, 23 Apr 2021 23:54:08 GMT  
		Size: 21.4 MB (21363413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:21.0.0.4-kernel-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:6f6653874c0eb28bb81144c3bc83a1895c1cde222cf3866e260bdd2daa7cb31b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:21.0.0.4-kernel-java11-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:089c25ea4ac42c4cedb0b974d8cf29185eb9c3ec4e86fa10817a8afa5de7f601
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107804910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98fb4f6747d498676b24bc7bf8aa4905b802d1f2ed2d3b27bce67a59d00748c5`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 03 Apr 2021 00:53:06 GMT
ADD file:27277aee655dd263ee698d1f2fe17f0b1dbba740615bcac8642723a6ac0d62be in / 
# Sat, 03 Apr 2021 00:53:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 03 Apr 2021 00:53:08 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Sat, 03 Apr 2021 00:53:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 03 Apr 2021 00:53:09 GMT
CMD ["/bin/bash"]
# Sat, 03 Apr 2021 01:29:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 03 Apr 2021 01:29:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 03 Apr 2021 01:32:52 GMT
ENV JAVA_VERSION=jdk-11.0.10+9_openj9-0.24.0
# Mon, 19 Apr 2021 18:22:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='5d2b2939637f999a1910d5cc0fb3d96756125941e5f8b9e3003635aa863664b5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        s390x)          ESUM='2ff9f50d6ffc345434703c43a1d67ac6d3d054b5d4925b4b73a3ce51b02940e5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7e5f97071f8b86c22c36ddfd7f821c3e8ec531c1128e2e6c931b2e64118a517a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 19 Apr 2021 18:22:34 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Apr 2021 18:22:34 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 19 Apr 2021 18:23:10 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 22 Apr 2021 21:40:48 GMT
ARG VERBOSE=false
# Thu, 22 Apr 2021 21:40:48 GMT
ARG OPENJ9_SCC=true
# Thu, 22 Apr 2021 21:40:48 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Thu, 22 Apr 2021 21:40:49 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Thu, 22 Apr 2021 21:40:49 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Thu, 22 Apr 2021 21:40:49 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 22 Apr 2021 21:40:49 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Thu, 22 Apr 2021 21:40:49 GMT
ARG LIBERTY_URL
# Thu, 22 Apr 2021 21:40:49 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 22 Apr 2021 21:40:58 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Apr 2021 21:40:58 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Apr 2021 21:40:58 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Thu, 22 Apr 2021 21:40:58 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 22 Apr 2021 21:41:00 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Apr 2021 21:41:00 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Thu, 22 Apr 2021 21:41:00 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Apr 2021 21:41:01 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Apr 2021 21:41:09 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Apr 2021 21:41:09 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 22 Apr 2021 21:41:09 GMT
USER 1001
# Thu, 22 Apr 2021 21:41:10 GMT
EXPOSE 9080 9443
# Thu, 22 Apr 2021 21:41:10 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Apr 2021 21:41:10 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:a70d879fa5984474288d52009479054b8bb2993de2a1859f43b5480600cecb24`  
		Last Modified: Thu, 01 Apr 2021 15:20:06 GMT  
		Size: 28.6 MB (28569016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4394a92d1f8760cf7d17fee0bcee732c94c5b858dd8d19c7ff02beecf3b4e83`  
		Last Modified: Sat, 03 Apr 2021 00:54:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e6159c56c084c858f5de2416454ac0a49ddda47b764e4379c5d5a147c9bf5f`  
		Last Modified: Sat, 03 Apr 2021 00:54:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04b772c31f76720583412a2507c5c53889985db45169a85f0d3cd7f842e041a`  
		Last Modified: Sat, 03 Apr 2021 01:39:30 GMT  
		Size: 16.0 MB (16032891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf71362343a962febc8c6ce8c4fd12d961c5712407993471f60ac0e5d43415e`  
		Last Modified: Mon, 19 Apr 2021 18:30:17 GMT  
		Size: 42.4 MB (42440313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9163852ff25e45c3b95c7b759a719b91afa29724136e68d1cf7f822c034c4df`  
		Last Modified: Mon, 19 Apr 2021 18:30:04 GMT  
		Size: 4.0 MB (4025359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a723eb5427857d3e6f939a462cbbaeedb1b248662076fe72f2fab621d9acc3`  
		Last Modified: Thu, 22 Apr 2021 21:57:15 GMT  
		Size: 14.2 MB (14160245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0598dd9101a4447350e39fc9445131bdeb5a9bee7fc233879f0451c08a79fe`  
		Last Modified: Thu, 22 Apr 2021 21:57:12 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf163d48e000642c258afeea2bb09c0cca8829f72fcd792c97840c181f7331f8`  
		Last Modified: Thu, 22 Apr 2021 21:57:12 GMT  
		Size: 9.6 KB (9550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5906189dfc1fa00888b59c4cefad5a2f4aa3085bcc6da5d37e63197585a231c`  
		Last Modified: Thu, 22 Apr 2021 21:57:10 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062608db9cb7d8e8fc2dfa23464525e84b5d5fe1bc979194b937d8b2a4de74a6`  
		Last Modified: Thu, 22 Apr 2021 21:57:11 GMT  
		Size: 10.5 KB (10531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc2d74ce76564c5e8a6dafde72882602b446b3d3d81d620c5b1f08232a5a019`  
		Last Modified: Thu, 22 Apr 2021 21:57:11 GMT  
		Size: 2.6 MB (2555007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.4-kernel-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:b76395a786647b5473b28d061e02e1c5276f807eddc0c4653dfdce8891c629f3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.7 MB (113662407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d1a5de89d5c2bac2a0c0f64e4b0f9560bb1f9b6fef00a8be97351e87832bc2`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:16:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 24 Apr 2021 01:19:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:28:36 GMT
ENV JAVA_VERSION=jdk-11.0.10+9_openj9-0.24.0
# Sat, 24 Apr 2021 01:30:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='5d2b2939637f999a1910d5cc0fb3d96756125941e5f8b9e3003635aa863664b5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        s390x)          ESUM='2ff9f50d6ffc345434703c43a1d67ac6d3d054b5d4925b4b73a3ce51b02940e5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7e5f97071f8b86c22c36ddfd7f821c3e8ec531c1128e2e6c931b2e64118a517a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 24 Apr 2021 01:30:48 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 24 Apr 2021 01:30:53 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Sat, 24 Apr 2021 01:31:37 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Sat, 24 Apr 2021 03:09:49 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 03:09:52 GMT
ARG OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:09:54 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Sat, 24 Apr 2021 03:09:57 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Sat, 24 Apr 2021 03:10:02 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Sat, 24 Apr 2021 03:10:05 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Sat, 24 Apr 2021 03:10:09 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Sat, 24 Apr 2021 03:10:15 GMT
ARG LIBERTY_URL
# Sat, 24 Apr 2021 03:10:19 GMT
ARG DOWNLOAD_OPTIONS=
# Sat, 24 Apr 2021 03:10:59 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 03:11:04 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 24 Apr 2021 03:11:08 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Sat, 24 Apr 2021 03:11:13 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:11:26 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Sat, 24 Apr 2021 03:11:28 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Sat, 24 Apr 2021 03:11:29 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Sat, 24 Apr 2021 03:11:41 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Sat, 24 Apr 2021 03:12:04 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Sat, 24 Apr 2021 03:12:09 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Sat, 24 Apr 2021 03:12:14 GMT
USER 1001
# Sat, 24 Apr 2021 03:12:25 GMT
EXPOSE 9080 9443
# Sat, 24 Apr 2021 03:12:36 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Sat, 24 Apr 2021 03:12:38 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da07529aeac8fe5c90c5bb8c4f516c9d6fd248cc1daa5fecd137c809bce39bb6`  
		Last Modified: Sat, 24 Apr 2021 01:40:58 GMT  
		Size: 17.2 MB (17209103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53f9612e78ec5df6fbbbab4098deb40150ceef63be58aec6c2dd4df6af9f634`  
		Last Modified: Sat, 24 Apr 2021 01:46:21 GMT  
		Size: 43.3 MB (43277570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec133c54d62c9541f8b987c7353d67bd5d58ea39050f8cd947bf150d5ce8bb7a`  
		Last Modified: Sat, 24 Apr 2021 01:46:15 GMT  
		Size: 3.3 MB (3289250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062a0799a977bb2eb37a4a5544f4bd9dcb11b4139484efeb167d51a76dca344a`  
		Last Modified: Sat, 24 Apr 2021 03:57:40 GMT  
		Size: 14.2 MB (14161560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17e6eee9e8f60faaa4a97342c2158cd7796ac7bb6b08f138f711a9005741b36`  
		Last Modified: Sat, 24 Apr 2021 03:57:35 GMT  
		Size: 697.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b718a9fd82bc2a543e1c729118139996c38bc7710b89c7ecc990debf128858a`  
		Last Modified: Sat, 24 Apr 2021 03:57:35 GMT  
		Size: 9.6 KB (9554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f60415893707e5b040738d7e8a87ff3fa04cc21d7b2d5c85562332e2d497ea5`  
		Last Modified: Sat, 24 Apr 2021 03:57:35 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe6a41ec43a7b373422e863b76d451d0137a52c137e44b547ac9ad39fb73de2`  
		Last Modified: Sat, 24 Apr 2021 03:57:35 GMT  
		Size: 10.5 KB (10534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8aebc0ca7b2fb770385f3b4cfd9d7e7bac63d078e6c70044101e080ed32788e`  
		Last Modified: Sat, 24 Apr 2021 03:57:36 GMT  
		Size: 2.4 MB (2447444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.4-kernel-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:7da2d996a0edd7759eef333322be612a3aa048d1c48ffec09bef5d1d8aca195e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105340236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0450ad9b23e181ff9223541e51f3bd15bdc098a0b0e011fda20432f21f2b5467`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 21:45:20 GMT
ADD file:282d950116f923276efabd13c7dc17b942821edb14ffac4b89b9a50bcdf99e17 in / 
# Fri, 23 Apr 2021 21:45:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 21:45:27 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 21:45:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 21:45:29 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 22:03:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Apr 2021 22:04:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:10:11 GMT
ENV JAVA_VERSION=jdk-11.0.10+9_openj9-0.24.0
# Fri, 23 Apr 2021 22:11:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='5d2b2939637f999a1910d5cc0fb3d96756125941e5f8b9e3003635aa863664b5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        s390x)          ESUM='2ff9f50d6ffc345434703c43a1d67ac6d3d054b5d4925b4b73a3ce51b02940e5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7e5f97071f8b86c22c36ddfd7f821c3e8ec531c1128e2e6c931b2e64118a517a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 23 Apr 2021 22:11:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Apr 2021 22:11:44 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 23 Apr 2021 22:12:20 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 23 Apr 2021 23:17:55 GMT
ARG VERBOSE=false
# Fri, 23 Apr 2021 23:17:56 GMT
ARG OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:17:56 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Fri, 23 Apr 2021 23:17:57 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Fri, 23 Apr 2021 23:17:57 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Fri, 23 Apr 2021 23:17:58 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 23 Apr 2021 23:17:59 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Fri, 23 Apr 2021 23:17:59 GMT
ARG LIBERTY_URL
# Fri, 23 Apr 2021 23:18:00 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 23 Apr 2021 23:18:14 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:18:15 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Apr 2021 23:18:16 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Fri, 23 Apr 2021 23:18:16 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:18:18 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 23 Apr 2021 23:18:19 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Fri, 23 Apr 2021 23:18:19 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 23 Apr 2021 23:18:22 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 23 Apr 2021 23:18:32 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 23 Apr 2021 23:18:33 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 23 Apr 2021 23:18:34 GMT
USER 1001
# Fri, 23 Apr 2021 23:18:35 GMT
EXPOSE 9080 9443
# Fri, 23 Apr 2021 23:18:36 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 23 Apr 2021 23:18:36 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:de53239ada2db01e7972c3f6eddcf6729f7cf3102be78e0b41363125ce7c2425`  
		Last Modified: Fri, 23 Apr 2021 21:47:14 GMT  
		Size: 27.1 MB (27136362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12932016d0f51acb5c5e5ba5b420a369401a7df47a219f24680bbc05ffde7e11`  
		Last Modified: Fri, 23 Apr 2021 21:47:10 GMT  
		Size: 840.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46997f76c5876e3274170b667463b3d88475cd696ccbc735d2f63965668673ad`  
		Last Modified: Fri, 23 Apr 2021 21:47:10 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bab416938acf6dd045c9fc9097e5768c61b5899b07d110ab3844f447e12b113`  
		Last Modified: Fri, 23 Apr 2021 22:19:05 GMT  
		Size: 15.7 MB (15741779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0273d3bc7cd55960a36b00d19e8d51f8bbeed03d24fd8d551c957fc19ef079b`  
		Last Modified: Fri, 23 Apr 2021 22:22:19 GMT  
		Size: 42.0 MB (41951613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95422aa686364d2877a279281f6eb1157805fa8516aa976b06ce8889dc9f932`  
		Last Modified: Fri, 23 Apr 2021 22:22:13 GMT  
		Size: 3.8 MB (3836026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f024126ee5e04e37dd48573fe2e6aefd2d98012df116b366e0aef9fa63b8ba93`  
		Last Modified: Fri, 23 Apr 2021 23:54:00 GMT  
		Size: 14.2 MB (14160729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a63a9d57fd3b2ed838f0044559d5cfa241eab25d7626378b2fd1c5463947a9`  
		Last Modified: Fri, 23 Apr 2021 23:53:57 GMT  
		Size: 687.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62def58659c4a5a6fd3cde1c4245691f62a7d197ac87536975c7c888e8fd5ff`  
		Last Modified: Fri, 23 Apr 2021 23:53:57 GMT  
		Size: 9.6 KB (9551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288fec31697eb659f1a7285ca37ce8460c07bd8485fdb21628ff246a6661660d`  
		Last Modified: Fri, 23 Apr 2021 23:53:57 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bce08718a41817d4e1e9dd6bb83ac83f3a1c3014753a04447805c257e51a9c3`  
		Last Modified: Fri, 23 Apr 2021 23:53:57 GMT  
		Size: 10.5 KB (10544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3096c60acccc8db5e2ef0df733a4693cf8068658a1fc8af639461c112c1589a`  
		Last Modified: Fri, 23 Apr 2021 23:53:57 GMT  
		Size: 2.5 MB (2491647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:21.0.0.4-kernel-java8-ibmjava`

```console
$ docker pull websphere-liberty@sha256:267b85caae5e988db295e1af8043390556fdb96d8fd2740f0c6a0ccfe1ab463d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:21.0.0.4-kernel-java8-ibmjava` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:f528365190e853e1ffbc72c586114358fb2eb6e0117c4134f68e0e57894f6f24
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180293270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79615f972bc823a2954599784f3311d9cd8c7d4e5bc2ee82a917c4f753326937`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 09:30:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 26 Mar 2021 09:31:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 09:31:04 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 26 Mar 2021 09:31:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Mar 2021 09:31:42 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 26 Mar 2021 21:31:17 GMT
ARG VERBOSE=false
# Fri, 26 Mar 2021 21:31:18 GMT
ARG OPENJ9_SCC=true
# Thu, 22 Apr 2021 21:40:06 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Thu, 22 Apr 2021 21:40:06 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Thu, 22 Apr 2021 21:40:06 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Thu, 22 Apr 2021 21:40:06 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 22 Apr 2021 21:40:06 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Thu, 22 Apr 2021 21:40:07 GMT
ARG LIBERTY_URL
# Thu, 22 Apr 2021 21:40:07 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 22 Apr 2021 21:40:24 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Apr 2021 21:40:24 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Apr 2021 21:40:24 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Thu, 22 Apr 2021 21:40:24 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 22 Apr 2021 21:40:26 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Apr 2021 21:40:26 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Thu, 22 Apr 2021 21:40:26 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Apr 2021 21:40:28 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Apr 2021 21:40:38 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Apr 2021 21:40:38 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 22 Apr 2021 21:40:38 GMT
USER 1001
# Thu, 22 Apr 2021 21:40:39 GMT
EXPOSE 9080 9443
# Thu, 22 Apr 2021 21:40:39 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Apr 2021 21:40:39 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4764ed71d2900c9874838108e377eb8821088502d5504fadeb080e5dd1a3e65d`  
		Last Modified: Fri, 26 Mar 2021 09:35:47 GMT  
		Size: 3.0 MB (2958415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf5000c541da177b7cfe59bf3ff8cb271529f443ee224bf88989910e9a2abb1`  
		Last Modified: Fri, 26 Mar 2021 09:36:01 GMT  
		Size: 130.8 MB (130805802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33df46370333075337eb25c08aa74c706467351aa5abe9711e870aa5e647baaf`  
		Last Modified: Thu, 22 Apr 2021 21:57:02 GMT  
		Size: 14.1 MB (14061162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d854faca6db468012fcae8e445cd69affeb82c5efbb89ac2b53b719cb4eabd`  
		Last Modified: Thu, 22 Apr 2021 21:56:58 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f56d571437c689e2188bb2653cbbaf3ef56de28093fd63e3229a142d9d87fa`  
		Last Modified: Thu, 22 Apr 2021 21:56:58 GMT  
		Size: 9.6 KB (9556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fde75a052b81ad9ca202510ebedb5083754ed163d499a6f28f1be76b6615ad`  
		Last Modified: Thu, 22 Apr 2021 21:56:58 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610a90e750f1b7eb794e24a2970acb3b9f79a569ed064d70771895e2cf5c4795`  
		Last Modified: Thu, 22 Apr 2021 21:56:58 GMT  
		Size: 10.5 KB (10544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3782c27b14b1eea6ec7f8a3c56182ccbf3a0db0e5a00cb4aad829f8b16f628b1`  
		Last Modified: Thu, 22 Apr 2021 21:56:59 GMT  
		Size: 5.7 MB (5734998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.4-kernel-java8-ibmjava` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:a6fba29d04471e2eff94691224c8ff16b7c962a1ec9e18b5d03865993d75613c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183281635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c365f977369905b70d1ba9f75dc6b19ce4ae1f730890957000463778aa9458`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 22:30:25 GMT
ADD file:818f810cd30ef74fd4690c6265d80265647ba3353880cf8323500df6d2c48b69 in / 
# Fri, 23 Apr 2021 22:30:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:31:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:31:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:31:32 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:16:58 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 23 Apr 2021 23:17:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:17:43 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 23 Apr 2021 23:18:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 23 Apr 2021 23:19:03 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Sat, 24 Apr 2021 03:07:07 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 03:07:12 GMT
ARG OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:07:15 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Sat, 24 Apr 2021 03:07:18 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Sat, 24 Apr 2021 03:07:22 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Sat, 24 Apr 2021 03:07:25 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Sat, 24 Apr 2021 03:07:30 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Sat, 24 Apr 2021 03:07:35 GMT
ARG LIBERTY_URL
# Sat, 24 Apr 2021 03:07:39 GMT
ARG DOWNLOAD_OPTIONS=
# Sat, 24 Apr 2021 03:08:16 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 03:08:18 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 24 Apr 2021 03:08:20 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Sat, 24 Apr 2021 03:08:21 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:08:37 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Sat, 24 Apr 2021 03:08:40 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Sat, 24 Apr 2021 03:08:42 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Sat, 24 Apr 2021 03:08:53 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Sat, 24 Apr 2021 03:09:13 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Sat, 24 Apr 2021 03:09:19 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Sat, 24 Apr 2021 03:09:24 GMT
USER 1001
# Sat, 24 Apr 2021 03:09:27 GMT
EXPOSE 9080 9443
# Sat, 24 Apr 2021 03:09:30 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Sat, 24 Apr 2021 03:09:34 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:bb3095714506c08a64a49e29ab001d7000d94957d52e05db35361fd4a54c460c`  
		Last Modified: Fri, 23 Apr 2021 22:36:52 GMT  
		Size: 30.4 MB (30407300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd29acc6f7bfef8034eaca0bfb069f0d66e50351c84b062e224d6eae710afa79`  
		Last Modified: Fri, 23 Apr 2021 22:36:46 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7645fc50c9e70df51732b36ef7f8b21ebacd148c3bee4f1b29ca6dcba1bbb949`  
		Last Modified: Fri, 23 Apr 2021 22:36:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab6dc42492fe0eca98f1e563f3e8dabb70f122b45b752264bacb4ea14f59354`  
		Last Modified: Fri, 23 Apr 2021 23:22:26 GMT  
		Size: 3.1 MB (3082775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510992b332e039a7852bef411702a4b667a17ae9ef201c9118477ccc53172fa8`  
		Last Modified: Fri, 23 Apr 2021 23:22:40 GMT  
		Size: 130.4 MB (130406625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de545400b0a4b20e99a41bb03dd0464d3f4e6b22326a58a0f8a6f27df35ed53`  
		Last Modified: Sat, 24 Apr 2021 03:57:21 GMT  
		Size: 14.1 MB (14062037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19c270fd954ab1850546a2f1fe907e5812464bb308554d74ff3b77fe4d085a5`  
		Last Modified: Sat, 24 Apr 2021 03:57:16 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b461e2c9230ad6d7e36d9fddcc2d3d04a394954d5b5437473fde9a958d54c05c`  
		Last Modified: Sat, 24 Apr 2021 03:57:15 GMT  
		Size: 9.6 KB (9557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0821ea49c2f2252a0938a998b8388c6f28a42fa11fcea87f34c94c523b2a1e`  
		Last Modified: Sat, 24 Apr 2021 03:57:15 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b875abf5447191fb37fb076a3def6e4623314c82cf9c399a82e81f2d7fbfdd`  
		Last Modified: Sat, 24 Apr 2021 03:57:16 GMT  
		Size: 10.5 KB (10548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1dc37ac444dea5f60b5a444e3fe1cf82f9c846fe2eef1d199c48742f541072e`  
		Last Modified: Sat, 24 Apr 2021 03:57:17 GMT  
		Size: 5.3 MB (5300774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:21.0.0.4-kernel-java8-ibmjava` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:0d7dafd042d0d2cc8eb4580d0db30ada5047e8848c332172235044b128158d2f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176103462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a099f0ae43c0fd8c3e964020f65971f96b5f6988450d42231f7333bb9b4fb8f2`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 21:45:00 GMT
ADD file:5e61a5300d520d61a2130623465ba2e46da8e80dc2afa042473a42cbcd8d88d2 in / 
# Fri, 23 Apr 2021 21:45:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 21:45:05 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 21:45:07 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 21:45:07 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 22:25:02 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 23 Apr 2021 22:25:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:25:17 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 23 Apr 2021 22:26:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 23 Apr 2021 22:26:15 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 23 Apr 2021 23:16:58 GMT
ARG VERBOSE=false
# Fri, 23 Apr 2021 23:16:58 GMT
ARG OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:16:59 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Fri, 23 Apr 2021 23:17:00 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Fri, 23 Apr 2021 23:17:00 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Fri, 23 Apr 2021 23:17:01 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 23 Apr 2021 23:17:02 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Fri, 23 Apr 2021 23:17:02 GMT
ARG LIBERTY_URL
# Fri, 23 Apr 2021 23:17:03 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 23 Apr 2021 23:17:18 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:17:20 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Apr 2021 23:17:21 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Fri, 23 Apr 2021 23:17:21 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:17:23 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 23 Apr 2021 23:17:24 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Fri, 23 Apr 2021 23:17:25 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 23 Apr 2021 23:17:27 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 23 Apr 2021 23:17:40 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 23 Apr 2021 23:17:41 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 23 Apr 2021 23:17:42 GMT
USER 1001
# Fri, 23 Apr 2021 23:17:42 GMT
EXPOSE 9080 9443
# Fri, 23 Apr 2021 23:17:43 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 23 Apr 2021 23:17:43 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:33ddddc4572ffe1f294f9f599ed989cc41eee5da4cdcf7db12d10700aa8c894e`  
		Last Modified: Fri, 23 Apr 2021 21:47:03 GMT  
		Size: 25.4 MB (25352756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4395f372a786db91b2f50dc8e43d8b7c3533eb4bd86f6728eb2a0c7108c077d2`  
		Last Modified: Fri, 23 Apr 2021 21:46:59 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e39753730df188282ca8193f14bbbb8cbe0b76ec02b34283a28449b1e41c05`  
		Last Modified: Fri, 23 Apr 2021 21:47:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e93b87da546ac7aa6705cd2f20bfe70cf04793ac73561e5dd8c579af88754aec`  
		Last Modified: Fri, 23 Apr 2021 22:28:41 GMT  
		Size: 2.7 MB (2676643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268462fc02d2bd9da227784f5f243759923a14cefb3648739ca02e8fa7d63ee7`  
		Last Modified: Fri, 23 Apr 2021 22:28:50 GMT  
		Size: 128.1 MB (128065984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895091e75a5c1ee863c074a41c334973d986bb55cef3d4ba2f8267a2887f8336`  
		Last Modified: Fri, 23 Apr 2021 23:53:50 GMT  
		Size: 14.1 MB (14061390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26d2145efe41abadeb2694f43164f1a155e500e85bf004da26812cd8532de7f`  
		Last Modified: Fri, 23 Apr 2021 23:53:47 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1dc41aa938b0af86dfd6446147e4484cb5d6bad6e84eb2edb074790b0615a1`  
		Last Modified: Fri, 23 Apr 2021 23:53:47 GMT  
		Size: 9.6 KB (9556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0e2666f7e25fefd1dfbbb522189283388626a78a6993958a175bfe3d453daa`  
		Last Modified: Fri, 23 Apr 2021 23:53:47 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1422da1f78c4ff3f196f908ccd43d884e84e4586193eab1bfe59df39b352b130`  
		Last Modified: Fri, 23 Apr 2021 23:53:47 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6a848b971c7539a51ff9771c57f7df448cc5b960c0be0fa5b3c3b547e8589c`  
		Last Modified: Fri, 23 Apr 2021 23:53:47 GMT  
		Size: 5.9 MB (5924580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:full`

```console
$ docker pull websphere-liberty@sha256:0fa2d01a01dd7a58472a2717c5067d89db1b966b2d780278cd7253be29f9ce3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:full` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:750da2549ddcfbd3e9ae2850b9ae2347adbb712410041faf8a02a81d635d2cde
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.8 MB (414810589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bfd08f9c2afdc6e2530607e9db350908221943ae7b3a387ed47fde3bad081c`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 09:30:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 26 Mar 2021 09:31:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 09:31:04 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 26 Mar 2021 09:31:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Mar 2021 09:31:42 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 26 Mar 2021 21:31:17 GMT
ARG VERBOSE=false
# Fri, 26 Mar 2021 21:31:18 GMT
ARG OPENJ9_SCC=true
# Thu, 22 Apr 2021 21:40:06 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Thu, 22 Apr 2021 21:40:06 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Thu, 22 Apr 2021 21:40:06 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Thu, 22 Apr 2021 21:40:06 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 22 Apr 2021 21:40:06 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Thu, 22 Apr 2021 21:40:07 GMT
ARG LIBERTY_URL
# Thu, 22 Apr 2021 21:40:07 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 22 Apr 2021 21:40:24 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Apr 2021 21:40:24 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Apr 2021 21:40:24 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Thu, 22 Apr 2021 21:40:24 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 22 Apr 2021 21:40:26 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Apr 2021 21:40:26 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Thu, 22 Apr 2021 21:40:26 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Apr 2021 21:40:28 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Apr 2021 21:40:38 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Apr 2021 21:40:38 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 22 Apr 2021 21:40:38 GMT
USER 1001
# Thu, 22 Apr 2021 21:40:39 GMT
EXPOSE 9080 9443
# Thu, 22 Apr 2021 21:40:39 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Apr 2021 21:40:39 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 22 Apr 2021 21:41:13 GMT
ARG VERBOSE=false
# Thu, 22 Apr 2021 21:41:13 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 22 Apr 2021 21:44:16 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Thu, 22 Apr 2021 21:44:16 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 22 Apr 2021 21:44:52 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4764ed71d2900c9874838108e377eb8821088502d5504fadeb080e5dd1a3e65d`  
		Last Modified: Fri, 26 Mar 2021 09:35:47 GMT  
		Size: 3.0 MB (2958415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf5000c541da177b7cfe59bf3ff8cb271529f443ee224bf88989910e9a2abb1`  
		Last Modified: Fri, 26 Mar 2021 09:36:01 GMT  
		Size: 130.8 MB (130805802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33df46370333075337eb25c08aa74c706467351aa5abe9711e870aa5e647baaf`  
		Last Modified: Thu, 22 Apr 2021 21:57:02 GMT  
		Size: 14.1 MB (14061162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d854faca6db468012fcae8e445cd69affeb82c5efbb89ac2b53b719cb4eabd`  
		Last Modified: Thu, 22 Apr 2021 21:56:58 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f56d571437c689e2188bb2653cbbaf3ef56de28093fd63e3229a142d9d87fa`  
		Last Modified: Thu, 22 Apr 2021 21:56:58 GMT  
		Size: 9.6 KB (9556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fde75a052b81ad9ca202510ebedb5083754ed163d499a6f28f1be76b6615ad`  
		Last Modified: Thu, 22 Apr 2021 21:56:58 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610a90e750f1b7eb794e24a2970acb3b9f79a569ed064d70771895e2cf5c4795`  
		Last Modified: Thu, 22 Apr 2021 21:56:58 GMT  
		Size: 10.5 KB (10544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3782c27b14b1eea6ec7f8a3c56182ccbf3a0db0e5a00cb4aad829f8b16f628b1`  
		Last Modified: Thu, 22 Apr 2021 21:56:59 GMT  
		Size: 5.7 MB (5734998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f94a4feba9d432ba504a626d7c726342855fc5baffbda070b24e905aa4d6f2`  
		Last Modified: Thu, 22 Apr 2021 21:57:36 GMT  
		Size: 213.4 MB (213364505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f32f1e0b41195d19cb5b1bc063af6b2ebd037fee723a18c58cee092d68b465`  
		Last Modified: Thu, 22 Apr 2021 21:57:24 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926bbbd582bf41deb09392c6714bc00b03c3a35a16db042c445f171588d03f52`  
		Last Modified: Thu, 22 Apr 2021 21:57:28 GMT  
		Size: 21.2 MB (21151866 bytes)  
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
$ docker pull websphere-liberty@sha256:9e6931d099e61e14b50000de09a805e628326d2ca36b7f785fb87afddb5f31b7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.8 MB (414816829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:145832e765296a2c9cf6f91cac745f6fdb49cea3740a2436251f4f16d501ae05`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 22:30:25 GMT
ADD file:818f810cd30ef74fd4690c6265d80265647ba3353880cf8323500df6d2c48b69 in / 
# Fri, 23 Apr 2021 22:30:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:31:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:31:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:31:32 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:16:58 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 23 Apr 2021 23:17:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:17:43 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 23 Apr 2021 23:18:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 23 Apr 2021 23:19:03 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Sat, 24 Apr 2021 03:07:07 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 03:07:12 GMT
ARG OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:07:15 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Sat, 24 Apr 2021 03:07:18 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Sat, 24 Apr 2021 03:07:22 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Sat, 24 Apr 2021 03:07:25 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Sat, 24 Apr 2021 03:07:30 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Sat, 24 Apr 2021 03:07:35 GMT
ARG LIBERTY_URL
# Sat, 24 Apr 2021 03:07:39 GMT
ARG DOWNLOAD_OPTIONS=
# Sat, 24 Apr 2021 03:08:16 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 03:08:18 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 24 Apr 2021 03:08:20 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Sat, 24 Apr 2021 03:08:21 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:08:37 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Sat, 24 Apr 2021 03:08:40 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Sat, 24 Apr 2021 03:08:42 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Sat, 24 Apr 2021 03:08:53 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Sat, 24 Apr 2021 03:09:13 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Sat, 24 Apr 2021 03:09:19 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Sat, 24 Apr 2021 03:09:24 GMT
USER 1001
# Sat, 24 Apr 2021 03:09:27 GMT
EXPOSE 9080 9443
# Sat, 24 Apr 2021 03:09:30 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Sat, 24 Apr 2021 03:09:34 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Sat, 24 Apr 2021 03:12:46 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 03:12:51 GMT
ARG REPOSITORIES_PROPERTIES=
# Sat, 24 Apr 2021 03:17:43 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Sat, 24 Apr 2021 03:17:46 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Sat, 24 Apr 2021 03:18:58 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:bb3095714506c08a64a49e29ab001d7000d94957d52e05db35361fd4a54c460c`  
		Last Modified: Fri, 23 Apr 2021 22:36:52 GMT  
		Size: 30.4 MB (30407300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd29acc6f7bfef8034eaca0bfb069f0d66e50351c84b062e224d6eae710afa79`  
		Last Modified: Fri, 23 Apr 2021 22:36:46 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7645fc50c9e70df51732b36ef7f8b21ebacd148c3bee4f1b29ca6dcba1bbb949`  
		Last Modified: Fri, 23 Apr 2021 22:36:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab6dc42492fe0eca98f1e563f3e8dabb70f122b45b752264bacb4ea14f59354`  
		Last Modified: Fri, 23 Apr 2021 23:22:26 GMT  
		Size: 3.1 MB (3082775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510992b332e039a7852bef411702a4b667a17ae9ef201c9118477ccc53172fa8`  
		Last Modified: Fri, 23 Apr 2021 23:22:40 GMT  
		Size: 130.4 MB (130406625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de545400b0a4b20e99a41bb03dd0464d3f4e6b22326a58a0f8a6f27df35ed53`  
		Last Modified: Sat, 24 Apr 2021 03:57:21 GMT  
		Size: 14.1 MB (14062037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19c270fd954ab1850546a2f1fe907e5812464bb308554d74ff3b77fe4d085a5`  
		Last Modified: Sat, 24 Apr 2021 03:57:16 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b461e2c9230ad6d7e36d9fddcc2d3d04a394954d5b5437473fde9a958d54c05c`  
		Last Modified: Sat, 24 Apr 2021 03:57:15 GMT  
		Size: 9.6 KB (9557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0821ea49c2f2252a0938a998b8388c6f28a42fa11fcea87f34c94c523b2a1e`  
		Last Modified: Sat, 24 Apr 2021 03:57:15 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b875abf5447191fb37fb076a3def6e4623314c82cf9c399a82e81f2d7fbfdd`  
		Last Modified: Sat, 24 Apr 2021 03:57:16 GMT  
		Size: 10.5 KB (10548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1dc37ac444dea5f60b5a444e3fe1cf82f9c846fe2eef1d199c48742f541072e`  
		Last Modified: Sat, 24 Apr 2021 03:57:17 GMT  
		Size: 5.3 MB (5300774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340964737ae2ffbf89a010557d283b9a17b7d52790d89962d818463313818768`  
		Last Modified: Sat, 24 Apr 2021 03:58:11 GMT  
		Size: 212.9 MB (212930880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba214ef51994cf88584d070810d932460f4e7341911cbf935ff7cbe006e467d`  
		Last Modified: Sat, 24 Apr 2021 03:57:49 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c830a72dca5b968adec807675fd7d07de4a08456b2188cbf92acdf09a5132f`  
		Last Modified: Sat, 24 Apr 2021 03:57:53 GMT  
		Size: 18.6 MB (18603368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:1813d2e44e1f79784ab44778359fd80a47b37726d4ded32db082ca08eb72f80f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.0 MB (411023034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1109636c471215912302d8affaad06caa663cedee902a569c14ebc0e70e6a9a`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 21:45:00 GMT
ADD file:5e61a5300d520d61a2130623465ba2e46da8e80dc2afa042473a42cbcd8d88d2 in / 
# Fri, 23 Apr 2021 21:45:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 21:45:05 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 21:45:07 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 21:45:07 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 22:25:02 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 23 Apr 2021 22:25:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:25:17 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 23 Apr 2021 22:26:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 23 Apr 2021 22:26:15 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 23 Apr 2021 23:16:58 GMT
ARG VERBOSE=false
# Fri, 23 Apr 2021 23:16:58 GMT
ARG OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:16:59 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Fri, 23 Apr 2021 23:17:00 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Fri, 23 Apr 2021 23:17:00 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Fri, 23 Apr 2021 23:17:01 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 23 Apr 2021 23:17:02 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Fri, 23 Apr 2021 23:17:02 GMT
ARG LIBERTY_URL
# Fri, 23 Apr 2021 23:17:03 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 23 Apr 2021 23:17:18 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:17:20 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Apr 2021 23:17:21 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Fri, 23 Apr 2021 23:17:21 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:17:23 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 23 Apr 2021 23:17:24 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Fri, 23 Apr 2021 23:17:25 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 23 Apr 2021 23:17:27 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 23 Apr 2021 23:17:40 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 23 Apr 2021 23:17:41 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 23 Apr 2021 23:17:42 GMT
USER 1001
# Fri, 23 Apr 2021 23:17:42 GMT
EXPOSE 9080 9443
# Fri, 23 Apr 2021 23:17:43 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 23 Apr 2021 23:17:43 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 23 Apr 2021 23:18:44 GMT
ARG VERBOSE=false
# Fri, 23 Apr 2021 23:18:45 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 23 Apr 2021 23:22:46 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Fri, 23 Apr 2021 23:23:00 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 23 Apr 2021 23:23:44 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:33ddddc4572ffe1f294f9f599ed989cc41eee5da4cdcf7db12d10700aa8c894e`  
		Last Modified: Fri, 23 Apr 2021 21:47:03 GMT  
		Size: 25.4 MB (25352756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4395f372a786db91b2f50dc8e43d8b7c3533eb4bd86f6728eb2a0c7108c077d2`  
		Last Modified: Fri, 23 Apr 2021 21:46:59 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e39753730df188282ca8193f14bbbb8cbe0b76ec02b34283a28449b1e41c05`  
		Last Modified: Fri, 23 Apr 2021 21:47:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e93b87da546ac7aa6705cd2f20bfe70cf04793ac73561e5dd8c579af88754aec`  
		Last Modified: Fri, 23 Apr 2021 22:28:41 GMT  
		Size: 2.7 MB (2676643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268462fc02d2bd9da227784f5f243759923a14cefb3648739ca02e8fa7d63ee7`  
		Last Modified: Fri, 23 Apr 2021 22:28:50 GMT  
		Size: 128.1 MB (128065984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895091e75a5c1ee863c074a41c334973d986bb55cef3d4ba2f8267a2887f8336`  
		Last Modified: Fri, 23 Apr 2021 23:53:50 GMT  
		Size: 14.1 MB (14061390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26d2145efe41abadeb2694f43164f1a155e500e85bf004da26812cd8532de7f`  
		Last Modified: Fri, 23 Apr 2021 23:53:47 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1dc41aa938b0af86dfd6446147e4484cb5d6bad6e84eb2edb074790b0615a1`  
		Last Modified: Fri, 23 Apr 2021 23:53:47 GMT  
		Size: 9.6 KB (9556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0e2666f7e25fefd1dfbbb522189283388626a78a6993958a175bfe3d453daa`  
		Last Modified: Fri, 23 Apr 2021 23:53:47 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1422da1f78c4ff3f196f908ccd43d884e84e4586193eab1bfe59df39b352b130`  
		Last Modified: Fri, 23 Apr 2021 23:53:47 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6a848b971c7539a51ff9771c57f7df448cc5b960c0be0fa5b3c3b547e8589c`  
		Last Modified: Fri, 23 Apr 2021 23:53:47 GMT  
		Size: 5.9 MB (5924580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a29d9ef14335af914d1a4155de231f338e3649b1e962477e8f3c3007227195`  
		Last Modified: Fri, 23 Apr 2021 23:54:16 GMT  
		Size: 213.6 MB (213555213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85098d48d9a85bbbdc1b5f863692bf7b326b94c5f44d091ff39e53fb34a41cc`  
		Last Modified: Fri, 23 Apr 2021 23:54:05 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1e656c995305a66ce28c668c88b221183600d735978d891b72351644e890c2`  
		Last Modified: Fri, 23 Apr 2021 23:54:08 GMT  
		Size: 21.4 MB (21363413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:full-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:d92942e9b32f987f620c47fe75f32d533a206a05c775f2856948bac34f6a7fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:full-java11-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:35cc2096f3510a3db928f854c16a9bedad246d1252f311c839f1c572d9c73dff
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.6 MB (329563878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a13fac28833e00b5e3a59ae871ccdd0fbdf78ae2ea63171016753dc05b77a32`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 03 Apr 2021 00:53:06 GMT
ADD file:27277aee655dd263ee698d1f2fe17f0b1dbba740615bcac8642723a6ac0d62be in / 
# Sat, 03 Apr 2021 00:53:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 03 Apr 2021 00:53:08 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Sat, 03 Apr 2021 00:53:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 03 Apr 2021 00:53:09 GMT
CMD ["/bin/bash"]
# Sat, 03 Apr 2021 01:29:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 03 Apr 2021 01:29:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 03 Apr 2021 01:32:52 GMT
ENV JAVA_VERSION=jdk-11.0.10+9_openj9-0.24.0
# Mon, 19 Apr 2021 18:22:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='5d2b2939637f999a1910d5cc0fb3d96756125941e5f8b9e3003635aa863664b5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        s390x)          ESUM='2ff9f50d6ffc345434703c43a1d67ac6d3d054b5d4925b4b73a3ce51b02940e5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7e5f97071f8b86c22c36ddfd7f821c3e8ec531c1128e2e6c931b2e64118a517a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 19 Apr 2021 18:22:34 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Apr 2021 18:22:34 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 19 Apr 2021 18:23:10 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 22 Apr 2021 21:40:48 GMT
ARG VERBOSE=false
# Thu, 22 Apr 2021 21:40:48 GMT
ARG OPENJ9_SCC=true
# Thu, 22 Apr 2021 21:40:48 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Thu, 22 Apr 2021 21:40:49 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Thu, 22 Apr 2021 21:40:49 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Thu, 22 Apr 2021 21:40:49 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 22 Apr 2021 21:40:49 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Thu, 22 Apr 2021 21:40:49 GMT
ARG LIBERTY_URL
# Thu, 22 Apr 2021 21:40:49 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 22 Apr 2021 21:40:58 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Apr 2021 21:40:58 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Apr 2021 21:40:58 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Thu, 22 Apr 2021 21:40:58 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 22 Apr 2021 21:41:00 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Apr 2021 21:41:00 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Thu, 22 Apr 2021 21:41:00 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Apr 2021 21:41:01 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Apr 2021 21:41:09 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Apr 2021 21:41:09 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 22 Apr 2021 21:41:09 GMT
USER 1001
# Thu, 22 Apr 2021 21:41:10 GMT
EXPOSE 9080 9443
# Thu, 22 Apr 2021 21:41:10 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Apr 2021 21:41:10 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 22 Apr 2021 21:44:55 GMT
ARG VERBOSE=false
# Thu, 22 Apr 2021 21:44:55 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 22 Apr 2021 21:47:40 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Thu, 22 Apr 2021 21:47:41 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 22 Apr 2021 21:48:15 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:a70d879fa5984474288d52009479054b8bb2993de2a1859f43b5480600cecb24`  
		Last Modified: Thu, 01 Apr 2021 15:20:06 GMT  
		Size: 28.6 MB (28569016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4394a92d1f8760cf7d17fee0bcee732c94c5b858dd8d19c7ff02beecf3b4e83`  
		Last Modified: Sat, 03 Apr 2021 00:54:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e6159c56c084c858f5de2416454ac0a49ddda47b764e4379c5d5a147c9bf5f`  
		Last Modified: Sat, 03 Apr 2021 00:54:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04b772c31f76720583412a2507c5c53889985db45169a85f0d3cd7f842e041a`  
		Last Modified: Sat, 03 Apr 2021 01:39:30 GMT  
		Size: 16.0 MB (16032891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf71362343a962febc8c6ce8c4fd12d961c5712407993471f60ac0e5d43415e`  
		Last Modified: Mon, 19 Apr 2021 18:30:17 GMT  
		Size: 42.4 MB (42440313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9163852ff25e45c3b95c7b759a719b91afa29724136e68d1cf7f822c034c4df`  
		Last Modified: Mon, 19 Apr 2021 18:30:04 GMT  
		Size: 4.0 MB (4025359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a723eb5427857d3e6f939a462cbbaeedb1b248662076fe72f2fab621d9acc3`  
		Last Modified: Thu, 22 Apr 2021 21:57:15 GMT  
		Size: 14.2 MB (14160245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0598dd9101a4447350e39fc9445131bdeb5a9bee7fc233879f0451c08a79fe`  
		Last Modified: Thu, 22 Apr 2021 21:57:12 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf163d48e000642c258afeea2bb09c0cca8829f72fcd792c97840c181f7331f8`  
		Last Modified: Thu, 22 Apr 2021 21:57:12 GMT  
		Size: 9.6 KB (9550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5906189dfc1fa00888b59c4cefad5a2f4aa3085bcc6da5d37e63197585a231c`  
		Last Modified: Thu, 22 Apr 2021 21:57:10 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062608db9cb7d8e8fc2dfa23464525e84b5d5fe1bc979194b937d8b2a4de74a6`  
		Last Modified: Thu, 22 Apr 2021 21:57:11 GMT  
		Size: 10.5 KB (10531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc2d74ce76564c5e8a6dafde72882602b446b3d3d81d620c5b1f08232a5a019`  
		Last Modified: Thu, 22 Apr 2021 21:57:11 GMT  
		Size: 2.6 MB (2555007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2717086accd7d50a5527b2b70f1177f08e904718f5388f702983ce093761304`  
		Last Modified: Thu, 22 Apr 2021 21:58:02 GMT  
		Size: 207.7 MB (207669936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b59e20e338e249cff7c3435973456929f13dfea41138604d3fe1696e479dc61`  
		Last Modified: Thu, 22 Apr 2021 21:57:50 GMT  
		Size: 944.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455eb33d7a0b34ae7cec9f9f41505c10dd6db2bd14f0f792b193a312a1c64b9e`  
		Last Modified: Thu, 22 Apr 2021 21:57:53 GMT  
		Size: 14.1 MB (14088088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:58d2df36fa80fd34c6efd19e002465a236bf9863e4fb5910f188695f8f0c6f0c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.5 MB (334494224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f187bd2be5cc7237467c10fb9155ab68dffc18d8c2e2b99ecd81a3b016a7f9`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:16:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 24 Apr 2021 01:19:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:28:36 GMT
ENV JAVA_VERSION=jdk-11.0.10+9_openj9-0.24.0
# Sat, 24 Apr 2021 01:30:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='5d2b2939637f999a1910d5cc0fb3d96756125941e5f8b9e3003635aa863664b5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        s390x)          ESUM='2ff9f50d6ffc345434703c43a1d67ac6d3d054b5d4925b4b73a3ce51b02940e5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7e5f97071f8b86c22c36ddfd7f821c3e8ec531c1128e2e6c931b2e64118a517a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 24 Apr 2021 01:30:48 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 24 Apr 2021 01:30:53 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Sat, 24 Apr 2021 01:31:37 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Sat, 24 Apr 2021 03:09:49 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 03:09:52 GMT
ARG OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:09:54 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Sat, 24 Apr 2021 03:09:57 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Sat, 24 Apr 2021 03:10:02 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Sat, 24 Apr 2021 03:10:05 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Sat, 24 Apr 2021 03:10:09 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Sat, 24 Apr 2021 03:10:15 GMT
ARG LIBERTY_URL
# Sat, 24 Apr 2021 03:10:19 GMT
ARG DOWNLOAD_OPTIONS=
# Sat, 24 Apr 2021 03:10:59 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 03:11:04 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 24 Apr 2021 03:11:08 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Sat, 24 Apr 2021 03:11:13 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:11:26 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Sat, 24 Apr 2021 03:11:28 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Sat, 24 Apr 2021 03:11:29 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Sat, 24 Apr 2021 03:11:41 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Sat, 24 Apr 2021 03:12:04 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Sat, 24 Apr 2021 03:12:09 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Sat, 24 Apr 2021 03:12:14 GMT
USER 1001
# Sat, 24 Apr 2021 03:12:25 GMT
EXPOSE 9080 9443
# Sat, 24 Apr 2021 03:12:36 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Sat, 24 Apr 2021 03:12:38 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Sat, 24 Apr 2021 03:19:14 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 03:19:16 GMT
ARG REPOSITORIES_PROPERTIES=
# Sat, 24 Apr 2021 03:22:47 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Sat, 24 Apr 2021 03:22:55 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Sat, 24 Apr 2021 03:24:07 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da07529aeac8fe5c90c5bb8c4f516c9d6fd248cc1daa5fecd137c809bce39bb6`  
		Last Modified: Sat, 24 Apr 2021 01:40:58 GMT  
		Size: 17.2 MB (17209103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53f9612e78ec5df6fbbbab4098deb40150ceef63be58aec6c2dd4df6af9f634`  
		Last Modified: Sat, 24 Apr 2021 01:46:21 GMT  
		Size: 43.3 MB (43277570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec133c54d62c9541f8b987c7353d67bd5d58ea39050f8cd947bf150d5ce8bb7a`  
		Last Modified: Sat, 24 Apr 2021 01:46:15 GMT  
		Size: 3.3 MB (3289250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062a0799a977bb2eb37a4a5544f4bd9dcb11b4139484efeb167d51a76dca344a`  
		Last Modified: Sat, 24 Apr 2021 03:57:40 GMT  
		Size: 14.2 MB (14161560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17e6eee9e8f60faaa4a97342c2158cd7796ac7bb6b08f138f711a9005741b36`  
		Last Modified: Sat, 24 Apr 2021 03:57:35 GMT  
		Size: 697.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b718a9fd82bc2a543e1c729118139996c38bc7710b89c7ecc990debf128858a`  
		Last Modified: Sat, 24 Apr 2021 03:57:35 GMT  
		Size: 9.6 KB (9554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f60415893707e5b040738d7e8a87ff3fa04cc21d7b2d5c85562332e2d497ea5`  
		Last Modified: Sat, 24 Apr 2021 03:57:35 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe6a41ec43a7b373422e863b76d451d0137a52c137e44b547ac9ad39fb73de2`  
		Last Modified: Sat, 24 Apr 2021 03:57:35 GMT  
		Size: 10.5 KB (10534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8aebc0ca7b2fb770385f3b4cfd9d7e7bac63d078e6c70044101e080ed32788e`  
		Last Modified: Sat, 24 Apr 2021 03:57:36 GMT  
		Size: 2.4 MB (2447444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b635648abb6c1d815d8bd988b55c7440c3dd8cd34211c0774827f2721c6022`  
		Last Modified: Sat, 24 Apr 2021 03:58:47 GMT  
		Size: 207.7 MB (207669849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52431dbbec59f34a44a99af91356d620b21524fe914b30b4c0dd9080ca5dee05`  
		Last Modified: Sat, 24 Apr 2021 03:58:27 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221e0c907c55b23b136a53cd5ece658f13412cb017e26a7c8b7d236b5ffcdaa9`  
		Last Modified: Sat, 24 Apr 2021 03:58:30 GMT  
		Size: 13.2 MB (13161022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:full-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:0d02e361435df46fff35ebc173579ebb1dafbc0713fa6fa5882156f0ac9abb76
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.6 MB (326645376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c382f67d2996379923080d0c01ae3039c6ef3b9f1e0b452d32958d81cd7e7487`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 21:45:20 GMT
ADD file:282d950116f923276efabd13c7dc17b942821edb14ffac4b89b9a50bcdf99e17 in / 
# Fri, 23 Apr 2021 21:45:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 21:45:27 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 21:45:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 21:45:29 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 22:03:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Apr 2021 22:04:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:10:11 GMT
ENV JAVA_VERSION=jdk-11.0.10+9_openj9-0.24.0
# Fri, 23 Apr 2021 22:11:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='5d2b2939637f999a1910d5cc0fb3d96756125941e5f8b9e3003635aa863664b5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        s390x)          ESUM='2ff9f50d6ffc345434703c43a1d67ac6d3d054b5d4925b4b73a3ce51b02940e5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7e5f97071f8b86c22c36ddfd7f821c3e8ec531c1128e2e6c931b2e64118a517a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 23 Apr 2021 22:11:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Apr 2021 22:11:44 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 23 Apr 2021 22:12:20 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 23 Apr 2021 23:17:55 GMT
ARG VERBOSE=false
# Fri, 23 Apr 2021 23:17:56 GMT
ARG OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:17:56 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Fri, 23 Apr 2021 23:17:57 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Fri, 23 Apr 2021 23:17:57 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Fri, 23 Apr 2021 23:17:58 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 23 Apr 2021 23:17:59 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Fri, 23 Apr 2021 23:17:59 GMT
ARG LIBERTY_URL
# Fri, 23 Apr 2021 23:18:00 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 23 Apr 2021 23:18:14 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:18:15 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Apr 2021 23:18:16 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Fri, 23 Apr 2021 23:18:16 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:18:18 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 23 Apr 2021 23:18:19 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Fri, 23 Apr 2021 23:18:19 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 23 Apr 2021 23:18:22 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 23 Apr 2021 23:18:32 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 23 Apr 2021 23:18:33 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 23 Apr 2021 23:18:34 GMT
USER 1001
# Fri, 23 Apr 2021 23:18:35 GMT
EXPOSE 9080 9443
# Fri, 23 Apr 2021 23:18:36 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 23 Apr 2021 23:18:36 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 23 Apr 2021 23:24:07 GMT
ARG VERBOSE=false
# Fri, 23 Apr 2021 23:24:07 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 23 Apr 2021 23:28:09 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Fri, 23 Apr 2021 23:28:21 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 23 Apr 2021 23:29:08 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:de53239ada2db01e7972c3f6eddcf6729f7cf3102be78e0b41363125ce7c2425`  
		Last Modified: Fri, 23 Apr 2021 21:47:14 GMT  
		Size: 27.1 MB (27136362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12932016d0f51acb5c5e5ba5b420a369401a7df47a219f24680bbc05ffde7e11`  
		Last Modified: Fri, 23 Apr 2021 21:47:10 GMT  
		Size: 840.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46997f76c5876e3274170b667463b3d88475cd696ccbc735d2f63965668673ad`  
		Last Modified: Fri, 23 Apr 2021 21:47:10 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bab416938acf6dd045c9fc9097e5768c61b5899b07d110ab3844f447e12b113`  
		Last Modified: Fri, 23 Apr 2021 22:19:05 GMT  
		Size: 15.7 MB (15741779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0273d3bc7cd55960a36b00d19e8d51f8bbeed03d24fd8d551c957fc19ef079b`  
		Last Modified: Fri, 23 Apr 2021 22:22:19 GMT  
		Size: 42.0 MB (41951613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95422aa686364d2877a279281f6eb1157805fa8516aa976b06ce8889dc9f932`  
		Last Modified: Fri, 23 Apr 2021 22:22:13 GMT  
		Size: 3.8 MB (3836026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f024126ee5e04e37dd48573fe2e6aefd2d98012df116b366e0aef9fa63b8ba93`  
		Last Modified: Fri, 23 Apr 2021 23:54:00 GMT  
		Size: 14.2 MB (14160729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a63a9d57fd3b2ed838f0044559d5cfa241eab25d7626378b2fd1c5463947a9`  
		Last Modified: Fri, 23 Apr 2021 23:53:57 GMT  
		Size: 687.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62def58659c4a5a6fd3cde1c4245691f62a7d197ac87536975c7c888e8fd5ff`  
		Last Modified: Fri, 23 Apr 2021 23:53:57 GMT  
		Size: 9.6 KB (9551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288fec31697eb659f1a7285ca37ce8460c07bd8485fdb21628ff246a6661660d`  
		Last Modified: Fri, 23 Apr 2021 23:53:57 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bce08718a41817d4e1e9dd6bb83ac83f3a1c3014753a04447805c257e51a9c3`  
		Last Modified: Fri, 23 Apr 2021 23:53:57 GMT  
		Size: 10.5 KB (10544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3096c60acccc8db5e2ef0df733a4693cf8068658a1fc8af639461c112c1589a`  
		Last Modified: Fri, 23 Apr 2021 23:53:57 GMT  
		Size: 2.5 MB (2491647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d29297ab00722488619fd9526e89b49277ed66bac34206e8f7e2cb0917e1945`  
		Last Modified: Fri, 23 Apr 2021 23:54:35 GMT  
		Size: 207.7 MB (207671747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b7a66a256bd33f418c1622886d5384d5a5abc02e2c3b042d528a7153211728`  
		Last Modified: Fri, 23 Apr 2021 23:54:24 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba111cf88078cf3a5f862c69d813cf4940c21337daefa46d9c6a9818aae58d8e`  
		Last Modified: Fri, 23 Apr 2021 23:54:26 GMT  
		Size: 13.6 MB (13632445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:kernel`

```console
$ docker pull websphere-liberty@sha256:74c8aa16d709c8f57af5fd0a01f701cce4e0dfbeafa65473e585dbb44898935c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:kernel` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:f528365190e853e1ffbc72c586114358fb2eb6e0117c4134f68e0e57894f6f24
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180293270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79615f972bc823a2954599784f3311d9cd8c7d4e5bc2ee82a917c4f753326937`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 09:30:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 26 Mar 2021 09:31:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 09:31:04 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 26 Mar 2021 09:31:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Mar 2021 09:31:42 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 26 Mar 2021 21:31:17 GMT
ARG VERBOSE=false
# Fri, 26 Mar 2021 21:31:18 GMT
ARG OPENJ9_SCC=true
# Thu, 22 Apr 2021 21:40:06 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Thu, 22 Apr 2021 21:40:06 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Thu, 22 Apr 2021 21:40:06 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Thu, 22 Apr 2021 21:40:06 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 22 Apr 2021 21:40:06 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Thu, 22 Apr 2021 21:40:07 GMT
ARG LIBERTY_URL
# Thu, 22 Apr 2021 21:40:07 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 22 Apr 2021 21:40:24 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Apr 2021 21:40:24 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Apr 2021 21:40:24 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Thu, 22 Apr 2021 21:40:24 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 22 Apr 2021 21:40:26 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Apr 2021 21:40:26 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Thu, 22 Apr 2021 21:40:26 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Apr 2021 21:40:28 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Apr 2021 21:40:38 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Apr 2021 21:40:38 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 22 Apr 2021 21:40:38 GMT
USER 1001
# Thu, 22 Apr 2021 21:40:39 GMT
EXPOSE 9080 9443
# Thu, 22 Apr 2021 21:40:39 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Apr 2021 21:40:39 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4764ed71d2900c9874838108e377eb8821088502d5504fadeb080e5dd1a3e65d`  
		Last Modified: Fri, 26 Mar 2021 09:35:47 GMT  
		Size: 3.0 MB (2958415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf5000c541da177b7cfe59bf3ff8cb271529f443ee224bf88989910e9a2abb1`  
		Last Modified: Fri, 26 Mar 2021 09:36:01 GMT  
		Size: 130.8 MB (130805802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33df46370333075337eb25c08aa74c706467351aa5abe9711e870aa5e647baaf`  
		Last Modified: Thu, 22 Apr 2021 21:57:02 GMT  
		Size: 14.1 MB (14061162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d854faca6db468012fcae8e445cd69affeb82c5efbb89ac2b53b719cb4eabd`  
		Last Modified: Thu, 22 Apr 2021 21:56:58 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f56d571437c689e2188bb2653cbbaf3ef56de28093fd63e3229a142d9d87fa`  
		Last Modified: Thu, 22 Apr 2021 21:56:58 GMT  
		Size: 9.6 KB (9556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fde75a052b81ad9ca202510ebedb5083754ed163d499a6f28f1be76b6615ad`  
		Last Modified: Thu, 22 Apr 2021 21:56:58 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610a90e750f1b7eb794e24a2970acb3b9f79a569ed064d70771895e2cf5c4795`  
		Last Modified: Thu, 22 Apr 2021 21:56:58 GMT  
		Size: 10.5 KB (10544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3782c27b14b1eea6ec7f8a3c56182ccbf3a0db0e5a00cb4aad829f8b16f628b1`  
		Last Modified: Thu, 22 Apr 2021 21:56:59 GMT  
		Size: 5.7 MB (5734998 bytes)  
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
$ docker pull websphere-liberty@sha256:a6fba29d04471e2eff94691224c8ff16b7c962a1ec9e18b5d03865993d75613c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183281635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c365f977369905b70d1ba9f75dc6b19ce4ae1f730890957000463778aa9458`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 22:30:25 GMT
ADD file:818f810cd30ef74fd4690c6265d80265647ba3353880cf8323500df6d2c48b69 in / 
# Fri, 23 Apr 2021 22:30:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:31:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:31:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:31:32 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:16:58 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 23 Apr 2021 23:17:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:17:43 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 23 Apr 2021 23:18:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 23 Apr 2021 23:19:03 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Sat, 24 Apr 2021 03:07:07 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 03:07:12 GMT
ARG OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:07:15 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Sat, 24 Apr 2021 03:07:18 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Sat, 24 Apr 2021 03:07:22 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Sat, 24 Apr 2021 03:07:25 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Sat, 24 Apr 2021 03:07:30 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Sat, 24 Apr 2021 03:07:35 GMT
ARG LIBERTY_URL
# Sat, 24 Apr 2021 03:07:39 GMT
ARG DOWNLOAD_OPTIONS=
# Sat, 24 Apr 2021 03:08:16 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 03:08:18 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 24 Apr 2021 03:08:20 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Sat, 24 Apr 2021 03:08:21 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:08:37 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Sat, 24 Apr 2021 03:08:40 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Sat, 24 Apr 2021 03:08:42 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Sat, 24 Apr 2021 03:08:53 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Sat, 24 Apr 2021 03:09:13 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Sat, 24 Apr 2021 03:09:19 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Sat, 24 Apr 2021 03:09:24 GMT
USER 1001
# Sat, 24 Apr 2021 03:09:27 GMT
EXPOSE 9080 9443
# Sat, 24 Apr 2021 03:09:30 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Sat, 24 Apr 2021 03:09:34 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:bb3095714506c08a64a49e29ab001d7000d94957d52e05db35361fd4a54c460c`  
		Last Modified: Fri, 23 Apr 2021 22:36:52 GMT  
		Size: 30.4 MB (30407300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd29acc6f7bfef8034eaca0bfb069f0d66e50351c84b062e224d6eae710afa79`  
		Last Modified: Fri, 23 Apr 2021 22:36:46 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7645fc50c9e70df51732b36ef7f8b21ebacd148c3bee4f1b29ca6dcba1bbb949`  
		Last Modified: Fri, 23 Apr 2021 22:36:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab6dc42492fe0eca98f1e563f3e8dabb70f122b45b752264bacb4ea14f59354`  
		Last Modified: Fri, 23 Apr 2021 23:22:26 GMT  
		Size: 3.1 MB (3082775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510992b332e039a7852bef411702a4b667a17ae9ef201c9118477ccc53172fa8`  
		Last Modified: Fri, 23 Apr 2021 23:22:40 GMT  
		Size: 130.4 MB (130406625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de545400b0a4b20e99a41bb03dd0464d3f4e6b22326a58a0f8a6f27df35ed53`  
		Last Modified: Sat, 24 Apr 2021 03:57:21 GMT  
		Size: 14.1 MB (14062037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19c270fd954ab1850546a2f1fe907e5812464bb308554d74ff3b77fe4d085a5`  
		Last Modified: Sat, 24 Apr 2021 03:57:16 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b461e2c9230ad6d7e36d9fddcc2d3d04a394954d5b5437473fde9a958d54c05c`  
		Last Modified: Sat, 24 Apr 2021 03:57:15 GMT  
		Size: 9.6 KB (9557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0821ea49c2f2252a0938a998b8388c6f28a42fa11fcea87f34c94c523b2a1e`  
		Last Modified: Sat, 24 Apr 2021 03:57:15 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b875abf5447191fb37fb076a3def6e4623314c82cf9c399a82e81f2d7fbfdd`  
		Last Modified: Sat, 24 Apr 2021 03:57:16 GMT  
		Size: 10.5 KB (10548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1dc37ac444dea5f60b5a444e3fe1cf82f9c846fe2eef1d199c48742f541072e`  
		Last Modified: Sat, 24 Apr 2021 03:57:17 GMT  
		Size: 5.3 MB (5300774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:0d7dafd042d0d2cc8eb4580d0db30ada5047e8848c332172235044b128158d2f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176103462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a099f0ae43c0fd8c3e964020f65971f96b5f6988450d42231f7333bb9b4fb8f2`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 21:45:00 GMT
ADD file:5e61a5300d520d61a2130623465ba2e46da8e80dc2afa042473a42cbcd8d88d2 in / 
# Fri, 23 Apr 2021 21:45:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 21:45:05 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 21:45:07 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 21:45:07 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 22:25:02 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 23 Apr 2021 22:25:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:25:17 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 23 Apr 2021 22:26:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 23 Apr 2021 22:26:15 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 23 Apr 2021 23:16:58 GMT
ARG VERBOSE=false
# Fri, 23 Apr 2021 23:16:58 GMT
ARG OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:16:59 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Fri, 23 Apr 2021 23:17:00 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Fri, 23 Apr 2021 23:17:00 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Fri, 23 Apr 2021 23:17:01 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 23 Apr 2021 23:17:02 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Fri, 23 Apr 2021 23:17:02 GMT
ARG LIBERTY_URL
# Fri, 23 Apr 2021 23:17:03 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 23 Apr 2021 23:17:18 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:17:20 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Apr 2021 23:17:21 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Fri, 23 Apr 2021 23:17:21 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:17:23 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 23 Apr 2021 23:17:24 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Fri, 23 Apr 2021 23:17:25 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 23 Apr 2021 23:17:27 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 23 Apr 2021 23:17:40 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 23 Apr 2021 23:17:41 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 23 Apr 2021 23:17:42 GMT
USER 1001
# Fri, 23 Apr 2021 23:17:42 GMT
EXPOSE 9080 9443
# Fri, 23 Apr 2021 23:17:43 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 23 Apr 2021 23:17:43 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:33ddddc4572ffe1f294f9f599ed989cc41eee5da4cdcf7db12d10700aa8c894e`  
		Last Modified: Fri, 23 Apr 2021 21:47:03 GMT  
		Size: 25.4 MB (25352756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4395f372a786db91b2f50dc8e43d8b7c3533eb4bd86f6728eb2a0c7108c077d2`  
		Last Modified: Fri, 23 Apr 2021 21:46:59 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e39753730df188282ca8193f14bbbb8cbe0b76ec02b34283a28449b1e41c05`  
		Last Modified: Fri, 23 Apr 2021 21:47:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e93b87da546ac7aa6705cd2f20bfe70cf04793ac73561e5dd8c579af88754aec`  
		Last Modified: Fri, 23 Apr 2021 22:28:41 GMT  
		Size: 2.7 MB (2676643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268462fc02d2bd9da227784f5f243759923a14cefb3648739ca02e8fa7d63ee7`  
		Last Modified: Fri, 23 Apr 2021 22:28:50 GMT  
		Size: 128.1 MB (128065984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895091e75a5c1ee863c074a41c334973d986bb55cef3d4ba2f8267a2887f8336`  
		Last Modified: Fri, 23 Apr 2021 23:53:50 GMT  
		Size: 14.1 MB (14061390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26d2145efe41abadeb2694f43164f1a155e500e85bf004da26812cd8532de7f`  
		Last Modified: Fri, 23 Apr 2021 23:53:47 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1dc41aa938b0af86dfd6446147e4484cb5d6bad6e84eb2edb074790b0615a1`  
		Last Modified: Fri, 23 Apr 2021 23:53:47 GMT  
		Size: 9.6 KB (9556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0e2666f7e25fefd1dfbbb522189283388626a78a6993958a175bfe3d453daa`  
		Last Modified: Fri, 23 Apr 2021 23:53:47 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1422da1f78c4ff3f196f908ccd43d884e84e4586193eab1bfe59df39b352b130`  
		Last Modified: Fri, 23 Apr 2021 23:53:47 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6a848b971c7539a51ff9771c57f7df448cc5b960c0be0fa5b3c3b547e8589c`  
		Last Modified: Fri, 23 Apr 2021 23:53:47 GMT  
		Size: 5.9 MB (5924580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:kernel-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:6f6653874c0eb28bb81144c3bc83a1895c1cde222cf3866e260bdd2daa7cb31b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:kernel-java11-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:089c25ea4ac42c4cedb0b974d8cf29185eb9c3ec4e86fa10817a8afa5de7f601
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107804910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98fb4f6747d498676b24bc7bf8aa4905b802d1f2ed2d3b27bce67a59d00748c5`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Sat, 03 Apr 2021 00:53:06 GMT
ADD file:27277aee655dd263ee698d1f2fe17f0b1dbba740615bcac8642723a6ac0d62be in / 
# Sat, 03 Apr 2021 00:53:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Sat, 03 Apr 2021 00:53:08 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Sat, 03 Apr 2021 00:53:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Sat, 03 Apr 2021 00:53:09 GMT
CMD ["/bin/bash"]
# Sat, 03 Apr 2021 01:29:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 03 Apr 2021 01:29:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 03 Apr 2021 01:32:52 GMT
ENV JAVA_VERSION=jdk-11.0.10+9_openj9-0.24.0
# Mon, 19 Apr 2021 18:22:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='5d2b2939637f999a1910d5cc0fb3d96756125941e5f8b9e3003635aa863664b5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        s390x)          ESUM='2ff9f50d6ffc345434703c43a1d67ac6d3d054b5d4925b4b73a3ce51b02940e5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7e5f97071f8b86c22c36ddfd7f821c3e8ec531c1128e2e6c931b2e64118a517a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 19 Apr 2021 18:22:34 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Apr 2021 18:22:34 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 19 Apr 2021 18:23:10 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Thu, 22 Apr 2021 21:40:48 GMT
ARG VERBOSE=false
# Thu, 22 Apr 2021 21:40:48 GMT
ARG OPENJ9_SCC=true
# Thu, 22 Apr 2021 21:40:48 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Thu, 22 Apr 2021 21:40:49 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Thu, 22 Apr 2021 21:40:49 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Thu, 22 Apr 2021 21:40:49 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 22 Apr 2021 21:40:49 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Thu, 22 Apr 2021 21:40:49 GMT
ARG LIBERTY_URL
# Thu, 22 Apr 2021 21:40:49 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 22 Apr 2021 21:40:58 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Apr 2021 21:40:58 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Apr 2021 21:40:58 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Thu, 22 Apr 2021 21:40:58 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 22 Apr 2021 21:41:00 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Apr 2021 21:41:00 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Thu, 22 Apr 2021 21:41:00 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Apr 2021 21:41:01 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Apr 2021 21:41:09 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Apr 2021 21:41:09 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Thu, 22 Apr 2021 21:41:09 GMT
USER 1001
# Thu, 22 Apr 2021 21:41:10 GMT
EXPOSE 9080 9443
# Thu, 22 Apr 2021 21:41:10 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Apr 2021 21:41:10 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:a70d879fa5984474288d52009479054b8bb2993de2a1859f43b5480600cecb24`  
		Last Modified: Thu, 01 Apr 2021 15:20:06 GMT  
		Size: 28.6 MB (28569016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4394a92d1f8760cf7d17fee0bcee732c94c5b858dd8d19c7ff02beecf3b4e83`  
		Last Modified: Sat, 03 Apr 2021 00:54:10 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e6159c56c084c858f5de2416454ac0a49ddda47b764e4379c5d5a147c9bf5f`  
		Last Modified: Sat, 03 Apr 2021 00:54:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04b772c31f76720583412a2507c5c53889985db45169a85f0d3cd7f842e041a`  
		Last Modified: Sat, 03 Apr 2021 01:39:30 GMT  
		Size: 16.0 MB (16032891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf71362343a962febc8c6ce8c4fd12d961c5712407993471f60ac0e5d43415e`  
		Last Modified: Mon, 19 Apr 2021 18:30:17 GMT  
		Size: 42.4 MB (42440313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9163852ff25e45c3b95c7b759a719b91afa29724136e68d1cf7f822c034c4df`  
		Last Modified: Mon, 19 Apr 2021 18:30:04 GMT  
		Size: 4.0 MB (4025359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a723eb5427857d3e6f939a462cbbaeedb1b248662076fe72f2fab621d9acc3`  
		Last Modified: Thu, 22 Apr 2021 21:57:15 GMT  
		Size: 14.2 MB (14160245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0598dd9101a4447350e39fc9445131bdeb5a9bee7fc233879f0451c08a79fe`  
		Last Modified: Thu, 22 Apr 2021 21:57:12 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf163d48e000642c258afeea2bb09c0cca8829f72fcd792c97840c181f7331f8`  
		Last Modified: Thu, 22 Apr 2021 21:57:12 GMT  
		Size: 9.6 KB (9550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5906189dfc1fa00888b59c4cefad5a2f4aa3085bcc6da5d37e63197585a231c`  
		Last Modified: Thu, 22 Apr 2021 21:57:10 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062608db9cb7d8e8fc2dfa23464525e84b5d5fe1bc979194b937d8b2a4de74a6`  
		Last Modified: Thu, 22 Apr 2021 21:57:11 GMT  
		Size: 10.5 KB (10531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc2d74ce76564c5e8a6dafde72882602b446b3d3d81d620c5b1f08232a5a019`  
		Last Modified: Thu, 22 Apr 2021 21:57:11 GMT  
		Size: 2.6 MB (2555007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel-java11-openj9` - linux; ppc64le

```console
$ docker pull websphere-liberty@sha256:b76395a786647b5473b28d061e02e1c5276f807eddc0c4653dfdce8891c629f3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.7 MB (113662407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d1a5de89d5c2bac2a0c0f64e4b0f9560bb1f9b6fef00a8be97351e87832bc2`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 22:31:45 GMT
ADD file:ec80070ca931734843261734e9ca18cd45a6130030c1a25abac3268e54776be5 in / 
# Fri, 23 Apr 2021 22:32:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:32:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:32:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:32:38 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 01:16:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 24 Apr 2021 01:19:33 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 01:28:36 GMT
ENV JAVA_VERSION=jdk-11.0.10+9_openj9-0.24.0
# Sat, 24 Apr 2021 01:30:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='5d2b2939637f999a1910d5cc0fb3d96756125941e5f8b9e3003635aa863664b5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        s390x)          ESUM='2ff9f50d6ffc345434703c43a1d67ac6d3d054b5d4925b4b73a3ce51b02940e5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7e5f97071f8b86c22c36ddfd7f821c3e8ec531c1128e2e6c931b2e64118a517a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 24 Apr 2021 01:30:48 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 24 Apr 2021 01:30:53 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Sat, 24 Apr 2021 01:31:37 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Sat, 24 Apr 2021 03:09:49 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 03:09:52 GMT
ARG OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:09:54 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Sat, 24 Apr 2021 03:09:57 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Sat, 24 Apr 2021 03:10:02 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Sat, 24 Apr 2021 03:10:05 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Sat, 24 Apr 2021 03:10:09 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Sat, 24 Apr 2021 03:10:15 GMT
ARG LIBERTY_URL
# Sat, 24 Apr 2021 03:10:19 GMT
ARG DOWNLOAD_OPTIONS=
# Sat, 24 Apr 2021 03:10:59 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 03:11:04 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 24 Apr 2021 03:11:08 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Sat, 24 Apr 2021 03:11:13 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:11:26 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Sat, 24 Apr 2021 03:11:28 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Sat, 24 Apr 2021 03:11:29 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Sat, 24 Apr 2021 03:11:41 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Sat, 24 Apr 2021 03:12:04 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Sat, 24 Apr 2021 03:12:09 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Sat, 24 Apr 2021 03:12:14 GMT
USER 1001
# Sat, 24 Apr 2021 03:12:25 GMT
EXPOSE 9080 9443
# Sat, 24 Apr 2021 03:12:36 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Sat, 24 Apr 2021 03:12:38 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:8cdb522ceff72cef6133f5b26b5f9eac72760a06a86d5d6b7db34a5dde7b156f`  
		Last Modified: Fri, 23 Apr 2021 22:37:11 GMT  
		Size: 33.3 MB (33255388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21136d6107eea0892211e712ba6b20d15f74a37dd1bde1b2f0802e083e85c183`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a03f1456f472e398050e94cf3ac8873969ce172a153bb511be780fe49403c47`  
		Last Modified: Fri, 23 Apr 2021 22:37:05 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da07529aeac8fe5c90c5bb8c4f516c9d6fd248cc1daa5fecd137c809bce39bb6`  
		Last Modified: Sat, 24 Apr 2021 01:40:58 GMT  
		Size: 17.2 MB (17209103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53f9612e78ec5df6fbbbab4098deb40150ceef63be58aec6c2dd4df6af9f634`  
		Last Modified: Sat, 24 Apr 2021 01:46:21 GMT  
		Size: 43.3 MB (43277570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec133c54d62c9541f8b987c7353d67bd5d58ea39050f8cd947bf150d5ce8bb7a`  
		Last Modified: Sat, 24 Apr 2021 01:46:15 GMT  
		Size: 3.3 MB (3289250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062a0799a977bb2eb37a4a5544f4bd9dcb11b4139484efeb167d51a76dca344a`  
		Last Modified: Sat, 24 Apr 2021 03:57:40 GMT  
		Size: 14.2 MB (14161560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d17e6eee9e8f60faaa4a97342c2158cd7796ac7bb6b08f138f711a9005741b36`  
		Last Modified: Sat, 24 Apr 2021 03:57:35 GMT  
		Size: 697.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b718a9fd82bc2a543e1c729118139996c38bc7710b89c7ecc990debf128858a`  
		Last Modified: Sat, 24 Apr 2021 03:57:35 GMT  
		Size: 9.6 KB (9554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f60415893707e5b040738d7e8a87ff3fa04cc21d7b2d5c85562332e2d497ea5`  
		Last Modified: Sat, 24 Apr 2021 03:57:35 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe6a41ec43a7b373422e863b76d451d0137a52c137e44b547ac9ad39fb73de2`  
		Last Modified: Sat, 24 Apr 2021 03:57:35 GMT  
		Size: 10.5 KB (10534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8aebc0ca7b2fb770385f3b4cfd9d7e7bac63d078e6c70044101e080ed32788e`  
		Last Modified: Sat, 24 Apr 2021 03:57:36 GMT  
		Size: 2.4 MB (2447444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:kernel-java11-openj9` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:7da2d996a0edd7759eef333322be612a3aa048d1c48ffec09bef5d1d8aca195e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105340236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0450ad9b23e181ff9223541e51f3bd15bdc098a0b0e011fda20432f21f2b5467`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 21:45:20 GMT
ADD file:282d950116f923276efabd13c7dc17b942821edb14ffac4b89b9a50bcdf99e17 in / 
# Fri, 23 Apr 2021 21:45:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 21:45:27 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 21:45:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 21:45:29 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 22:03:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Apr 2021 22:04:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:10:11 GMT
ENV JAVA_VERSION=jdk-11.0.10+9_openj9-0.24.0
# Fri, 23 Apr 2021 22:11:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='5d2b2939637f999a1910d5cc0fb3d96756125941e5f8b9e3003635aa863664b5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        s390x)          ESUM='2ff9f50d6ffc345434703c43a1d67ac6d3d054b5d4925b4b73a3ce51b02940e5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7e5f97071f8b86c22c36ddfd7f821c3e8ec531c1128e2e6c931b2e64118a517a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 23 Apr 2021 22:11:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Apr 2021 22:11:44 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 23 Apr 2021 22:12:20 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 23 Apr 2021 23:17:55 GMT
ARG VERBOSE=false
# Fri, 23 Apr 2021 23:17:56 GMT
ARG OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:17:56 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Fri, 23 Apr 2021 23:17:57 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Fri, 23 Apr 2021 23:17:57 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Fri, 23 Apr 2021 23:17:58 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 23 Apr 2021 23:17:59 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Fri, 23 Apr 2021 23:17:59 GMT
ARG LIBERTY_URL
# Fri, 23 Apr 2021 23:18:00 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 23 Apr 2021 23:18:14 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:18:15 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Apr 2021 23:18:16 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Fri, 23 Apr 2021 23:18:16 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:18:18 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 23 Apr 2021 23:18:19 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Fri, 23 Apr 2021 23:18:19 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 23 Apr 2021 23:18:22 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 23 Apr 2021 23:18:32 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 23 Apr 2021 23:18:33 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Fri, 23 Apr 2021 23:18:34 GMT
USER 1001
# Fri, 23 Apr 2021 23:18:35 GMT
EXPOSE 9080 9443
# Fri, 23 Apr 2021 23:18:36 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 23 Apr 2021 23:18:36 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
```

-	Layers:
	-	`sha256:de53239ada2db01e7972c3f6eddcf6729f7cf3102be78e0b41363125ce7c2425`  
		Last Modified: Fri, 23 Apr 2021 21:47:14 GMT  
		Size: 27.1 MB (27136362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12932016d0f51acb5c5e5ba5b420a369401a7df47a219f24680bbc05ffde7e11`  
		Last Modified: Fri, 23 Apr 2021 21:47:10 GMT  
		Size: 840.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46997f76c5876e3274170b667463b3d88475cd696ccbc735d2f63965668673ad`  
		Last Modified: Fri, 23 Apr 2021 21:47:10 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bab416938acf6dd045c9fc9097e5768c61b5899b07d110ab3844f447e12b113`  
		Last Modified: Fri, 23 Apr 2021 22:19:05 GMT  
		Size: 15.7 MB (15741779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0273d3bc7cd55960a36b00d19e8d51f8bbeed03d24fd8d551c957fc19ef079b`  
		Last Modified: Fri, 23 Apr 2021 22:22:19 GMT  
		Size: 42.0 MB (41951613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95422aa686364d2877a279281f6eb1157805fa8516aa976b06ce8889dc9f932`  
		Last Modified: Fri, 23 Apr 2021 22:22:13 GMT  
		Size: 3.8 MB (3836026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f024126ee5e04e37dd48573fe2e6aefd2d98012df116b366e0aef9fa63b8ba93`  
		Last Modified: Fri, 23 Apr 2021 23:54:00 GMT  
		Size: 14.2 MB (14160729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a63a9d57fd3b2ed838f0044559d5cfa241eab25d7626378b2fd1c5463947a9`  
		Last Modified: Fri, 23 Apr 2021 23:53:57 GMT  
		Size: 687.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62def58659c4a5a6fd3cde1c4245691f62a7d197ac87536975c7c888e8fd5ff`  
		Last Modified: Fri, 23 Apr 2021 23:53:57 GMT  
		Size: 9.6 KB (9551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288fec31697eb659f1a7285ca37ce8460c07bd8485fdb21628ff246a6661660d`  
		Last Modified: Fri, 23 Apr 2021 23:53:57 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bce08718a41817d4e1e9dd6bb83ac83f3a1c3014753a04447805c257e51a9c3`  
		Last Modified: Fri, 23 Apr 2021 23:53:57 GMT  
		Size: 10.5 KB (10544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3096c60acccc8db5e2ef0df733a4693cf8068658a1fc8af639461c112c1589a`  
		Last Modified: Fri, 23 Apr 2021 23:53:57 GMT  
		Size: 2.5 MB (2491647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `websphere-liberty:latest`

```console
$ docker pull websphere-liberty@sha256:0fa2d01a01dd7a58472a2717c5067d89db1b966b2d780278cd7253be29f9ce3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:latest` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:750da2549ddcfbd3e9ae2850b9ae2347adbb712410041faf8a02a81d635d2cde
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.8 MB (414810589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bfd08f9c2afdc6e2530607e9db350908221943ae7b3a387ed47fde3bad081c`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 09:30:54 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 26 Mar 2021 09:31:04 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 09:31:04 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 26 Mar 2021 09:31:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 26 Mar 2021 09:31:42 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 26 Mar 2021 21:31:17 GMT
ARG VERBOSE=false
# Fri, 26 Mar 2021 21:31:18 GMT
ARG OPENJ9_SCC=true
# Thu, 22 Apr 2021 21:40:06 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Thu, 22 Apr 2021 21:40:06 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Thu, 22 Apr 2021 21:40:06 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Thu, 22 Apr 2021 21:40:06 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Thu, 22 Apr 2021 21:40:06 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Thu, 22 Apr 2021 21:40:07 GMT
ARG LIBERTY_URL
# Thu, 22 Apr 2021 21:40:07 GMT
ARG DOWNLOAD_OPTIONS=
# Thu, 22 Apr 2021 21:40:24 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Thu, 22 Apr 2021 21:40:24 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Apr 2021 21:40:24 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Thu, 22 Apr 2021 21:40:24 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Thu, 22 Apr 2021 21:40:26 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Thu, 22 Apr 2021 21:40:26 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Thu, 22 Apr 2021 21:40:26 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Thu, 22 Apr 2021 21:40:28 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Thu, 22 Apr 2021 21:40:38 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Thu, 22 Apr 2021 21:40:38 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Thu, 22 Apr 2021 21:40:38 GMT
USER 1001
# Thu, 22 Apr 2021 21:40:39 GMT
EXPOSE 9080 9443
# Thu, 22 Apr 2021 21:40:39 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Thu, 22 Apr 2021 21:40:39 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Thu, 22 Apr 2021 21:41:13 GMT
ARG VERBOSE=false
# Thu, 22 Apr 2021 21:41:13 GMT
ARG REPOSITORIES_PROPERTIES=
# Thu, 22 Apr 2021 21:44:16 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Thu, 22 Apr 2021 21:44:16 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Thu, 22 Apr 2021 21:44:52 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4764ed71d2900c9874838108e377eb8821088502d5504fadeb080e5dd1a3e65d`  
		Last Modified: Fri, 26 Mar 2021 09:35:47 GMT  
		Size: 3.0 MB (2958415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf5000c541da177b7cfe59bf3ff8cb271529f443ee224bf88989910e9a2abb1`  
		Last Modified: Fri, 26 Mar 2021 09:36:01 GMT  
		Size: 130.8 MB (130805802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33df46370333075337eb25c08aa74c706467351aa5abe9711e870aa5e647baaf`  
		Last Modified: Thu, 22 Apr 2021 21:57:02 GMT  
		Size: 14.1 MB (14061162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d854faca6db468012fcae8e445cd69affeb82c5efbb89ac2b53b719cb4eabd`  
		Last Modified: Thu, 22 Apr 2021 21:56:58 GMT  
		Size: 699.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f56d571437c689e2188bb2653cbbaf3ef56de28093fd63e3229a142d9d87fa`  
		Last Modified: Thu, 22 Apr 2021 21:56:58 GMT  
		Size: 9.6 KB (9556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5fde75a052b81ad9ca202510ebedb5083754ed163d499a6f28f1be76b6615ad`  
		Last Modified: Thu, 22 Apr 2021 21:56:58 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610a90e750f1b7eb794e24a2970acb3b9f79a569ed064d70771895e2cf5c4795`  
		Last Modified: Thu, 22 Apr 2021 21:56:58 GMT  
		Size: 10.5 KB (10544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3782c27b14b1eea6ec7f8a3c56182ccbf3a0db0e5a00cb4aad829f8b16f628b1`  
		Last Modified: Thu, 22 Apr 2021 21:56:59 GMT  
		Size: 5.7 MB (5734998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f94a4feba9d432ba504a626d7c726342855fc5baffbda070b24e905aa4d6f2`  
		Last Modified: Thu, 22 Apr 2021 21:57:36 GMT  
		Size: 213.4 MB (213364505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f32f1e0b41195d19cb5b1bc063af6b2ebd037fee723a18c58cee092d68b465`  
		Last Modified: Thu, 22 Apr 2021 21:57:24 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926bbbd582bf41deb09392c6714bc00b03c3a35a16db042c445f171588d03f52`  
		Last Modified: Thu, 22 Apr 2021 21:57:28 GMT  
		Size: 21.2 MB (21151866 bytes)  
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
$ docker pull websphere-liberty@sha256:9e6931d099e61e14b50000de09a805e628326d2ca36b7f785fb87afddb5f31b7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.8 MB (414816829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:145832e765296a2c9cf6f91cac745f6fdb49cea3740a2436251f4f16d501ae05`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 22:30:25 GMT
ADD file:818f810cd30ef74fd4690c6265d80265647ba3353880cf8323500df6d2c48b69 in / 
# Fri, 23 Apr 2021 22:30:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:31:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:31:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:31:32 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:16:58 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 23 Apr 2021 23:17:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:17:43 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 23 Apr 2021 23:18:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 23 Apr 2021 23:19:03 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Sat, 24 Apr 2021 03:07:07 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 03:07:12 GMT
ARG OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:07:15 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Sat, 24 Apr 2021 03:07:18 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Sat, 24 Apr 2021 03:07:22 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Sat, 24 Apr 2021 03:07:25 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Sat, 24 Apr 2021 03:07:30 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Sat, 24 Apr 2021 03:07:35 GMT
ARG LIBERTY_URL
# Sat, 24 Apr 2021 03:07:39 GMT
ARG DOWNLOAD_OPTIONS=
# Sat, 24 Apr 2021 03:08:16 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 03:08:18 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 24 Apr 2021 03:08:20 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Sat, 24 Apr 2021 03:08:21 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Sat, 24 Apr 2021 03:08:37 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Sat, 24 Apr 2021 03:08:40 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Sat, 24 Apr 2021 03:08:42 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Sat, 24 Apr 2021 03:08:53 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Sat, 24 Apr 2021 03:09:13 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Sat, 24 Apr 2021 03:09:19 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Sat, 24 Apr 2021 03:09:24 GMT
USER 1001
# Sat, 24 Apr 2021 03:09:27 GMT
EXPOSE 9080 9443
# Sat, 24 Apr 2021 03:09:30 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Sat, 24 Apr 2021 03:09:34 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Sat, 24 Apr 2021 03:12:46 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 03:12:51 GMT
ARG REPOSITORIES_PROPERTIES=
# Sat, 24 Apr 2021 03:17:43 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Sat, 24 Apr 2021 03:17:46 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Sat, 24 Apr 2021 03:18:58 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:bb3095714506c08a64a49e29ab001d7000d94957d52e05db35361fd4a54c460c`  
		Last Modified: Fri, 23 Apr 2021 22:36:52 GMT  
		Size: 30.4 MB (30407300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd29acc6f7bfef8034eaca0bfb069f0d66e50351c84b062e224d6eae710afa79`  
		Last Modified: Fri, 23 Apr 2021 22:36:46 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7645fc50c9e70df51732b36ef7f8b21ebacd148c3bee4f1b29ca6dcba1bbb949`  
		Last Modified: Fri, 23 Apr 2021 22:36:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab6dc42492fe0eca98f1e563f3e8dabb70f122b45b752264bacb4ea14f59354`  
		Last Modified: Fri, 23 Apr 2021 23:22:26 GMT  
		Size: 3.1 MB (3082775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510992b332e039a7852bef411702a4b667a17ae9ef201c9118477ccc53172fa8`  
		Last Modified: Fri, 23 Apr 2021 23:22:40 GMT  
		Size: 130.4 MB (130406625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de545400b0a4b20e99a41bb03dd0464d3f4e6b22326a58a0f8a6f27df35ed53`  
		Last Modified: Sat, 24 Apr 2021 03:57:21 GMT  
		Size: 14.1 MB (14062037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19c270fd954ab1850546a2f1fe907e5812464bb308554d74ff3b77fe4d085a5`  
		Last Modified: Sat, 24 Apr 2021 03:57:16 GMT  
		Size: 701.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b461e2c9230ad6d7e36d9fddcc2d3d04a394954d5b5437473fde9a958d54c05c`  
		Last Modified: Sat, 24 Apr 2021 03:57:15 GMT  
		Size: 9.6 KB (9557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0821ea49c2f2252a0938a998b8388c6f28a42fa11fcea87f34c94c523b2a1e`  
		Last Modified: Sat, 24 Apr 2021 03:57:15 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b875abf5447191fb37fb076a3def6e4623314c82cf9c399a82e81f2d7fbfdd`  
		Last Modified: Sat, 24 Apr 2021 03:57:16 GMT  
		Size: 10.5 KB (10548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1dc37ac444dea5f60b5a444e3fe1cf82f9c846fe2eef1d199c48742f541072e`  
		Last Modified: Sat, 24 Apr 2021 03:57:17 GMT  
		Size: 5.3 MB (5300774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340964737ae2ffbf89a010557d283b9a17b7d52790d89962d818463313818768`  
		Last Modified: Sat, 24 Apr 2021 03:58:11 GMT  
		Size: 212.9 MB (212930880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba214ef51994cf88584d070810d932460f4e7341911cbf935ff7cbe006e467d`  
		Last Modified: Sat, 24 Apr 2021 03:57:49 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c830a72dca5b968adec807675fd7d07de4a08456b2188cbf92acdf09a5132f`  
		Last Modified: Sat, 24 Apr 2021 03:57:53 GMT  
		Size: 18.6 MB (18603368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `websphere-liberty:latest` - linux; s390x

```console
$ docker pull websphere-liberty@sha256:1813d2e44e1f79784ab44778359fd80a47b37726d4ded32db082ca08eb72f80f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.0 MB (411023034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1109636c471215912302d8affaad06caa663cedee902a569c14ebc0e70e6a9a`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 21:45:00 GMT
ADD file:5e61a5300d520d61a2130623465ba2e46da8e80dc2afa042473a42cbcd8d88d2 in / 
# Fri, 23 Apr 2021 21:45:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 21:45:05 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 21:45:07 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 21:45:07 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 22:25:02 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 23 Apr 2021 22:25:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:25:17 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 23 Apr 2021 22:26:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 23 Apr 2021 22:26:15 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Fri, 23 Apr 2021 23:16:58 GMT
ARG VERBOSE=false
# Fri, 23 Apr 2021 23:16:58 GMT
ARG OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:16:59 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Fri, 23 Apr 2021 23:17:00 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Fri, 23 Apr 2021 23:17:00 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Fri, 23 Apr 2021 23:17:01 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with IBM's Java and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Fri, 23 Apr 2021 23:17:02 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Fri, 23 Apr 2021 23:17:02 GMT
ARG LIBERTY_URL
# Fri, 23 Apr 2021 23:17:03 GMT
ARG DOWNLOAD_OPTIONS=
# Fri, 23 Apr 2021 23:17:18 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:17:20 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Apr 2021 23:17:21 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Fri, 23 Apr 2021 23:17:21 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Fri, 23 Apr 2021 23:17:23 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Fri, 23 Apr 2021 23:17:24 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Fri, 23 Apr 2021 23:17:25 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Fri, 23 Apr 2021 23:17:27 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Fri, 23 Apr 2021 23:17:40 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Fri, 23 Apr 2021 23:17:41 GMT
ENV RANDFILE=/tmp/.rnd IBM_JAVA_OPTIONS=-Xshareclasses:name=liberty,nonfatal,cacheDir=/output/.classCache/ -Dosgi.checkConfiguration=false -XX:+UseContainerSupport
# Fri, 23 Apr 2021 23:17:42 GMT
USER 1001
# Fri, 23 Apr 2021 23:17:42 GMT
EXPOSE 9080 9443
# Fri, 23 Apr 2021 23:17:43 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Fri, 23 Apr 2021 23:17:43 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Fri, 23 Apr 2021 23:18:44 GMT
ARG VERBOSE=false
# Fri, 23 Apr 2021 23:18:45 GMT
ARG REPOSITORIES_PROPERTIES=
# Fri, 23 Apr 2021 23:22:46 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Fri, 23 Apr 2021 23:23:00 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Fri, 23 Apr 2021 23:23:44 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:33ddddc4572ffe1f294f9f599ed989cc41eee5da4cdcf7db12d10700aa8c894e`  
		Last Modified: Fri, 23 Apr 2021 21:47:03 GMT  
		Size: 25.4 MB (25352756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4395f372a786db91b2f50dc8e43d8b7c3533eb4bd86f6728eb2a0c7108c077d2`  
		Last Modified: Fri, 23 Apr 2021 21:46:59 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e39753730df188282ca8193f14bbbb8cbe0b76ec02b34283a28449b1e41c05`  
		Last Modified: Fri, 23 Apr 2021 21:47:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e93b87da546ac7aa6705cd2f20bfe70cf04793ac73561e5dd8c579af88754aec`  
		Last Modified: Fri, 23 Apr 2021 22:28:41 GMT  
		Size: 2.7 MB (2676643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268462fc02d2bd9da227784f5f243759923a14cefb3648739ca02e8fa7d63ee7`  
		Last Modified: Fri, 23 Apr 2021 22:28:50 GMT  
		Size: 128.1 MB (128065984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895091e75a5c1ee863c074a41c334973d986bb55cef3d4ba2f8267a2887f8336`  
		Last Modified: Fri, 23 Apr 2021 23:53:50 GMT  
		Size: 14.1 MB (14061390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26d2145efe41abadeb2694f43164f1a155e500e85bf004da26812cd8532de7f`  
		Last Modified: Fri, 23 Apr 2021 23:53:47 GMT  
		Size: 700.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1dc41aa938b0af86dfd6446147e4484cb5d6bad6e84eb2edb074790b0615a1`  
		Last Modified: Fri, 23 Apr 2021 23:53:47 GMT  
		Size: 9.6 KB (9556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0e2666f7e25fefd1dfbbb522189283388626a78a6993958a175bfe3d453daa`  
		Last Modified: Fri, 23 Apr 2021 23:53:47 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1422da1f78c4ff3f196f908ccd43d884e84e4586193eab1bfe59df39b352b130`  
		Last Modified: Fri, 23 Apr 2021 23:53:47 GMT  
		Size: 10.5 KB (10540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6a848b971c7539a51ff9771c57f7df448cc5b960c0be0fa5b3c3b547e8589c`  
		Last Modified: Fri, 23 Apr 2021 23:53:47 GMT  
		Size: 5.9 MB (5924580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a29d9ef14335af914d1a4155de231f338e3649b1e962477e8f3c3007227195`  
		Last Modified: Fri, 23 Apr 2021 23:54:16 GMT  
		Size: 213.6 MB (213555213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85098d48d9a85bbbdc1b5f863692bf7b326b94c5f44d091ff39e53fb34a41cc`  
		Last Modified: Fri, 23 Apr 2021 23:54:05 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1e656c995305a66ce28c668c88b221183600d735978d891b72351644e890c2`  
		Last Modified: Fri, 23 Apr 2021 23:54:08 GMT  
		Size: 21.4 MB (21363413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

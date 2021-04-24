## `websphere-liberty:full-java11-openj9`

```console
$ docker pull websphere-liberty@sha256:db15fc7b62534e33977ddc7cb72115b8b277ac75974d5d5a457e06d593937d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `websphere-liberty:full-java11-openj9` - linux; amd64

```console
$ docker pull websphere-liberty@sha256:0971042d3215862a23f4f9a60351abbc3e09100930f2648199d8db53950ef69b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.8 MB (329844822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f11f968ede3087bc5041afc0bc019fafb1e937d819c113261d1dc7bdb392a986`
-	Entrypoint: `["\/opt\/ibm\/helpers\/runtime\/docker-server.sh"]`
-	Default Command: `["\/opt\/ibm\/wlp\/bin\/server","run","defaultServer"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:22:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 23 Apr 2021 23:23:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:26:10 GMT
ENV JAVA_VERSION=jdk-11.0.10+9_openj9-0.24.0
# Fri, 23 Apr 2021 23:27:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        ppc64el|ppc64le)          ESUM='5d2b2939637f999a1910d5cc0fb3d96756125941e5f8b9e3003635aa863664b5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_ppc64le_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        s390x)          ESUM='2ff9f50d6ffc345434703c43a1d67ac6d3d054b5d4925b4b73a3ce51b02940e5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_s390x_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        amd64|x86_64)          ESUM='7e5f97071f8b86c22c36ddfd7f821c3e8ec531c1128e2e6c931b2e64118a517a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9_openj9-0.24.0/OpenJDK11U-jre_x64_linux_openj9_11.0.10_9_openj9-0.24.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 23 Apr 2021 23:27:05 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Apr 2021 23:27:06 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 23 Apr 2021 23:27:42 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Sat, 24 Apr 2021 04:53:21 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 04:53:22 GMT
ARG OPENJ9_SCC=true
# Sat, 24 Apr 2021 04:53:22 GMT
ARG EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c
# Sat, 24 Apr 2021 04:53:22 GMT
ARG NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1
# Sat, 24 Apr 2021 04:53:22 GMT
ARG NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096
# Sat, 24 Apr 2021 04:53:22 GMT
LABEL org.opencontainers.image.authors=Arthur De Magalhaes, Chris Potter, Christy Jesuraj org.opencontainers.image.vendor=IBM org.opencontainers.image.url=http://wasdev.net org.opencontainers.image.documentation=https://www.ibm.com/support/knowledgecenter/SSAW57_liberty/com.ibm.websphere.wlp.nd.multiplatform.doc/ae/cwlp_about.html org.opencontainers.image.version=21.0.0.4 org.opencontainers.image.revision=cl210420210407-0944 org.opencontainers.image.description=This image contains the WebSphere Liberty runtime with AdoptOpenJDK with OpenJ9 and Ubuntu as the base OS.  For more information on this image please see https://github.com/WASdev/ci.docker#building-an-application-image org.opencontainers.image.title=IBM WebSphere Liberty
# Sat, 24 Apr 2021 04:53:22 GMT
ENV LIBERTY_VERSION=21.0.0_04
# Sat, 24 Apr 2021 04:53:23 GMT
ARG LIBERTY_URL
# Sat, 24 Apr 2021 04:53:23 GMT
ARG DOWNLOAD_OPTIONS=
# Sat, 24 Apr 2021 04:53:31 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 OPENJ9_SCC=true VERBOSE=false
RUN apt-get update     && apt-get install -y --no-install-recommends unzip wget openssl     && rm -rf /var/lib/apt/lists/*     && mkdir /licenses/     && useradd -u 1001 -r -g 0 -s /usr/sbin/nologin default     && LIBERTY_URL=${LIBERTY_URL:-$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*kernel:\s//p' | tr -d '\r' )}      && wget $DOWNLOAD_OPTIONS $LIBERTY_URL -U UA-IBM-WebSphere-Liberty-Docker -O /tmp/wlp.zip     && unzip -q /tmp/wlp.zip -d /opt/ibm     && rm /tmp/wlp.zip     && chown -R 1001:0 /opt/ibm/wlp     && chmod -R g+rw /opt/ibm/wlp     && LICENSE_BASE=$(wget -q -O - https://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/index.yml  | grep $LIBERTY_VERSION -A 6 | sed -n 's/\s*license:\s//p' | sed 's/\(.*\)\/.*/\1\//' | tr -d '\r')     && wget ${LICENSE_BASE}en.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/en.html     && wget ${LICENSE_BASE}non_ibm_license.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/non_ibm_license.html     && wget ${LICENSE_BASE}notices.html -U UA-IBM-WebSphere-Liberty-Docker -O /licenses/notices.html     && echo "$EN_SHA /licenses/en.html" | sha256sum -c --strict --check     && echo "$NON_IBM_SHA /licenses/non_ibm_license.html" | sha256sum -c --strict --check     && echo "$NOTICES_SHA /licenses/notices.html" | sha256sum -c --strict --check     && apt-get purge --auto-remove -y unzip     && apt-get purge --auto-remove -y wget     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 04:53:31 GMT
ENV PATH=/opt/ibm/wlp/bin:/opt/ibm/helpers/build:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 24 Apr 2021 04:53:31 GMT
LABEL ProductID=fbf6a96d49214c0abc6a3bc5da6e48cd ProductName=WebSphere Application Server Liberty ProductVersion=21.0.0.4 BuildLabel=cl210420210407-0944
# Sat, 24 Apr 2021 04:53:31 GMT
ENV LOG_DIR=/logs WLP_OUTPUT_DIR=/opt/ibm/wlp/output OPENJ9_SCC=true
# Sat, 24 Apr 2021 04:53:33 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN /opt/ibm/wlp/bin/server create     && rm -rf $WLP_OUTPUT_DIR/.classCache /output/workarea
# Sat, 24 Apr 2021 04:53:33 GMT
COPY dir:97a8e76f74c504c9fb35f9416fa56b7ba9d48a4796f6cdac0d566ee62c1fb2fb in /opt/ibm/helpers/ 
# Sat, 24 Apr 2021 04:53:33 GMT
COPY dir:1cf5cc2663c6235241a5228340a9c566587fe27b3e434a313debbf75dacd7a4b in /opt/ibm/fixes/ 
# Sat, 24 Apr 2021 04:53:34 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN mkdir /logs     && mkdir /etc/wlp     && mkdir -p /opt/ibm/wlp/usr/shared/resources/lib.index.cache     && mkdir -p /home/default     && mkdir /output     && chmod -t /output     && rm -rf /output     && ln -s $WLP_OUTPUT_DIR/defaultServer /output     && ln -s /opt/ibm/wlp/usr/servers/defaultServer /config     && ln -s /opt/ibm /liberty     && ln -s /opt/ibm/wlp/usr/shared/resources/lib.index.cache /lib.index.cache     && mkdir -p /config/configDropins/defaults     && mkdir -p /config/configDropins/overrides     && chown -R 1001:0 /config     && chmod -R g+rw /config     && chown -R 1001:0 /opt/ibm/helpers     && chmod -R g+rwx /opt/ibm/helpers     && chown -R 1001:0 /opt/ibm/fixes     && chmod -R g+rwx /opt/ibm/fixes     && chown -R 1001:0 /opt/ibm/wlp/usr     && chmod -R g+rw /opt/ibm/wlp/usr     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rw /opt/ibm/wlp/output     && chown -R 1001:0 /logs     && chmod -R g+rw /logs     && chown -R 1001:0 /etc/wlp     && chmod -R g+rw /etc/wlp     && chown -R 1001:0 /home/default     && chmod -R g+rw /home/default
# Sat, 24 Apr 2021 04:53:42 GMT
# ARGS: DOWNLOAD_OPTIONS= EN_SHA=97928b10f7247e2412a5dd78528ae1bd218212eec342f938dec6202a9680616c NON_IBM_SHA=2a518255f7a59a1a003fd0646c8b2424ba655683f8394940a0cad693a7a1fbf1 NOTICES_SHA=d4b0236a5fc49b6308923b87fcd6b4ba4aac33efc02c27f8292c3aa7a532d096 VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
# Sat, 24 Apr 2021 04:53:42 GMT
ENV RANDFILE=/tmp/.rnd OPENJ9_JAVA_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal -Dosgi.checkConfiguration=false
# Sat, 24 Apr 2021 04:53:42 GMT
USER 1001
# Sat, 24 Apr 2021 04:53:43 GMT
EXPOSE 9080 9443
# Sat, 24 Apr 2021 04:53:43 GMT
ENTRYPOINT ["/opt/ibm/helpers/runtime/docker-server.sh"]
# Sat, 24 Apr 2021 04:53:43 GMT
CMD ["/opt/ibm/wlp/bin/server" "run" "defaultServer"]
# Sat, 24 Apr 2021 04:57:28 GMT
ARG VERBOSE=false
# Sat, 24 Apr 2021 04:57:28 GMT
ARG REPOSITORIES_PROPERTIES=
# Sat, 24 Apr 2021 05:00:00 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ ! -z $REPOSITORIES_PROPERTIES ]; then mkdir /opt/ibm/wlp/etc/   && echo $REPOSITORIES_PROPERTIES > /opt/ibm/wlp/etc/repositories.properties; fi   && installUtility install --acceptLicense baseBundle   && if [ ! -z $REPOSITORIES_PROPERTIES ]; then rm /opt/ibm/wlp/etc/repositories.properties; fi   && rm -rf /output/workarea /output/logs   && chmod -R g+rwx /opt/ibm/wlp/output/*
# Sat, 24 Apr 2021 05:00:01 GMT
COPY --chown=1001:0file:f212cc38605f508baa0f75a07632700533ad28792dd9761a792209e709b00f23 in /config/ 
# Sat, 24 Apr 2021 05:00:36 GMT
# ARGS: REPOSITORIES_PROPERTIES= VERBOSE=false
RUN if [ "$OPENJ9_SCC" = "true" ]; then populate_scc.sh; fi     && rm -rf /output/messaging /output/resources/security /logs/* $WLP_OUTPUT_DIR/.classCache     && chown -R 1001:0 /opt/ibm/wlp/output     && chmod -R g+rwx /opt/ibm/wlp/output
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592ec2d7c1370aca6ef48ee1d20fbb3a4c148db400adc5dc575778c681f5dba0`  
		Last Modified: Fri, 23 Apr 2021 23:32:39 GMT  
		Size: 16.0 MB (16034099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c7638b64a72cbb37900547cb3e701621a1b36381d5a9cb7c35a404d59467c5`  
		Last Modified: Fri, 23 Apr 2021 23:37:22 GMT  
		Size: 42.4 MB (42440359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd8ce666aab5f92a69f7131bfbd1c65694c16d94a8d11076099436abec78eac`  
		Last Modified: Fri, 23 Apr 2021 23:37:15 GMT  
		Size: 4.1 MB (4106588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5106b877149857a69dd815b6deae3a80cefd798486999eecf8fee1dd51361bd3`  
		Last Modified: Sat, 24 Apr 2021 05:17:06 GMT  
		Size: 14.2 MB (14161689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91967f6dbfeda65b9ddf24c12609fc03aacccf18cf905db6cd6eb2dde37b9ff1`  
		Last Modified: Sat, 24 Apr 2021 05:17:01 GMT  
		Size: 691.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb64aeceb3d49adea890ce5b5c4de178c686a0b02e9f3319f70a221973b2f99c`  
		Last Modified: Sat, 24 Apr 2021 05:17:01 GMT  
		Size: 9.5 KB (9546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21de79857f982350ef8d5823c0e8d1f4d55b6f37745359ef0d84c9371aacd75`  
		Last Modified: Sat, 24 Apr 2021 05:17:02 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6aece3251c24ad0ab927332b25478b09a465703082fb7fddc83308a151ac5e4`  
		Last Modified: Sat, 24 Apr 2021 05:17:02 GMT  
		Size: 10.5 KB (10528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b846a39837073cd619ea5e26d7f565f6a1e85485550d880eec884595fb3355`  
		Last Modified: Sat, 24 Apr 2021 05:17:02 GMT  
		Size: 2.5 MB (2464918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42e691b1ca36bc3e409b513ae27daa09c53fe605596911413430769afe89a30`  
		Last Modified: Sat, 24 Apr 2021 05:17:50 GMT  
		Size: 207.7 MB (207669386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658b9135c54dbcec5c8f48262685ecef217afa3e7a301bde30e45a82f507ff51`  
		Last Modified: Sat, 24 Apr 2021 05:17:38 GMT  
		Size: 940.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7be4aeb244f08b4d1fc94c5ce9edc94ea8e6639f2a620a02b5273c93ff06ad9`  
		Last Modified: Sat, 24 Apr 2021 05:17:40 GMT  
		Size: 14.4 MB (14405144 bytes)  
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

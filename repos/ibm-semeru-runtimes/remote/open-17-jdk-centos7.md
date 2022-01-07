## `ibm-semeru-runtimes:open-17-jdk-centos7`

```console
$ docker pull ibm-semeru-runtimes@sha256:389f8c34f68bf1079dd8eae69b915b7df53dc2864f75e65a46e6a85ef14a1bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `ibm-semeru-runtimes:open-17-jdk-centos7` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:2216620bbb103643d911b854d9c761de58bf0edf3205c506a5479aba79e87ed1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.1 MB (303084197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7efe1b16b1b07caebacdb91d449f86796bd45346ca381406dd8bc65fe44cd48b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 18:51:21 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Sep 2021 18:51:48 GMT
RUN yum install -y tzdata openssl curl ca-certificates fontconfig gzip tar     && yum clean all
# Mon, 13 Dec 2021 19:31:51 GMT
ENV JAVA_VERSION=jdk-17.0.1+12_openj9-0.29.1
# Mon, 13 Dec 2021 19:32:00 GMT
RUN set -eux;     ARCH="$(uname -m)";     case "${ARCH}" in        aarch64|arm64)          ESUM='5e0f80052ac4613d2d689904b20ff8b6e2bbd1edd87271db0659a646a24dfeb6';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.1%2B12_openj9-0.29.1/ibm-semeru-open-jdk_aarch64_linux_17.0.1_12_openj9-0.29.1.tar.gz';          ;;        amd64|x86_64)          ESUM='154f6411742ee1f8cbf004d72e7e71053b9ad4e89090cb930b6f16951e56503e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.1%2B12_openj9-0.29.1/ibm-semeru-open-jdk_x64_linux_17.0.1_12_openj9-0.29.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='80b6389dbed9b7de9c63b1cb423e719aa5e6fbab42387fdb1f68d9d199bf5196';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.1%2B12_openj9-0.29.1/ibm-semeru-open-jdk_ppc64le_linux_17.0.1_12_openj9-0.29.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 13 Dec 2021 19:32:00 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Dec 2021 19:32:01 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 13 Dec 2021 19:32:37 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Mon, 13 Dec 2021 19:32:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df6893209e3a4a16d453c0b998ba34f62067ad6099b971afc4f30040eb1467d`  
		Last Modified: Wed, 15 Sep 2021 18:54:13 GMT  
		Size: 12.7 MB (12706445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d754637804f8d29b0a46ca1b15fa6aade447fd3c8ad9fae96caabd9f381b848c`  
		Last Modified: Mon, 13 Dec 2021 19:35:59 GMT  
		Size: 208.4 MB (208389868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beee268bb9c3eff1a9ad7ce68b62a34bedb666e10959a188e4714b1e05e2299e`  
		Last Modified: Mon, 13 Dec 2021 19:35:43 GMT  
		Size: 5.9 MB (5890727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibm-semeru-runtimes:open-17-jdk-centos7` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:a3b0ddf642d7f1a6a49c615d574753f02f1102b085fa0924b18b8f6f7b4b35a1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.4 MB (330378066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1df486861bbfd786ddbd59fd959157529c2068f4d60e077b6629a50ea2e2a9`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Sep 2021 17:39:58 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Wed, 15 Sep 2021 17:39:58 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 17:39:59 GMT
CMD ["/bin/bash"]
# Sat, 16 Oct 2021 03:25:52 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 03:26:24 GMT
RUN yum install -y tzdata openssl curl ca-certificates fontconfig gzip tar     && yum clean all
# Fri, 07 Jan 2022 19:41:31 GMT
ENV JAVA_VERSION=jdk-17.0.1+12_openj9-0.29.1
# Fri, 07 Jan 2022 19:41:51 GMT
RUN set -eux;     ARCH="$(uname -m)";     case "${ARCH}" in        aarch64|arm64)          ESUM='5e0f80052ac4613d2d689904b20ff8b6e2bbd1edd87271db0659a646a24dfeb6';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.1%2B12_openj9-0.29.1/ibm-semeru-open-jdk_aarch64_linux_17.0.1_12_openj9-0.29.1.tar.gz';          ;;        amd64|x86_64)          ESUM='154f6411742ee1f8cbf004d72e7e71053b9ad4e89090cb930b6f16951e56503e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.1%2B12_openj9-0.29.1/ibm-semeru-open-jdk_x64_linux_17.0.1_12_openj9-0.29.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='80b6389dbed9b7de9c63b1cb423e719aa5e6fbab42387fdb1f68d9d199bf5196';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.1%2B12_openj9-0.29.1/ibm-semeru-open-jdk_ppc64le_linux_17.0.1_12_openj9-0.29.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 07 Jan 2022 19:41:52 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jan 2022 19:41:52 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 07 Jan 2022 19:42:28 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 07 Jan 2022 19:42:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ed710eb0a2f63323ad5c292c7cfd48094b0fee69aa1c789341819797baca66`  
		Last Modified: Sat, 16 Oct 2021 03:32:08 GMT  
		Size: 13.1 MB (13066395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f75f0b65026f6b3a52241e704cfd6dc64afed32895daa8dd48d53bea9a55301`  
		Last Modified: Fri, 07 Jan 2022 19:46:33 GMT  
		Size: 203.3 MB (203291953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1c07d33ed4dcbf45d0b651d94f78bff94a83ed0d456f4e01b9387d48601e7c`  
		Last Modified: Fri, 07 Jan 2022 19:46:15 GMT  
		Size: 5.6 MB (5644773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibm-semeru-runtimes:open-17-jdk-centos7` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:5f88b3d76839df4eac945a76719f345eaa8bfd8ee076eecdfc5656c29888b2ed
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.7 MB (306701815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cca65cca1b58ed6960b3ee154cc63faf27a2f66d1c2de8dc0a84fe9ea9f2a80`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Sep 2021 18:29:27 GMT
ADD file:7f21ae7d20a8e347d8b678bcf26be83abb1ee27d3b567c9cddd993e45ce8ac34 in / 
# Wed, 15 Sep 2021 18:29:31 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:29:40 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 21:27:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 15 Sep 2021 21:29:19 GMT
RUN yum install -y tzdata openssl curl ca-certificates fontconfig gzip tar     && yum clean all
# Mon, 13 Dec 2021 19:20:01 GMT
ENV JAVA_VERSION=jdk-17.0.1+12_openj9-0.29.1
# Mon, 13 Dec 2021 19:20:34 GMT
RUN set -eux;     ARCH="$(uname -m)";     case "${ARCH}" in        aarch64|arm64)          ESUM='5e0f80052ac4613d2d689904b20ff8b6e2bbd1edd87271db0659a646a24dfeb6';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.1%2B12_openj9-0.29.1/ibm-semeru-open-jdk_aarch64_linux_17.0.1_12_openj9-0.29.1.tar.gz';          ;;        amd64|x86_64)          ESUM='154f6411742ee1f8cbf004d72e7e71053b9ad4e89090cb930b6f16951e56503e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.1%2B12_openj9-0.29.1/ibm-semeru-open-jdk_x64_linux_17.0.1_12_openj9-0.29.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='80b6389dbed9b7de9c63b1cb423e719aa5e6fbab42387fdb1f68d9d199bf5196';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.1%2B12_openj9-0.29.1/ibm-semeru-open-jdk_ppc64le_linux_17.0.1_12_openj9-0.29.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Mon, 13 Dec 2021 19:20:44 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Dec 2021 19:20:47 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Mon, 13 Dec 2021 19:21:29 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Mon, 13 Dec 2021 19:21:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3fe478aaff9b8f3ba958253e7339e9016ec07c075b805ebfc8cd372ddd01ee64`  
		Last Modified: Tue, 17 Nov 2020 04:06:20 GMT  
		Size: 80.5 MB (80516460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f502386ff4e2195af1b6b4432c6ccd0fabc7a63dd38550f635eacaa707c74a`  
		Last Modified: Wed, 15 Sep 2021 21:38:40 GMT  
		Size: 12.6 MB (12616024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e854802f3f557a122c8f98cba4d3728fd22cd6138362b06a7077bc42270a7c1`  
		Last Modified: Mon, 13 Dec 2021 19:26:51 GMT  
		Size: 208.8 MB (208782435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06df1c47266cc8d4c841675f32c3ca590a24e53bed6e288d2e5bb1fd1b1fd6e3`  
		Last Modified: Mon, 13 Dec 2021 19:26:29 GMT  
		Size: 4.8 MB (4786896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

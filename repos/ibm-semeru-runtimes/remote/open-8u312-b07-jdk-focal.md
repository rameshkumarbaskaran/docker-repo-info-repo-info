## `ibm-semeru-runtimes:open-8u312-b07-jdk-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:da951b10381a46093952540b7d27c98bcfde173e3c25870e08da7d2b82e42356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ibm-semeru-runtimes:open-8u312-b07-jdk-focal` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:297813e12f3c1225d546473a75ac974a562df82e249a632a4632685f0ba3a281
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165431545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3a3f8dd35462a9ee288693a6aa7eb74da0a931b40f84d35a4c2f923160757b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 04:41:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 07 Jan 2022 04:49:04 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 04:49:04 GMT
ENV JAVA_VERSION=jdk8u312-b07_openj9-0.29.0
# Fri, 07 Jan 2022 04:49:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='055e51b462fac3af198424ab41804959bf769274ebdffef9ac8bf036a9d73b95';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u312-b07_openj9-0.29.0/ibm-semeru-open-jdk_aarch64_linux_8u312b07_openj9-0.29.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='ebd9d0b4e9ecca578b684e080f0c45fa4edb1a4d5f572ea21ff61b301dd7c870';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u312-b07_openj9-0.29.0/ibm-semeru-open-jdk_ppc64le_linux_8u312b07_openj9-0.29.0.tar.gz';          ;;        s390x)          ESUM='6908fb701b5834cbf2e8d6f1345aa29039ab95bc0c125631f310afe1c1715eae';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u312-b07_openj9-0.29.0/ibm-semeru-open-jdk_s390x_linux_8u312b07_openj9-0.29.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c7306112201b45cc8b96e6d6fb3f6de727ddbbb51022cbd9cff98b661e37a510';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u312-b07_openj9-0.29.0/ibm-semeru-open-jdk_x64_linux_8u312b07_openj9-0.29.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 07 Jan 2022 04:49:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jan 2022 04:49:16 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 07 Jan 2022 04:49:51 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149e13f4c7fd2fb114074531c521dac0a966a3415bdd74da538677ecf096b757`  
		Last Modified: Fri, 07 Jan 2022 04:57:29 GMT  
		Size: 16.0 MB (16032427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba63d9013f21ab530258860f78faa480e52bf4e87adf68b0eebfd3f49e0ce83d`  
		Last Modified: Fri, 07 Jan 2022 04:57:36 GMT  
		Size: 116.6 MB (116618371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f7c6b911570739bb9f4e75e085e0abbe6fba29f6f59c28df6afcf995447315`  
		Last Modified: Fri, 07 Jan 2022 04:57:27 GMT  
		Size: 4.2 MB (4214322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibm-semeru-runtimes:open-8u312-b07-jdk-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:ce67d21a5e68f493b76b15d869f942b50d4766d8f8a0c0ae52e539fb2a4314ad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161149589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a3ce6700bd936838d75f68c02d9dc665c175cf52b6470b4eb004f1fe0ebf7a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:45 GMT
ADD file:521a8ada4ac06e6f7720904486d481d216a8c3e08c0c7db1376c39a33e709668 in / 
# Fri, 07 Jan 2022 01:53:45 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:32:58 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 07 Jan 2022 02:41:57 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:41:58 GMT
ENV JAVA_VERSION=jdk8u312-b07_openj9-0.29.0
# Fri, 07 Jan 2022 02:42:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='055e51b462fac3af198424ab41804959bf769274ebdffef9ac8bf036a9d73b95';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u312-b07_openj9-0.29.0/ibm-semeru-open-jdk_aarch64_linux_8u312b07_openj9-0.29.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='ebd9d0b4e9ecca578b684e080f0c45fa4edb1a4d5f572ea21ff61b301dd7c870';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u312-b07_openj9-0.29.0/ibm-semeru-open-jdk_ppc64le_linux_8u312b07_openj9-0.29.0.tar.gz';          ;;        s390x)          ESUM='6908fb701b5834cbf2e8d6f1345aa29039ab95bc0c125631f310afe1c1715eae';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u312-b07_openj9-0.29.0/ibm-semeru-open-jdk_s390x_linux_8u312b07_openj9-0.29.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c7306112201b45cc8b96e6d6fb3f6de727ddbbb51022cbd9cff98b661e37a510';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u312-b07_openj9-0.29.0/ibm-semeru-open-jdk_x64_linux_8u312b07_openj9-0.29.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 07 Jan 2022 02:42:09 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jan 2022 02:42:10 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 07 Jan 2022 02:42:46 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
```

-	Layers:
	-	`sha256:5f3d23ccb99f6c9462a15efcf35aef0863858073a06d56df671d0e791b26222a`  
		Last Modified: Fri, 07 Jan 2022 01:55:32 GMT  
		Size: 27.2 MB (27171074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d29c227106c1dba2893356b67a809c01fd77c745e8543df25145dfe5e7ef84`  
		Last Modified: Fri, 07 Jan 2022 02:46:50 GMT  
		Size: 15.9 MB (15894303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6326b6570532aac714c9093cda34a23171d40ea6b124e41c86b416ae2281d5`  
		Last Modified: Fri, 07 Jan 2022 02:46:58 GMT  
		Size: 114.1 MB (114076640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd4b31c49168c826f497266756b32f7e86e390d70fafb2d50dd96208f95bd53`  
		Last Modified: Fri, 07 Jan 2022 02:46:48 GMT  
		Size: 4.0 MB (4007572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibm-semeru-runtimes:open-8u312-b07-jdk-focal` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:a55a8a267cb8c1c5c7d9d073a8ddb71aca7ff5fc1b3e9632dcfbeab8d39ad18c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.7 MB (170660407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd33c1c322f86370836da7654f4818d461967b514fc8f397fea32d737ebee659`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:20:15 GMT
ADD file:014236839eaee978894ae0bd6aecc246177a0a2c11af73f86d9cfafe5478ce18 in / 
# Fri, 07 Jan 2022 02:20:19 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:15:29 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 07 Jan 2022 04:22:19 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 04:22:22 GMT
ENV JAVA_VERSION=jdk8u312-b07_openj9-0.29.0
# Fri, 07 Jan 2022 04:22:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='055e51b462fac3af198424ab41804959bf769274ebdffef9ac8bf036a9d73b95';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u312-b07_openj9-0.29.0/ibm-semeru-open-jdk_aarch64_linux_8u312b07_openj9-0.29.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='ebd9d0b4e9ecca578b684e080f0c45fa4edb1a4d5f572ea21ff61b301dd7c870';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u312-b07_openj9-0.29.0/ibm-semeru-open-jdk_ppc64le_linux_8u312b07_openj9-0.29.0.tar.gz';          ;;        s390x)          ESUM='6908fb701b5834cbf2e8d6f1345aa29039ab95bc0c125631f310afe1c1715eae';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u312-b07_openj9-0.29.0/ibm-semeru-open-jdk_s390x_linux_8u312b07_openj9-0.29.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c7306112201b45cc8b96e6d6fb3f6de727ddbbb51022cbd9cff98b661e37a510';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u312-b07_openj9-0.29.0/ibm-semeru-open-jdk_x64_linux_8u312b07_openj9-0.29.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 07 Jan 2022 04:22:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jan 2022 04:22:44 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 07 Jan 2022 04:23:23 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
```

-	Layers:
	-	`sha256:e6e6dea5a8cc4bdc9e5e51e2bfa948159b69d5fbc2dca99bc41776fb04dab967`  
		Last Modified: Fri, 07 Jan 2022 02:22:43 GMT  
		Size: 33.3 MB (33286892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2db03674d664c4c13747eecf6ee9d3578adc9eb95e5a3993661ba5f37f676f8`  
		Last Modified: Fri, 07 Jan 2022 04:34:49 GMT  
		Size: 17.2 MB (17206916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70107645589c4439fc4a34e07ca849aab3fe84e47ad3cbd67fd74fb8cdeec363`  
		Last Modified: Fri, 07 Jan 2022 04:34:59 GMT  
		Size: 116.7 MB (116711977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431b08934a87ee071cfe50cdc4742ac5877f7a1baac0ca512d8be50d5fe13186`  
		Last Modified: Fri, 07 Jan 2022 04:34:46 GMT  
		Size: 3.5 MB (3454622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibm-semeru-runtimes:open-8u312-b07-jdk-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:835c4ef1503d9a2363bd540008aa61fa3d0c4463fb9ab3b81eac15b1bb9f6c15
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162387639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cacc26a153b0fb55802d6c016bf8f488480b24863cd426250a6c176fb6d4cc5b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:20 GMT
ADD file:b6119f4fcd6a113749f515278b315ffd96aecce7006f086acb060f981e5c59db in / 
# Fri, 07 Jan 2022 01:42:22 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:15:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 07 Jan 2022 02:24:31 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:24:32 GMT
ENV JAVA_VERSION=jdk8u312-b07_openj9-0.29.0
# Fri, 07 Jan 2022 02:24:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='055e51b462fac3af198424ab41804959bf769274ebdffef9ac8bf036a9d73b95';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u312-b07_openj9-0.29.0/ibm-semeru-open-jdk_aarch64_linux_8u312b07_openj9-0.29.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='ebd9d0b4e9ecca578b684e080f0c45fa4edb1a4d5f572ea21ff61b301dd7c870';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u312-b07_openj9-0.29.0/ibm-semeru-open-jdk_ppc64le_linux_8u312b07_openj9-0.29.0.tar.gz';          ;;        s390x)          ESUM='6908fb701b5834cbf2e8d6f1345aa29039ab95bc0c125631f310afe1c1715eae';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u312-b07_openj9-0.29.0/ibm-semeru-open-jdk_s390x_linux_8u312b07_openj9-0.29.0.tar.gz';          ;;        amd64|x86_64)          ESUM='c7306112201b45cc8b96e6d6fb3f6de727ddbbb51022cbd9cff98b661e37a510';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u312-b07_openj9-0.29.0/ibm-semeru-open-jdk_x64_linux_8u312b07_openj9-0.29.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 07 Jan 2022 02:24:40 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Jan 2022 02:24:40 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 07 Jan 2022 02:25:13 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
```

-	Layers:
	-	`sha256:6d200361446626b53394c2a1a520a74a1221795562eac9b318c58e0abe147e23`  
		Last Modified: Fri, 07 Jan 2022 01:44:09 GMT  
		Size: 27.1 MB (27120999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2ea75c80fa68be6367734322b7c053932a41106663b880c832691c5c615f18`  
		Last Modified: Fri, 07 Jan 2022 02:32:46 GMT  
		Size: 15.7 MB (15739670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023aeff8999e938d0bfe0f681a07fb93a47c34d1497b52f433a89d47960c9d23`  
		Last Modified: Fri, 07 Jan 2022 02:32:53 GMT  
		Size: 115.3 MB (115270894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004c486eeead069137c5702f8ab62346bd92680d59bc31cf9a091071ae01db2c`  
		Last Modified: Fri, 07 Jan 2022 02:32:45 GMT  
		Size: 4.3 MB (4256076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

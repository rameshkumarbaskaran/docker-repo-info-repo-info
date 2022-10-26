## `ibm-semeru-runtimes:open-8-jdk-jammy`

```console
$ docker pull ibm-semeru-runtimes@sha256:d66b4ddb4be51b0765aaf7fd1ae9384c6ac658152ec42839fb8a122aa573b4eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; s390x

### `ibm-semeru-runtimes:open-8-jdk-jammy` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:367a6af9743bb0870d0f9ba82c735b6215b1e67e47029fbbe4aa424725bc724c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163413033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d3a7814baba5de23c6e19b38cbce32e2404448044c4fd0a78040ab9343d658`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 16:37:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Oct 2022 16:38:11 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 16:38:11 GMT
ENV JAVA_VERSION=jdk8u345-b01_openj9-0.33.1
# Tue, 25 Oct 2022 16:38:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='55eb440eedc331081012664e18b4640988a210d6443289410662ff03c0b2bf05';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u345-b01_openj9-0.33.1/ibm-semeru-open-jdk_aarch64_linux_8u345b01_openj9-0.33.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7b9da287bd3c77142a1b3e42e0ff3aa3ce5ad9aeb9ae81e4894a742fe08c057f';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u345-b01_openj9-0.33.1/ibm-semeru-open-jdk_ppc64le_linux_8u345b01_openj9-0.33.1.tar.gz';          ;;        amd64|x86_64)          ESUM='b748ef07a800b4f12ade9337e4f3e42ee5207e57e688367ab0dd978ebd1876ea';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u345-b01_openj9-0.33.1/ibm-semeru-open-jdk_x64_linux_8u345b01_openj9-0.33.1.tar.gz';          ;;        s390x)          ESUM='a87652c8150390777aa98bbe6452788522d01fd0a68ab3133663191a9cd32555';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u345-b01_openj9-0.33.1/ibm-semeru-open-jdk_s390x_linux_8u345b01_openj9-0.33.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 25 Oct 2022 16:38:18 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 16:38:18 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 25 Oct 2022 16:38:53 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b300d2fee7d84af1211e2426a51e807a613efaab4d320be92c692f61b537d82e`  
		Last Modified: Wed, 26 Oct 2022 16:28:45 GMT  
		Size: 12.1 MB (12104218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94fa458129553c01514821b2012195ef971075f056f49e9c062725f241dad16`  
		Last Modified: Wed, 26 Oct 2022 16:28:52 GMT  
		Size: 116.6 MB (116645147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccbae0d75b3e9e9c033a4592ed0821021c8ef8a57cef19c2ab384e561e21ae4b`  
		Last Modified: Wed, 26 Oct 2022 16:28:42 GMT  
		Size: 4.2 MB (4237294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibm-semeru-runtimes:open-8-jdk-jammy` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:9e25c8845ea8f3331fb796b468cb4825abc9d49667b6946f38431f062b145e62
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158590247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b57d9c77deb50b1af238fb7a9b0ea9fc09bac77e81faeea5b7e285314c63cc4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:55:02 GMT
ADD file:515177312f20fb1814b89bfccfe695fa2354bbb6d43fdb6e018bf5b1acc17e9f in / 
# Tue, 25 Oct 2022 05:55:02 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 01:25:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 26 Oct 2022 01:26:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 01:26:07 GMT
ENV JAVA_VERSION=jdk8u345-b01_openj9-0.33.1
# Wed, 26 Oct 2022 01:26:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='55eb440eedc331081012664e18b4640988a210d6443289410662ff03c0b2bf05';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u345-b01_openj9-0.33.1/ibm-semeru-open-jdk_aarch64_linux_8u345b01_openj9-0.33.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7b9da287bd3c77142a1b3e42e0ff3aa3ce5ad9aeb9ae81e4894a742fe08c057f';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u345-b01_openj9-0.33.1/ibm-semeru-open-jdk_ppc64le_linux_8u345b01_openj9-0.33.1.tar.gz';          ;;        amd64|x86_64)          ESUM='b748ef07a800b4f12ade9337e4f3e42ee5207e57e688367ab0dd978ebd1876ea';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u345-b01_openj9-0.33.1/ibm-semeru-open-jdk_x64_linux_8u345b01_openj9-0.33.1.tar.gz';          ;;        s390x)          ESUM='a87652c8150390777aa98bbe6452788522d01fd0a68ab3133663191a9cd32555';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u345-b01_openj9-0.33.1/ibm-semeru-open-jdk_s390x_linux_8u345b01_openj9-0.33.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 26 Oct 2022 01:26:13 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 01:26:14 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 26 Oct 2022 01:26:48 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
```

-	Layers:
	-	`sha256:56a2caa6b2c66e01954c1a013b37ea359b6e6af8989dbfb958124b6318771af4`  
		Last Modified: Tue, 25 Oct 2022 05:56:14 GMT  
		Size: 28.4 MB (28382489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c11c12d0bb785e08a5b2215960c3c293ccc8a41ecb51a99c9c684551b48a65f`  
		Last Modified: Wed, 26 Oct 2022 01:47:57 GMT  
		Size: 12.1 MB (12062752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc847c5be91130ddf84d18a1cf85e2346ededfb70772afdef2e36a634d960ce`  
		Last Modified: Wed, 26 Oct 2022 01:48:03 GMT  
		Size: 114.1 MB (114111402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46aa85fe5dc3654e220fcf17fa7841f873401d7c79e9299b938bed574437b762`  
		Last Modified: Wed, 26 Oct 2022 01:47:56 GMT  
		Size: 4.0 MB (4033604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibm-semeru-runtimes:open-8-jdk-jammy` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:6f0f1bec674e95b77d8b17c4028cca37e533563d6285566ea2e3a0371a50163b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161119356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb01ef50de52db458af5e7ab571c730456f3ae2511ce442307e07eb484161a3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:21 GMT
ADD file:d9af7670f58e9478e400dac85a0fcb07a4209846dbd1ea560fdc6de6e2cb5e4e in / 
# Tue, 25 Oct 2022 01:23:22 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:16:04 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 25 Oct 2022 08:16:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:16:26 GMT
ENV JAVA_VERSION=jdk8u345-b01_openj9-0.33.1
# Tue, 25 Oct 2022 08:16:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='55eb440eedc331081012664e18b4640988a210d6443289410662ff03c0b2bf05';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u345-b01_openj9-0.33.1/ibm-semeru-open-jdk_aarch64_linux_8u345b01_openj9-0.33.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7b9da287bd3c77142a1b3e42e0ff3aa3ce5ad9aeb9ae81e4894a742fe08c057f';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u345-b01_openj9-0.33.1/ibm-semeru-open-jdk_ppc64le_linux_8u345b01_openj9-0.33.1.tar.gz';          ;;        amd64|x86_64)          ESUM='b748ef07a800b4f12ade9337e4f3e42ee5207e57e688367ab0dd978ebd1876ea';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u345-b01_openj9-0.33.1/ibm-semeru-open-jdk_x64_linux_8u345b01_openj9-0.33.1.tar.gz';          ;;        s390x)          ESUM='a87652c8150390777aa98bbe6452788522d01fd0a68ab3133663191a9cd32555';          BINARY_URL='https://github.com/ibmruntimes/semeru8-binaries/releases/download/jdk8u345-b01_openj9-0.33.1/ibm-semeru-open-jdk_s390x_linux_8u345b01_openj9-0.33.1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 25 Oct 2022 08:16:35 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 25 Oct 2022 08:16:35 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 25 Oct 2022 08:17:33 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
```

-	Layers:
	-	`sha256:9aed974aece14dd3aed00810d58a89e87eb5be9ad1c6fbb1ed077dc3f145dccc`  
		Last Modified: Tue, 25 Oct 2022 01:24:48 GMT  
		Size: 28.6 MB (28641668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12a873edc3afb09f0e209f7dbffa40cc274edd1bd4ca2ace16f933f6f66b158`  
		Last Modified: Tue, 25 Oct 2022 08:43:49 GMT  
		Size: 12.1 MB (12146980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2404567e93f94f6af9ad4ba2fc4a91ab9ca92e6539809a0418018c81678eb80f`  
		Last Modified: Tue, 25 Oct 2022 08:43:56 GMT  
		Size: 116.0 MB (115997403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:076a953a017710c6f781a25e4291a76c79933dea07e4f1c05eb1f2d322bcb63b`  
		Last Modified: Tue, 25 Oct 2022 08:43:48 GMT  
		Size: 4.3 MB (4333305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

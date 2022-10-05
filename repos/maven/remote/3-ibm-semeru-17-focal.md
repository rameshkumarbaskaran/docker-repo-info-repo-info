## `maven:3-ibm-semeru-17-focal`

```console
$ docker pull maven@sha256:454d28bd3a5577bfcbaaececc6bcb81bdf40a0d2617b7b5c0743dc52e3563001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `maven:3-ibm-semeru-17-focal` - linux; amd64

```console
$ docker pull maven@sha256:140480bc22c7d04b83f6d8e5c9858aa07e15c686666ec4730766844feb4d2303
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.7 MB (298726048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458c3aec633194a3e54ad26dfc810d1ed3cc308b04479551927346789c26a70e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:17:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 02 Sep 2022 03:17:54 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:23:49 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1_openj9-0.33.1
# Fri, 02 Sep 2022 03:24:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='323b02b1b4312107217dab14641617f8f41b6ab6d2662d899a50750e3a8b9af8';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jdk_aarch64_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        amd64|x86_64)          ESUM='dcdacbff5f4c8d81d5cbf5b7385a37b7935ae3b35b233b9b5d9de059246dd1c7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jdk_x64_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a89929f080c1602762d0a59d6afaf5d7e1ad536d198eecfd9b024ae7481edab5';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jdk_ppc64le_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        s390x)          ESUM='81953c5cd13fed4e0acfa0721d7d0664a9d36c20b4154e2417e68903f172454e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jdk_s390x_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 02 Sep 2022 03:24:04 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Sep 2022 03:24:04 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Fri, 02 Sep 2022 03:24:40 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Fri, 02 Sep 2022 03:24:40 GMT
CMD ["jshell"]
# Fri, 02 Sep 2022 07:16:12 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 07:16:13 GMT
ARG MAVEN_VERSION=3.8.6
# Fri, 02 Sep 2022 07:16:13 GMT
ARG USER_HOME_DIR=/root
# Fri, 02 Sep 2022 07:16:13 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Fri, 02 Sep 2022 07:16:13 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Fri, 02 Sep 2022 07:16:15 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 02 Sep 2022 07:16:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 02 Sep 2022 07:16:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 02 Sep 2022 07:16:15 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 02 Sep 2022 07:16:15 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 02 Sep 2022 07:16:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 02 Sep 2022 07:16:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d642f39b1087c24de3648cfa4a5a57017b2065655f2534de49f99c9c47642de`  
		Last Modified: Fri, 02 Sep 2022 03:28:57 GMT  
		Size: 16.0 MB (16014639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b0d5489a9f90f980fd5c5c860bc279942e717707027634da2b9c10a9b88a21`  
		Last Modified: Fri, 02 Sep 2022 03:31:13 GMT  
		Size: 208.3 MB (208343637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779a6e64cd959b8e62a00d7a331c65299fb125758987534982464e9f34769c3d`  
		Last Modified: Fri, 02 Sep 2022 03:30:59 GMT  
		Size: 5.9 MB (5870369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f232cc07c50e76473cabe68d4dc825303c103b84cfa04a3cb06d0d7b214a8f`  
		Last Modified: Fri, 02 Sep 2022 07:21:57 GMT  
		Size: 31.2 MB (31184024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962e4e238e8b8f74eb791a33046dc472b6ee60e892757dd419a05d415c5b19ee`  
		Last Modified: Fri, 02 Sep 2022 07:21:53 GMT  
		Size: 8.7 MB (8739482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7faa35d832cdb6b16f34c26697a9878a03e995af5956de6540d7814546159f53`  
		Last Modified: Fri, 02 Sep 2022 07:21:52 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b307f885d508c9a95f882241f610655cd1e0bb9d61058c162ac14cbbe655d212`  
		Last Modified: Fri, 02 Sep 2022 07:21:52 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-ibm-semeru-17-focal` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:17a4e6cac539ad2886000410b4a9e100d27314b7c51e4ad0f69da2b94d9ed7ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.0 MB (293021254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a72b289e84de2981f6fdf3662879d9a3e0f727db906ea05f6c7e38b4287282`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 16:29:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 05 Oct 2022 16:29:19 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 16:37:06 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1_openj9-0.33.1
# Wed, 05 Oct 2022 16:37:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='323b02b1b4312107217dab14641617f8f41b6ab6d2662d899a50750e3a8b9af8';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jdk_aarch64_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        amd64|x86_64)          ESUM='dcdacbff5f4c8d81d5cbf5b7385a37b7935ae3b35b233b9b5d9de059246dd1c7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jdk_x64_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a89929f080c1602762d0a59d6afaf5d7e1ad536d198eecfd9b024ae7481edab5';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jdk_ppc64le_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        s390x)          ESUM='81953c5cd13fed4e0acfa0721d7d0664a9d36c20b4154e2417e68903f172454e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jdk_s390x_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 05 Oct 2022 16:37:29 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 16:37:30 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 05 Oct 2022 16:38:06 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 05 Oct 2022 16:38:06 GMT
CMD ["jshell"]
# Wed, 05 Oct 2022 22:22:30 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 22:22:30 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 05 Oct 2022 22:22:31 GMT
ARG USER_HOME_DIR=/root
# Wed, 05 Oct 2022 22:22:32 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 05 Oct 2022 22:22:33 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 05 Oct 2022 22:22:37 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 05 Oct 2022 22:22:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 05 Oct 2022 22:22:39 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 05 Oct 2022 22:22:41 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 05 Oct 2022 22:22:42 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 05 Oct 2022 22:22:42 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 05 Oct 2022 22:22:43 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45fe284569aa12b41d3f50aebe2784a2dfd361ffe10cd93a9514885370c8da1`  
		Last Modified: Wed, 05 Oct 2022 16:47:42 GMT  
		Size: 15.9 MB (15873653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30291d04c1b4588034d96b897aff2bafceca6e53e80ff2aac7ee963563e0ec0`  
		Last Modified: Wed, 05 Oct 2022 16:50:58 GMT  
		Size: 204.5 MB (204523779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1f4bd3ddd0886bd6d9697c9cc53473f32dfa5db1131e77fc52467842bd500a8`  
		Last Modified: Wed, 05 Oct 2022 16:50:41 GMT  
		Size: 5.7 MB (5708644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c44edbe43a6a7d8d85c85131d63c0ade29822c8301d4e8306619702f002564`  
		Last Modified: Wed, 05 Oct 2022 22:28:46 GMT  
		Size: 31.0 MB (30982871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834868c521e54bac8980ebb65aa5afd08e32d83b615c54b4c9234258d3f2ddd0`  
		Last Modified: Wed, 05 Oct 2022 22:28:42 GMT  
		Size: 8.7 MB (8739474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecc706e11c28491e263322ec46267f870619dfd417ddf3d512429091dcec2ef`  
		Last Modified: Wed, 05 Oct 2022 22:28:41 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0dd1c0d25b035da6145ded8cf260209bcf745a5723bd16c98f5a3cbd4b64e`  
		Last Modified: Wed, 05 Oct 2022 22:28:41 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-ibm-semeru-17-focal` - linux; ppc64le

```console
$ docker pull maven@sha256:c2757e184498c8ab8934a51ca0aad5df6cb3a5459cea6cd068b083a8334d9a7b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.2 MB (313153874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d796313baa5847aca23a6d86cfd1a7980eb851caa8d63eb578041035059afdff`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 05 Oct 2022 10:52:08 GMT
ADD file:75224b75d955b3021df8214497d6835e1aff42b5ce83f96b779b63c4a8e15faf in / 
# Wed, 05 Oct 2022 10:52:10 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 19:23:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 05 Oct 2022 19:23:42 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 19:28:13 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1_openj9-0.33.1
# Wed, 05 Oct 2022 19:28:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='323b02b1b4312107217dab14641617f8f41b6ab6d2662d899a50750e3a8b9af8';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jdk_aarch64_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        amd64|x86_64)          ESUM='dcdacbff5f4c8d81d5cbf5b7385a37b7935ae3b35b233b9b5d9de059246dd1c7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jdk_x64_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a89929f080c1602762d0a59d6afaf5d7e1ad536d198eecfd9b024ae7481edab5';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jdk_ppc64le_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        s390x)          ESUM='81953c5cd13fed4e0acfa0721d7d0664a9d36c20b4154e2417e68903f172454e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jdk_s390x_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 05 Oct 2022 19:28:42 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 19:28:43 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 05 Oct 2022 19:29:20 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 05 Oct 2022 19:29:21 GMT
CMD ["jshell"]
# Wed, 05 Oct 2022 21:49:50 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 21:49:52 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 05 Oct 2022 21:49:52 GMT
ARG USER_HOME_DIR=/root
# Wed, 05 Oct 2022 21:49:52 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 05 Oct 2022 21:49:53 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 05 Oct 2022 21:49:54 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 05 Oct 2022 21:49:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 05 Oct 2022 21:49:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 05 Oct 2022 21:49:55 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 05 Oct 2022 21:49:56 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 05 Oct 2022 21:49:56 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 05 Oct 2022 21:49:56 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ecaa0fe591301d50850e37b61a6fac5429c04a3c39272da2f7b748eaed7f5c52`  
		Last Modified: Wed, 05 Oct 2022 10:54:26 GMT  
		Size: 33.3 MB (33296076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6d370b8f9860863a3dd8ff29fa9838d9d89f67331ce806ddf2fc681d5891b3`  
		Last Modified: Wed, 05 Oct 2022 19:34:51 GMT  
		Size: 17.2 MB (17186880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230651bfa5530bfa5b468360c5690fe3329ce6ec3a767f9074fdbe03ab56464a`  
		Last Modified: Wed, 05 Oct 2022 19:37:15 GMT  
		Size: 210.6 MB (210647428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de93c6d2d20eb4e1283fd7494bf07e6fc95f3e5cd9081385df129f56907975e`  
		Last Modified: Wed, 05 Oct 2022 19:36:50 GMT  
		Size: 4.9 MB (4893077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a067bba651e7220d608a77d0ea8f912178856c7d37721cd204ea5869615f746e`  
		Last Modified: Wed, 05 Oct 2022 21:56:42 GMT  
		Size: 38.4 MB (38389700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf9bf285b8894bc8759d98a2f9ac146388f2df4fa1d6cef10504917a0137740`  
		Last Modified: Wed, 05 Oct 2022 21:56:32 GMT  
		Size: 8.7 MB (8739504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b58d5b199a7f136f0f83269ba45509c2860ef5bbc9601dfe06ad73fb056bb9`  
		Last Modified: Wed, 05 Oct 2022 21:56:31 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7effe79a40ab80d074bb494a292d48fe11f1caef2e1d4b6ef746b0dfddef79`  
		Last Modified: Wed, 05 Oct 2022 21:56:31 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-ibm-semeru-17-focal` - linux; s390x

```console
$ docker pull maven@sha256:cd85ec121beaeafbcbc085c29922e42cab2124fd41d00c91886b4ebed1532cba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294524927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:505b94fc2fb49ed5ea193d29358753a1fd3eac44ea8c6047738300dfc8ed9106`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 04 Oct 2022 23:52:44 GMT
ADD file:f82ae9ee8436728ac9abdb4af38412611ab80a6dc434a66f2acd4f531df16e41 in / 
# Tue, 04 Oct 2022 23:52:47 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 07:13:49 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 05 Oct 2022 07:14:21 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 07:22:25 GMT
ENV JAVA_VERSION=jdk-17.0.4.1+1_openj9-0.33.1
# Wed, 05 Oct 2022 07:22:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='323b02b1b4312107217dab14641617f8f41b6ab6d2662d899a50750e3a8b9af8';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jdk_aarch64_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        amd64|x86_64)          ESUM='dcdacbff5f4c8d81d5cbf5b7385a37b7935ae3b35b233b9b5d9de059246dd1c7';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jdk_x64_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a89929f080c1602762d0a59d6afaf5d7e1ad536d198eecfd9b024ae7481edab5';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jdk_ppc64le_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;        s390x)          ESUM='81953c5cd13fed4e0acfa0721d7d0664a9d36c20b4154e2417e68903f172454e';          BINARY_URL='https://github.com/ibmruntimes/semeru17-binaries/releases/download/jdk-17.0.4.1%2B1_openj9-0.33.1/ibm-semeru-open-jdk_s390x_linux_17.0.4.1_1_openj9-0.33.1.tar.gz';          ;;       *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 05 Oct 2022 07:22:39 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 07:22:39 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Wed, 05 Oct 2022 07:23:13 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
# Wed, 05 Oct 2022 07:23:13 GMT
CMD ["jshell"]
# Wed, 05 Oct 2022 17:41:59 GMT
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 17:42:00 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 05 Oct 2022 17:42:00 GMT
ARG USER_HOME_DIR=/root
# Wed, 05 Oct 2022 17:42:00 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 05 Oct 2022 17:42:00 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 05 Oct 2022 17:42:11 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 05 Oct 2022 17:42:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 05 Oct 2022 17:42:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 05 Oct 2022 17:42:11 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 05 Oct 2022 17:42:12 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 05 Oct 2022 17:42:12 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 05 Oct 2022 17:42:12 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:55110f99e16edd33cca5c8eacd76396b8cd5660b1e57a10cbdea2b85f8c1dce5`  
		Last Modified: Tue, 04 Oct 2022 23:54:22 GMT  
		Size: 27.0 MB (27044870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f5e035abdeefe914653d062282c5e617e991637104d73ee68cc933ab06e5ae`  
		Last Modified: Wed, 05 Oct 2022 07:33:16 GMT  
		Size: 15.7 MB (15712319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c59680132b4d8288d6beb6bf97bac011a8f7e6ae4ed81eddb0ba44bf38606c`  
		Last Modified: Wed, 05 Oct 2022 07:35:30 GMT  
		Size: 206.3 MB (206278908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cb1db88675164ccf84c45ed734410a397c33bf6e1437c85e6773eda5f380dd`  
		Last Modified: Wed, 05 Oct 2022 07:35:18 GMT  
		Size: 6.1 MB (6053102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce16f6459ec0014a0ce0104410e6f4f04ad61ddf3864b49c3ee3023458ba86e0`  
		Last Modified: Wed, 05 Oct 2022 17:45:14 GMT  
		Size: 30.7 MB (30695012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:544954f4e5f843e5bc582271a3701dfe436933ad7432c185a0988daeb505db70`  
		Last Modified: Wed, 05 Oct 2022 17:45:11 GMT  
		Size: 8.7 MB (8739507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983026fb3ff632cd57799d0aa797b6ab50e72a1c9b2ad66dcf26c9c74d934cef`  
		Last Modified: Wed, 05 Oct 2022 17:45:10 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7aa60f6ac8eb1f9504f0278e6cf63a18b6ad37621bc96bb685577ac9e85cfd5`  
		Last Modified: Wed, 05 Oct 2022 17:45:10 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

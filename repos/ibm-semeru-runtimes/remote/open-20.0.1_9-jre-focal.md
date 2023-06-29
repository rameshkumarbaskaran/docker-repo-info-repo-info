## `ibm-semeru-runtimes:open-20.0.1_9-jre-focal`

```console
$ docker pull ibm-semeru-runtimes@sha256:fe3718030c7eebe68c5874288deaab8b4f7b7619893f93b726e7a4a0178f3dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	linux; s390x

### `ibm-semeru-runtimes:open-20.0.1_9-jre-focal` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:8cea528e61351069ec3a9aab9dadbe5f17c0176c491186510f6b3e338af480f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96228080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9fe4fc96c3e7e571c2348caf46afc4cef898104ed8071f4375f1505c61b173`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:07:59 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:07:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:07:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:07:59 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:08:02 GMT
ADD file:6c0661b94e27ede70ca2a8842bdab5bc26b9ae4760b17870eda9d595672795ff in / 
# Mon, 05 Jun 2023 17:08:02 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:54:14 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 16 Jun 2023 02:54:26 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 29 Jun 2023 20:40:01 GMT
ENV JAVA_VERSION=jdk-20.0.1+9_openj9-0.39.0
# Thu, 29 Jun 2023 20:42:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6194947c7edc4f570e009e966f96919251f122c641eefc6caa52f4ba98051955';          BINARY_URL='https://github.com/ibmruntimes/semeru20-binaries/releases/download/jdk-20.0.1%2B9_openj9-0.39.0/ibm-semeru-open-jre_aarch64_linux_20.0.1_9_openj9-0.39.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='b85300ee71fd77f5dbe425c64b1be175387f3605dd87c20395475184d86f9ad4';          BINARY_URL='https://github.com/ibmruntimes/semeru20-binaries/releases/download/jdk-20.0.1%2B9_openj9-0.39.0/ibm-semeru-open-jre_ppc64le_linux_20.0.1_9_openj9-0.39.0.tar.gz';          ;;        amd64|x86_64)          ESUM='2f150f140954eb4bfbbda380a3613d9dc87f4b397409bf8b7999993530b634a0';          BINARY_URL='https://github.com/ibmruntimes/semeru20-binaries/releases/download/jdk-20.0.1%2B9_openj9-0.39.0/ibm-semeru-open-jre_x64_linux_20.0.1_9_openj9-0.39.0.tar.gz';          ;;        s390x)          ESUM='446fa6d854c4925547c07b1ccead46f62d33b819dc9432c2297c5bb7b6240ad6';          BINARY_URL='https://github.com/ibmruntimes/semeru20-binaries/releases/download/jdk-20.0.1%2B9_openj9-0.39.0/ibm-semeru-open-jre_s390x_linux_20.0.1_9_openj9-0.39.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 29 Jun 2023 20:42:48 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jun 2023 20:42:48 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 29 Jun 2023 20:43:23 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
```

-	Layers:
	-	`sha256:29c851dfb906fc3c51d9a9d53a0cfa8ea88e10040baaf47155e04bf87ce3f3a5`  
		Last Modified: Fri, 09 Jun 2023 02:40:24 GMT  
		Size: 27.2 MB (27200436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908d2a4439128f77a97999ae3e8e9e21642cbb5fe6d8e9516d0c2c579a631ee2`  
		Last Modified: Fri, 16 Jun 2023 03:07:56 GMT  
		Size: 15.9 MB (15926389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e1c766098ccb1496eded86c9c9050a5cde0f5ed19dbf16846c48453109e0d2`  
		Last Modified: Thu, 29 Jun 2023 20:47:16 GMT  
		Size: 48.4 MB (48439465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40456fee149579d4bef767f727c28825de26a29b1abead60d3a7c24f8baada26`  
		Last Modified: Thu, 29 Jun 2023 20:47:12 GMT  
		Size: 4.7 MB (4661790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibm-semeru-runtimes:open-20.0.1_9-jre-focal` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:c958d9de4e5981653bfe568b1f3496392535cf253128b288dca05bcc854022fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97225467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6e94a1df21780072713caf7a17af30e9155ea5acc5d30b50ba993ef3643139`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:07:58 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:07:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:07:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:07:58 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 05 Jun 2023 17:08:00 GMT
ADD file:3aeae4efd27981f5d9d2894756f698b4fab4fbc6de4258ebd03baad8bf626d5c in / 
# Mon, 05 Jun 2023 17:08:00 GMT
CMD ["/bin/bash"]
# Sat, 17 Jun 2023 10:04:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 17 Jun 2023 10:04:18 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 29 Jun 2023 20:43:19 GMT
ENV JAVA_VERSION=jdk-20.0.1+9_openj9-0.39.0
# Thu, 29 Jun 2023 20:46:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6194947c7edc4f570e009e966f96919251f122c641eefc6caa52f4ba98051955';          BINARY_URL='https://github.com/ibmruntimes/semeru20-binaries/releases/download/jdk-20.0.1%2B9_openj9-0.39.0/ibm-semeru-open-jre_aarch64_linux_20.0.1_9_openj9-0.39.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='b85300ee71fd77f5dbe425c64b1be175387f3605dd87c20395475184d86f9ad4';          BINARY_URL='https://github.com/ibmruntimes/semeru20-binaries/releases/download/jdk-20.0.1%2B9_openj9-0.39.0/ibm-semeru-open-jre_ppc64le_linux_20.0.1_9_openj9-0.39.0.tar.gz';          ;;        amd64|x86_64)          ESUM='2f150f140954eb4bfbbda380a3613d9dc87f4b397409bf8b7999993530b634a0';          BINARY_URL='https://github.com/ibmruntimes/semeru20-binaries/releases/download/jdk-20.0.1%2B9_openj9-0.39.0/ibm-semeru-open-jre_x64_linux_20.0.1_9_openj9-0.39.0.tar.gz';          ;;        s390x)          ESUM='446fa6d854c4925547c07b1ccead46f62d33b819dc9432c2297c5bb7b6240ad6';          BINARY_URL='https://github.com/ibmruntimes/semeru20-binaries/releases/download/jdk-20.0.1%2B9_openj9-0.39.0/ibm-semeru-open-jre_s390x_linux_20.0.1_9_openj9-0.39.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 29 Jun 2023 20:46:11 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jun 2023 20:46:11 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Thu, 29 Jun 2023 20:46:44 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="0db27185d9fc3174f2c670f814df3dda8a008b89d1a38a5d96cbbe119767ebfb1cf0bce956b27954aee9be19c4a7b91f2579d967932207976322033a86075f98";     TOMCAT_DWNLD_URL="https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.35/bin/apache-tomcat-9.0.35.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed";
```

-	Layers:
	-	`sha256:bb7140b141bfafcc2950b11e56e5cb2fe27bf5fd81e61bd4bae6ad3d9b97a085`  
		Last Modified: Fri, 16 Jun 2023 18:23:16 GMT  
		Size: 27.0 MB (27013970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f398bbcfb343cda9b05009c1e9ca81450a86b7222435bd628c44a925a48aa0da`  
		Last Modified: Sat, 17 Jun 2023 10:22:00 GMT  
		Size: 15.8 MB (15754278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932c1e1bab49a2f860f3d642f0b99b6314d3d91085cbdeef575a116afb9ed584`  
		Last Modified: Thu, 29 Jun 2023 20:50:24 GMT  
		Size: 49.5 MB (49485113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15df8502b4412e0e7570cd11db66c12ea1d055e5b74b3b5c992dece30141bc80`  
		Last Modified: Thu, 29 Jun 2023 20:50:18 GMT  
		Size: 5.0 MB (4972106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

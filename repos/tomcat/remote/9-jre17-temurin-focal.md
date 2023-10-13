## `tomcat:9-jre17-temurin-focal`

```console
$ docker pull tomcat@sha256:826b1c183e518ed0022b0daf07ae3d9cd1bdbb1ca998587b1a7b55882948715c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `tomcat:9-jre17-temurin-focal` - linux; amd64

```console
$ docker pull tomcat@sha256:7703718061fadaa72d38da10065e836f4f8f6f9e1534799dd6f3dbc9f90cb27e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109287181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4f01fa487443e45b1569caf3aada4c18d6fed23a67f54919577aea666e6e99`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 02:34:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Aug 2023 02:34:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 02:34:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Aug 2023 19:23:35 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Aug 2023 20:23:47 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Thu, 31 Aug 2023 20:24:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a1c5c9ee9d20832c87bd1e99a4c4a96947b59bb35c72683fe895d705f202737';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='8af898c5d356f0b2cee2db67ff9c8e7a8e738c0f6b3a61c383150b3168b9ea58';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4aadc18e58d20c37c69cf6ec2cc3299b76f5b21073fc8e6101e11268d7a33b5b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='5eff8141fd282b3473fd649e04c113ba044cf19f0c513b951b700c28a81c1d6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ab68857594792474a3049ede09ea1178e42df29803a6a41be771794f571b2d4e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 31 Aug 2023 20:25:00 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 31 Aug 2023 20:25:00 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 31 Aug 2023 20:25:00 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 31 Aug 2023 22:32:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 31 Aug 2023 22:32:03 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Aug 2023 22:32:04 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 31 Aug 2023 22:32:04 GMT
WORKDIR /usr/local/tomcat
# Thu, 31 Aug 2023 22:32:04 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 31 Aug 2023 22:32:04 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 31 Aug 2023 22:32:04 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 31 Aug 2023 22:32:04 GMT
ENV TOMCAT_MAJOR=9
# Fri, 13 Oct 2023 00:22:22 GMT
ENV TOMCAT_VERSION=9.0.81
# Fri, 13 Oct 2023 00:22:22 GMT
ENV TOMCAT_SHA512=919957776addb26570f4c4cc2a65159409baf6b5851b3524cc07ffb7ede289ce00f454e547d309eb772e543eea0956201067e0a7b4627d182eff7e2ce042e298
# Fri, 13 Oct 2023 00:22:23 GMT
COPY dir:6380058eab87f66aa8935580d2f0bebd7b3ad73aecb3cd11dd101e3b9532be59 in /usr/local/tomcat 
# Fri, 13 Oct 2023 00:22:28 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 00:22:29 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 13 Oct 2023 00:22:29 GMT
EXPOSE 8080
# Fri, 13 Oct 2023 00:22:29 GMT
ENTRYPOINT []
# Fri, 13 Oct 2023 00:22:29 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c7ccc62e5c5023fda398ded7921663ef21bf901061cd7db06fd23dfa445d7f`  
		Last Modified: Tue, 08 Aug 2023 19:31:43 GMT  
		Size: 20.7 MB (20661907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b8056fe6bb6a89b50a9c53b459dba09de5711892a54f5100c9257909e011d4`  
		Last Modified: Thu, 31 Aug 2023 20:32:13 GMT  
		Size: 47.2 MB (47210815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb5f8cfd154d8c01073fb78f8b6088f8751d7f4cc955923809bd07585ae150b`  
		Last Modified: Thu, 31 Aug 2023 20:32:07 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6adb21bdb1e7e0da487ab662d7512c70256e874acc2251e2855a3ba33c8404b7`  
		Last Modified: Thu, 31 Aug 2023 20:32:06 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d2164433db8ddc3af1c42d888ef99670d9fd83c17883184406fa1c3b8d57da`  
		Last Modified: Thu, 31 Aug 2023 22:42:53 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e759c3ff9e8e93db83a940dbbb8526294a9b3ec1e05b4260e584ef2da186ff6a`  
		Last Modified: Fri, 13 Oct 2023 00:49:15 GMT  
		Size: 12.4 MB (12379849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90de31e6beff206db106959a3d3a4e7ac0c88c796cedc18f5ce2f2515bed127`  
		Last Modified: Fri, 13 Oct 2023 00:49:14 GMT  
		Size: 452.7 KB (452742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7784ebaf96c1a0eeda3fc2b5a67459f1b48e50bca1ec32f8129f24cba940aa11`  
		Last Modified: Fri, 13 Oct 2023 00:49:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre17-temurin-focal` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:ea4e967ffd8fe88b005e5ac063925d592101c41d6a714b00210bd84633eadfca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (102036491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c64e954cf4e062ea657753e5155236e4d5665a8eaa94e5428e5448abdbd767a2`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 03 Oct 2023 10:47:59 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:47:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:48:06 GMT
ADD file:8dffbfada6e0bebb2858525182aef87ac2cbd88c624f32696ec2cb947e71a4f3 in / 
# Tue, 03 Oct 2023 10:48:07 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 01:15:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:15:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:15:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 13 Oct 2023 01:18:28 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:18:29 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Fri, 13 Oct 2023 01:19:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a1c5c9ee9d20832c87bd1e99a4c4a96947b59bb35c72683fe895d705f202737';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='8af898c5d356f0b2cee2db67ff9c8e7a8e738c0f6b3a61c383150b3168b9ea58';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4aadc18e58d20c37c69cf6ec2cc3299b76f5b21073fc8e6101e11268d7a33b5b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='5eff8141fd282b3473fd649e04c113ba044cf19f0c513b951b700c28a81c1d6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ab68857594792474a3049ede09ea1178e42df29803a6a41be771794f571b2d4e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 13 Oct 2023 01:19:37 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 13 Oct 2023 01:19:37 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 13 Oct 2023 01:19:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 13 Oct 2023 04:24:15 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 13 Oct 2023 04:24:16 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 04:24:16 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 13 Oct 2023 04:24:16 GMT
WORKDIR /usr/local/tomcat
# Fri, 13 Oct 2023 04:24:16 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 13 Oct 2023 04:24:16 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 13 Oct 2023 04:24:16 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Fri, 13 Oct 2023 04:24:17 GMT
ENV TOMCAT_MAJOR=9
# Fri, 13 Oct 2023 04:24:17 GMT
ENV TOMCAT_VERSION=9.0.81
# Fri, 13 Oct 2023 04:24:17 GMT
ENV TOMCAT_SHA512=919957776addb26570f4c4cc2a65159409baf6b5851b3524cc07ffb7ede289ce00f454e547d309eb772e543eea0956201067e0a7b4627d182eff7e2ce042e298
# Fri, 13 Oct 2023 04:24:17 GMT
COPY dir:3d5e15a44983e4661ebe64b6e4c2f740c5f44173d1b2d3e0577d6e35dc893b86 in /usr/local/tomcat 
# Fri, 13 Oct 2023 04:24:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:24:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 13 Oct 2023 04:24:23 GMT
EXPOSE 8080
# Fri, 13 Oct 2023 04:24:23 GMT
ENTRYPOINT []
# Fri, 13 Oct 2023 04:24:23 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:3b5f1ba1b648ae0824ed6a95ab17335537f8e689df99917fd374af5dd34078eb`  
		Last Modified: Fri, 13 Oct 2023 01:11:42 GMT  
		Size: 24.6 MB (24592174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1527106f17a5b629b350869074ec790617e95a6e7701e167ea159107d7c5b2f2`  
		Last Modified: Fri, 13 Oct 2023 01:23:19 GMT  
		Size: 20.0 MB (19961731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193b39735ca70fca14bbbd3c985bab0c36f37f9ad618b9e008494e734a4adcbd`  
		Last Modified: Fri, 13 Oct 2023 01:24:23 GMT  
		Size: 44.7 MB (44720903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d665b6de6d8427c9d0721315ee4bb32cee4e31b647fe475bd972a3d7b2634b`  
		Last Modified: Fri, 13 Oct 2023 01:24:14 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8114fba4c9ed8e0b89f41105b8f2aa4d0ab56c06705a0f762e281f71f1fb2f2`  
		Last Modified: Fri, 13 Oct 2023 01:24:14 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd0231aed164652e0302a43810d2758fd9320ce8b9808d1909d1307ab83b6f3`  
		Last Modified: Fri, 13 Oct 2023 04:37:17 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356022ca67ba842812e2dccfbfcbd09e149cb02a0115c1a16509768db800bc45`  
		Last Modified: Fri, 13 Oct 2023 04:37:19 GMT  
		Size: 12.3 MB (12331253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1264b409e3dca508dd7fa621662231e2b8b50eeac4935f606e449a9c468a38`  
		Last Modified: Fri, 13 Oct 2023 04:37:17 GMT  
		Size: 429.2 KB (429238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435370b74f39e5bc4d3b967c955beea0066141ba2bbd53fc148c566b8dae90ee`  
		Last Modified: Fri, 13 Oct 2023 04:37:17 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre17-temurin-focal` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:406952dd3e8ff94f446048d489d906b2543194ac9e1c121ff5b5412a3ee53508
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108093307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84ff267ae5a5395e7e0cfe1a7361e3292a84aa74150a663fed9fbec71654699`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:56 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:57 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:21:03 GMT
ADD file:ef6e767091d76c1461d099d5bc7a18c526ec80834cf87280803ab6480192f766 in / 
# Tue, 01 Aug 2023 06:21:03 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 01:05:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Aug 2023 01:05:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 01:05:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Aug 2023 19:42:11 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Aug 2023 20:42:14 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Thu, 31 Aug 2023 20:43:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a1c5c9ee9d20832c87bd1e99a4c4a96947b59bb35c72683fe895d705f202737';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='8af898c5d356f0b2cee2db67ff9c8e7a8e738c0f6b3a61c383150b3168b9ea58';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4aadc18e58d20c37c69cf6ec2cc3299b76f5b21073fc8e6101e11268d7a33b5b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='5eff8141fd282b3473fd649e04c113ba044cf19f0c513b951b700c28a81c1d6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ab68857594792474a3049ede09ea1178e42df29803a6a41be771794f571b2d4e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 31 Aug 2023 20:43:17 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 31 Aug 2023 20:43:17 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 31 Aug 2023 20:43:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 31 Aug 2023 22:39:21 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 31 Aug 2023 22:39:21 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Aug 2023 22:39:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 31 Aug 2023 22:39:22 GMT
WORKDIR /usr/local/tomcat
# Thu, 31 Aug 2023 22:39:22 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 31 Aug 2023 22:39:22 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 31 Aug 2023 22:39:22 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 31 Aug 2023 22:39:22 GMT
ENV TOMCAT_MAJOR=9
# Fri, 13 Oct 2023 00:19:40 GMT
ENV TOMCAT_VERSION=9.0.81
# Fri, 13 Oct 2023 00:19:40 GMT
ENV TOMCAT_SHA512=919957776addb26570f4c4cc2a65159409baf6b5851b3524cc07ffb7ede289ce00f454e547d309eb772e543eea0956201067e0a7b4627d182eff7e2ce042e298
# Fri, 13 Oct 2023 00:19:41 GMT
COPY dir:13d6dbaa8e34ef38f92bb5fc6de52f227f540e8724f889f5ea77cb9a43c647d2 in /usr/local/tomcat 
# Fri, 13 Oct 2023 00:19:44 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 00:19:45 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 13 Oct 2023 00:19:45 GMT
EXPOSE 8080
# Fri, 13 Oct 2023 00:19:46 GMT
ENTRYPOINT []
# Fri, 13 Oct 2023 00:19:46 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:875232cbc2421e5da851922d68776b50b144eeec92140e53f296882c0ccbadbb`  
		Last Modified: Tue, 08 Aug 2023 19:47:26 GMT  
		Size: 21.4 MB (21378921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dfddfd1af6a93eab9c97b8137bfc08607b64bbadee5b4137233ad413e5864d9`  
		Last Modified: Thu, 31 Aug 2023 20:48:19 GMT  
		Size: 46.7 MB (46663430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09fbd5a1523bd2e25db0c6c960a6f7a1a47646beb66ad73f51f832d09e513758`  
		Last Modified: Thu, 31 Aug 2023 20:48:14 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf6d58c6c1225db9a93c4a9622bec1547cae2e84ef24f486efae173c91c799e`  
		Last Modified: Thu, 31 Aug 2023 20:48:14 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4bcaee353b75db4b0a96b5c26ded150a6f207936b1fa36c90a1f1f99797d839`  
		Last Modified: Thu, 31 Aug 2023 22:48:46 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3664a734a875d9e489a7f4e53c5516418c56882e28dcd17a1c24c535baf15b`  
		Last Modified: Fri, 13 Oct 2023 00:44:04 GMT  
		Size: 12.4 MB (12396232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721040c076d70cd6a5ef0c8b1470713aa46b9e7b6350ff319341081fce1d72fb`  
		Last Modified: Fri, 13 Oct 2023 00:44:02 GMT  
		Size: 452.9 KB (452941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79578a9424c15aeaabe72effb7344664e22311a5575ccbf0aaa03f00b1437d26`  
		Last Modified: Fri, 13 Oct 2023 00:44:02 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre17-temurin-focal` - linux; ppc64le

```console
$ docker pull tomcat@sha256:6e2bcc12ca7c29ca0f35a522fafaa1069aced7c28402615bdc1fcf3c337fff2b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.0 MB (115969854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c16465d06534eb351dbd440e4a09bd1ddcf1b48868629684d9eb4628ce05c55`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 01 Aug 2023 06:20:36 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:20:36 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:20:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:20:37 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:20:40 GMT
ADD file:822df76493d1d533c1a283ab7bb20ce81309f57279422a0eebb2ffb9fab55963 in / 
# Tue, 01 Aug 2023 06:20:40 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 02:44:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Aug 2023 02:44:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 02:44:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Aug 2023 19:23:36 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Aug 2023 20:19:26 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Thu, 31 Aug 2023 20:21:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a1c5c9ee9d20832c87bd1e99a4c4a96947b59bb35c72683fe895d705f202737';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='8af898c5d356f0b2cee2db67ff9c8e7a8e738c0f6b3a61c383150b3168b9ea58';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4aadc18e58d20c37c69cf6ec2cc3299b76f5b21073fc8e6101e11268d7a33b5b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='5eff8141fd282b3473fd649e04c113ba044cf19f0c513b951b700c28a81c1d6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ab68857594792474a3049ede09ea1178e42df29803a6a41be771794f571b2d4e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 31 Aug 2023 20:21:28 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 31 Aug 2023 20:21:29 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 31 Aug 2023 20:21:29 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 31 Aug 2023 21:41:26 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 31 Aug 2023 21:41:27 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Aug 2023 21:41:29 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 31 Aug 2023 21:41:30 GMT
WORKDIR /usr/local/tomcat
# Thu, 31 Aug 2023 21:41:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 31 Aug 2023 21:41:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 31 Aug 2023 21:41:32 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 31 Aug 2023 21:41:32 GMT
ENV TOMCAT_MAJOR=9
# Fri, 13 Oct 2023 03:48:48 GMT
ENV TOMCAT_VERSION=9.0.81
# Fri, 13 Oct 2023 03:48:50 GMT
ENV TOMCAT_SHA512=919957776addb26570f4c4cc2a65159409baf6b5851b3524cc07ffb7ede289ce00f454e547d309eb772e543eea0956201067e0a7b4627d182eff7e2ce042e298
# Fri, 13 Oct 2023 03:48:51 GMT
COPY dir:b0b2bbae2b68b25bae05e6a7bb23ed55427093fe0f35cf75e9731153a03a08be in /usr/local/tomcat 
# Fri, 13 Oct 2023 03:49:07 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 03:49:12 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 13 Oct 2023 03:49:13 GMT
EXPOSE 8080
# Fri, 13 Oct 2023 03:49:13 GMT
ENTRYPOINT []
# Fri, 13 Oct 2023 03:49:14 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:be0253994e7bea97e6b44cdeec04bf996c8dd3380e70409de3783a1d1971e747`  
		Last Modified: Thu, 03 Aug 2023 02:50:24 GMT  
		Size: 33.3 MB (33306772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c319e9f2f43271a889bc0a799583ae694861671f43953fbee6291bc1b238d87`  
		Last Modified: Tue, 08 Aug 2023 19:33:50 GMT  
		Size: 22.7 MB (22708501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32be4f711462ee4544ec5a627a42c62512a8151b8d146db1ed62d62c27bd116`  
		Last Modified: Thu, 31 Aug 2023 20:29:41 GMT  
		Size: 47.1 MB (47056164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fdf074a1cc0049c447f72414da9a0b3a34010de9011f3fead1f9de74eefee6c`  
		Last Modified: Thu, 31 Aug 2023 20:29:30 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89e3304d6063c9521e576f4194d9ded8683ea4065ef74154d472598f440fbb1`  
		Last Modified: Thu, 31 Aug 2023 20:29:30 GMT  
		Size: 732.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadd3237c940b62b5efbfcc52287b0fc78d9e1a72c56020cfcd9d0a94740c2a1`  
		Last Modified: Thu, 31 Aug 2023 22:01:19 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ceb004bf03b39e51135967d71bab6290c6c561cb4d71281a32d6f83b8c6ef2a`  
		Last Modified: Fri, 13 Oct 2023 04:27:52 GMT  
		Size: 12.4 MB (12419256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c8fc75b277e4a333847054ddf39c2ca84bea22b39f9fc87fc89b74951a0092`  
		Last Modified: Fri, 13 Oct 2023 04:27:51 GMT  
		Size: 478.0 KB (477967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b5e7fa9a3e5a52e53ffe7be9f3099c9253993e1be0853ef687059df2886f72`  
		Last Modified: Fri, 13 Oct 2023 04:27:51 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre17-temurin-focal` - linux; s390x

```console
$ docker pull tomcat@sha256:b8bd7834e4d6341a154c996f257296b7f7157762f9da0cb8b3ef6d7ebf446743
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103864494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2a1b8abc8faae93eeecd1f25e88203c6ef7e30d45302762b602a3612a22371`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 01 Aug 2023 06:17:39 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:17:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:17:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:17:39 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:17:41 GMT
ADD file:36efc3ec29bb54e0987fe91be1aa7cc849909b3cd2534af3de2d3d07a03804cf in / 
# Tue, 01 Aug 2023 06:17:41 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 00:24:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Aug 2023 00:24:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 00:24:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Aug 2023 19:43:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 31 Aug 2023 19:43:25 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Thu, 31 Aug 2023 19:44:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a1c5c9ee9d20832c87bd1e99a4c4a96947b59bb35c72683fe895d705f202737';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='8af898c5d356f0b2cee2db67ff9c8e7a8e738c0f6b3a61c383150b3168b9ea58';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4aadc18e58d20c37c69cf6ec2cc3299b76f5b21073fc8e6101e11268d7a33b5b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='5eff8141fd282b3473fd649e04c113ba044cf19f0c513b951b700c28a81c1d6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ab68857594792474a3049ede09ea1178e42df29803a6a41be771794f571b2d4e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Thu, 31 Aug 2023 19:44:36 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Thu, 31 Aug 2023 19:44:36 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 31 Aug 2023 19:44:36 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 31 Aug 2023 20:31:35 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 31 Aug 2023 20:31:35 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Aug 2023 20:31:36 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 31 Aug 2023 20:31:36 GMT
WORKDIR /usr/local/tomcat
# Thu, 31 Aug 2023 20:31:36 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 31 Aug 2023 20:31:36 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 31 Aug 2023 20:31:36 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Thu, 31 Aug 2023 20:31:36 GMT
ENV TOMCAT_MAJOR=9
# Fri, 13 Oct 2023 08:41:26 GMT
ENV TOMCAT_VERSION=9.0.81
# Fri, 13 Oct 2023 08:41:26 GMT
ENV TOMCAT_SHA512=919957776addb26570f4c4cc2a65159409baf6b5851b3524cc07ffb7ede289ce00f454e547d309eb772e543eea0956201067e0a7b4627d182eff7e2ce042e298
# Fri, 13 Oct 2023 08:41:26 GMT
COPY dir:96844b87667bc63f95537c76fe80dc305ffdc30422ef755762e5febf547345b4 in /usr/local/tomcat 
# Fri, 13 Oct 2023 08:41:31 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 08:41:32 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 13 Oct 2023 08:41:32 GMT
EXPOSE 8080
# Fri, 13 Oct 2023 08:41:33 GMT
ENTRYPOINT []
# Fri, 13 Oct 2023 08:41:33 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:365fa2124eb5f6f369204f3fe0210d9965952628707dfacd4194a8e15caf0420`  
		Last Modified: Thu, 03 Aug 2023 00:03:37 GMT  
		Size: 27.0 MB (27014233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0414709677855fc542ff87fcafa89b2a23938e36f9374a6d9a4d9db9f0723fc`  
		Last Modified: Tue, 08 Aug 2023 19:47:26 GMT  
		Size: 20.1 MB (20141237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d9d09f2aa91424acfaedc5a262913f92139a2abf8d2575b0b0c6ee4fb13cf6`  
		Last Modified: Thu, 31 Aug 2023 19:47:54 GMT  
		Size: 43.9 MB (43861819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc43d1d068393c9e7d74a99336282dbcefba3923d87f910ac33f99ddb3f740f`  
		Last Modified: Thu, 31 Aug 2023 19:47:48 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be457dd3ffaffa23664afad1accef710fbf420e6ee13a0b2f671779063c068e8`  
		Last Modified: Thu, 31 Aug 2023 19:47:48 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8c9bb503be15628defcba47cb4f4d597c4d6dc9b2638f7603910b30f46f2f5`  
		Last Modified: Thu, 31 Aug 2023 20:39:30 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6730a57e218c584a920dfbfbe5fba84fba945c0d83cb792b5f4525bc1245de58`  
		Last Modified: Fri, 13 Oct 2023 08:50:31 GMT  
		Size: 12.4 MB (12391574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58a7cca332a66a93e85f68de6746bb7452ae4b4af87940ebf145adae043f57f`  
		Last Modified: Fri, 13 Oct 2023 08:50:29 GMT  
		Size: 454.4 KB (454435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e0488c702ca5f630ecfaab5eb5a5fdf940ab3d4e3780e199d34bfd0bb57544`  
		Last Modified: Fri, 13 Oct 2023 08:50:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `tomcat:jre8-temurin`

```console
$ docker pull tomcat@sha256:9c285cef8a2ec91e68eb254e2ec56bfa244b28bd12a133702202b401d2b0902a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `tomcat:jre8-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:cff6ebe0cd80db17d33b98e296dd4698f160c8029c1c295b39e70a4051188383
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101291136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d024f1dbc1c488571d7b691a57ad6aa5469ccc6ad12d7b2ebdd61f30f9fb1e5`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:44:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 02:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 05 Nov 2021 19:19:30 GMT
ENV JAVA_VERSION=jdk8u312-b07
# Fri, 05 Nov 2021 19:19:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='961df2d520987c2252496fbee024f84c8c8c4d0be80e9fe043d221191666899e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u312b07.tar.gz';          ;;        armhf|arm)          ESUM='5f37cbf311a5c2928aff8e83a82aebcf37b5911b193b5ab8538108381dcd6276';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_arm_linux_hotspot_8u312b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='7914a2efcb7edb28df71b2d4e5194907163da06841a16f7c8c96d60677551f93';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u312b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='18fd13e77621f712326bfcf79c3e3cc08c880e3e4b8f63a1e5da619f3054b063';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_x64_linux_hotspot_8u312b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 05 Nov 2021 19:19:57 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Nov 2021 19:19:58 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 05 Nov 2021 20:05:12 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 05 Nov 2021 20:05:13 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Nov 2021 20:05:13 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 05 Nov 2021 20:05:14 GMT
WORKDIR /usr/local/tomcat
# Fri, 05 Nov 2021 20:05:14 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 05 Nov 2021 20:05:14 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 05 Nov 2021 20:05:14 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 05 Nov 2021 20:05:14 GMT
ENV TOMCAT_MAJOR=10
# Mon, 15 Nov 2021 21:07:36 GMT
ENV TOMCAT_VERSION=10.0.13
# Mon, 15 Nov 2021 21:07:36 GMT
ENV TOMCAT_SHA512=fecfe06f38ff31e31fa43c15f2566f6fcd26bb874a9b7c0533087be81d1decd97f81eefeaca7ecb5ab2b79a3ea69ed0459adff5f9d55c05f5af45f69b0725608
# Mon, 15 Nov 2021 21:07:36 GMT
COPY dir:31fd63857871178492387614a5bbe56e89d30975a98b8446253912f88412f1ac in /usr/local/tomcat 
# Mon, 15 Nov 2021 21:07:41 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Mon, 15 Nov 2021 21:07:43 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 15 Nov 2021 21:07:43 GMT
EXPOSE 8080
# Mon, 15 Nov 2021 21:07:43 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237daeb1ae282fe20092079ef6d5de7924746d0f2e9ad88797d08524a4d842fd`  
		Last Modified: Sat, 16 Oct 2021 02:47:20 GMT  
		Size: 16.0 MB (16036029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3419b8cb4a0ee9c135de60cdde81e3d4eab8e5bcf39e520c2af6b801ae607f13`  
		Last Modified: Fri, 05 Nov 2021 19:23:25 GMT  
		Size: 41.7 MB (41740806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2769989b035b1b3e743f48e8d4a5b0c56faca6618a85efb4ae7e2bfcf58d9ca`  
		Last Modified: Fri, 05 Nov 2021 19:23:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f43eb0858f19f3ed4d3451bdf32dfd26abc77e4d1ddedf2a92d12384a3f5a3a`  
		Last Modified: Fri, 05 Nov 2021 20:23:11 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec427596a558de3e061a8bb98c72ab580f27eb1f712a7c9548d40c70e87a21f`  
		Last Modified: Mon, 15 Nov 2021 21:36:18 GMT  
		Size: 12.6 MB (12593904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ab8c4d1531541131353ea33a97f780749cf5060e9880b9b0f7b01719939f10`  
		Last Modified: Mon, 15 Nov 2021 21:36:18 GMT  
		Size: 2.4 MB (2352833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b580a6d8957ab185f2e7974ff7718cdb2999b62ca12b0a6eb1503ea818e14e`  
		Last Modified: Mon, 15 Nov 2021 21:36:17 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre8-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:a1020c3d51f2ee045de7ce7f55fbc165546acebc809801928b5c8755a020b000
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 MB (96619908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1641f9980a3102eef6dacd11348de70c009e4cc71bb439097a70e6fbc1dda694`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 16 Oct 2021 01:47:45 GMT
ADD file:ff4909f2124325dac58d43c617132325934ed48a5ab4c534d05f931fcf700a2f in / 
# Sat, 16 Oct 2021 01:47:45 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 03:25:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 03:25:37 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 05 Nov 2021 19:39:29 GMT
ENV JAVA_VERSION=jdk8u312-b07
# Fri, 05 Nov 2021 19:40:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='961df2d520987c2252496fbee024f84c8c8c4d0be80e9fe043d221191666899e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u312b07.tar.gz';          ;;        armhf|arm)          ESUM='5f37cbf311a5c2928aff8e83a82aebcf37b5911b193b5ab8538108381dcd6276';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_arm_linux_hotspot_8u312b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='7914a2efcb7edb28df71b2d4e5194907163da06841a16f7c8c96d60677551f93';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u312b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='18fd13e77621f712326bfcf79c3e3cc08c880e3e4b8f63a1e5da619f3054b063';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_x64_linux_hotspot_8u312b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 05 Nov 2021 19:40:12 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Nov 2021 19:40:13 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Fri, 05 Nov 2021 20:21:03 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 05 Nov 2021 20:21:04 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Nov 2021 20:21:05 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 05 Nov 2021 20:21:06 GMT
WORKDIR /usr/local/tomcat
# Fri, 05 Nov 2021 20:21:07 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 05 Nov 2021 20:21:08 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 05 Nov 2021 20:21:09 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 05 Nov 2021 20:21:10 GMT
ENV TOMCAT_MAJOR=10
# Fri, 05 Nov 2021 20:21:11 GMT
ENV TOMCAT_VERSION=10.0.12
# Fri, 05 Nov 2021 20:21:12 GMT
ENV TOMCAT_SHA512=e084fc0cc243c0a9ac7de85ffd4b96d00b40b5493ed7ef276d91373fe8036bc953406cd3c48db6b5ae116f2af162fd1bfb13ecdddf5d64523fdd69a9463de8a3
# Fri, 05 Nov 2021 20:21:14 GMT
COPY dir:e76f19e5e49c36fae25621b982e772146e0fd77a8c4962ce58069f406e650b90 in /usr/local/tomcat 
# Fri, 05 Nov 2021 20:21:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Nov 2021 20:21:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 05 Nov 2021 20:21:24 GMT
EXPOSE 8080
# Fri, 05 Nov 2021 20:21:25 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a39c84e173f038958d338f55a9e8ee64bb6643e8ac6ae98e08ca65146e668d86`  
		Last Modified: Sat, 09 Oct 2021 15:32:18 GMT  
		Size: 27.2 MB (27170900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de699fc152b0c7a1bb0178ab0b7c6d0d2299c9f200d69a1e73d96ce334f2996d`  
		Last Modified: Sat, 16 Oct 2021 03:31:46 GMT  
		Size: 15.9 MB (15896303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7ddc58555486d3778a27bb789fafeb10a26b105adc5c091d857a9610f19079`  
		Last Modified: Fri, 05 Nov 2021 19:44:13 GMT  
		Size: 40.8 MB (40768899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefe60b4f48cf0edce71ac5a59ec44940470768ab985d797a2e31be1012859b3`  
		Last Modified: Fri, 05 Nov 2021 19:44:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbc4904c0e144e1da4e556a050b1e1963b320597ca2447a9b37c6b60733564a`  
		Last Modified: Fri, 05 Nov 2021 20:52:49 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e50c1fb950dd249578c7363b8354890b137b54667ecacbeaf7914c703304af8`  
		Last Modified: Fri, 05 Nov 2021 20:52:51 GMT  
		Size: 12.6 MB (12575043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed3342c7125a3f15612c24d677b8281a9a6a522686e59f2d645f0fdf25e8c0c`  
		Last Modified: Fri, 05 Nov 2021 20:52:49 GMT  
		Size: 208.5 KB (208497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre8-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:916398c5bec1c4029c3b0b2e6775aa3a8955fce5647897ddd06afc08f85a39bc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104714794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0733e7f4b3ecb3111bc941040440115d8de979a99e66c86b4d383820a9a723c`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:54:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:55:56 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 05 Nov 2021 20:39:01 GMT
ENV JAVA_VERSION=jdk8u312-b07
# Fri, 05 Nov 2021 20:40:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='961df2d520987c2252496fbee024f84c8c8c4d0be80e9fe043d221191666899e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u312b07.tar.gz';          ;;        armhf|arm)          ESUM='5f37cbf311a5c2928aff8e83a82aebcf37b5911b193b5ab8538108381dcd6276';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_arm_linux_hotspot_8u312b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='7914a2efcb7edb28df71b2d4e5194907163da06841a16f7c8c96d60677551f93';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u312b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='18fd13e77621f712326bfcf79c3e3cc08c880e3e4b8f63a1e5da619f3054b063';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u312-b07/OpenJDK8U-jre_x64_linux_hotspot_8u312b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 05 Nov 2021 20:40:49 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Nov 2021 20:41:07 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 06 Nov 2021 00:14:46 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 06 Nov 2021 00:14:48 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 06 Nov 2021 00:14:57 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 06 Nov 2021 00:15:01 GMT
WORKDIR /usr/local/tomcat
# Sat, 06 Nov 2021 00:15:04 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 06 Nov 2021 00:15:08 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 06 Nov 2021 00:15:11 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Sat, 06 Nov 2021 00:15:13 GMT
ENV TOMCAT_MAJOR=10
# Sat, 06 Nov 2021 00:15:16 GMT
ENV TOMCAT_VERSION=10.0.12
# Sat, 06 Nov 2021 00:15:19 GMT
ENV TOMCAT_SHA512=e084fc0cc243c0a9ac7de85ffd4b96d00b40b5493ed7ef276d91373fe8036bc953406cd3c48db6b5ae116f2af162fd1bfb13ecdddf5d64523fdd69a9463de8a3
# Sat, 06 Nov 2021 00:15:22 GMT
COPY dir:dad9ed2f0d2ca7b3d40e9703937fd403a77853121848635074b9959312d1aa75 in /usr/local/tomcat 
# Sat, 06 Nov 2021 00:15:43 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 06 Nov 2021 00:15:55 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 06 Nov 2021 00:16:01 GMT
EXPOSE 8080
# Sat, 06 Nov 2021 00:16:06 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c930749dacf55e37561edab7967f5a2f51660034fee0da501c2d71cb783301`  
		Last Modified: Sat, 16 Oct 2021 01:03:26 GMT  
		Size: 17.2 MB (17210510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8328ccd6508833e8a520d09389a536363c7280e58c4b718a755344474ea6d79d`  
		Last Modified: Fri, 05 Nov 2021 20:48:15 GMT  
		Size: 41.1 MB (41146765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25dcc78f9ba7858f03a4591c1a80c070df665d531f0423f0ab516d8604a64e2`  
		Last Modified: Fri, 05 Nov 2021 20:48:08 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7dc9e20e4f9ec54494ac0da448c214f02dde822e74d3ae96c22b2e1a9ceeac`  
		Last Modified: Sat, 06 Nov 2021 00:46:18 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca728eb5ffeeb4e0bcd0b5b14b0670d9b7396a0291fb5137d6ff108967d6479d`  
		Last Modified: Sat, 06 Nov 2021 00:46:19 GMT  
		Size: 12.6 MB (12598419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f610a8c749b6ac280f3cd9834066b0e672b5448009a95cacefad8753a14d78`  
		Last Modified: Sat, 06 Nov 2021 00:46:17 GMT  
		Size: 471.4 KB (471397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab516e80a887b3da747c669849887119d6679f1605a1baae10e671fbb0bb1df`  
		Last Modified: Sat, 06 Nov 2021 00:46:17 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

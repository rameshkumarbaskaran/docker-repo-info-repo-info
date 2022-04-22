## `tomcat:10-jre11-temurin-focal`

```console
$ docker pull tomcat@sha256:f61667e28b41b1287a9d8404c4d89c2d488d62de6053d16cebd39c4367185a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `tomcat:10-jre11-temurin-focal` - linux; amd64

```console
$ docker pull tomcat@sha256:ee0445b06ae3074375c54a8c8d7a494bf2491a713593fb8b9d0bdd675c023418
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100854370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:963c7d741ee27b06d38036630325cd25c666cd20afcb8b928bda2a8323a0f5d3`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 21 Apr 2022 23:00:07 GMT
ADD file:064c61cc9ceed678689d2eaf3b3e61ec3bf5baf9288e5a7febcbab28c6adbfb6 in / 
# Thu, 21 Apr 2022 23:00:07 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:04:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 22 Apr 2022 02:04:35 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:05:03 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Fri, 22 Apr 2022 02:05:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6426ce7dfdacaa798ec7779e0bec30ec8510df491fb2c965e8e6bf2f88af27e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='964a5d3c1f63209e5ad908a302220b3ba2e81a6574b7b7a5020f736e1496835f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c9efc13680f43b742a54ecb3be614efd62749d401e780143fef3ac5403a6284';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6b2f0292b5cf9db9ff73bbd75cb0500ec03b3dc10c95c0c8e287a95648ce7785';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b5a6960bc6bb0b1a967e307f908ea9b06ad7adbbd9df0b8954ab51374faa8a98';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 22 Apr 2022 02:05:24 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Apr 2022 02:05:24 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Fri, 22 Apr 2022 05:30:22 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 22 Apr 2022 05:30:22 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Apr 2022 05:30:23 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 22 Apr 2022 05:30:23 GMT
WORKDIR /usr/local/tomcat
# Fri, 22 Apr 2022 05:30:23 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 22 Apr 2022 05:30:23 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 22 Apr 2022 05:30:23 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 22 Apr 2022 05:30:23 GMT
ENV TOMCAT_MAJOR=10
# Fri, 22 Apr 2022 05:34:17 GMT
ENV TOMCAT_VERSION=10.0.20
# Fri, 22 Apr 2022 05:34:17 GMT
ENV TOMCAT_SHA512=53bfdbac2e6af5cca97dc01fffb0428380fbe21d8375f45d015c16a57017ff946fdc555ebad9e9fcbcb97b438c4f6daf3aa39d36ca79fd5a372cfc1a80b7117f
# Fri, 22 Apr 2022 05:34:17 GMT
COPY dir:69cc03b9df3620943cc3de4e0e2e6a70fed84c60d3819ee0e4d9b7d14750e21e in /usr/local/tomcat 
# Fri, 22 Apr 2022 05:34:21 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 05:34:23 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 22 Apr 2022 05:34:23 GMT
EXPOSE 8080
# Fri, 22 Apr 2022 05:34:23 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8e5c1b329fe39c318c0d49821b339fb94a215c5dc0a2898c8030b5a4d091bcba`  
		Last Modified: Sun, 17 Apr 2022 03:03:46 GMT  
		Size: 28.6 MB (28565998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b11e2aa9202b3c11a943dfa8adc2bef4462ab2165124b84051d10250faff2a0`  
		Last Modified: Fri, 22 Apr 2022 02:08:16 GMT  
		Size: 16.0 MB (16030117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472f4f0c5d6412755b08c96f99771c7aeb53b2208d7c34a03f9c7be592a8a412`  
		Last Modified: Fri, 22 Apr 2022 02:09:28 GMT  
		Size: 43.2 MB (43230162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8794c46632ab780fe47457f40fdcba994389c7cdf193ca9f20045b952c4254a`  
		Last Modified: Fri, 22 Apr 2022 02:09:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd17d438044115ca03bc2a263db022471e1abf82ae0621258251c45eb5afd15c`  
		Last Modified: Fri, 22 Apr 2022 05:58:08 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4c338728e5fdf6e8293fecdaae41958524e5747f508c150dbb26dc750c7ff3`  
		Last Modified: Fri, 22 Apr 2022 06:01:25 GMT  
		Size: 12.6 MB (12582482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bed270903a8b64c8a86716e48bd1db23011be1f4d17aabcbea6b85dd733fcc4`  
		Last Modified: Fri, 22 Apr 2022 06:01:24 GMT  
		Size: 445.1 KB (445149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc02371a1a372e0486af4f957b7843d71fa5c26b3338fb85253e3b3071586cd4`  
		Last Modified: Fri, 22 Apr 2022 06:01:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre11-temurin-focal` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:890e979dbb4171b9526164a5629f441452dd0e899cd917171d9d5fdafb8d4858
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93779474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350d62a8fe1ce5229b219f14c95d613e80d085b460a706f5a6310f35975915ab`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 06 Apr 2022 03:26:01 GMT
ADD file:be35fd9a0ef4a49afbe583edf1750187cad18b1bde4e7bf0ab344464740b5749 in / 
# Wed, 06 Apr 2022 03:26:01 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:03:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Apr 2022 04:03:57 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:05:10 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Wed, 06 Apr 2022 04:06:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6426ce7dfdacaa798ec7779e0bec30ec8510df491fb2c965e8e6bf2f88af27e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='964a5d3c1f63209e5ad908a302220b3ba2e81a6574b7b7a5020f736e1496835f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c9efc13680f43b742a54ecb3be614efd62749d401e780143fef3ac5403a6284';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6b2f0292b5cf9db9ff73bbd75cb0500ec03b3dc10c95c0c8e287a95648ce7785';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b5a6960bc6bb0b1a967e307f908ea9b06ad7adbbd9df0b8954ab51374faa8a98';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Apr 2022 04:06:01 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 04:06:02 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 06 Apr 2022 07:59:34 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Apr 2022 07:59:35 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 07:59:36 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 06 Apr 2022 07:59:37 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Apr 2022 07:59:37 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Apr 2022 07:59:38 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Apr 2022 07:59:38 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 06 Apr 2022 07:59:38 GMT
ENV TOMCAT_MAJOR=10
# Wed, 06 Apr 2022 08:05:10 GMT
ENV TOMCAT_VERSION=10.0.20
# Wed, 06 Apr 2022 08:05:11 GMT
ENV TOMCAT_SHA512=53bfdbac2e6af5cca97dc01fffb0428380fbe21d8375f45d015c16a57017ff946fdc555ebad9e9fcbcb97b438c4f6daf3aa39d36ca79fd5a372cfc1a80b7117f
# Wed, 06 Apr 2022 08:05:13 GMT
COPY dir:64ebde0eff29a76e3baff8da57085245f55d02e83d0fac2c34541a3dffe701f5 in /usr/local/tomcat 
# Wed, 06 Apr 2022 08:05:23 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 08:05:27 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 06 Apr 2022 08:05:27 GMT
EXPOSE 8080
# Wed, 06 Apr 2022 08:05:28 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:de340d6c69b8bed917b969ad75b8fe4fe951502bc050b013dc9151c3632fb704`  
		Last Modified: Tue, 05 Apr 2022 13:15:39 GMT  
		Size: 24.1 MB (24073792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a319b7b639fd75994a3f8c3a0d6d5c796fe594f9aa331d464280662ba19da6b`  
		Last Modified: Wed, 06 Apr 2022 04:12:16 GMT  
		Size: 14.9 MB (14900542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa85bc24dc516a1e4fbc573adbf5cbc173fc45553d4c3d8e220ca62ed46d898`  
		Last Modified: Wed, 06 Apr 2022 04:15:28 GMT  
		Size: 41.9 MB (41850617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d691e727fa9da7b8d4cbf21e9207ef94b77a88fb30e4a879d7bb8773cfaad330`  
		Last Modified: Wed, 06 Apr 2022 04:15:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0aa797710818e037fb99552192ce119e36abf27f546d89e634ff5455210e962`  
		Last Modified: Wed, 06 Apr 2022 10:16:52 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73c8d27f8fc9b52f8850a0a87bd017fd2b544bd41dacb551596ebdd6704dda9`  
		Last Modified: Wed, 06 Apr 2022 10:20:13 GMT  
		Size: 12.5 MB (12532274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25330965e6a2697bb23de432837a8a3b6c2522932f4470da64cc2bdf272cf4a`  
		Last Modified: Wed, 06 Apr 2022 10:20:08 GMT  
		Size: 421.8 KB (421785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86b65e6f7ab034c9fcb12ae4e364a54722d452d8b9a30dcf945d5dd85bbe970`  
		Last Modified: Wed, 06 Apr 2022 10:20:09 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre11-temurin-focal` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:5f60b168f4432ad060b4bb691f0f1754f7d21d4d1ea627ca2c310687b8446e01
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.4 MB (97444652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b56590ddb33940ce345860698d948ebbcd2210aac24e1325ebdf00128caf960`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 22 Apr 2022 00:54:11 GMT
ADD file:6ca4a270cea388f6267a1c7739fd787a34793f48bf8480740a383b5e73299af2 in / 
# Fri, 22 Apr 2022 00:54:11 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 02:56:28 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 22 Apr 2022 02:56:46 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 02:57:27 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Fri, 22 Apr 2022 02:57:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6426ce7dfdacaa798ec7779e0bec30ec8510df491fb2c965e8e6bf2f88af27e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='964a5d3c1f63209e5ad908a302220b3ba2e81a6574b7b7a5020f736e1496835f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c9efc13680f43b742a54ecb3be614efd62749d401e780143fef3ac5403a6284';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6b2f0292b5cf9db9ff73bbd75cb0500ec03b3dc10c95c0c8e287a95648ce7785';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b5a6960bc6bb0b1a967e307f908ea9b06ad7adbbd9df0b8954ab51374faa8a98';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 22 Apr 2022 02:57:56 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Apr 2022 02:57:57 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Fri, 22 Apr 2022 05:30:58 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 22 Apr 2022 05:30:59 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Apr 2022 05:31:00 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 22 Apr 2022 05:31:01 GMT
WORKDIR /usr/local/tomcat
# Fri, 22 Apr 2022 05:31:02 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 22 Apr 2022 05:31:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 22 Apr 2022 05:31:04 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 22 Apr 2022 05:31:05 GMT
ENV TOMCAT_MAJOR=10
# Fri, 22 Apr 2022 05:36:25 GMT
ENV TOMCAT_VERSION=10.0.20
# Fri, 22 Apr 2022 05:36:25 GMT
ENV TOMCAT_SHA512=53bfdbac2e6af5cca97dc01fffb0428380fbe21d8375f45d015c16a57017ff946fdc555ebad9e9fcbcb97b438c4f6daf3aa39d36ca79fd5a372cfc1a80b7117f
# Fri, 22 Apr 2022 05:36:27 GMT
COPY dir:d6caf9024794838cb720d43c08abd00fce66728b09bcbeb76623f2b223c33e52 in /usr/local/tomcat 
# Fri, 22 Apr 2022 05:36:33 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 05:36:35 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 22 Apr 2022 05:36:36 GMT
EXPOSE 8080
# Fri, 22 Apr 2022 05:36:37 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:61e1864f78be077e322819a4ce1e09da9389c8119cf552629dc048b713a3f42b`  
		Last Modified: Tue, 19 Apr 2022 13:13:57 GMT  
		Size: 27.2 MB (27169141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89015ff109b922c48ff7f1847b2e63f33dc54bd022e11f479dbed2eb7fb5da0`  
		Last Modified: Fri, 22 Apr 2022 03:02:05 GMT  
		Size: 15.9 MB (15895876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec453ac99a9939a498000b4312da74d702ea3ae510b1c61e2b2ba6ab1705d75`  
		Last Modified: Fri, 22 Apr 2022 03:03:27 GMT  
		Size: 41.6 MB (41572364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a091800aef8bea9c75d3ed17faa03c050e35d951671879d52ee8508abbe4854c`  
		Last Modified: Fri, 22 Apr 2022 03:03:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce13cf1c55c6277ca2a04781cb0ea52854c1cca50920d4708312183bd80f07e`  
		Last Modified: Fri, 22 Apr 2022 07:56:14 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b9c1ff3ae25e67e104b88391a786de922ad034a69ba9cec8bae033762bcb23`  
		Last Modified: Fri, 22 Apr 2022 08:00:21 GMT  
		Size: 12.6 MB (12598630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9324854195addd76f2afee002d2fa5e5354b9a976968e0cdc019226036821b32`  
		Last Modified: Fri, 22 Apr 2022 08:00:19 GMT  
		Size: 208.4 KB (208375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre11-temurin-focal` - linux; ppc64le

```console
$ docker pull tomcat@sha256:654358dfa0e7423eabf6a1cbc45877a43d1fa192257204ba1fe9ae571d2cfaa1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102232370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed41dccd14c2ba061607c616d81892873260c0151f73633079fc0a7ca9eab1aa`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 06 Apr 2022 03:35:37 GMT
ADD file:c1af9c0e405f7eecbc87225c13709becfd46d66f87a4c5b8e30a1b82de7337e5 in / 
# Wed, 06 Apr 2022 03:35:41 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:53:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 06 Apr 2022 04:55:12 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:57:20 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Wed, 06 Apr 2022 04:58:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6426ce7dfdacaa798ec7779e0bec30ec8510df491fb2c965e8e6bf2f88af27e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='964a5d3c1f63209e5ad908a302220b3ba2e81a6574b7b7a5020f736e1496835f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c9efc13680f43b742a54ecb3be614efd62749d401e780143fef3ac5403a6284';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6b2f0292b5cf9db9ff73bbd75cb0500ec03b3dc10c95c0c8e287a95648ce7785';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b5a6960bc6bb0b1a967e307f908ea9b06ad7adbbd9df0b8954ab51374faa8a98';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 06 Apr 2022 04:58:39 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 04:58:52 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Wed, 06 Apr 2022 08:54:05 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 06 Apr 2022 08:54:10 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Apr 2022 08:54:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 06 Apr 2022 08:54:27 GMT
WORKDIR /usr/local/tomcat
# Wed, 06 Apr 2022 08:54:31 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 06 Apr 2022 08:54:36 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 06 Apr 2022 08:54:39 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 06 Apr 2022 08:54:45 GMT
ENV TOMCAT_MAJOR=10
# Wed, 06 Apr 2022 09:17:15 GMT
ENV TOMCAT_VERSION=10.0.20
# Wed, 06 Apr 2022 09:17:20 GMT
ENV TOMCAT_SHA512=53bfdbac2e6af5cca97dc01fffb0428380fbe21d8375f45d015c16a57017ff946fdc555ebad9e9fcbcb97b438c4f6daf3aa39d36ca79fd5a372cfc1a80b7117f
# Wed, 06 Apr 2022 09:17:24 GMT
COPY dir:03b567f2bcf010def21eea432a11484ba5486fbbb0d12d69b7c97ff24cef51f4 in /usr/local/tomcat 
# Wed, 06 Apr 2022 09:17:50 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 09:18:00 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 06 Apr 2022 09:18:05 GMT
EXPOSE 8080
# Wed, 06 Apr 2022 09:18:08 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:83a2da48a82b52067676278a5eb4359bd7a79e7b57cabd370d77e11a9204121c`  
		Last Modified: Tue, 05 Apr 2022 13:16:22 GMT  
		Size: 33.3 MB (33291809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51134a7a9e0d0b603ce41f6ef7aa0f9d1a77696cb80e63a1e73b539ff51023b0`  
		Last Modified: Wed, 06 Apr 2022 05:08:30 GMT  
		Size: 17.2 MB (17204248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bdd8b3ba5b0f6527dcca4f33dae7e3d64de8b73ba86bfeb56b90ef03dcf3882`  
		Last Modified: Wed, 06 Apr 2022 05:10:05 GMT  
		Size: 38.6 MB (38640562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46788ba98b3a35d941d00afc371ac3f0bfaabacac1e036394b33b7a0b9222c9e`  
		Last Modified: Wed, 06 Apr 2022 05:09:58 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c137db0058d1869bcbee02ddfdd086b5148fb14f0615accbfdcbe9883ad1a1`  
		Last Modified: Wed, 06 Apr 2022 10:18:10 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b790a9558f56cce2620dd926669e273d1ac6fe535b5c872cacf7dbab1a20c7fb`  
		Last Modified: Wed, 06 Apr 2022 10:21:08 GMT  
		Size: 12.6 MB (12624263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40fa9c950de5b5daf04c7b18947e882dc829beec0be7a04959a27c0ee1756d7`  
		Last Modified: Wed, 06 Apr 2022 10:21:07 GMT  
		Size: 471.0 KB (471024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c585373f73ed60790659b30212ddba2e151820c79b034ac7893e94cc9fee911`  
		Last Modified: Wed, 06 Apr 2022 10:21:07 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre11-temurin-focal` - linux; s390x

```console
$ docker pull tomcat@sha256:36b196e4d8c670d1e046da882c4815a1d0c728d1ce67f4a4794239117ca14450
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93196378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3787c737917396a76c9fa47c54b89f2fa7f5ccc2a47026ca23e7469d40c2e4d`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Fri, 22 Apr 2022 00:39:34 GMT
ADD file:a5fe3b5fef5d5d99022e3a45894edf18c9e5f79c4be8020d61724cdc164256b3 in / 
# Fri, 22 Apr 2022 00:39:39 GMT
CMD ["bash"]
# Fri, 22 Apr 2022 01:54:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 22 Apr 2022 01:55:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 01:55:42 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Fri, 22 Apr 2022 01:56:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='6426ce7dfdacaa798ec7779e0bec30ec8510df491fb2c965e8e6bf2f88af27e9';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_aarch64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        armhf|arm)          ESUM='964a5d3c1f63209e5ad908a302220b3ba2e81a6574b7b7a5020f736e1496835f';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_arm_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='8c9efc13680f43b742a54ecb3be614efd62749d401e780143fef3ac5403a6284';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_ppc64le_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='6b2f0292b5cf9db9ff73bbd75cb0500ec03b3dc10c95c0c8e287a95648ce7785';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_s390x_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b5a6960bc6bb0b1a967e307f908ea9b06ad7adbbd9df0b8954ab51374faa8a98';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 22 Apr 2022 01:56:50 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Apr 2022 01:56:52 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
# Fri, 22 Apr 2022 06:48:16 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 22 Apr 2022 06:48:16 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Apr 2022 06:48:18 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 22 Apr 2022 06:48:18 GMT
WORKDIR /usr/local/tomcat
# Fri, 22 Apr 2022 06:48:18 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 22 Apr 2022 06:48:19 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 22 Apr 2022 06:48:19 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Fri, 22 Apr 2022 06:48:20 GMT
ENV TOMCAT_MAJOR=10
# Fri, 22 Apr 2022 06:50:55 GMT
ENV TOMCAT_VERSION=10.0.20
# Fri, 22 Apr 2022 06:50:55 GMT
ENV TOMCAT_SHA512=53bfdbac2e6af5cca97dc01fffb0428380fbe21d8375f45d015c16a57017ff946fdc555ebad9e9fcbcb97b438c4f6daf3aa39d36ca79fd5a372cfc1a80b7117f
# Fri, 22 Apr 2022 06:50:55 GMT
COPY dir:e724c3d6292db7f8a88c8b89cff34aa2e6481c5dc8f236a0f04345093cc67ad8 in /usr/local/tomcat 
# Fri, 22 Apr 2022 06:51:01 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 22 Apr 2022 06:51:02 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 22 Apr 2022 06:51:02 GMT
EXPOSE 8080
# Fri, 22 Apr 2022 06:51:02 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:716ba34a9a0241d7bed3fa68865e745000f025af68d21dab7d692215c5074a58`  
		Last Modified: Tue, 19 Apr 2022 13:16:37 GMT  
		Size: 27.1 MB (27085718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ad99882b01b0ab3e7045a65b2c93f1319b8763364d776de22578aaade5be51`  
		Last Modified: Fri, 22 Apr 2022 02:02:24 GMT  
		Size: 15.7 MB (15738876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15da2c30e27b3194fe4046ce2dcd7c67f9048ff42ac1cfa3d4e0b36e5aed15fe`  
		Last Modified: Fri, 22 Apr 2022 02:02:48 GMT  
		Size: 37.3 MB (37328896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48e5685d322efe09d5c7285e6d1bc46b5a8741d98b1fea71adc73d88c3436ad`  
		Last Modified: Fri, 22 Apr 2022 02:02:43 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02261d0639ef0a1175bb783984f7b90e358184e24706f3f1cab025fe52e1b402`  
		Last Modified: Fri, 22 Apr 2022 07:01:51 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9975030948dc95d19fab79c453fbd8e0958990022efa5c0803da0c3ab56a466`  
		Last Modified: Fri, 22 Apr 2022 07:03:41 GMT  
		Size: 12.6 MB (12595421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2575529139d9c764b3f8429f6cb921d9a3299210baad8ddf282b158307d12a`  
		Last Modified: Fri, 22 Apr 2022 07:03:40 GMT  
		Size: 447.0 KB (447005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a5d55ecc1857f39710c60c05a747c1124534a0265406c05a05a043f4fc0a5ab`  
		Last Modified: Fri, 22 Apr 2022 07:03:40 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

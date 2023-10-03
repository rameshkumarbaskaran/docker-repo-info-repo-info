## `tomcat:10-jre17-temurin`

```console
$ docker pull tomcat@sha256:679e2a1df1736a7233bb4202a78731981b6073488a61076c26e21a0ae0a914a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `tomcat:10-jre17-temurin` - linux; amd64

```console
$ docker pull tomcat@sha256:9474660dd81c6ac496e5f7eb7cbc86100abf0e30c52a63292f949744a117da33
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107772444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c24b139c7bba499c51395ab430803ba19c74d2915ba0aec5e35a10a472a561f`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 16 Aug 2023 06:01:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:01:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:01:54 GMT
ADD file:aa9b51e9f0067860cebbc9930374452d1384ec3c59badb5e4733130eedc90329 in / 
# Wed, 16 Aug 2023 06:01:54 GMT
CMD ["/bin/bash"]
# Sat, 02 Sep 2023 00:37:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Sep 2023 00:37:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 00:37:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 02 Sep 2023 00:39:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 00:39:30 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Sat, 02 Sep 2023 00:40:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a1c5c9ee9d20832c87bd1e99a4c4a96947b59bb35c72683fe895d705f202737';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='8af898c5d356f0b2cee2db67ff9c8e7a8e738c0f6b3a61c383150b3168b9ea58';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4aadc18e58d20c37c69cf6ec2cc3299b76f5b21073fc8e6101e11268d7a33b5b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='5eff8141fd282b3473fd649e04c113ba044cf19f0c513b951b700c28a81c1d6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ab68857594792474a3049ede09ea1178e42df29803a6a41be771794f571b2d4e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 02 Sep 2023 00:40:01 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 02 Sep 2023 00:40:01 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 02 Sep 2023 00:40:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 02 Sep 2023 03:42:30 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 02 Sep 2023 03:42:30 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 03:42:30 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 02 Sep 2023 03:42:30 GMT
WORKDIR /usr/local/tomcat
# Sat, 02 Sep 2023 03:42:30 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 02 Sep 2023 03:42:30 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 02 Sep 2023 03:42:30 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Sat, 02 Sep 2023 03:42:31 GMT
ENV TOMCAT_MAJOR=10
# Sat, 02 Sep 2023 03:42:31 GMT
ENV TOMCAT_VERSION=10.1.13
# Sat, 02 Sep 2023 03:42:31 GMT
ENV TOMCAT_SHA512=406c0c367ac6ad95bb724ecc3a3c340ad7ded8c62287d657811eeec496eaaca1f5add52d2f46111da1426ae67090c543f6deccfeb5fdf4bdae32f9b39e773265
# Sat, 02 Sep 2023 03:42:31 GMT
COPY dir:ebb556ae4aa614339839c4d572d8d5fd88682b599380a2354c5edfb2dbb528bc in /usr/local/tomcat 
# Sat, 02 Sep 2023 03:42:35 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 03:42:36 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 02 Sep 2023 03:42:36 GMT
EXPOSE 8080
# Sat, 02 Sep 2023 03:42:37 GMT
ENTRYPOINT []
# Sat, 02 Sep 2023 03:42:37 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:44ba2882f8eb14264e5f2f9f6ec55bcf5306527b637279f2cd9d4858762388af`  
		Last Modified: Wed, 16 Aug 2023 10:32:51 GMT  
		Size: 30.4 MB (30438977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cabec57fa3613116cbc641e1159ee0a7bde39ef9b3046a4e2122a5b390b7db5`  
		Last Modified: Sat, 02 Sep 2023 00:42:56 GMT  
		Size: 17.5 MB (17456268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20481384b6a46f3042a39f85fd4ab7f6745ce59baa6d09cace3e072d0edc5c2`  
		Last Modified: Sat, 02 Sep 2023 00:43:25 GMT  
		Size: 47.2 MB (47209785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7b17ee74f8bc587bd9f02a67aaea2199e2b417b8b310a2a61843b8b566dc1e`  
		Last Modified: Sat, 02 Sep 2023 00:43:18 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38617faac714d7db923ebee3829ba18873481eef3df7bb28d5f9de1dac27cbbb`  
		Last Modified: Sat, 02 Sep 2023 00:43:18 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3ef8a28ca72d66683b645424ac938924bc3431b00ffd858aced158dcbcded1`  
		Last Modified: Sat, 02 Sep 2023 03:51:31 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90f51d69351fa968ea18c3d19c9eac13576bbf39f1104943afc483e5e1aeb87`  
		Last Modified: Sat, 02 Sep 2023 03:51:32 GMT  
		Size: 12.2 MB (12207937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4681b3477bdf1595ece6e1d277a5c04868b039a6881381e889aff55a9bc0026`  
		Last Modified: Sat, 02 Sep 2023 03:51:31 GMT  
		Size: 458.3 KB (458282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc36c5603bf933cbc449da79387229f28f0a6ff8ef54e2f3f37c528265cfd3f`  
		Last Modified: Sat, 02 Sep 2023 03:51:31 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre17-temurin` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:16c88da3f714f698271831e9e3a5e0316cc7820fe92065b2feb8ecc1bae1e895
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102439117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3dbe05c619b6c37aa6efacf6a17f2cf97dea9ff43af06f0f4294ead22e69d7`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 25 Sep 2023 10:19:15 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:19:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:19:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:19:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:19:18 GMT
ADD file:0008d56422c09f73afbcd40ace46d311e36ba0d60eef05198ea3665172ba3433 in / 
# Mon, 25 Sep 2023 10:19:18 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:00:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 06:00:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 06:00:54 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Oct 2023 06:02:49 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:02:50 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Tue, 03 Oct 2023 06:03:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a1c5c9ee9d20832c87bd1e99a4c4a96947b59bb35c72683fe895d705f202737';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='8af898c5d356f0b2cee2db67ff9c8e7a8e738c0f6b3a61c383150b3168b9ea58';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4aadc18e58d20c37c69cf6ec2cc3299b76f5b21073fc8e6101e11268d7a33b5b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='5eff8141fd282b3473fd649e04c113ba044cf19f0c513b951b700c28a81c1d6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ab68857594792474a3049ede09ea1178e42df29803a6a41be771794f571b2d4e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 03 Oct 2023 06:03:14 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 03 Oct 2023 06:03:14 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 03 Oct 2023 06:03:14 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Oct 2023 06:55:31 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 03 Oct 2023 06:55:31 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 06:55:31 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 03 Oct 2023 06:55:32 GMT
WORKDIR /usr/local/tomcat
# Tue, 03 Oct 2023 06:55:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 03 Oct 2023 06:55:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 03 Oct 2023 06:55:32 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Tue, 03 Oct 2023 06:55:32 GMT
ENV TOMCAT_MAJOR=10
# Tue, 03 Oct 2023 06:55:32 GMT
ENV TOMCAT_VERSION=10.1.13
# Tue, 03 Oct 2023 06:55:32 GMT
ENV TOMCAT_SHA512=406c0c367ac6ad95bb724ecc3a3c340ad7ded8c62287d657811eeec496eaaca1f5add52d2f46111da1426ae67090c543f6deccfeb5fdf4bdae32f9b39e773265
# Tue, 03 Oct 2023 06:55:33 GMT
COPY dir:20f7e146b72723cd1370b752da0534ec3975805ae53a3782835faa14d3e1a5e9 in /usr/local/tomcat 
# Tue, 03 Oct 2023 06:55:37 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:55:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 03 Oct 2023 06:55:39 GMT
EXPOSE 8080
# Tue, 03 Oct 2023 06:55:39 GMT
ENTRYPOINT []
# Tue, 03 Oct 2023 06:55:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7271b2c80df6c73d794550b50f57d78c6fd5b85da7934c6506c76ea706087280`  
		Last Modified: Tue, 26 Sep 2023 02:07:56 GMT  
		Size: 27.5 MB (27515498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a42f949007cfbde4e09ba505ced26b019abd8a7ea5591c2ee0c80fe213191ee`  
		Last Modified: Tue, 03 Oct 2023 06:05:16 GMT  
		Size: 17.6 MB (17587273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145989d52f31b92e2cb1ee36172544f5011e1ffd647b3c3f8c84cbcb896762d8`  
		Last Modified: Tue, 03 Oct 2023 06:05:46 GMT  
		Size: 44.7 MB (44720426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0301b0a89e028bdae255db9cee1f9a0868e11532c7ef1e248d291ef9bc306ef6`  
		Last Modified: Tue, 03 Oct 2023 06:05:39 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c371b266a446481f73698616b8de8bce137ea75da76aa21685fb67cab1c732c`  
		Last Modified: Tue, 03 Oct 2023 06:05:39 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:605b83551005ecc509d7c17a2dfd7e1b28d8f91425df0d466c749d7a752773db`  
		Last Modified: Tue, 03 Oct 2023 07:03:49 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa248cfaeb82c9900411f29b4799c8d0af5f9e8f645c50539534c8d9abaf1c2`  
		Last Modified: Tue, 03 Oct 2023 07:03:51 GMT  
		Size: 12.2 MB (12182573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439e2535dbc632e7887955d1997ea276614b374adb378e6d85b0d3a2257016cc`  
		Last Modified: Tue, 03 Oct 2023 07:03:49 GMT  
		Size: 432.1 KB (432150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a5ea906d26b2ce090ca6962450a9e17ef3ee70ff4ab7e9dbe05fccfad0af4e`  
		Last Modified: Tue, 03 Oct 2023 07:03:49 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre17-temurin` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:87f56bf4848ba62b2248534bfc85cb51d4e870727f5939bb930f979bee32c794
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106582600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1857b9fba5de929eb99cc04b1008e7ed03abb966cd832c8388c6d41131b22a8b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:41 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:44 GMT
ADD file:8540670760767f19eaf101fbce1da1881a2f24a7d65da6abdedc644b8fb00463 in / 
# Mon, 25 Sep 2023 10:17:45 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:06:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 06:06:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 06:06:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Oct 2023 06:08:16 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:08:17 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Tue, 03 Oct 2023 06:08:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a1c5c9ee9d20832c87bd1e99a4c4a96947b59bb35c72683fe895d705f202737';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='8af898c5d356f0b2cee2db67ff9c8e7a8e738c0f6b3a61c383150b3168b9ea58';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4aadc18e58d20c37c69cf6ec2cc3299b76f5b21073fc8e6101e11268d7a33b5b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='5eff8141fd282b3473fd649e04c113ba044cf19f0c513b951b700c28a81c1d6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ab68857594792474a3049ede09ea1178e42df29803a6a41be771794f571b2d4e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 03 Oct 2023 06:08:43 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 03 Oct 2023 06:08:43 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 03 Oct 2023 06:08:43 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Oct 2023 07:49:10 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 03 Oct 2023 07:49:11 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 07:49:11 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 03 Oct 2023 07:49:11 GMT
WORKDIR /usr/local/tomcat
# Tue, 03 Oct 2023 07:49:11 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 03 Oct 2023 07:49:11 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 03 Oct 2023 07:49:11 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Tue, 03 Oct 2023 07:49:11 GMT
ENV TOMCAT_MAJOR=10
# Tue, 03 Oct 2023 07:49:11 GMT
ENV TOMCAT_VERSION=10.1.13
# Tue, 03 Oct 2023 07:49:12 GMT
ENV TOMCAT_SHA512=406c0c367ac6ad95bb724ecc3a3c340ad7ded8c62287d657811eeec496eaaca1f5add52d2f46111da1426ae67090c543f6deccfeb5fdf4bdae32f9b39e773265
# Tue, 03 Oct 2023 07:49:12 GMT
COPY dir:f5a65ca5608ef61d1ef33a3c706dc35d5c6154a8cab5cfc6f47f93a7d5e62076 in /usr/local/tomcat 
# Tue, 03 Oct 2023 07:49:15 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 07:49:17 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 03 Oct 2023 07:49:17 GMT
EXPOSE 8080
# Tue, 03 Oct 2023 07:49:17 GMT
ENTRYPOINT []
# Tue, 03 Oct 2023 07:49:17 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6ea603f1df5e3d23206761eca19fba4cdf4e22d773256cb65b71b730aa5acced`  
		Last Modified: Mon, 25 Sep 2023 17:30:11 GMT  
		Size: 28.4 MB (28392073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba2aefbab3334adfc4bfa89dd448c89bc452ab89a02053172fb42a8e5288ba3`  
		Last Modified: Tue, 03 Oct 2023 06:11:30 GMT  
		Size: 18.9 MB (18859718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86987693004111861f9443dc32898933eec4343daaf42ab9dc3a6c2293a00f17`  
		Last Modified: Tue, 03 Oct 2023 06:11:58 GMT  
		Size: 46.7 MB (46662509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481239d57792994fec36a7d26628f989bba00fc6028177d526dc663c9ca282be`  
		Last Modified: Tue, 03 Oct 2023 06:11:52 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0707fa9330d33b1b893d8ce0bd2ff1686e61307f78edc6bd0903b07c35a5ffd3`  
		Last Modified: Tue, 03 Oct 2023 06:11:52 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d85fdbfd2b58b149fbdd4365ba1c580923ae4f74c0a6b29ecc7866eb04fa67c`  
		Last Modified: Tue, 03 Oct 2023 07:58:05 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1327aabe97ed75c076e3bdabe30f643b4d542996cfbbdde687e0d210084248`  
		Last Modified: Tue, 03 Oct 2023 07:58:06 GMT  
		Size: 12.2 MB (12208788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717e7cc545e3ae3922feda2932bf27f8bd928372bba9bce508cbe160159b3e70`  
		Last Modified: Tue, 03 Oct 2023 07:58:05 GMT  
		Size: 458.3 KB (458318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac647be1c1013ac4b21cedb2a5c098c20b6d4cc75ed1ef8d40fa4bfd10f06bd`  
		Last Modified: Tue, 03 Oct 2023 07:58:04 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre17-temurin` - linux; ppc64le

```console
$ docker pull tomcat@sha256:228d4eb03b883a96b4e9f0806911f712d583c2e5b3b110d917e2b5881c0352ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114201699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a6a156b57ba8c0ba3955d10a840104601e1e798a6e9b2ca9c5300ac72e43f5`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 16 Aug 2023 06:03:07 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:03:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:03:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:03:08 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:03:11 GMT
ADD file:632018deeaeb9e42f0026fb331dfb08381e46bd414b2b470b18ea22ac0653bf6 in / 
# Wed, 16 Aug 2023 06:03:11 GMT
CMD ["/bin/bash"]
# Sat, 02 Sep 2023 00:03:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Sep 2023 00:03:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 00:03:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 02 Sep 2023 00:06:39 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 00:06:41 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Sat, 02 Sep 2023 00:07:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a1c5c9ee9d20832c87bd1e99a4c4a96947b59bb35c72683fe895d705f202737';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='8af898c5d356f0b2cee2db67ff9c8e7a8e738c0f6b3a61c383150b3168b9ea58';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4aadc18e58d20c37c69cf6ec2cc3299b76f5b21073fc8e6101e11268d7a33b5b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='5eff8141fd282b3473fd649e04c113ba044cf19f0c513b951b700c28a81c1d6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ab68857594792474a3049ede09ea1178e42df29803a6a41be771794f571b2d4e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 02 Sep 2023 00:07:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Sat, 02 Sep 2023 00:07:41 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 02 Sep 2023 00:07:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 02 Sep 2023 02:16:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 02 Sep 2023 02:16:45 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 02:16:47 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 02 Sep 2023 02:16:47 GMT
WORKDIR /usr/local/tomcat
# Sat, 02 Sep 2023 02:16:47 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 02 Sep 2023 02:16:48 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 02 Sep 2023 02:16:48 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Sat, 02 Sep 2023 02:16:48 GMT
ENV TOMCAT_MAJOR=10
# Sat, 02 Sep 2023 02:16:49 GMT
ENV TOMCAT_VERSION=10.1.13
# Sat, 02 Sep 2023 02:16:49 GMT
ENV TOMCAT_SHA512=406c0c367ac6ad95bb724ecc3a3c340ad7ded8c62287d657811eeec496eaaca1f5add52d2f46111da1426ae67090c543f6deccfeb5fdf4bdae32f9b39e773265
# Sat, 02 Sep 2023 02:16:50 GMT
COPY dir:beb30acd294a561bc14a99d94dd9d216c13a0e39f8471a9f6388e7b245c47626 in /usr/local/tomcat 
# Sat, 02 Sep 2023 02:17:00 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 02:17:05 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 02 Sep 2023 02:17:05 GMT
EXPOSE 8080
# Sat, 02 Sep 2023 02:17:06 GMT
ENTRYPOINT []
# Sat, 02 Sep 2023 02:17:08 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5d4cfc5435802883c4aaa9fa4afcc1b07f40e20bee68f058f0671804ab6bc3a0`  
		Last Modified: Sat, 02 Sep 2023 00:08:58 GMT  
		Size: 35.7 MB (35705651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cf6ea565778c3d8bea7e7e22e09a388b4e63b84893d5323563a7fb240485b0`  
		Last Modified: Sat, 02 Sep 2023 00:10:54 GMT  
		Size: 18.7 MB (18729609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3340461a79a4d9bffef028dea64af59cd1e93ccfb6a5baec05e5554f84b6abba`  
		Last Modified: Sat, 02 Sep 2023 00:11:40 GMT  
		Size: 47.1 MB (47054882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a02e00b3d8990b397d714688a4a656fbe67c93745fc43a6209a57a468a47fb9`  
		Last Modified: Sat, 02 Sep 2023 00:11:29 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e852b42b680d46d59d1c29633809e7da4869fa8886c262a39a20ac3215a5850b`  
		Last Modified: Sat, 02 Sep 2023 00:11:29 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e56abbfdffad4d7e17a4b208f6cac967f6f5ee60748860ba6d90cc15b1445b`  
		Last Modified: Sat, 02 Sep 2023 02:39:01 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a3ec023f47a4b781358acc7e52f08effbb97005d20f209713fa0ae6a7b53f9`  
		Last Modified: Sat, 02 Sep 2023 02:39:02 GMT  
		Size: 12.2 MB (12220778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f0385812203e54a54c7f0aefe9b9caac09a4d51c03a91b10c2e9a8e3126430`  
		Last Modified: Sat, 02 Sep 2023 02:39:01 GMT  
		Size: 489.6 KB (489582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c23441edf3f4164d29b44869884aa826e1e1a17e1becc61e9a5f562611c429c`  
		Last Modified: Sat, 02 Sep 2023 02:39:01 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:10-jre17-temurin` - linux; s390x

```console
$ docker pull tomcat@sha256:f0346a1a7d641b5dacbece017dda2e560b78ca8a208f0ad750c9efd69729781b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102432289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea1aa55cae7341e909d7642ac27bed21536b915d1d0d0dd3c50a8aeb84611ba`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 16 Aug 2023 06:05:03 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:05:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:05:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:05:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:05:05 GMT
ADD file:58eccd685d73ff80ea235016d6e33d093e1063800d869935b67b59a1b8891344 in / 
# Wed, 16 Aug 2023 06:05:05 GMT
CMD ["/bin/bash"]
# Fri, 01 Sep 2023 23:26:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Sep 2023 23:26:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Sep 2023 23:26:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Sep 2023 23:27:37 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Sep 2023 23:27:38 GMT
ENV JAVA_VERSION=jdk-17.0.8.1+1
# Fri, 01 Sep 2023 23:28:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0a1c5c9ee9d20832c87bd1e99a4c4a96947b59bb35c72683fe895d705f202737';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_aarch64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        armhf|arm)          ESUM='8af898c5d356f0b2cee2db67ff9c8e7a8e738c0f6b3a61c383150b3168b9ea58';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_arm_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='4aadc18e58d20c37c69cf6ec2cc3299b76f5b21073fc8e6101e11268d7a33b5b';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_ppc64le_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='5eff8141fd282b3473fd649e04c113ba044cf19f0c513b951b700c28a81c1d6a';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_s390x_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='ab68857594792474a3049ede09ea1178e42df29803a6a41be771794f571b2d4e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8.1%2B1/OpenJDK17U-jre_x64_linux_hotspot_17.0.8.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 01 Sep 2023 23:28:26 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Fri, 01 Sep 2023 23:28:26 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 01 Sep 2023 23:28:26 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 02 Sep 2023 00:28:29 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 02 Sep 2023 00:28:29 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 00:28:29 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 02 Sep 2023 00:28:30 GMT
WORKDIR /usr/local/tomcat
# Sat, 02 Sep 2023 00:28:30 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 02 Sep 2023 00:28:30 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 02 Sep 2023 00:28:30 GMT
ENV GPG_KEYS=5C3C5F3E314C866292F359A8F3AD5C94A67F707E A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Sat, 02 Sep 2023 00:28:30 GMT
ENV TOMCAT_MAJOR=10
# Sat, 02 Sep 2023 00:28:30 GMT
ENV TOMCAT_VERSION=10.1.13
# Sat, 02 Sep 2023 00:28:30 GMT
ENV TOMCAT_SHA512=406c0c367ac6ad95bb724ecc3a3c340ad7ded8c62287d657811eeec496eaaca1f5add52d2f46111da1426ae67090c543f6deccfeb5fdf4bdae32f9b39e773265
# Sat, 02 Sep 2023 00:28:31 GMT
COPY dir:bdb2e0b554034276631b35f0abe85f7408bf8c6da899ded9828f308c94dffbb9 in /usr/local/tomcat 
# Sat, 02 Sep 2023 00:28:36 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 00:28:37 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 02 Sep 2023 00:28:37 GMT
EXPOSE 8080
# Sat, 02 Sep 2023 00:28:38 GMT
ENTRYPOINT []
# Sat, 02 Sep 2023 00:28:38 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:e19a32372cc8a39496c7cbc80d6c7213997c1b24d50309e770a59738f35c719d`  
		Last Modified: Fri, 01 Sep 2023 23:23:30 GMT  
		Size: 28.6 MB (28645834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351bc6a2ce88dd5072fe74c40fe5a76147b4c44751fb62974f74bd1eaf40aafb`  
		Last Modified: Fri, 01 Sep 2023 23:29:38 GMT  
		Size: 17.3 MB (17255550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47038c1ad39d71dbbafe6c35f26aa34765647d8fbe02d71c73dc80ab22dbe0ed`  
		Last Modified: Fri, 01 Sep 2023 23:30:01 GMT  
		Size: 43.9 MB (43861255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc75b4cca7acde8cda5f7536df6c8a48695c8ae1905d60fe900f7be894296ca2`  
		Last Modified: Fri, 01 Sep 2023 23:29:55 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba2fb6df7c842dc604e4626020a401063dcf743892d8bbad2e31d74dae2a007`  
		Last Modified: Fri, 01 Sep 2023 23:29:55 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e191d963a094da6304a57a701f56643a2e2aaf7c157be1044514f1d45815b85d`  
		Last Modified: Sat, 02 Sep 2023 00:36:02 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b032815aa227791777335ef5c13a416065915e66cb3c11743cc8a0bffa3e2f`  
		Last Modified: Sat, 02 Sep 2023 00:36:02 GMT  
		Size: 12.2 MB (12208618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95f6efc8369a301f20bf18d1a94c87f7d0f0711a8808cfad0a7e6e50a985173`  
		Last Modified: Sat, 02 Sep 2023 00:36:02 GMT  
		Size: 459.8 KB (459836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37d2041ec1334184e8040c64c18171736a92dbeb50243bc6f509580443c223d2`  
		Last Modified: Sat, 02 Sep 2023 00:36:01 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

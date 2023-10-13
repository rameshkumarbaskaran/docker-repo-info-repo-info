## `tomcat:8-jre8-temurin-focal`

```console
$ docker pull tomcat@sha256:b3824f8e985d959a4dab8e3ac727a0ca809c4475a5de593262be3de6cdde3131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `tomcat:8-jre8-temurin-focal` - linux; amd64

```console
$ docker pull tomcat@sha256:b68a82de77239a68b52ac4872894eab43d1b55a7b72af45afba7dd8c981dd384
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99232056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2e01afee2a0a7da381fc7d430f66d0c1ab21cfecd87bacda4a879bc8ca2621`
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
# Tue, 08 Aug 2023 19:20:25 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 19:20:25 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 08 Aug 2023 19:21:28 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 08 Aug 2023 19:21:28 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Mon, 14 Aug 2023 18:09:37 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 14 Aug 2023 18:09:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 14 Aug 2023 21:57:00 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 14 Aug 2023 21:57:00 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Aug 2023 21:57:01 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 14 Aug 2023 21:57:01 GMT
WORKDIR /usr/local/tomcat
# Mon, 14 Aug 2023 21:57:01 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 14 Aug 2023 21:57:01 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 14 Aug 2023 22:02:16 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 14 Aug 2023 22:02:16 GMT
ENV TOMCAT_MAJOR=8
# Fri, 13 Oct 2023 00:37:54 GMT
ENV TOMCAT_VERSION=8.5.94
# Fri, 13 Oct 2023 00:37:54 GMT
ENV TOMCAT_SHA512=bee5399a0fef6dea774ac2b99ebf58b69c67079c0e870698be3c7786c88e9a120cb073223d0508621585e13f509f3fade9d276cfadeb0692e09feeb5f7bb2cc9
# Fri, 13 Oct 2023 00:37:54 GMT
COPY dir:e13606d056ac935ddf096a8db0e8598cdd94053256999cd303630d9f7da5c215 in /usr/local/tomcat 
# Fri, 13 Oct 2023 00:38:00 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 00:38:01 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 13 Oct 2023 00:38:01 GMT
EXPOSE 8080
# Fri, 13 Oct 2023 00:38:01 GMT
ENTRYPOINT []
# Fri, 13 Oct 2023 00:38:01 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f32e041863d53bbb7f9f65ba31f023a9f344dd4105bf5345c6e748e3cc3e71a`  
		Last Modified: Tue, 08 Aug 2023 19:26:48 GMT  
		Size: 16.9 MB (16919807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac9d7d98ff971a63c75b2c0c207e6a750b3b58da46582d2a1dbe02b9d4b93787`  
		Last Modified: Tue, 08 Aug 2023 19:28:06 GMT  
		Size: 41.9 MB (41853336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3c98a5c1ef59f71417c2f7aa3eb5faf44292f37cf038a91e990d7916405ec5`  
		Last Modified: Tue, 08 Aug 2023 19:28:01 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6774a689a1e2ff513a3b845fffa60a0c0e386274fc5413de0b25274f474a2c0b`  
		Last Modified: Mon, 14 Aug 2023 18:10:45 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ede39422df70fb2ba93a440255d430249cbf4e37b4961f7779423a176f13141`  
		Last Modified: Mon, 14 Aug 2023 22:11:01 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cc5a8674f9c57a28b482a094d87bcb8f0c11fbe70b2869ef4837393d8df0b1`  
		Last Modified: Fri, 13 Oct 2023 00:58:45 GMT  
		Size: 11.4 MB (11427490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb36ca0f5563e607208a9a06360f6fa38b8772db0a2e72a1e4f058468767ef58`  
		Last Modified: Fri, 13 Oct 2023 00:58:44 GMT  
		Size: 449.6 KB (449557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e8f1dcfb3a3a4b73e9c148fae4a2a818a9ff7402d1513925c6485a1f5abddd`  
		Last Modified: Fri, 13 Oct 2023 00:58:44 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-temurin-focal` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:b74d8ae3b8d11c213f807a275a47cc4f617256054e68216e6241f6d290893345
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91621125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0127012b137ff9c0c5e08f756ffba4b0570035d1974c60261ded94baf7f634`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:45 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:49 GMT
ADD file:60aa8465a6ba5538decc41365cc9b78ae86131e8c2cfc9177b4a336354ead988 in / 
# Tue, 01 Aug 2023 06:16:50 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 01:27:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Aug 2023 01:27:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Aug 2023 01:27:39 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 08 Aug 2023 18:57:54 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 18:57:54 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 08 Aug 2023 18:59:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 08 Aug 2023 18:59:34 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Mon, 14 Aug 2023 18:09:37 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 14 Aug 2023 18:09:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 14 Aug 2023 18:57:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 14 Aug 2023 18:57:24 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Aug 2023 18:57:25 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 14 Aug 2023 18:57:25 GMT
WORKDIR /usr/local/tomcat
# Mon, 14 Aug 2023 18:57:25 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 14 Aug 2023 18:57:25 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 14 Aug 2023 19:01:59 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 14 Aug 2023 19:01:59 GMT
ENV TOMCAT_MAJOR=8
# Fri, 13 Oct 2023 00:21:02 GMT
ENV TOMCAT_VERSION=8.5.94
# Fri, 13 Oct 2023 00:21:02 GMT
ENV TOMCAT_SHA512=bee5399a0fef6dea774ac2b99ebf58b69c67079c0e870698be3c7786c88e9a120cb073223d0508621585e13f509f3fade9d276cfadeb0692e09feeb5f7bb2cc9
# Fri, 13 Oct 2023 00:21:02 GMT
COPY dir:a78a60d55aead4e3c111d74a8268446c2abd317bea61f16fafd50e5524f898ba in /usr/local/tomcat 
# Fri, 13 Oct 2023 00:21:06 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 00:21:07 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 13 Oct 2023 00:21:07 GMT
EXPOSE 8080
# Fri, 13 Oct 2023 00:21:07 GMT
ENTRYPOINT []
# Fri, 13 Oct 2023 00:21:07 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:c429b4536d4b2ab209b0a779f71ba68570f10acf9dd806c7e2011fce49bd5c97`  
		Last Modified: Wed, 02 Aug 2023 04:28:29 GMT  
		Size: 24.6 MB (24591882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cd3a8f320fb2da0d9f7694604e369817023cd4b7b62173714bbff7cad25aae`  
		Last Modified: Tue, 08 Aug 2023 19:02:31 GMT  
		Size: 15.7 MB (15659457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc192fb182dee2d7612c050999c38e61957cb33e82008c05d27235a8e3fe56e6`  
		Last Modified: Tue, 08 Aug 2023 19:03:21 GMT  
		Size: 39.6 MB (39565281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12a390193aea1f01c652d775ef22ad164f7307f4759992bafc614418ac046f7d`  
		Last Modified: Tue, 08 Aug 2023 19:03:15 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6774a689a1e2ff513a3b845fffa60a0c0e386274fc5413de0b25274f474a2c0b`  
		Last Modified: Mon, 14 Aug 2023 18:10:45 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82051fc31dc8217061400b98b3fa7e989fedc26a823c5866c823aa910bc026f`  
		Last Modified: Mon, 14 Aug 2023 19:09:45 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e122414635c79de808760bc417d3a08ee30c4e962dfc0bc81f029303d9d87`  
		Last Modified: Fri, 13 Oct 2023 00:33:43 GMT  
		Size: 11.4 MB (11376108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ceb868f52405d6f8c2181c8e10cf908d725cea75d988f09dadbd9c6056d1103`  
		Last Modified: Fri, 13 Oct 2023 00:33:42 GMT  
		Size: 427.2 KB (427202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd197bd494f6502cf024d409244e595350adbeaa71fcaaabbd1acde49275042`  
		Last Modified: Fri, 13 Oct 2023 00:33:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-temurin-focal` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:e92c26073e2ae2cc3e3263b8abbb946d0ed6c5970b438453208e895a092dd1a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96714015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4b9b312e4975d538cef8bf2ca70ac4adeaed7286cd1850fd962ee7990570ed`
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
# Tue, 08 Aug 2023 19:40:01 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 19:40:01 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 08 Aug 2023 19:40:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 08 Aug 2023 19:40:58 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Mon, 14 Aug 2023 18:09:00 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 14 Aug 2023 18:09:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 14 Aug 2023 20:09:02 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 14 Aug 2023 20:09:02 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Aug 2023 20:09:02 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 14 Aug 2023 20:09:03 GMT
WORKDIR /usr/local/tomcat
# Mon, 14 Aug 2023 20:09:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 14 Aug 2023 20:09:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 14 Aug 2023 20:13:21 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 14 Aug 2023 20:13:21 GMT
ENV TOMCAT_MAJOR=8
# Fri, 13 Oct 2023 00:32:52 GMT
ENV TOMCAT_VERSION=8.5.94
# Fri, 13 Oct 2023 00:32:52 GMT
ENV TOMCAT_SHA512=bee5399a0fef6dea774ac2b99ebf58b69c67079c0e870698be3c7786c88e9a120cb073223d0508621585e13f509f3fade9d276cfadeb0692e09feeb5f7bb2cc9
# Fri, 13 Oct 2023 00:32:52 GMT
COPY dir:2a8ee49009a8178a1cfefe03ce0c25ae4559243031b31619ab67b3a32ec17d05 in /usr/local/tomcat 
# Fri, 13 Oct 2023 00:32:56 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 00:32:57 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 13 Oct 2023 00:32:57 GMT
EXPOSE 8080
# Fri, 13 Oct 2023 00:32:57 GMT
ENTRYPOINT []
# Fri, 13 Oct 2023 00:32:57 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:edab87ea811e56041127f5e9eb4115fb62cb96d0e6a14056e0d2dbf51a945a22`  
		Last Modified: Wed, 02 Aug 2023 04:28:23 GMT  
		Size: 27.2 MB (27200587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d3de389f9fd6a81c60e4d6444266df2002734ab5660161fa9bf374cd8cd473`  
		Last Modified: Tue, 08 Aug 2023 19:44:02 GMT  
		Size: 16.8 MB (16770361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a38e1a15eb64c0e5de312632034b95148af5db913c52cb13394b1d13bbead278`  
		Last Modified: Tue, 08 Aug 2023 19:45:02 GMT  
		Size: 40.8 MB (40845589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc205dbb8e87149f5c654cec84153fc45f773abfed792d89b50995a9a06ceee`  
		Last Modified: Tue, 08 Aug 2023 19:44:58 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb01df2a7da9ab9661df264c6a3bc150298c73e8d9550daf0b19f9ec85771e6`  
		Last Modified: Mon, 14 Aug 2023 18:11:27 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1e65b5462697390cc9704a0c4a8e8050340f6fd38b5acd50dbb3bd6868f78e`  
		Last Modified: Mon, 14 Aug 2023 20:21:45 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046ec3750abb77a9e380d7461357ec46a95e398448c14d9c38a543c952fec3c4`  
		Last Modified: Fri, 13 Oct 2023 00:53:38 GMT  
		Size: 11.4 MB (11445920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b29716f8b6059e76f2e9ba1aef9bb81dc96c32abc86c18a4f06d50b52a65b5`  
		Last Modified: Fri, 13 Oct 2023 00:53:38 GMT  
		Size: 450.4 KB (450361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23fbd1ed5ea8aa6bb2cca4dfff4527b69b2a39ac276bcdd47f7cbfe7782e8ee`  
		Last Modified: Fri, 13 Oct 2023 00:53:37 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:8-jre8-temurin-focal` - linux; ppc64le

```console
$ docker pull tomcat@sha256:823d898f2a8d3b3e14dd7e7f21c72faba2f04b282cacc8cfa545a36f9ba2b877
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104665334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c752782021f0e0ffaf40f9f0c919fc384fba3dbb83b3d843708b3e67f0bf23d`
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
# Tue, 08 Aug 2023 19:18:01 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 08 Aug 2023 19:18:03 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 08 Aug 2023 19:20:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 08 Aug 2023 19:20:20 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Mon, 14 Aug 2023 18:09:18 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 14 Aug 2023 18:09:18 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 14 Aug 2023 19:55:01 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 14 Aug 2023 19:55:01 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Aug 2023 19:55:02 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 14 Aug 2023 19:55:03 GMT
WORKDIR /usr/local/tomcat
# Mon, 14 Aug 2023 19:55:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 14 Aug 2023 19:55:04 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 14 Aug 2023 20:08:03 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 5C3C5F3E314C866292F359A8F3AD5C94A67F707E 765908099ACF92702C7D949BFA0C35EA8AA299F1 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 14 Aug 2023 20:08:04 GMT
ENV TOMCAT_MAJOR=8
# Sat, 26 Aug 2023 08:02:49 GMT
ENV TOMCAT_VERSION=8.5.93
# Sat, 26 Aug 2023 08:02:49 GMT
ENV TOMCAT_SHA512=fdd9bd768c2c8b7f57c75f1a4863bd2bde55e8ea7c8b9cb81427ea8be652540bdcb1ff1cd625b9fb0dd48eb750ebef0f0244d12ac574998d5df3a0d339699bcc
# Sat, 26 Aug 2023 08:02:51 GMT
COPY dir:1f8aaabc11abb2f6a1ec685c70eae6f86a2bbbd9478d238af6bd1d5979f07e3a in /usr/local/tomcat 
# Sat, 26 Aug 2023 08:03:03 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 26 Aug 2023 08:03:09 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 26 Aug 2023 08:03:09 GMT
EXPOSE 8080
# Sat, 26 Aug 2023 08:03:09 GMT
ENTRYPOINT []
# Sat, 26 Aug 2023 08:03:10 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:be0253994e7bea97e6b44cdeec04bf996c8dd3380e70409de3783a1d1971e747`  
		Last Modified: Thu, 03 Aug 2023 02:50:24 GMT  
		Size: 33.3 MB (33306772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af03d96af036322b1cf090be8f29d0a3931c623558764bccaca2826ee7b9af6b`  
		Last Modified: Tue, 08 Aug 2023 19:28:27 GMT  
		Size: 18.2 MB (18215568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bc55568138949e8ff568ebe6a09a0881a82c301f410a3f03c4f7d3fd02ddf1`  
		Last Modified: Tue, 08 Aug 2023 19:30:05 GMT  
		Size: 41.2 MB (41230356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b59f5af9e2ff64bfd6cfdd87cbb524bee65529f470532af63115a3e76eb57b6`  
		Last Modified: Tue, 08 Aug 2023 19:29:57 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929d1b01e9cf28804fb27e3db89a30729c714922bbeb49e6a5ff4e99a4b5c01c`  
		Last Modified: Mon, 14 Aug 2023 18:13:01 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64e6629e99bbc0cb2c1d222e38ca8db9b6e0106ba8c663cf9dbf372646beaf7`  
		Last Modified: Mon, 14 Aug 2023 20:20:19 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b09e6b091e92f47ff995c61fcd0e65cfe36479ce3b9c12d8c5c3102a03a026c`  
		Last Modified: Sat, 26 Aug 2023 08:20:03 GMT  
		Size: 11.4 MB (11436224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ac1a06aa08cefb26549f964457d981fb8ac6d604d9216f909c5082b2d87f78`  
		Last Modified: Sat, 26 Aug 2023 08:20:01 GMT  
		Size: 475.2 KB (475216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99770f89bc23ab07127efd24d310d17b5bfa74189d4c080a6c505f6d401c63bb`  
		Last Modified: Sat, 26 Aug 2023 08:20:01 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

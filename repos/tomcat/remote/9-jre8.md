## `tomcat:9-jre8`

```console
$ docker pull tomcat@sha256:5dc6a8f9d2333e2545424d5bb6edf6029c103b18fdaf5ccc2413a6ef714b154d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `tomcat:9-jre8` - linux; amd64

```console
$ docker pull tomcat@sha256:22dce7e93943f3e2f1ce88fcb38e71944676040a353daf5c60262d58957a9ce1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 MB (97934922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c0991c7e7a75ffa1cf6380bd25c0df178089156bd707c152d28bfd4ce4daa51`
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
# Sat, 02 Sep 2023 00:37:58 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 00:37:58 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Sat, 02 Sep 2023 00:38:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Sat, 02 Sep 2023 00:38:23 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 02 Sep 2023 00:38:23 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 02 Sep 2023 00:38:23 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 02 Sep 2023 03:45:51 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 02 Sep 2023 03:45:51 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 03:45:51 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 02 Sep 2023 03:45:51 GMT
WORKDIR /usr/local/tomcat
# Sat, 02 Sep 2023 03:45:51 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 02 Sep 2023 03:45:51 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 02 Sep 2023 03:45:51 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 02 Sep 2023 03:45:52 GMT
ENV TOMCAT_MAJOR=9
# Sat, 02 Sep 2023 03:45:52 GMT
ENV TOMCAT_VERSION=9.0.80
# Sat, 02 Sep 2023 03:45:52 GMT
ENV TOMCAT_SHA512=24014441b0ccdd2dda238efa56e1a039476488943e6cf04f8a372a340a49dd21ce174ed68e2f5fcc43401e85fae6d00c5eac3d357653e91601737b6fa94476de
# Sat, 02 Sep 2023 03:45:52 GMT
COPY dir:83ab8cc8617744119ffe703bbc536bbab89aca628b09138ead18f8863ffcc855 in /usr/local/tomcat 
# Sat, 02 Sep 2023 03:45:56 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 03:45:58 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 02 Sep 2023 03:45:58 GMT
EXPOSE 8080
# Sat, 02 Sep 2023 03:45:58 GMT
ENTRYPOINT []
# Sat, 02 Sep 2023 03:45:58 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:44ba2882f8eb14264e5f2f9f6ec55bcf5306527b637279f2cd9d4858762388af`  
		Last Modified: Wed, 16 Aug 2023 10:32:51 GMT  
		Size: 30.4 MB (30438977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274fb0278626020650ff7c358074255903c792176a61a1ebce3055ba27e11436`  
		Last Modified: Sat, 02 Sep 2023 00:41:34 GMT  
		Size: 12.9 MB (12902882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d793d7430eae5aea34cf447e2cde89ed850a797c3fe7aa2b240b9c943b4db82`  
		Last Modified: Sat, 02 Sep 2023 00:41:57 GMT  
		Size: 41.9 MB (41851986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04512f56d66ddc5d6b321254f552bba1e7647996b183185d76f6c65d6b33e4dc`  
		Last Modified: Sat, 02 Sep 2023 00:41:52 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea2ec836723a785fb655a875e3764a6a3305ccbb2bd2a668d482f19bd715e80`  
		Last Modified: Sat, 02 Sep 2023 00:41:52 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c8dd9a040c896e1d9dab33367bd7cffa62de9be69adec37531ca4af71d0a7a`  
		Last Modified: Sat, 02 Sep 2023 03:55:06 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d163a72e01eec60db9a91beeda6702076842948593d5aa4ad78201225aaf6bc`  
		Last Modified: Sat, 02 Sep 2023 03:55:07 GMT  
		Size: 12.3 MB (12284326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2d82152e91fefe1b86c895e924ca85dbe2275f3554c5c20721ec9826990168`  
		Last Modified: Sat, 02 Sep 2023 03:55:06 GMT  
		Size: 455.6 KB (455556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519e83e60b767b07dc8e8372359d1297e4ad5c6e4fe53e0feec9cbb8106f4146`  
		Last Modified: Sat, 02 Sep 2023 03:55:06 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:66e21566786770e5e8fb89ef02e357fac297a5d30a90903060d85cbfdb9b8412
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92218820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fba619f6c8f7cae3beac93f56bc69dfa92d04e44c9b5a8255bac26b5fdba2f1`
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
# Tue, 03 Oct 2023 06:01:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:01:30 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 03 Oct 2023 06:02:00 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 03 Oct 2023 06:02:00 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 03 Oct 2023 06:02:01 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 03 Oct 2023 06:02:01 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Oct 2023 06:58:31 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 03 Oct 2023 06:58:31 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 06:58:32 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 03 Oct 2023 06:58:32 GMT
WORKDIR /usr/local/tomcat
# Tue, 03 Oct 2023 06:58:32 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 03 Oct 2023 06:58:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 03 Oct 2023 06:58:32 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 03 Oct 2023 06:58:32 GMT
ENV TOMCAT_MAJOR=9
# Tue, 03 Oct 2023 06:58:32 GMT
ENV TOMCAT_VERSION=9.0.80
# Tue, 03 Oct 2023 06:58:32 GMT
ENV TOMCAT_SHA512=24014441b0ccdd2dda238efa56e1a039476488943e6cf04f8a372a340a49dd21ce174ed68e2f5fcc43401e85fae6d00c5eac3d357653e91601737b6fa94476de
# Tue, 03 Oct 2023 06:58:33 GMT
COPY dir:ecee6d04af0c43e9ce4a9e142204c745d2d35a4a9618b0de410783bd43335805 in /usr/local/tomcat 
# Tue, 03 Oct 2023 06:58:37 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:58:39 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 03 Oct 2023 06:58:39 GMT
EXPOSE 8080
# Tue, 03 Oct 2023 06:58:39 GMT
ENTRYPOINT []
# Tue, 03 Oct 2023 06:58:39 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:7271b2c80df6c73d794550b50f57d78c6fd5b85da7934c6506c76ea706087280`  
		Last Modified: Tue, 26 Sep 2023 02:07:56 GMT  
		Size: 27.5 MB (27515498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eda8dd86380daebf30969cb41ed0b268657958a7e1447d39fc3a2fc0d9c8c636`  
		Last Modified: Tue, 03 Oct 2023 06:03:57 GMT  
		Size: 12.5 MB (12491478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d197e8772d782c92e0a1d712b7312a5fe65b271de4e5b59fb168badacd7fdbbd`  
		Last Modified: Tue, 03 Oct 2023 06:04:21 GMT  
		Size: 39.6 MB (39564004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63429c1e46514ea3865b3cba08dd41b9a6c390010bd7b8bfb39b47069d03fe9`  
		Last Modified: Tue, 03 Oct 2023 06:04:16 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d2b305a60827dc19ee5b96b9de64b7b58fae882f5a3c27c0f00a1744268ed2`  
		Last Modified: Tue, 03 Oct 2023 06:04:16 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da64074704c0be4ae93f0a2695c56e5d2195163d0675263b481b0da144ffee03`  
		Last Modified: Tue, 03 Oct 2023 07:07:42 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09f5fa18e0c27a7ba3733e13b9b0a43753f64dbc6a18375b111d0c53b600ee7b`  
		Last Modified: Tue, 03 Oct 2023 07:07:43 GMT  
		Size: 12.2 MB (12216456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84968ffae37df205976e2e8f6a50fdf2010ae9e9ee4f66f24be890c7bb4bd8b`  
		Last Modified: Tue, 03 Oct 2023 07:07:42 GMT  
		Size: 430.2 KB (430187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afafd2c80ddaeec79362566500fb1e56936c1b64f5a6211971700acd822408f0`  
		Last Modified: Tue, 03 Oct 2023 07:07:42 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:b5962b46156e85002d4e9e0e1b14eae2325a74243a18e0b158b0cdde0fb0e324
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94828849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281bcb61309c2f78858a10931df3d035e4fb6ab278819dffd4298d8e87e101c5`
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
# Tue, 03 Oct 2023 06:07:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:07:11 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 03 Oct 2023 06:07:29 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Tue, 03 Oct 2023 06:07:30 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 03 Oct 2023 06:07:30 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 03 Oct 2023 06:07:30 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 03 Oct 2023 07:52:08 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 03 Oct 2023 07:52:09 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 07:52:09 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 03 Oct 2023 07:52:09 GMT
WORKDIR /usr/local/tomcat
# Tue, 03 Oct 2023 07:52:09 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 03 Oct 2023 07:52:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 03 Oct 2023 07:52:09 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Tue, 03 Oct 2023 07:52:09 GMT
ENV TOMCAT_MAJOR=9
# Tue, 03 Oct 2023 07:52:09 GMT
ENV TOMCAT_VERSION=9.0.80
# Tue, 03 Oct 2023 07:52:10 GMT
ENV TOMCAT_SHA512=24014441b0ccdd2dda238efa56e1a039476488943e6cf04f8a372a340a49dd21ce174ed68e2f5fcc43401e85fae6d00c5eac3d357653e91601737b6fa94476de
# Tue, 03 Oct 2023 07:52:10 GMT
COPY dir:264fcd46979a384300bed06ad2955a3b3fd2580906362405ed3d91eec03473e8 in /usr/local/tomcat 
# Tue, 03 Oct 2023 07:52:13 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 07:52:15 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Tue, 03 Oct 2023 07:52:15 GMT
EXPOSE 8080
# Tue, 03 Oct 2023 07:52:15 GMT
ENTRYPOINT []
# Tue, 03 Oct 2023 07:52:15 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:6ea603f1df5e3d23206761eca19fba4cdf4e22d773256cb65b71b730aa5acced`  
		Last Modified: Mon, 25 Sep 2023 17:30:11 GMT  
		Size: 28.4 MB (28392073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db904450c39fc4ef39317a37a19b15df4a74bf6bb91100343e382470ce034d79`  
		Last Modified: Tue, 03 Oct 2023 06:10:10 GMT  
		Size: 12.8 MB (12843603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a826ff1e45b089d907ba5edc8d634a8e4d5c2b7a1f3208b26b1e1b67231618`  
		Last Modified: Tue, 03 Oct 2023 06:10:36 GMT  
		Size: 40.8 MB (40845874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5de800e72995f8a424db97e9a0becc80e074d963e4bd88516341b8c00b9ffc3`  
		Last Modified: Tue, 03 Oct 2023 06:10:32 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb94950a9d79fb0e1bb9e51c194211110274f6529c48318a8676a7bdb7da1ce8`  
		Last Modified: Tue, 03 Oct 2023 06:10:32 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b9969ca47471d36d2311ba37b5d39d706a1d2f8febf372e1b29c4045ea2b38`  
		Last Modified: Tue, 03 Oct 2023 08:02:24 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057bae78a91cfee096a89b6a037b2612335b94547d5854e405f04bbefcf8079c`  
		Last Modified: Tue, 03 Oct 2023 08:02:25 GMT  
		Size: 12.3 MB (12290193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90be0610afe0c5ead9e06717f5ce443f69b817a38964827f3eb06b5a881be5b`  
		Last Modified: Tue, 03 Oct 2023 08:02:24 GMT  
		Size: 455.9 KB (455912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b54a77720d5dc91ccc87f2214da7548ac8e106581eae3e5f673eb4a2810655`  
		Last Modified: Tue, 03 Oct 2023 08:02:24 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8` - linux; ppc64le

```console
$ docker pull tomcat@sha256:2ff8f0b58d5e3c726eb608c2dd05c7749bb1e80bf1c9bc4fff922447d10323bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103505772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f503e93e5ad4ab85dbc852f7e4ff9346cebd81b391cfe2f9cdeb3d1bb5c8cad5`
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
# Sat, 02 Sep 2023 00:04:06 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 00:04:09 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Sat, 02 Sep 2023 00:04:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='8cf329aa76d5b6abe35dd94e5087d9d14993fa13b43bbaed3b26bda4c57162c4';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_aarch64_linux_hotspot_8u382b05.tar.gz';          ;;        armhf|arm)          ESUM='b92fb3972372b5d1f9fb51815def903105722b747f680b7ecf2ba2ba863ab156';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_arm_linux_hotspot_8u382b05.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='8f0706f16373078e46666a6035325792584cd565b4cc5a793a37312599f3af0b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_ppc64le_linux_hotspot_8u382b05.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1fad165cc243e8db1b9cf226134acdfe3dc5919cd98c5fd9210de3cf9edeabd7';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Sat, 02 Sep 2023 00:04:56 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 02 Sep 2023 00:04:56 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 02 Sep 2023 00:04:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 02 Sep 2023 02:27:52 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 02 Sep 2023 02:27:53 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 02:27:55 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 02 Sep 2023 02:27:56 GMT
WORKDIR /usr/local/tomcat
# Sat, 02 Sep 2023 02:27:57 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 02 Sep 2023 02:27:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 02 Sep 2023 02:27:58 GMT
ENV GPG_KEYS=48F8E69F6390C9F25CFEDCD268248959359E722B A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243
# Sat, 02 Sep 2023 02:27:59 GMT
ENV TOMCAT_MAJOR=9
# Sat, 02 Sep 2023 02:28:00 GMT
ENV TOMCAT_VERSION=9.0.80
# Sat, 02 Sep 2023 02:28:00 GMT
ENV TOMCAT_SHA512=24014441b0ccdd2dda238efa56e1a039476488943e6cf04f8a372a340a49dd21ce174ed68e2f5fcc43401e85fae6d00c5eac3d357653e91601737b6fa94476de
# Sat, 02 Sep 2023 02:28:01 GMT
COPY dir:62c9da7334b1cb1c87928de6ec1d0dc4135efe061bf2a75745a8109c7b6a6935 in /usr/local/tomcat 
# Sat, 02 Sep 2023 02:28:12 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 02:28:16 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 02 Sep 2023 02:28:17 GMT
EXPOSE 8080
# Sat, 02 Sep 2023 02:28:18 GMT
ENTRYPOINT []
# Sat, 02 Sep 2023 02:28:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5d4cfc5435802883c4aaa9fa4afcc1b07f40e20bee68f058f0671804ab6bc3a0`  
		Last Modified: Sat, 02 Sep 2023 00:08:58 GMT  
		Size: 35.7 MB (35705651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20bbdfadf6550699bed2516a6d795d42d07af539ddc96ec121092535bbfefc27`  
		Last Modified: Sat, 02 Sep 2023 00:08:53 GMT  
		Size: 13.8 MB (13770760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3491922dce00e53ac88b583ce3866784ce392a08a727537d39870b50c218f6`  
		Last Modified: Sat, 02 Sep 2023 00:09:29 GMT  
		Size: 41.2 MB (41229765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3669fc21d38df525e6651cd26caef781b51fa5525f87a0a5ef8ab284ab77c74d`  
		Last Modified: Sat, 02 Sep 2023 00:09:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd9043fd3b0b128332eaf928081b591521951c156fe8a7a1a15f62c3cb993f91`  
		Last Modified: Sat, 02 Sep 2023 00:09:21 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47fa518f85d6c17b97ce242c110754db75f7181c0b3ef0cd5befa876fa16af2c`  
		Last Modified: Sat, 02 Sep 2023 02:44:38 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd0733a13146b6297f3a867839b9e55273277a260ea95ff7c331a4cfca3efcf`  
		Last Modified: Sat, 02 Sep 2023 02:44:40 GMT  
		Size: 12.3 MB (12311445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bca88b9ceb358f58ec90762af1d8e0978167e65a0fec6a4036da1bad801a38`  
		Last Modified: Sat, 02 Sep 2023 02:44:39 GMT  
		Size: 487.0 KB (486955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644011797e4d4913bf25b2141bb9668f70abfbe616085abaa208616a42962965`  
		Last Modified: Sat, 02 Sep 2023 02:44:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

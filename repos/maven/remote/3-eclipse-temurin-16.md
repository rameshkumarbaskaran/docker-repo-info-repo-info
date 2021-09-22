## `maven:3-eclipse-temurin-16`

```console
$ docker pull maven@sha256:5789ba3ae8366cc0b6266ef417306fa1006d9c26a8e0b4d277c4b9bbe868f1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `maven:3-eclipse-temurin-16` - linux; amd64

```console
$ docker pull maven@sha256:3469da451fd8c529c1f487b28b4d924c7057f203d176f2292a2784d2fe127766
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.4 MB (295388402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baaba159dc4960bc797908c017009bf5e30f248d56171e5b6d044c9ea33c5164`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:55 GMT
ADD file:d2abf27fe2e8b0b5f4da68c018560c73e11c53098329246e3e6fe176698ef941 in / 
# Tue, 31 Aug 2021 01:20:56 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:26:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Aug 2021 03:32:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:32:07 GMT
ENV JAVA_VERSION=jdk-16.0.2+7
# Wed, 22 Sep 2021 19:57:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cb77d9d126f97898dfdc8b5fb694d1e0e5d93d13a0a6cb2aeda76f8635384340';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_aarch64_linux_hotspot_16.0.2_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='36ebe6c72f2fc19b8b17371f731390e15fa3aab08c28b55b9a8b71d0a578adc9';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_ppc64le_linux_hotspot_16.0.2_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='fa3ab64ae26727196323105714ac50589ed2782a4c92a29730f7aa886c15807e';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_s390x_linux_hotspot_16.0.2_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='323d6d7474a359a28eff7ddd0df8e65bd61554a8ed12ef42fd9365349e573c2c';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_x64_linux_hotspot_16.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 22 Sep 2021 19:57:01 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Sep 2021 19:57:02 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 22 Sep 2021 19:57:03 GMT
CMD ["jshell"]
# Wed, 22 Sep 2021 20:53:10 GMT
ARG MAVEN_VERSION=3.8.2
# Wed, 22 Sep 2021 20:53:10 GMT
ARG USER_HOME_DIR=/root
# Wed, 22 Sep 2021 20:53:10 GMT
ARG SHA=b0bf39460348b2d8eae1c861ced6c3e8a077b6e761fb3d4669be5de09490521a74db294cf031b0775b2dfcd57bd82246e42ce10904063ef8e3806222e686f222
# Wed, 22 Sep 2021 20:53:11 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.2/binaries
# Wed, 22 Sep 2021 20:53:30 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.2/binaries MAVEN_VERSION=3.8.2 SHA=b0bf39460348b2d8eae1c861ced6c3e8a077b6e761fb3d4669be5de09490521a74db294cf031b0775b2dfcd57bd82246e42ce10904063ef8e3806222e686f222 USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 22 Sep 2021 20:53:37 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.2/binaries MAVEN_VERSION=3.8.2 SHA=b0bf39460348b2d8eae1c861ced6c3e8a077b6e761fb3d4669be5de09490521a74db294cf031b0775b2dfcd57bd82246e42ce10904063ef8e3806222e686f222 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 22 Sep 2021 20:53:37 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 22 Sep 2021 20:53:37 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 22 Sep 2021 20:53:37 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 22 Sep 2021 20:53:37 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 22 Sep 2021 20:53:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 22 Sep 2021 20:53:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:35807b77a593c1147d13dc926a91dcc3015616ff7307cc30442c5a8e07546283`  
		Last Modified: Sat, 28 Aug 2021 03:03:19 GMT  
		Size: 28.6 MB (28570074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501c2591907676ca691db1c93900af330416fe68009c9ceabb59897a6a5d30c7`  
		Last Modified: Tue, 31 Aug 2021 03:34:11 GMT  
		Size: 19.8 MB (19775466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42dd77081f563729a2d37bc70caf578b937df89c6507dfbb57a8a1f0416c656`  
		Last Modified: Wed, 22 Sep 2021 20:00:32 GMT  
		Size: 206.5 MB (206462458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3eefb36d9ce74db42bd79691d3d3b9e9e77f934278ff0db84c6e3b6a13e6196`  
		Last Modified: Wed, 22 Sep 2021 20:00:17 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f943d4cd3b22b465f83f885f5fe6d225f44caac40136d0548dc5a4859b096cac`  
		Last Modified: Wed, 22 Sep 2021 20:56:41 GMT  
		Size: 31.2 MB (31173569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b9fee5a1ef72b36f5c71762e9692d85722c644606e864a5f8ed1d597d7cc9f`  
		Last Modified: Wed, 22 Sep 2021 20:56:37 GMT  
		Size: 9.4 MB (9405460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3276a3963a46e6575c6f74e70ea2b929c57ba13acd7b9b2156851423a0d0e858`  
		Last Modified: Wed, 22 Sep 2021 20:56:35 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce6ad92c996f3c1c815c96aa9443eb3cfd0909d74528901b4af14596322fc24`  
		Last Modified: Wed, 22 Sep 2021 20:56:35 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-16` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d84fc9744169cb5772fad7149883cc37088751d45b1e532d8b6f8385983b2014
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.4 MB (292406071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a23a0c451825c732b958fce072fcf44b315c83123c1e9399cb935331ddfc0f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:44 GMT
ADD file:cec21619ecbd37b4cf8da15153b8957a343cd25c6f714e3ac3969b6003704a58 in / 
# Tue, 31 Aug 2021 01:40:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 01:59:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Aug 2021 02:26:35 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:26:35 GMT
ENV JAVA_VERSION=jdk-16.0.2+7
# Wed, 22 Sep 2021 19:41:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cb77d9d126f97898dfdc8b5fb694d1e0e5d93d13a0a6cb2aeda76f8635384340';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_aarch64_linux_hotspot_16.0.2_7.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='36ebe6c72f2fc19b8b17371f731390e15fa3aab08c28b55b9a8b71d0a578adc9';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_ppc64le_linux_hotspot_16.0.2_7.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='fa3ab64ae26727196323105714ac50589ed2782a4c92a29730f7aa886c15807e';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_s390x_linux_hotspot_16.0.2_7.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='323d6d7474a359a28eff7ddd0df8e65bd61554a8ed12ef42fd9365349e573c2c';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_x64_linux_hotspot_16.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 22 Sep 2021 19:41:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Sep 2021 19:41:16 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 22 Sep 2021 19:41:16 GMT
CMD ["jshell"]
# Wed, 22 Sep 2021 21:00:16 GMT
ARG MAVEN_VERSION=3.8.2
# Wed, 22 Sep 2021 21:00:16 GMT
ARG USER_HOME_DIR=/root
# Wed, 22 Sep 2021 21:00:16 GMT
ARG SHA=b0bf39460348b2d8eae1c861ced6c3e8a077b6e761fb3d4669be5de09490521a74db294cf031b0775b2dfcd57bd82246e42ce10904063ef8e3806222e686f222
# Wed, 22 Sep 2021 21:00:16 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.2/binaries
# Wed, 22 Sep 2021 21:00:26 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.2/binaries MAVEN_VERSION=3.8.2 SHA=b0bf39460348b2d8eae1c861ced6c3e8a077b6e761fb3d4669be5de09490521a74db294cf031b0775b2dfcd57bd82246e42ce10904063ef8e3806222e686f222 USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Wed, 22 Sep 2021 21:00:28 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.2/binaries MAVEN_VERSION=3.8.2 SHA=b0bf39460348b2d8eae1c861ced6c3e8a077b6e761fb3d4669be5de09490521a74db294cf031b0775b2dfcd57bd82246e42ce10904063ef8e3806222e686f222 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 22 Sep 2021 21:00:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 22 Sep 2021 21:00:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 22 Sep 2021 21:00:29 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 22 Sep 2021 21:00:29 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 22 Sep 2021 21:00:29 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 22 Sep 2021 21:00:29 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ab2d02b1ec420fdb84c9f52abda403b6aef20f5de904a2ecda5ae4f5cd6e4d46`  
		Last Modified: Tue, 31 Aug 2021 01:42:34 GMT  
		Size: 27.2 MB (27173099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5934ee80201d19949e41e2951c6f612c948b78bd574891b2dd3fa9911cacf52`  
		Last Modified: Tue, 31 Aug 2021 02:29:31 GMT  
		Size: 20.5 MB (20499296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952f36f91924a505445dff021327658bab98b96e30ae2082134827fe6546968b`  
		Last Modified: Wed, 22 Sep 2021 19:45:29 GMT  
		Size: 204.1 MB (204124082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b382032eb98eb47c20a0818d04b7d6ae642768ddc5e98e3734b4788a2078125`  
		Last Modified: Wed, 22 Sep 2021 19:45:13 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9ab22d5b287a7fc3d59b27f7e6180d2b98e55a7fa0546e9d68869bf55118fe`  
		Last Modified: Wed, 22 Sep 2021 21:05:12 GMT  
		Size: 31.2 MB (31202755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d71bb58640b39ae4e85e3742f37646f2ff7cc42f858fee2e39e6f39705db65`  
		Last Modified: Wed, 22 Sep 2021 21:05:08 GMT  
		Size: 9.4 MB (9405468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e6a2b7c44cb5554669ce2bb89671c7cff77e0502997035768ed15d6f3e87d5`  
		Last Modified: Wed, 22 Sep 2021 21:05:07 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0510b4692178ba0fe81160e7052d8850636e0f54ed2a8bd07b3caf3674d249ff`  
		Last Modified: Wed, 22 Sep 2021 21:05:07 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-eclipse-temurin-16` - linux; ppc64le

```console
$ docker pull maven@sha256:907815abfc46538609053f504e7f7bd9bef9f8099988244509d51c3cff837bc3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289703380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d106c2dcc5b9355442ccdb872d65c457b94c2293f2387b91c8cb3d9d372dbfee`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 31 Aug 2021 02:10:40 GMT
ADD file:7e5ee5560faaa801aa10a76122190026f8c1da00c809f4fb6ff441751ba0c90f in / 
# Tue, 31 Aug 2021 02:10:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:31:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Aug 2021 05:48:51 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 05:48:56 GMT
ENV JAVA_VERSION=jdk-16.0.2+7
# Tue, 31 Aug 2021 05:49:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='cb77d9d126f97898dfdc8b5fb694d1e0e5d93d13a0a6cb2aeda76f8635384340';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_aarch64_linux_hotspot_16.0.2_7.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='36ebe6c72f2fc19b8b17371f731390e15fa3aab08c28b55b9a8b71d0a578adc9';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_ppc64le_linux_hotspot_16.0.2_7.tar.gz';          ;;        s390x)          ESUM='fa3ab64ae26727196323105714ac50589ed2782a4c92a29730f7aa886c15807e';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_s390x_linux_hotspot_16.0.2_7.tar.gz';          ;;        amd64|x86_64)          ESUM='323d6d7474a359a28eff7ddd0df8e65bd61554a8ed12ef42fd9365349e573c2c';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_x64_linux_hotspot_16.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 31 Aug 2021 05:49:25 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Sep 2021 20:47:59 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 13 Sep 2021 20:48:08 GMT
CMD ["jshell"]
# Mon, 13 Sep 2021 21:21:07 GMT
ARG MAVEN_VERSION=3.8.2
# Mon, 13 Sep 2021 21:21:14 GMT
ARG USER_HOME_DIR=/root
# Mon, 13 Sep 2021 21:21:21 GMT
ARG SHA=b0bf39460348b2d8eae1c861ced6c3e8a077b6e761fb3d4669be5de09490521a74db294cf031b0775b2dfcd57bd82246e42ce10904063ef8e3806222e686f222
# Mon, 13 Sep 2021 21:21:26 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.2/binaries
# Mon, 13 Sep 2021 21:23:32 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.2/binaries MAVEN_VERSION=3.8.2 SHA=b0bf39460348b2d8eae1c861ced6c3e8a077b6e761fb3d4669be5de09490521a74db294cf031b0775b2dfcd57bd82246e42ce10904063ef8e3806222e686f222 USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Mon, 13 Sep 2021 21:24:09 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.2/binaries MAVEN_VERSION=3.8.2 SHA=b0bf39460348b2d8eae1c861ced6c3e8a077b6e761fb3d4669be5de09490521a74db294cf031b0775b2dfcd57bd82246e42ce10904063ef8e3806222e686f222 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 13 Sep 2021 21:24:19 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 13 Sep 2021 21:24:47 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 13 Sep 2021 21:24:58 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 13 Sep 2021 21:25:03 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 13 Sep 2021 21:25:09 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 13 Sep 2021 21:25:22 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:59390c695558464c51dc1fced64934b549770630192a1639ac6a90f59bd63b13`  
		Last Modified: Tue, 31 Aug 2021 02:14:21 GMT  
		Size: 33.3 MB (33291791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfd0e54245d66dbe1860c5910ae98258ddf167d4a91ce996844c4ce3e7ef29a`  
		Last Modified: Tue, 31 Aug 2021 05:52:29 GMT  
		Size: 21.7 MB (21685958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed25aafe5f625bbcb3c783e1a0afd2bd91b2a00c70e694bbfecebbe12f367f9`  
		Last Modified: Tue, 31 Aug 2021 05:52:46 GMT  
		Size: 186.9 MB (186948249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68bda3185c65859e5b1e5c02f33c7b9d90bc255eb24f16e6f0c79a28bc65270`  
		Last Modified: Mon, 13 Sep 2021 20:57:19 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f251bd9715fd61566727005d09ded6fda2f0f92825f8134c89f53515ffd922c9`  
		Last Modified: Mon, 13 Sep 2021 21:31:39 GMT  
		Size: 38.4 MB (38370562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2b0b04df1390286d06ab9e9a63ed2c72a0256b2be79c5ba0306c8640885597`  
		Last Modified: Mon, 13 Sep 2021 21:31:32 GMT  
		Size: 9.4 MB (9405443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0bfcd207583aa06762b14a76fea63bf4f93766cd994d0597e62af2be1ffba1`  
		Last Modified: Mon, 13 Sep 2021 21:31:31 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f410d7d0b4c8e24f6d495e5af05802a5f6d5f139dc9b973c7911705ecdb5d5e6`  
		Last Modified: Mon, 13 Sep 2021 21:31:31 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

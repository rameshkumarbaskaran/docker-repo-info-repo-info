## `tomee:jre8-plus`

```console
$ docker pull tomee@sha256:83dc91d428718d7ef132eedb3d347d572a9e2a8965cc4515012f1173beef3b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `tomee:jre8-plus` - linux; amd64

```console
$ docker pull tomee@sha256:a74232284bf696451feec6672536306df2b75dca6092ea4a2f37ebde558a6705
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160905518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0272dfdfeeb49eecd9aed51a86d0cb98714529462cdce81df4fb70817603c001`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 28 Nov 2023 05:17:39 GMT
ARG RELEASE
# Tue, 28 Nov 2023 05:17:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 28 Nov 2023 05:17:39 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 28 Nov 2023 05:17:41 GMT
ADD file:9169bb1d6ef21313aed17e924538fee03d858460ae6b05e01968457dfc043bd7 in / 
# Tue, 28 Nov 2023 05:17:41 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 01:57:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 01:57:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 01:57:27 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 02 Dec 2023 01:57:57 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 01:57:57 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Sat, 02 Dec 2023 01:58:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='37b997f12cd572da979283fccafec9ba903041a209605b50fcb46cc34f1a9917';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u392b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='91d31027da0d985be3549714389593d9e0da3da5057d87e3831c7c538b9a2a0f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_x64_linux_hotspot_8u392b08.tar.gz';          ;;        armhf|arm)          ESUM='877953bfabcdbcd000c11364d806456ca579a921085de2ca942280ebe168cac2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_arm_linux_hotspot_8u392b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='0ecb0aeb54fb9d3c9e1a7ea411490127e8e298d93219fafc4dd6051a5b74671f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u392b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Sat, 02 Dec 2023 01:58:53 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete."
# Sat, 02 Dec 2023 01:58:54 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 02 Dec 2023 01:58:54 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 02 Dec 2023 10:39:39 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 10:39:40 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg
# Sat, 02 Dec 2023 10:39:40 GMT
WORKDIR /usr/local/tomee
# Sat, 02 Dec 2023 10:39:46 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent   && rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 10:40:01 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 02 Dec 2023 10:40:01 GMT
ENV TOMEE_VER=8.0.16
# Sat, 02 Dec 2023 10:40:36 GMT
ENV TOMEE_BUILD=plus
# Sat, 02 Dec 2023 10:40:43 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz*
# Sat, 02 Dec 2023 10:40:44 GMT
EXPOSE 8080
# Sat, 02 Dec 2023 10:40:44 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:30ecab32a3b65c6ec04c63a65b90e627b49d1297d8793896ed50b656377d8a06`  
		Last Modified: Tue, 28 Nov 2023 10:11:56 GMT  
		Size: 28.6 MB (28584029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b3ed95e21625a2f60f42187379932a7ccaed17dc9647e941ced64e1124b3342`  
		Last Modified: Sat, 02 Dec 2023 02:03:26 GMT  
		Size: 16.9 MB (16920158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4241c3cdc52ee7f775d335ffcb8d963485f199febc690674ba3ccaa77d3e2a5`  
		Last Modified: Sat, 02 Dec 2023 02:04:08 GMT  
		Size: 41.9 MB (41859127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a10156a9e03d1fca1fcd43e32a20a1d167252ae7541aecd574b434bb290d3a60`  
		Last Modified: Sat, 02 Dec 2023 02:04:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c346f95791868709d38488a14ea95739281acbd48a11a99b59fdb605e0dc7b7a`  
		Last Modified: Sat, 02 Dec 2023 02:04:03 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a56d361c4ecf9f4f1e7393a2bf0780747f92345141d0c6f4411b0147ed4c04`  
		Last Modified: Sat, 02 Dec 2023 11:02:14 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e652a8ec4902cf83469726978cc9543a96f546c6050eeefdb836e16d17cd0061`  
		Last Modified: Sat, 02 Dec 2023 11:02:15 GMT  
		Size: 2.2 MB (2196347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7314a3ac16a3253a98f16b689a630ab4db3a920ed41381bcfd6c3d32b58d211e`  
		Last Modified: Sat, 02 Dec 2023 11:02:14 GMT  
		Size: 69.3 KB (69313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f3ff26f241c6488918a0c472bd470ef222a9c373dc83b7c706f164ad56aaa8`  
		Last Modified: Sat, 02 Dec 2023 11:04:48 GMT  
		Size: 71.3 MB (71275431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomee:jre8-plus` - linux; arm64 variant v8

```console
$ docker pull tomee@sha256:24cff50d23c08381d456a81369109328a37a9a893d65266755bb48c4b26bde1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.4 MB (158352564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e034ef6210c210a10d255d2a280e1e1f0eeed4d021e39917a26c8d19574b18`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Wed, 13 Dec 2023 10:29:33 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:29:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:29:34 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:29:41 GMT
ADD file:9ec8b7bbb2fbc8c90f1f24e19ab22130e03be1cc4727459e1265d2ed652377a1 in / 
# Wed, 13 Dec 2023 10:29:42 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 10:01:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 10:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 10:02:00 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 10:02:15 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 10:02:15 GMT
ENV JAVA_VERSION=jdk8u392-b08
# Sat, 16 Dec 2023 10:02:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='37b997f12cd572da979283fccafec9ba903041a209605b50fcb46cc34f1a9917';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_aarch64_linux_hotspot_8u392b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='91d31027da0d985be3549714389593d9e0da3da5057d87e3831c7c538b9a2a0f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_x64_linux_hotspot_8u392b08.tar.gz';          ;;        armhf|arm)          ESUM='877953bfabcdbcd000c11364d806456ca579a921085de2ca942280ebe168cac2';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_arm_linux_hotspot_8u392b08.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el|powerpc:common64)          ESUM='0ecb0aeb54fb9d3c9e1a7ea411490127e8e298d93219fafc4dd6051a5b74671f';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u392-b08/OpenJDK8U-jre_ppc64le_linux_hotspot_8u392b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;
# Sat, 16 Dec 2023 10:02:57 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java -version"; java -version;     echo "Complete."
# Sat, 16 Dec 2023 10:02:57 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 16 Dec 2023 10:02:57 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 16 Dec 2023 14:14:03 GMT
ENV PATH=/usr/local/tomee/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 14:14:03 GMT
RUN mkdir -p /usr/local/tomee ~/.gnupg
# Sat, 16 Dec 2023 14:14:03 GMT
WORKDIR /usr/local/tomee
# Sat, 16 Dec 2023 14:14:07 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends gpg dirmngr gpg-agent   && rm -rf /var/lib/apt/lists/*
# Sat, 16 Dec 2023 14:14:17 GMT
RUN set -xe;   for key in   9056B710F1E332780DE7AF34CBAEBE39A46C4CA1   F067B8140F5DD80E1D3B5D92318242FE9A0B1183   223D3A74B068ECA354DC385CE126833F9CF64915   DBCCD103B8B24F86FFAAB025C8BB472CD297D428   7A2744A8A9AAF063C23EB7868EBE7DBE8D050EEF   B8B301E6105DF628076BD92C5483E55897ABD9B9   FAA603D58B1BA4EDF65896D0ED340E0E6D545F97   A57DAF81C1B69921F4BA8723A8DE0A4DB863A7C1   82D8419BA697F0E7FB85916EE91287822FDB81B1   B7574789F5018690043E6DD9C212662E12F3E1DD   C23A3F6F595EBD0F960270CC997C8F1A5BE6E4C1   678F2D98F1FD9643811639FB622B8F2D043F71D8   BDD0BBEB753192957EFC5F896A62FC8EF17D8FEF   D11DF12CC2CA4894BDE638B967C1227A2678363C   C92604B0DEC5C62CFF5801E73D4683C24EDC64D1   626C542EDA7C113814B77AF09C04914D63645D20   3948829384B269D333CC5B98358807C52B4B0E23   B83D15E72253ED1104EB4FBBDAB472F0E5B8A431   871638A21A7F2C38066471420306A354336B4F0D   ; do     gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done
# Sat, 16 Dec 2023 14:14:17 GMT
ENV TOMEE_VER=8.0.16
# Sat, 16 Dec 2023 14:14:47 GMT
ENV TOMEE_BUILD=plus
# Sat, 16 Dec 2023 14:14:54 GMT
RUN set -x   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.asc -o tomee.tar.gz.asc   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz.sha512 -o tomee.tar.gz.sha512   && curl -fSL https://dist.apache.org/repos/dist/release/tomee/tomee-${TOMEE_VER}/apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz -o apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && gpg --batch --verify tomee.tar.gz.asc apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && echo `cat tomee.tar.gz.sha512` | sha512sum -c -   && tar -zxf apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && mv apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}/* /usr/local/tomee   && rm apache-tomee-${TOMEE_VER}-${TOMEE_BUILD}.tar.gz   && rm -Rf apache-tomee-${TOMEE_BUILD}-${TOMEE_VER}   && rm bin/*.bat   && rm bin/*.exe   && rm bin/*.tar.gz*   && rm tomee.tar.gz.asc   && rm tomee.tar.gz*
# Sat, 16 Dec 2023 14:14:54 GMT
EXPOSE 8080
# Sat, 16 Dec 2023 14:14:54 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:a5319f8e5f3f0f8f6e663c807041d5294b7c309e06b86d115409bbdb4c9d7165`  
		Last Modified: Thu, 14 Dec 2023 13:03:55 GMT  
		Size: 27.2 MB (27203144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b69f35fd155c9c0a485e63ad002a7b98a6ce1921e230d386f1cffd2c8c16878`  
		Last Modified: Sat, 16 Dec 2023 10:06:15 GMT  
		Size: 16.8 MB (16769031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972efbb5355605bd1c767d5dcde6521e9f4a65d5fc131991fc3fc2765f5b296c`  
		Last Modified: Sat, 16 Dec 2023 10:06:53 GMT  
		Size: 40.8 MB (40843989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65564342016555a11d4fe73450771971acc24e7f4cead917494041cea128a870`  
		Last Modified: Sat, 16 Dec 2023 10:06:49 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293ddc00a8b82e80cd076cb453963214d1bcf167354d57d4cb26fc4a0f64335a`  
		Last Modified: Sat, 16 Dec 2023 10:06:49 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c56a9da0b17908baf483e15b944751484a4c0c400edc6b6290ef94cdc0a5699c`  
		Last Modified: Sat, 16 Dec 2023 14:33:14 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:515f88205274d2cbad31a6b9b89a3497588956e3ec359dd56785c8f9e01c2049`  
		Last Modified: Sat, 16 Dec 2023 14:33:15 GMT  
		Size: 2.2 MB (2190561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8352b9693c0e7399cb563e4dc9b4394ee43d714db59b92ceecdcd06883100410`  
		Last Modified: Sat, 16 Dec 2023 14:33:14 GMT  
		Size: 69.3 KB (69284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b7140d2da7ce7ff97af0f97d5fcc37f45d4182ee641043ce27e32f3d0bc943`  
		Last Modified: Sat, 16 Dec 2023 14:35:45 GMT  
		Size: 71.3 MB (71275441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

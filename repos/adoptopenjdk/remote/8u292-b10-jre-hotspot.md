## `adoptopenjdk:8u292-b10-jre-hotspot`

```console
$ docker pull adoptopenjdk@sha256:491102021b950ee7d130afac67fb286266a7d53f11643b0775a03a5c68dfd791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.2183; amd64
	-	windows version 10.0.14393.4651; amd64

### `adoptopenjdk:8u292-b10-jre-hotspot` - linux; amd64

```console
$ docker pull adoptopenjdk@sha256:0b9cf1c86d1706529aaac1f364810de315917d2564f24acfc81853d951289a58
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86313241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9664e78a29b50f74ce0ebdf05db72c0c026bc40a0a733cbf7e1661257950a737`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:55 GMT
ADD file:d2abf27fe2e8b0b5f4da68c018560c73e11c53098329246e3e6fe176698ef941 in / 
# Tue, 31 Aug 2021 01:20:56 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:26:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Aug 2021 02:26:55 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:26:55 GMT
ENV JAVA_VERSION=jdk8u292-b10
# Tue, 31 Aug 2021 02:27:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b062ec775e6c2961532d9afeae4027fe3ac2cf4344cbc912a401be5bfb6ca221';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_aarch64_linux_hotspot_8u292b10.tar.gz';          ;;        armhf|armv7l)          ESUM='7f7707a7a3998737d2221080ea65d50ea96f5dde5226961ebcebd3ec99a82a32';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_arm_linux_hotspot_8u292b10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='245ecd0dfde7e763c0b65028aa0440489466926be2ba018977ac9047dc328a8e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_ppc64le_linux_hotspot_8u292b10.tar.gz';          ;;        s390x)          ESUM='170c12f2017c212b23c1ba47728dcf9f5f2c9f2e29abf503136a8e55f513e048';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_s390x_linux_hotspot_8u292b10.tar.gz';          LIBFFI_SUM='05e456a2e8ad9f20db846ccb96c483235c3243e27025c3e8e8e358411fd48be9';          LIBFFI_URL='http://launchpadlibrarian.net/354371408/libffi6_3.2.1-8_s390x.deb';          curl -LfsSo /tmp/libffi6.deb ${LIBFFI_URL};          echo "${LIBFFI_SUM} /tmp/libffi6.deb" | sha256sum -c -;          apt-get install -y --no-install-recommends /tmp/libffi6.deb;          rm -rf /tmp/libffi6.deb;          ;;        amd64|x86_64)          ESUM='cad66f48f90167ed19030c71f8f0580702c43cce5ce5a0d76833f7a5ae7c402a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_x64_linux_hotspot_8u292b10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 31 Aug 2021 02:27:10 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:35807b77a593c1147d13dc926a91dcc3015616ff7307cc30442c5a8e07546283`  
		Last Modified: Sat, 28 Aug 2021 03:03:19 GMT  
		Size: 28.6 MB (28570074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d71b8f96bb4f1c00b7375be1090b56f03343a56b15fdcdf40d5ac4a207e217`  
		Last Modified: Tue, 31 Aug 2021 02:37:06 GMT  
		Size: 16.0 MB (16033698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a858f023115a42de64cc4a26555800b16fbb463f312e367908e5a1e7d20622`  
		Last Modified: Tue, 31 Aug 2021 02:37:32 GMT  
		Size: 41.7 MB (41709469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:8u292-b10-jre-hotspot` - linux; arm variant v7

```console
$ docker pull adoptopenjdk@sha256:8fb8260521a55b3b489ab74ded7bf95b345c6258b2e259677058bb2a57eb3574
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78126127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb6e17ccc47c991f0df4e92f7c460edcffcbb53d6422696be360ed2d63923f8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:52 GMT
ADD file:f9dcf17ef0f45719dff5ed961907d78a1ea6671fecdb434536f3fc8cf15fbb3b in / 
# Tue, 31 Aug 2021 01:40:53 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:51:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Aug 2021 02:52:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:52:02 GMT
ENV JAVA_VERSION=jdk8u292-b10
# Tue, 31 Aug 2021 02:52:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b062ec775e6c2961532d9afeae4027fe3ac2cf4344cbc912a401be5bfb6ca221';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_aarch64_linux_hotspot_8u292b10.tar.gz';          ;;        armhf|armv7l)          ESUM='7f7707a7a3998737d2221080ea65d50ea96f5dde5226961ebcebd3ec99a82a32';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_arm_linux_hotspot_8u292b10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='245ecd0dfde7e763c0b65028aa0440489466926be2ba018977ac9047dc328a8e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_ppc64le_linux_hotspot_8u292b10.tar.gz';          ;;        s390x)          ESUM='170c12f2017c212b23c1ba47728dcf9f5f2c9f2e29abf503136a8e55f513e048';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_s390x_linux_hotspot_8u292b10.tar.gz';          LIBFFI_SUM='05e456a2e8ad9f20db846ccb96c483235c3243e27025c3e8e8e358411fd48be9';          LIBFFI_URL='http://launchpadlibrarian.net/354371408/libffi6_3.2.1-8_s390x.deb';          curl -LfsSo /tmp/libffi6.deb ${LIBFFI_URL};          echo "${LIBFFI_SUM} /tmp/libffi6.deb" | sha256sum -c -;          apt-get install -y --no-install-recommends /tmp/libffi6.deb;          rm -rf /tmp/libffi6.deb;          ;;        amd64|x86_64)          ESUM='cad66f48f90167ed19030c71f8f0580702c43cce5ce5a0d76833f7a5ae7c402a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_x64_linux_hotspot_8u292b10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 31 Aug 2021 02:52:49 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:cccc98128e2b3db00394b4e59c3f674a52e4b861786d9fab388357a88fc428a2`  
		Last Modified: Tue, 31 Aug 2021 01:44:57 GMT  
		Size: 24.1 MB (24068823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b915f774c910de28b940b41c37fc76946eb150ac0a4048d2d2cbc5b3b0983c26`  
		Last Modified: Tue, 31 Aug 2021 02:59:59 GMT  
		Size: 14.9 MB (14902564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcac37691c406c1621a61b7378423c1657bc42b516c9a19db301507dc23f9ded`  
		Last Modified: Tue, 31 Aug 2021 03:01:10 GMT  
		Size: 39.2 MB (39154740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:8u292-b10-jre-hotspot` - linux; arm64 variant v8

```console
$ docker pull adoptopenjdk@sha256:9436b46ff17bd7b5d36b7b0ac61eaad7e0449cd024f8c622d6d39ce76f57f404
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84096754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86a31d18ebf6c70979ae636c743ff7763fb1b5f64a1f9d5cf95ecb69554a671`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:02:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:02:25 GMT
ENV JAVA_VERSION=jdk8u292-b10
# Fri, 01 Oct 2021 03:02:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b062ec775e6c2961532d9afeae4027fe3ac2cf4344cbc912a401be5bfb6ca221';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_aarch64_linux_hotspot_8u292b10.tar.gz';          ;;        armhf|armv7l)          ESUM='7f7707a7a3998737d2221080ea65d50ea96f5dde5226961ebcebd3ec99a82a32';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_arm_linux_hotspot_8u292b10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='245ecd0dfde7e763c0b65028aa0440489466926be2ba018977ac9047dc328a8e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_ppc64le_linux_hotspot_8u292b10.tar.gz';          ;;        s390x)          ESUM='170c12f2017c212b23c1ba47728dcf9f5f2c9f2e29abf503136a8e55f513e048';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_s390x_linux_hotspot_8u292b10.tar.gz';          LIBFFI_SUM='05e456a2e8ad9f20db846ccb96c483235c3243e27025c3e8e8e358411fd48be9';          LIBFFI_URL='http://launchpadlibrarian.net/354371408/libffi6_3.2.1-8_s390x.deb';          curl -LfsSo /tmp/libffi6.deb ${LIBFFI_URL};          echo "${LIBFFI_SUM} /tmp/libffi6.deb" | sha256sum -c -;          apt-get install -y --no-install-recommends /tmp/libffi6.deb;          rm -rf /tmp/libffi6.deb;          ;;        amd64|x86_64)          ESUM='cad66f48f90167ed19030c71f8f0580702c43cce5ce5a0d76833f7a5ae7c402a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_x64_linux_hotspot_8u292b10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:02:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965f9c84d32763760a8a95b798239bf2dd8423aeb8fb56015ddd90196d483d9f`  
		Last Modified: Fri, 01 Oct 2021 03:06:06 GMT  
		Size: 15.9 MB (15895939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d39b157357558e3d7cf405528e5416f0a5835e8cfe8d5b2f19b47e74c8f6bb`  
		Last Modified: Fri, 01 Oct 2021 03:06:34 GMT  
		Size: 41.0 MB (41028410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:8u292-b10-jre-hotspot` - linux; ppc64le

```console
$ docker pull adoptopenjdk@sha256:2e21f5c18e9fac6597b9fe52e9450b46d0c509155e5ddb23e06e9de25a0f5297
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91603267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87216ac4842f084d74ef4debe5cfb3b249ea2be09b9b2631691f29020605cfa6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Aug 2021 02:10:40 GMT
ADD file:7e5ee5560faaa801aa10a76122190026f8c1da00c809f4fb6ff441751ba0c90f in / 
# Tue, 31 Aug 2021 02:10:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:31:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Aug 2021 02:33:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:33:30 GMT
ENV JAVA_VERSION=jdk8u292-b10
# Tue, 31 Aug 2021 02:34:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b062ec775e6c2961532d9afeae4027fe3ac2cf4344cbc912a401be5bfb6ca221';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_aarch64_linux_hotspot_8u292b10.tar.gz';          ;;        armhf|armv7l)          ESUM='7f7707a7a3998737d2221080ea65d50ea96f5dde5226961ebcebd3ec99a82a32';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_arm_linux_hotspot_8u292b10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='245ecd0dfde7e763c0b65028aa0440489466926be2ba018977ac9047dc328a8e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_ppc64le_linux_hotspot_8u292b10.tar.gz';          ;;        s390x)          ESUM='170c12f2017c212b23c1ba47728dcf9f5f2c9f2e29abf503136a8e55f513e048';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_s390x_linux_hotspot_8u292b10.tar.gz';          LIBFFI_SUM='05e456a2e8ad9f20db846ccb96c483235c3243e27025c3e8e8e358411fd48be9';          LIBFFI_URL='http://launchpadlibrarian.net/354371408/libffi6_3.2.1-8_s390x.deb';          curl -LfsSo /tmp/libffi6.deb ${LIBFFI_URL};          echo "${LIBFFI_SUM} /tmp/libffi6.deb" | sha256sum -c -;          apt-get install -y --no-install-recommends /tmp/libffi6.deb;          rm -rf /tmp/libffi6.deb;          ;;        amd64|x86_64)          ESUM='cad66f48f90167ed19030c71f8f0580702c43cce5ce5a0d76833f7a5ae7c402a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_x64_linux_hotspot_8u292b10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 31 Aug 2021 02:34:43 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:59390c695558464c51dc1fced64934b549770630192a1639ac6a90f59bd63b13`  
		Last Modified: Tue, 31 Aug 2021 02:14:21 GMT  
		Size: 33.3 MB (33291791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6df1a3e21a26bf9e0775ad823e1762b00bf8c2a0650a891b7860b7fe18741a`  
		Last Modified: Tue, 31 Aug 2021 02:54:54 GMT  
		Size: 17.2 MB (17208636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:121e26cc3659bce95cb43befcb6a8398aeef57e93b2f05ce094abe841223bb22`  
		Last Modified: Tue, 31 Aug 2021 02:55:23 GMT  
		Size: 41.1 MB (41102840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:8u292-b10-jre-hotspot` - linux; s390x

```console
$ docker pull adoptopenjdk@sha256:e77ca967163a6fd6e1bb41cf1342746814d8da810ae92de8ee9a746eff6854af
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81702207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffdee81ab65496aedb4d0e377dbebc1abac3a7d82694d1be36048335f93905f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Oct 2021 01:42:28 GMT
ADD file:28b3d1959812d7666f9f73b52562cdaaaf84ff25ce6331995e21c66bb31b0cc2 in / 
# Fri, 01 Oct 2021 01:42:30 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 02:00:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 02:00:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 02:00:18 GMT
ENV JAVA_VERSION=jdk8u292-b10
# Fri, 01 Oct 2021 02:00:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='b062ec775e6c2961532d9afeae4027fe3ac2cf4344cbc912a401be5bfb6ca221';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_aarch64_linux_hotspot_8u292b10.tar.gz';          ;;        armhf|armv7l)          ESUM='7f7707a7a3998737d2221080ea65d50ea96f5dde5226961ebcebd3ec99a82a32';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_arm_linux_hotspot_8u292b10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='245ecd0dfde7e763c0b65028aa0440489466926be2ba018977ac9047dc328a8e';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_ppc64le_linux_hotspot_8u292b10.tar.gz';          ;;        s390x)          ESUM='170c12f2017c212b23c1ba47728dcf9f5f2c9f2e29abf503136a8e55f513e048';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_s390x_linux_hotspot_8u292b10.tar.gz';          LIBFFI_SUM='05e456a2e8ad9f20db846ccb96c483235c3243e27025c3e8e8e358411fd48be9';          LIBFFI_URL='http://launchpadlibrarian.net/354371408/libffi6_3.2.1-8_s390x.deb';          curl -LfsSo /tmp/libffi6.deb ${LIBFFI_URL};          echo "${LIBFFI_SUM} /tmp/libffi6.deb" | sha256sum -c -;          apt-get install -y --no-install-recommends /tmp/libffi6.deb;          rm -rf /tmp/libffi6.deb;          ;;        amd64|x86_64)          ESUM='cad66f48f90167ed19030c71f8f0580702c43cce5ce5a0d76833f7a5ae7c402a';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_x64_linux_hotspot_8u292b10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 02:00:41 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:21245da3aae0a4172d9a415c8ba92069601c8a55fc39b783bce7981e97de1b4d`  
		Last Modified: Fri, 01 Oct 2021 01:44:02 GMT  
		Size: 27.1 MB (27122910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b23a8bdcc3c25fc238593c281d2480b42fe86d322be5a1580ea62c30b309a9`  
		Last Modified: Fri, 01 Oct 2021 02:12:12 GMT  
		Size: 15.7 MB (15739781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d900be9ae7cbd426195cefae59e43d30cb93a358be4c25953d4b7c11f5d665`  
		Last Modified: Fri, 01 Oct 2021 02:12:29 GMT  
		Size: 38.8 MB (38839516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:8u292-b10-jre-hotspot` - windows version 10.0.17763.2183; amd64

```console
$ docker pull adoptopenjdk@sha256:14471ca6e3009d1fb45a3e71cc539892739cc283e924237b7bc8366ce2f3cd9c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2761411481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe99a12bb915bdf40cf7c6895df499c7459a17d77288072b3e1216b60feca57`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Sep 2021 04:08:33 GMT
RUN Install update 1809-amd64
# Wed, 15 Sep 2021 00:29:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Sep 2021 17:06:23 GMT
ENV JAVA_VERSION=jdk8u292-b10
# Wed, 15 Sep 2021 17:10:13 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_x64_windows_hotspot_8u292b10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_x64_windows_hotspot_8u292b10.msi ;     Write-Host ('Verifying sha256 (4365ea6d753ce61ce809fcd94e6cda1723673b3a79b4ca71a01599eb0aecef0a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4365ea6d753ce61ce809fcd94e6cda1723673b3a79b4ca71a01599eb0aecef0a') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {             Write-Host 'FAILED installing MSI!' ;             exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0ddf88812f10c7d6edc858aa9784ff5ca9de4a7bb631909c090090343abd059`  
		Size: 968.4 MB (968365008 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92dd43eae724dbe7e9e517c7fded74c5920ae7eb160042055178ceadf1916505`  
		Last Modified: Wed, 15 Sep 2021 01:09:40 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a4de21e2555698cee55a4c837cdf4c76050088ebf2a2cb2ea0f1e3fc0763e6`  
		Last Modified: Wed, 15 Sep 2021 17:55:20 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d072a8f65973109027d3d66a2a58a8c34dd30d35a49a738b8e802e3550581d2`  
		Last Modified: Wed, 15 Sep 2021 17:59:29 GMT  
		Size: 74.7 MB (74710740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:8u292-b10-jre-hotspot` - windows version 10.0.14393.4651; amd64

```console
$ docker pull adoptopenjdk@sha256:5d016f7aee3ef79f1627928306fcbe53dde704ac893d5098735c9ef2b4866e7e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6345963808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d4c8ed7398cbe1fa1dc545c37ed636071189433a05fe6290589fecb1d7df3b5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 13 Sep 2021 01:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Sep 2021 00:34:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Sep 2021 17:07:48 GMT
ENV JAVA_VERSION=jdk8u292-b10
# Wed, 15 Sep 2021 17:11:26 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_x64_windows_hotspot_8u292b10.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12 ; Invoke-WebRequest -Uri https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jre_x64_windows_hotspot_8u292b10.msi -O 'openjdk.msi' ;     Write-Host ('Verifying sha256 (4365ea6d753ce61ce809fcd94e6cda1723673b3a79b4ca71a01599eb0aecef0a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4365ea6d753ce61ce809fcd94e6cda1723673b3a79b4ca71a01599eb0aecef0a') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {             Write-Host 'FAILED installing MSI!' ;             exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9b8281bf21e46c781fb54e4f15f5728e2c44dea4219c9e6deeb732f1d909d3b`  
		Size: 2.2 GB (2201342322 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8721f004192f15fe71b8626ef3f3e34cbf2cfe1d15a63b6b544ab946162ef707`  
		Last Modified: Wed, 15 Sep 2021 01:10:18 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac152e942da701b8e968f1bd5bbfb5997f176706a5fd86a1dd9f648f6621552`  
		Last Modified: Wed, 15 Sep 2021 17:58:54 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751a9d23ee4dfece8d5810daf9ca0dff05911e3472a843e9f1a0b9aeb0cd324d`  
		Last Modified: Wed, 15 Sep 2021 17:59:47 GMT  
		Size: 74.6 MB (74632862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

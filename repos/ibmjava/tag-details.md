<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ibmjava`

-	[`ibmjava:8`](#ibmjava8)
-	[`ibmjava:8-jre`](#ibmjava8-jre)
-	[`ibmjava:8-sdk`](#ibmjava8-sdk)
-	[`ibmjava:8-sfj`](#ibmjava8-sfj)
-	[`ibmjava:jre`](#ibmjavajre)
-	[`ibmjava:latest`](#ibmjavalatest)
-	[`ibmjava:sdk`](#ibmjavasdk)
-	[`ibmjava:sfj`](#ibmjavasfj)

## `ibmjava:8`

```console
$ docker pull ibmjava@sha256:2a67f2f53268d284058e63cbbfe03689d1b076f777f13e89339141f95cf35fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8` - linux; amd64

```console
$ docker pull ibmjava@sha256:fd0d5341c971d0082f905f80cf5e470728540169aa3b2d00a941752a09482948
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158983700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff72f24255133d38805f1cac5f7ec214137f7327ce10cdc4b2062cd82feb154`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:11 GMT
ADD file:3c88cea17de40599dc8b8da90adc8439635066835e930f9573ec6cc856c5c096 in / 
# Fri, 09 Dec 2022 01:20:12 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 04:21:18 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 04:21:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 04:21:25 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 04:22:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 04:22:24 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:fb668870d8a72b5d72a3b6d98ee626e00f9f7c29c6f4f7d3a63673d747dbffe7`  
		Last Modified: Fri, 09 Dec 2022 01:21:25 GMT  
		Size: 26.7 MB (26711459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acae8945e830b26864e6f4dcccac1c0f41145f5792c80fa11241789b45ce0c0`  
		Last Modified: Fri, 09 Dec 2022 04:24:50 GMT  
		Size: 2.9 MB (2949577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb0aaff24d2e9d944fe20d8d7b841c223905eed0cad23da4932cdc722436b29`  
		Last Modified: Fri, 09 Dec 2022 04:24:59 GMT  
		Size: 129.3 MB (129322664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; 386

```console
$ docker pull ibmjava@sha256:d978d740ac7089e74cd101a2fba08a0cea544602b389666de103660a9dd01749
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147606546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01470d6cfe5eaaf9ae3e01c75a9fce78c93171476756f8c8678594f5f019807`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Jan 2023 18:00:42 GMT
ADD file:dc76519390168deb6f9bb6052d08c6e7840908a831276d99bb19c6c245f8517b in / 
# Mon, 02 Jan 2023 18:00:43 GMT
CMD ["bash"]
# Mon, 02 Jan 2023 18:16:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Mon, 02 Jan 2023 18:17:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Mon, 02 Jan 2023 18:17:02 GMT
ENV JAVA_VERSION=8.0.7.20
# Mon, 02 Jan 2023 18:17:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Mon, 02 Jan 2023 18:17:53 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1b284dbae22f155bfee2a25073c97c9758e66aa7129a455cb533d8e2cbc873f9`  
		Last Modified: Mon, 02 Jan 2023 18:01:17 GMT  
		Size: 27.2 MB (27165399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfed9768a70dc0ba56e7fd9969f79fa2ebac801784981b1c52ca8415df7ae55`  
		Last Modified: Mon, 02 Jan 2023 18:20:25 GMT  
		Size: 3.0 MB (2981625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27931503bf0f6eccf183f3a58a7e17d21e3a43b785cfe41e51c4a0bc43c766c9`  
		Last Modified: Mon, 02 Jan 2023 18:20:35 GMT  
		Size: 117.5 MB (117459522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:2417c6045e0c9c23a7da37faaf25f81265ad7fe3ff68309abb22a419cc69337c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162514573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476711c0b02342d898ae41f60ab4491fc0d6811dfb1ad53ddfef82b695143bf8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:27:15 GMT
ADD file:05ec256cb279f6d94111b2413d31c85c4e1ff1365bce34d2fc4aa2788885fa06 in / 
# Fri, 09 Dec 2022 01:27:17 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:02:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 03:02:46 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 03:02:47 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 03:05:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 03:05:19 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:29d5a8bf9800ea1d873fe104fc2b0b6d4efed1269ce0f9a80e4d65e96d3246e2`  
		Last Modified: Fri, 09 Dec 2022 01:29:45 GMT  
		Size: 30.4 MB (30442475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b911794ae1ce4902a6daaf989e919ecf0eec34798ddaf26f80408d03d5779c`  
		Last Modified: Fri, 09 Dec 2022 03:10:49 GMT  
		Size: 3.1 MB (3075733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103bba608e4bcf78845fbe100e090c5cbdd4d12ecd86a1d8aaab5fb5d5778837`  
		Last Modified: Fri, 09 Dec 2022 03:11:06 GMT  
		Size: 129.0 MB (128996365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; s390x

```console
$ docker pull ibmjava@sha256:00f041bf4980f625ae0da5ada4eaa44da6eb6e78cff06ecc6bba7a3135d83698
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154511264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844157c990acd48fcba5a3da83890dab87aa7db830bfd80ee4165f6bb4b0b0f4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:52:21 GMT
ADD file:c2fcdae7883d865c232dfc26d514c111189f6940ba74273c78067624cd02c962 in / 
# Fri, 09 Dec 2022 01:52:24 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:15:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 03:16:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 03:16:12 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 03:17:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 03:17:19 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3fb013d46f2fda49d6c671f39f55c3330f927a4c55ae7e5096daf0a638dc38ec`  
		Last Modified: Fri, 09 Dec 2022 01:54:45 GMT  
		Size: 25.4 MB (25371298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49e7e6835b120e4486c693b4f03bdf01ba76a250b74306406b7bd9fbb2d737c`  
		Last Modified: Fri, 09 Dec 2022 03:20:23 GMT  
		Size: 2.7 MB (2667341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fdd86aa56415e723ad1c625e8e84de704bd93370cb5380694e05e888e84210`  
		Last Modified: Fri, 09 Dec 2022 03:20:31 GMT  
		Size: 126.5 MB (126472625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:2a67f2f53268d284058e63cbbfe03689d1b076f777f13e89339141f95cf35fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:fd0d5341c971d0082f905f80cf5e470728540169aa3b2d00a941752a09482948
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158983700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff72f24255133d38805f1cac5f7ec214137f7327ce10cdc4b2062cd82feb154`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:11 GMT
ADD file:3c88cea17de40599dc8b8da90adc8439635066835e930f9573ec6cc856c5c096 in / 
# Fri, 09 Dec 2022 01:20:12 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 04:21:18 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 04:21:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 04:21:25 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 04:22:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 04:22:24 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:fb668870d8a72b5d72a3b6d98ee626e00f9f7c29c6f4f7d3a63673d747dbffe7`  
		Last Modified: Fri, 09 Dec 2022 01:21:25 GMT  
		Size: 26.7 MB (26711459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acae8945e830b26864e6f4dcccac1c0f41145f5792c80fa11241789b45ce0c0`  
		Last Modified: Fri, 09 Dec 2022 04:24:50 GMT  
		Size: 2.9 MB (2949577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb0aaff24d2e9d944fe20d8d7b841c223905eed0cad23da4932cdc722436b29`  
		Last Modified: Fri, 09 Dec 2022 04:24:59 GMT  
		Size: 129.3 MB (129322664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; 386

```console
$ docker pull ibmjava@sha256:d978d740ac7089e74cd101a2fba08a0cea544602b389666de103660a9dd01749
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147606546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01470d6cfe5eaaf9ae3e01c75a9fce78c93171476756f8c8678594f5f019807`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Jan 2023 18:00:42 GMT
ADD file:dc76519390168deb6f9bb6052d08c6e7840908a831276d99bb19c6c245f8517b in / 
# Mon, 02 Jan 2023 18:00:43 GMT
CMD ["bash"]
# Mon, 02 Jan 2023 18:16:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Mon, 02 Jan 2023 18:17:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Mon, 02 Jan 2023 18:17:02 GMT
ENV JAVA_VERSION=8.0.7.20
# Mon, 02 Jan 2023 18:17:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Mon, 02 Jan 2023 18:17:53 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1b284dbae22f155bfee2a25073c97c9758e66aa7129a455cb533d8e2cbc873f9`  
		Last Modified: Mon, 02 Jan 2023 18:01:17 GMT  
		Size: 27.2 MB (27165399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfed9768a70dc0ba56e7fd9969f79fa2ebac801784981b1c52ca8415df7ae55`  
		Last Modified: Mon, 02 Jan 2023 18:20:25 GMT  
		Size: 3.0 MB (2981625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27931503bf0f6eccf183f3a58a7e17d21e3a43b785cfe41e51c4a0bc43c766c9`  
		Last Modified: Mon, 02 Jan 2023 18:20:35 GMT  
		Size: 117.5 MB (117459522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:2417c6045e0c9c23a7da37faaf25f81265ad7fe3ff68309abb22a419cc69337c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162514573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476711c0b02342d898ae41f60ab4491fc0d6811dfb1ad53ddfef82b695143bf8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:27:15 GMT
ADD file:05ec256cb279f6d94111b2413d31c85c4e1ff1365bce34d2fc4aa2788885fa06 in / 
# Fri, 09 Dec 2022 01:27:17 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:02:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 03:02:46 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 03:02:47 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 03:05:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 03:05:19 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:29d5a8bf9800ea1d873fe104fc2b0b6d4efed1269ce0f9a80e4d65e96d3246e2`  
		Last Modified: Fri, 09 Dec 2022 01:29:45 GMT  
		Size: 30.4 MB (30442475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b911794ae1ce4902a6daaf989e919ecf0eec34798ddaf26f80408d03d5779c`  
		Last Modified: Fri, 09 Dec 2022 03:10:49 GMT  
		Size: 3.1 MB (3075733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103bba608e4bcf78845fbe100e090c5cbdd4d12ecd86a1d8aaab5fb5d5778837`  
		Last Modified: Fri, 09 Dec 2022 03:11:06 GMT  
		Size: 129.0 MB (128996365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:00f041bf4980f625ae0da5ada4eaa44da6eb6e78cff06ecc6bba7a3135d83698
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154511264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844157c990acd48fcba5a3da83890dab87aa7db830bfd80ee4165f6bb4b0b0f4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:52:21 GMT
ADD file:c2fcdae7883d865c232dfc26d514c111189f6940ba74273c78067624cd02c962 in / 
# Fri, 09 Dec 2022 01:52:24 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:15:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 03:16:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 03:16:12 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 03:17:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 03:17:19 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3fb013d46f2fda49d6c671f39f55c3330f927a4c55ae7e5096daf0a638dc38ec`  
		Last Modified: Fri, 09 Dec 2022 01:54:45 GMT  
		Size: 25.4 MB (25371298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49e7e6835b120e4486c693b4f03bdf01ba76a250b74306406b7bd9fbb2d737c`  
		Last Modified: Fri, 09 Dec 2022 03:20:23 GMT  
		Size: 2.7 MB (2667341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fdd86aa56415e723ad1c625e8e84de704bd93370cb5380694e05e888e84210`  
		Last Modified: Fri, 09 Dec 2022 03:20:31 GMT  
		Size: 126.5 MB (126472625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:825bc6b1d083e59b05f07d26b0469c705eed06a870877972c8e4970f6170b203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:a956390b9139dac86da07a303411516fcb13a8db167c2638a14d448616c34b64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 MB (196135637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4d7186a6ea718b9cff7837b560b6b75dbe2a679b1b16b39ff3142f2e3bd29e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:11 GMT
ADD file:3c88cea17de40599dc8b8da90adc8439635066835e930f9573ec6cc856c5c096 in / 
# Fri, 09 Dec 2022 01:20:12 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 04:21:18 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 04:21:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 04:21:25 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 04:24:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0f6aef4c3550a8f85288da8bc6fada405b0ce2226d6b1b57d0aae98cd5eef5e4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='fa7661c2eb2982c4fb85c6894e7a975970b27b6ee82d5facb352f075cc1dfca3';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a56803671fe7d1c85f18d566dbcb7fbaf1d60c6f1d6de34e35a257e0c8095f9b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='71c913a1eed7daae952657e18eb9a2e71723106b6e7b56373f18564db77f551e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='c8641bc22443ebccaedf1822a12ec1303d89577d45c875702e1f628066c7f383';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 04:24:25 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:fb668870d8a72b5d72a3b6d98ee626e00f9f7c29c6f4f7d3a63673d747dbffe7`  
		Last Modified: Fri, 09 Dec 2022 01:21:25 GMT  
		Size: 26.7 MB (26711459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acae8945e830b26864e6f4dcccac1c0f41145f5792c80fa11241789b45ce0c0`  
		Last Modified: Fri, 09 Dec 2022 04:24:50 GMT  
		Size: 2.9 MB (2949577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02a1910973efec527f161388117cc460c6cf2d683e973a410ccbdea2cb220d6`  
		Last Modified: Fri, 09 Dec 2022 04:25:37 GMT  
		Size: 166.5 MB (166474601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; 386

```console
$ docker pull ibmjava@sha256:ec3c1234489b541cb77c46caa537e1c83712f6d6a42cefcfcbaa947ae1a6c047
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184641462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d086184a012ce6dc984c9aeb8a36013b00165ea97c3ffe0c29f65a34674aaf1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Jan 2023 18:00:42 GMT
ADD file:dc76519390168deb6f9bb6052d08c6e7840908a831276d99bb19c6c245f8517b in / 
# Mon, 02 Jan 2023 18:00:43 GMT
CMD ["bash"]
# Mon, 02 Jan 2023 18:16:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Mon, 02 Jan 2023 18:17:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Mon, 02 Jan 2023 18:17:02 GMT
ENV JAVA_VERSION=8.0.7.20
# Mon, 02 Jan 2023 18:19:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0f6aef4c3550a8f85288da8bc6fada405b0ce2226d6b1b57d0aae98cd5eef5e4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='fa7661c2eb2982c4fb85c6894e7a975970b27b6ee82d5facb352f075cc1dfca3';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a56803671fe7d1c85f18d566dbcb7fbaf1d60c6f1d6de34e35a257e0c8095f9b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='71c913a1eed7daae952657e18eb9a2e71723106b6e7b56373f18564db77f551e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='c8641bc22443ebccaedf1822a12ec1303d89577d45c875702e1f628066c7f383';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Mon, 02 Jan 2023 18:19:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1b284dbae22f155bfee2a25073c97c9758e66aa7129a455cb533d8e2cbc873f9`  
		Last Modified: Mon, 02 Jan 2023 18:01:17 GMT  
		Size: 27.2 MB (27165399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfed9768a70dc0ba56e7fd9969f79fa2ebac801784981b1c52ca8415df7ae55`  
		Last Modified: Mon, 02 Jan 2023 18:20:25 GMT  
		Size: 3.0 MB (2981625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2faac65d385f880ffda561872b05603633ac3eddd661fa6e9bd2a118642dbf61`  
		Last Modified: Mon, 02 Jan 2023 18:21:23 GMT  
		Size: 154.5 MB (154494438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:e263255780b671733d97402967d06b7e68dfa164434d4ac359d3b798c56f563f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.8 MB (199790229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd421c38a1ffbb340561f27c684606bfbdd33ce423d4342546cc52bd8f8ba5d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:27:15 GMT
ADD file:05ec256cb279f6d94111b2413d31c85c4e1ff1365bce34d2fc4aa2788885fa06 in / 
# Fri, 09 Dec 2022 01:27:17 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:02:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 03:02:46 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 03:02:47 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 03:10:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0f6aef4c3550a8f85288da8bc6fada405b0ce2226d6b1b57d0aae98cd5eef5e4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='fa7661c2eb2982c4fb85c6894e7a975970b27b6ee82d5facb352f075cc1dfca3';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a56803671fe7d1c85f18d566dbcb7fbaf1d60c6f1d6de34e35a257e0c8095f9b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='71c913a1eed7daae952657e18eb9a2e71723106b6e7b56373f18564db77f551e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='c8641bc22443ebccaedf1822a12ec1303d89577d45c875702e1f628066c7f383';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 03:10:15 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:29d5a8bf9800ea1d873fe104fc2b0b6d4efed1269ce0f9a80e4d65e96d3246e2`  
		Last Modified: Fri, 09 Dec 2022 01:29:45 GMT  
		Size: 30.4 MB (30442475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b911794ae1ce4902a6daaf989e919ecf0eec34798ddaf26f80408d03d5779c`  
		Last Modified: Fri, 09 Dec 2022 03:10:49 GMT  
		Size: 3.1 MB (3075733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d2c61b0c40100d38a276fbbb60c6af43afd4db814d5513a69ad6f5bbcf6eb8`  
		Last Modified: Fri, 09 Dec 2022 03:12:10 GMT  
		Size: 166.3 MB (166272021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:8b537094cf6e76ab6780f09a71760cb25113ae3ee677f51a3cfd0ce1afbaa3f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184803052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b021945b39e0bb4aacfe7daa2c1829c207148ecf3a7fbf2cdc2b6a08d49bfb4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:52:21 GMT
ADD file:c2fcdae7883d865c232dfc26d514c111189f6940ba74273c78067624cd02c962 in / 
# Fri, 09 Dec 2022 01:52:24 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:15:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 03:16:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 03:16:12 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 03:19:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0f6aef4c3550a8f85288da8bc6fada405b0ce2226d6b1b57d0aae98cd5eef5e4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='fa7661c2eb2982c4fb85c6894e7a975970b27b6ee82d5facb352f075cc1dfca3';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a56803671fe7d1c85f18d566dbcb7fbaf1d60c6f1d6de34e35a257e0c8095f9b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='71c913a1eed7daae952657e18eb9a2e71723106b6e7b56373f18564db77f551e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='c8641bc22443ebccaedf1822a12ec1303d89577d45c875702e1f628066c7f383';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 03:19:44 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3fb013d46f2fda49d6c671f39f55c3330f927a4c55ae7e5096daf0a638dc38ec`  
		Last Modified: Fri, 09 Dec 2022 01:54:45 GMT  
		Size: 25.4 MB (25371298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49e7e6835b120e4486c693b4f03bdf01ba76a250b74306406b7bd9fbb2d737c`  
		Last Modified: Fri, 09 Dec 2022 03:20:23 GMT  
		Size: 2.7 MB (2667341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b679b381ca767b8d80570c694f49d474020767caaac607fee5fab8f04403f2`  
		Last Modified: Fri, 09 Dec 2022 03:21:04 GMT  
		Size: 156.8 MB (156764413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:8370d4445c3a413239d8875b62d56cf744e3f50474836b0bd17715f8df090cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:93febaf81c4d9f76e1f885ba42c7da63bd5f00d1b41067dbeff1d472f4af5a6c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94669896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86512e789ad970c3957c44851442c02d3f81e8449d2ddec84992e25979d1f332`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:11 GMT
ADD file:3c88cea17de40599dc8b8da90adc8439635066835e930f9573ec6cc856c5c096 in / 
# Fri, 09 Dec 2022 01:20:12 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 04:21:18 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 04:21:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 04:21:25 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 04:23:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bb548976980c436b15e59e0db7b4e99a7ed273df39e17db60047f950c2863c1b';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='768e6f8df5c9735d703f2dd5352b7c063949d59c6e15bc7d5c31d7ac667a241a';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='1ce92e9c420b2d081c8cd63c8441b324e49348360490d61e08a0908b830748cb';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e790dc7707417153227e1f3164db1c699e3b6b9f697d9e1c9c9142bc0e3d3409';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='bfac3d6409a7996301d948faedfd4c19920dbb667ba699b7fd4719188366be8b';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 04:23:06 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:fb668870d8a72b5d72a3b6d98ee626e00f9f7c29c6f4f7d3a63673d747dbffe7`  
		Last Modified: Fri, 09 Dec 2022 01:21:25 GMT  
		Size: 26.7 MB (26711459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acae8945e830b26864e6f4dcccac1c0f41145f5792c80fa11241789b45ce0c0`  
		Last Modified: Fri, 09 Dec 2022 04:24:50 GMT  
		Size: 2.9 MB (2949577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418a294084d28a15701eab94ddac7b9b23dd9b9a965071887f43fbbb6d60c08b`  
		Last Modified: Fri, 09 Dec 2022 04:25:17 GMT  
		Size: 65.0 MB (65008860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; 386

```console
$ docker pull ibmjava@sha256:358a43ad8b9ac09544689fdc444d1bdf13a3287c54b9b530efd11c13376bf2bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94532127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b44bdfb616f53825307df86b887023a7ddf27e4f7157035e917597294465868e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Jan 2023 18:00:42 GMT
ADD file:dc76519390168deb6f9bb6052d08c6e7840908a831276d99bb19c6c245f8517b in / 
# Mon, 02 Jan 2023 18:00:43 GMT
CMD ["bash"]
# Mon, 02 Jan 2023 18:16:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Mon, 02 Jan 2023 18:17:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Mon, 02 Jan 2023 18:17:02 GMT
ENV JAVA_VERSION=8.0.7.20
# Mon, 02 Jan 2023 18:18:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bb548976980c436b15e59e0db7b4e99a7ed273df39e17db60047f950c2863c1b';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='768e6f8df5c9735d703f2dd5352b7c063949d59c6e15bc7d5c31d7ac667a241a';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='1ce92e9c420b2d081c8cd63c8441b324e49348360490d61e08a0908b830748cb';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e790dc7707417153227e1f3164db1c699e3b6b9f697d9e1c9c9142bc0e3d3409';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='bfac3d6409a7996301d948faedfd4c19920dbb667ba699b7fd4719188366be8b';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Mon, 02 Jan 2023 18:18:47 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1b284dbae22f155bfee2a25073c97c9758e66aa7129a455cb533d8e2cbc873f9`  
		Last Modified: Mon, 02 Jan 2023 18:01:17 GMT  
		Size: 27.2 MB (27165399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfed9768a70dc0ba56e7fd9969f79fa2ebac801784981b1c52ca8415df7ae55`  
		Last Modified: Mon, 02 Jan 2023 18:20:25 GMT  
		Size: 3.0 MB (2981625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97229bb82bc2a976df402be61e6622e55770c6ba9cf87bd06e661244bc3efc18`  
		Last Modified: Mon, 02 Jan 2023 18:21:02 GMT  
		Size: 64.4 MB (64385103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:510b44231e8c7dbd823a6352445fcdd82450b642e95e308f6d1f58fd2900fe2f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98807917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b92620008306b672c3411bc4acda1625ccd5e11316b97e694b202cd7d27cbe92`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:27:15 GMT
ADD file:05ec256cb279f6d94111b2413d31c85c4e1ff1365bce34d2fc4aa2788885fa06 in / 
# Fri, 09 Dec 2022 01:27:17 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:02:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 03:02:46 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 03:02:47 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 03:07:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bb548976980c436b15e59e0db7b4e99a7ed273df39e17db60047f950c2863c1b';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='768e6f8df5c9735d703f2dd5352b7c063949d59c6e15bc7d5c31d7ac667a241a';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='1ce92e9c420b2d081c8cd63c8441b324e49348360490d61e08a0908b830748cb';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e790dc7707417153227e1f3164db1c699e3b6b9f697d9e1c9c9142bc0e3d3409';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='bfac3d6409a7996301d948faedfd4c19920dbb667ba699b7fd4719188366be8b';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 03:07:09 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:29d5a8bf9800ea1d873fe104fc2b0b6d4efed1269ce0f9a80e4d65e96d3246e2`  
		Last Modified: Fri, 09 Dec 2022 01:29:45 GMT  
		Size: 30.4 MB (30442475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b911794ae1ce4902a6daaf989e919ecf0eec34798ddaf26f80408d03d5779c`  
		Last Modified: Fri, 09 Dec 2022 03:10:49 GMT  
		Size: 3.1 MB (3075733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6483ca4de227708018f79d4040e212e4afbf3a2960d20405e990569c6a62163`  
		Last Modified: Fri, 09 Dec 2022 03:11:38 GMT  
		Size: 65.3 MB (65289709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:5a1ceedf454081b9b5b04f6e129a05bc940ceb8afa9a9d81de7459698e08ff2a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94161761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9fe6165d115618482c50a742d945885d73ac35bedd8106e940e62dfde10dae`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:52:21 GMT
ADD file:c2fcdae7883d865c232dfc26d514c111189f6940ba74273c78067624cd02c962 in / 
# Fri, 09 Dec 2022 01:52:24 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:15:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 03:16:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 03:16:12 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 03:18:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bb548976980c436b15e59e0db7b4e99a7ed273df39e17db60047f950c2863c1b';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='768e6f8df5c9735d703f2dd5352b7c063949d59c6e15bc7d5c31d7ac667a241a';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='1ce92e9c420b2d081c8cd63c8441b324e49348360490d61e08a0908b830748cb';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e790dc7707417153227e1f3164db1c699e3b6b9f697d9e1c9c9142bc0e3d3409';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='bfac3d6409a7996301d948faedfd4c19920dbb667ba699b7fd4719188366be8b';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 03:18:14 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3fb013d46f2fda49d6c671f39f55c3330f927a4c55ae7e5096daf0a638dc38ec`  
		Last Modified: Fri, 09 Dec 2022 01:54:45 GMT  
		Size: 25.4 MB (25371298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49e7e6835b120e4486c693b4f03bdf01ba76a250b74306406b7bd9fbb2d737c`  
		Last Modified: Fri, 09 Dec 2022 03:20:23 GMT  
		Size: 2.7 MB (2667341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0cd8775a84894340cf7748f3238f0279db045c4e1d15c1256b87823a27951ad`  
		Last Modified: Fri, 09 Dec 2022 03:20:47 GMT  
		Size: 66.1 MB (66123122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:2a67f2f53268d284058e63cbbfe03689d1b076f777f13e89339141f95cf35fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:fd0d5341c971d0082f905f80cf5e470728540169aa3b2d00a941752a09482948
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158983700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff72f24255133d38805f1cac5f7ec214137f7327ce10cdc4b2062cd82feb154`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:11 GMT
ADD file:3c88cea17de40599dc8b8da90adc8439635066835e930f9573ec6cc856c5c096 in / 
# Fri, 09 Dec 2022 01:20:12 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 04:21:18 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 04:21:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 04:21:25 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 04:22:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 04:22:24 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:fb668870d8a72b5d72a3b6d98ee626e00f9f7c29c6f4f7d3a63673d747dbffe7`  
		Last Modified: Fri, 09 Dec 2022 01:21:25 GMT  
		Size: 26.7 MB (26711459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acae8945e830b26864e6f4dcccac1c0f41145f5792c80fa11241789b45ce0c0`  
		Last Modified: Fri, 09 Dec 2022 04:24:50 GMT  
		Size: 2.9 MB (2949577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb0aaff24d2e9d944fe20d8d7b841c223905eed0cad23da4932cdc722436b29`  
		Last Modified: Fri, 09 Dec 2022 04:24:59 GMT  
		Size: 129.3 MB (129322664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; 386

```console
$ docker pull ibmjava@sha256:d978d740ac7089e74cd101a2fba08a0cea544602b389666de103660a9dd01749
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147606546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01470d6cfe5eaaf9ae3e01c75a9fce78c93171476756f8c8678594f5f019807`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Jan 2023 18:00:42 GMT
ADD file:dc76519390168deb6f9bb6052d08c6e7840908a831276d99bb19c6c245f8517b in / 
# Mon, 02 Jan 2023 18:00:43 GMT
CMD ["bash"]
# Mon, 02 Jan 2023 18:16:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Mon, 02 Jan 2023 18:17:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Mon, 02 Jan 2023 18:17:02 GMT
ENV JAVA_VERSION=8.0.7.20
# Mon, 02 Jan 2023 18:17:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Mon, 02 Jan 2023 18:17:53 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1b284dbae22f155bfee2a25073c97c9758e66aa7129a455cb533d8e2cbc873f9`  
		Last Modified: Mon, 02 Jan 2023 18:01:17 GMT  
		Size: 27.2 MB (27165399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfed9768a70dc0ba56e7fd9969f79fa2ebac801784981b1c52ca8415df7ae55`  
		Last Modified: Mon, 02 Jan 2023 18:20:25 GMT  
		Size: 3.0 MB (2981625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27931503bf0f6eccf183f3a58a7e17d21e3a43b785cfe41e51c4a0bc43c766c9`  
		Last Modified: Mon, 02 Jan 2023 18:20:35 GMT  
		Size: 117.5 MB (117459522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:2417c6045e0c9c23a7da37faaf25f81265ad7fe3ff68309abb22a419cc69337c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162514573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476711c0b02342d898ae41f60ab4491fc0d6811dfb1ad53ddfef82b695143bf8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:27:15 GMT
ADD file:05ec256cb279f6d94111b2413d31c85c4e1ff1365bce34d2fc4aa2788885fa06 in / 
# Fri, 09 Dec 2022 01:27:17 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:02:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 03:02:46 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 03:02:47 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 03:05:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 03:05:19 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:29d5a8bf9800ea1d873fe104fc2b0b6d4efed1269ce0f9a80e4d65e96d3246e2`  
		Last Modified: Fri, 09 Dec 2022 01:29:45 GMT  
		Size: 30.4 MB (30442475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b911794ae1ce4902a6daaf989e919ecf0eec34798ddaf26f80408d03d5779c`  
		Last Modified: Fri, 09 Dec 2022 03:10:49 GMT  
		Size: 3.1 MB (3075733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103bba608e4bcf78845fbe100e090c5cbdd4d12ecd86a1d8aaab5fb5d5778837`  
		Last Modified: Fri, 09 Dec 2022 03:11:06 GMT  
		Size: 129.0 MB (128996365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:00f041bf4980f625ae0da5ada4eaa44da6eb6e78cff06ecc6bba7a3135d83698
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154511264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844157c990acd48fcba5a3da83890dab87aa7db830bfd80ee4165f6bb4b0b0f4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:52:21 GMT
ADD file:c2fcdae7883d865c232dfc26d514c111189f6940ba74273c78067624cd02c962 in / 
# Fri, 09 Dec 2022 01:52:24 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:15:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 03:16:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 03:16:12 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 03:17:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 03:17:19 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3fb013d46f2fda49d6c671f39f55c3330f927a4c55ae7e5096daf0a638dc38ec`  
		Last Modified: Fri, 09 Dec 2022 01:54:45 GMT  
		Size: 25.4 MB (25371298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49e7e6835b120e4486c693b4f03bdf01ba76a250b74306406b7bd9fbb2d737c`  
		Last Modified: Fri, 09 Dec 2022 03:20:23 GMT  
		Size: 2.7 MB (2667341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fdd86aa56415e723ad1c625e8e84de704bd93370cb5380694e05e888e84210`  
		Last Modified: Fri, 09 Dec 2022 03:20:31 GMT  
		Size: 126.5 MB (126472625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:latest`

```console
$ docker pull ibmjava@sha256:2a67f2f53268d284058e63cbbfe03689d1b076f777f13e89339141f95cf35fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:latest` - linux; amd64

```console
$ docker pull ibmjava@sha256:fd0d5341c971d0082f905f80cf5e470728540169aa3b2d00a941752a09482948
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158983700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff72f24255133d38805f1cac5f7ec214137f7327ce10cdc4b2062cd82feb154`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:11 GMT
ADD file:3c88cea17de40599dc8b8da90adc8439635066835e930f9573ec6cc856c5c096 in / 
# Fri, 09 Dec 2022 01:20:12 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 04:21:18 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 04:21:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 04:21:25 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 04:22:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 04:22:24 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:fb668870d8a72b5d72a3b6d98ee626e00f9f7c29c6f4f7d3a63673d747dbffe7`  
		Last Modified: Fri, 09 Dec 2022 01:21:25 GMT  
		Size: 26.7 MB (26711459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acae8945e830b26864e6f4dcccac1c0f41145f5792c80fa11241789b45ce0c0`  
		Last Modified: Fri, 09 Dec 2022 04:24:50 GMT  
		Size: 2.9 MB (2949577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb0aaff24d2e9d944fe20d8d7b841c223905eed0cad23da4932cdc722436b29`  
		Last Modified: Fri, 09 Dec 2022 04:24:59 GMT  
		Size: 129.3 MB (129322664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; 386

```console
$ docker pull ibmjava@sha256:d978d740ac7089e74cd101a2fba08a0cea544602b389666de103660a9dd01749
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147606546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01470d6cfe5eaaf9ae3e01c75a9fce78c93171476756f8c8678594f5f019807`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Jan 2023 18:00:42 GMT
ADD file:dc76519390168deb6f9bb6052d08c6e7840908a831276d99bb19c6c245f8517b in / 
# Mon, 02 Jan 2023 18:00:43 GMT
CMD ["bash"]
# Mon, 02 Jan 2023 18:16:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Mon, 02 Jan 2023 18:17:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Mon, 02 Jan 2023 18:17:02 GMT
ENV JAVA_VERSION=8.0.7.20
# Mon, 02 Jan 2023 18:17:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Mon, 02 Jan 2023 18:17:53 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1b284dbae22f155bfee2a25073c97c9758e66aa7129a455cb533d8e2cbc873f9`  
		Last Modified: Mon, 02 Jan 2023 18:01:17 GMT  
		Size: 27.2 MB (27165399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfed9768a70dc0ba56e7fd9969f79fa2ebac801784981b1c52ca8415df7ae55`  
		Last Modified: Mon, 02 Jan 2023 18:20:25 GMT  
		Size: 3.0 MB (2981625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27931503bf0f6eccf183f3a58a7e17d21e3a43b785cfe41e51c4a0bc43c766c9`  
		Last Modified: Mon, 02 Jan 2023 18:20:35 GMT  
		Size: 117.5 MB (117459522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:2417c6045e0c9c23a7da37faaf25f81265ad7fe3ff68309abb22a419cc69337c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162514573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476711c0b02342d898ae41f60ab4491fc0d6811dfb1ad53ddfef82b695143bf8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:27:15 GMT
ADD file:05ec256cb279f6d94111b2413d31c85c4e1ff1365bce34d2fc4aa2788885fa06 in / 
# Fri, 09 Dec 2022 01:27:17 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:02:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 03:02:46 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 03:02:47 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 03:05:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 03:05:19 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:29d5a8bf9800ea1d873fe104fc2b0b6d4efed1269ce0f9a80e4d65e96d3246e2`  
		Last Modified: Fri, 09 Dec 2022 01:29:45 GMT  
		Size: 30.4 MB (30442475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b911794ae1ce4902a6daaf989e919ecf0eec34798ddaf26f80408d03d5779c`  
		Last Modified: Fri, 09 Dec 2022 03:10:49 GMT  
		Size: 3.1 MB (3075733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103bba608e4bcf78845fbe100e090c5cbdd4d12ecd86a1d8aaab5fb5d5778837`  
		Last Modified: Fri, 09 Dec 2022 03:11:06 GMT  
		Size: 129.0 MB (128996365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; s390x

```console
$ docker pull ibmjava@sha256:00f041bf4980f625ae0da5ada4eaa44da6eb6e78cff06ecc6bba7a3135d83698
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154511264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844157c990acd48fcba5a3da83890dab87aa7db830bfd80ee4165f6bb4b0b0f4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:52:21 GMT
ADD file:c2fcdae7883d865c232dfc26d514c111189f6940ba74273c78067624cd02c962 in / 
# Fri, 09 Dec 2022 01:52:24 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:15:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 03:16:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 03:16:12 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 03:17:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4abf605bdffc703f48c506177ee874da9498a4ee5ef322bfb9b4170b097bf2a8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='225a8406e9a3134eb8674206caa131a7d5f528de96797a7a0cf69e292465d205';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='052efe7ee98f17af3f027c11b9ef57edd136bf9431b8264a790d48cce905fffd';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='47384a0933d2a60b0126eeb49c44be66124320f70355cd09a238a830906819ff';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='bea07ae6d8d56ad7ae2d4937bed352d39622d364be848a036b111fdf15e50cab';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 03:17:19 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3fb013d46f2fda49d6c671f39f55c3330f927a4c55ae7e5096daf0a638dc38ec`  
		Last Modified: Fri, 09 Dec 2022 01:54:45 GMT  
		Size: 25.4 MB (25371298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49e7e6835b120e4486c693b4f03bdf01ba76a250b74306406b7bd9fbb2d737c`  
		Last Modified: Fri, 09 Dec 2022 03:20:23 GMT  
		Size: 2.7 MB (2667341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fdd86aa56415e723ad1c625e8e84de704bd93370cb5380694e05e888e84210`  
		Last Modified: Fri, 09 Dec 2022 03:20:31 GMT  
		Size: 126.5 MB (126472625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:825bc6b1d083e59b05f07d26b0469c705eed06a870877972c8e4970f6170b203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:a956390b9139dac86da07a303411516fcb13a8db167c2638a14d448616c34b64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 MB (196135637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4d7186a6ea718b9cff7837b560b6b75dbe2a679b1b16b39ff3142f2e3bd29e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:11 GMT
ADD file:3c88cea17de40599dc8b8da90adc8439635066835e930f9573ec6cc856c5c096 in / 
# Fri, 09 Dec 2022 01:20:12 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 04:21:18 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 04:21:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 04:21:25 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 04:24:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0f6aef4c3550a8f85288da8bc6fada405b0ce2226d6b1b57d0aae98cd5eef5e4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='fa7661c2eb2982c4fb85c6894e7a975970b27b6ee82d5facb352f075cc1dfca3';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a56803671fe7d1c85f18d566dbcb7fbaf1d60c6f1d6de34e35a257e0c8095f9b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='71c913a1eed7daae952657e18eb9a2e71723106b6e7b56373f18564db77f551e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='c8641bc22443ebccaedf1822a12ec1303d89577d45c875702e1f628066c7f383';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 04:24:25 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:fb668870d8a72b5d72a3b6d98ee626e00f9f7c29c6f4f7d3a63673d747dbffe7`  
		Last Modified: Fri, 09 Dec 2022 01:21:25 GMT  
		Size: 26.7 MB (26711459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acae8945e830b26864e6f4dcccac1c0f41145f5792c80fa11241789b45ce0c0`  
		Last Modified: Fri, 09 Dec 2022 04:24:50 GMT  
		Size: 2.9 MB (2949577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02a1910973efec527f161388117cc460c6cf2d683e973a410ccbdea2cb220d6`  
		Last Modified: Fri, 09 Dec 2022 04:25:37 GMT  
		Size: 166.5 MB (166474601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; 386

```console
$ docker pull ibmjava@sha256:ec3c1234489b541cb77c46caa537e1c83712f6d6a42cefcfcbaa947ae1a6c047
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184641462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d086184a012ce6dc984c9aeb8a36013b00165ea97c3ffe0c29f65a34674aaf1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Jan 2023 18:00:42 GMT
ADD file:dc76519390168deb6f9bb6052d08c6e7840908a831276d99bb19c6c245f8517b in / 
# Mon, 02 Jan 2023 18:00:43 GMT
CMD ["bash"]
# Mon, 02 Jan 2023 18:16:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Mon, 02 Jan 2023 18:17:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Mon, 02 Jan 2023 18:17:02 GMT
ENV JAVA_VERSION=8.0.7.20
# Mon, 02 Jan 2023 18:19:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0f6aef4c3550a8f85288da8bc6fada405b0ce2226d6b1b57d0aae98cd5eef5e4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='fa7661c2eb2982c4fb85c6894e7a975970b27b6ee82d5facb352f075cc1dfca3';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a56803671fe7d1c85f18d566dbcb7fbaf1d60c6f1d6de34e35a257e0c8095f9b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='71c913a1eed7daae952657e18eb9a2e71723106b6e7b56373f18564db77f551e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='c8641bc22443ebccaedf1822a12ec1303d89577d45c875702e1f628066c7f383';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Mon, 02 Jan 2023 18:19:54 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1b284dbae22f155bfee2a25073c97c9758e66aa7129a455cb533d8e2cbc873f9`  
		Last Modified: Mon, 02 Jan 2023 18:01:17 GMT  
		Size: 27.2 MB (27165399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfed9768a70dc0ba56e7fd9969f79fa2ebac801784981b1c52ca8415df7ae55`  
		Last Modified: Mon, 02 Jan 2023 18:20:25 GMT  
		Size: 3.0 MB (2981625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2faac65d385f880ffda561872b05603633ac3eddd661fa6e9bd2a118642dbf61`  
		Last Modified: Mon, 02 Jan 2023 18:21:23 GMT  
		Size: 154.5 MB (154494438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:e263255780b671733d97402967d06b7e68dfa164434d4ac359d3b798c56f563f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.8 MB (199790229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd421c38a1ffbb340561f27c684606bfbdd33ce423d4342546cc52bd8f8ba5d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:27:15 GMT
ADD file:05ec256cb279f6d94111b2413d31c85c4e1ff1365bce34d2fc4aa2788885fa06 in / 
# Fri, 09 Dec 2022 01:27:17 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:02:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 03:02:46 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 03:02:47 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 03:10:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0f6aef4c3550a8f85288da8bc6fada405b0ce2226d6b1b57d0aae98cd5eef5e4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='fa7661c2eb2982c4fb85c6894e7a975970b27b6ee82d5facb352f075cc1dfca3';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a56803671fe7d1c85f18d566dbcb7fbaf1d60c6f1d6de34e35a257e0c8095f9b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='71c913a1eed7daae952657e18eb9a2e71723106b6e7b56373f18564db77f551e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='c8641bc22443ebccaedf1822a12ec1303d89577d45c875702e1f628066c7f383';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 03:10:15 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:29d5a8bf9800ea1d873fe104fc2b0b6d4efed1269ce0f9a80e4d65e96d3246e2`  
		Last Modified: Fri, 09 Dec 2022 01:29:45 GMT  
		Size: 30.4 MB (30442475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b911794ae1ce4902a6daaf989e919ecf0eec34798ddaf26f80408d03d5779c`  
		Last Modified: Fri, 09 Dec 2022 03:10:49 GMT  
		Size: 3.1 MB (3075733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d2c61b0c40100d38a276fbbb60c6af43afd4db814d5513a69ad6f5bbcf6eb8`  
		Last Modified: Fri, 09 Dec 2022 03:12:10 GMT  
		Size: 166.3 MB (166272021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:8b537094cf6e76ab6780f09a71760cb25113ae3ee677f51a3cfd0ce1afbaa3f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184803052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b021945b39e0bb4aacfe7daa2c1829c207148ecf3a7fbf2cdc2b6a08d49bfb4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:52:21 GMT
ADD file:c2fcdae7883d865c232dfc26d514c111189f6940ba74273c78067624cd02c962 in / 
# Fri, 09 Dec 2022 01:52:24 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:15:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 03:16:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 03:16:12 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 03:19:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0f6aef4c3550a8f85288da8bc6fada405b0ce2226d6b1b57d0aae98cd5eef5e4';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='fa7661c2eb2982c4fb85c6894e7a975970b27b6ee82d5facb352f075cc1dfca3';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='a56803671fe7d1c85f18d566dbcb7fbaf1d60c6f1d6de34e35a257e0c8095f9b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='71c913a1eed7daae952657e18eb9a2e71723106b6e7b56373f18564db77f551e';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='c8641bc22443ebccaedf1822a12ec1303d89577d45c875702e1f628066c7f383';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 03:19:44 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3fb013d46f2fda49d6c671f39f55c3330f927a4c55ae7e5096daf0a638dc38ec`  
		Last Modified: Fri, 09 Dec 2022 01:54:45 GMT  
		Size: 25.4 MB (25371298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49e7e6835b120e4486c693b4f03bdf01ba76a250b74306406b7bd9fbb2d737c`  
		Last Modified: Fri, 09 Dec 2022 03:20:23 GMT  
		Size: 2.7 MB (2667341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b679b381ca767b8d80570c694f49d474020767caaac607fee5fab8f04403f2`  
		Last Modified: Fri, 09 Dec 2022 03:21:04 GMT  
		Size: 156.8 MB (156764413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:8370d4445c3a413239d8875b62d56cf744e3f50474836b0bd17715f8df090cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:93febaf81c4d9f76e1f885ba42c7da63bd5f00d1b41067dbeff1d472f4af5a6c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94669896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86512e789ad970c3957c44851442c02d3f81e8449d2ddec84992e25979d1f332`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:11 GMT
ADD file:3c88cea17de40599dc8b8da90adc8439635066835e930f9573ec6cc856c5c096 in / 
# Fri, 09 Dec 2022 01:20:12 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 04:21:18 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 04:21:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 04:21:25 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 04:23:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bb548976980c436b15e59e0db7b4e99a7ed273df39e17db60047f950c2863c1b';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='768e6f8df5c9735d703f2dd5352b7c063949d59c6e15bc7d5c31d7ac667a241a';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='1ce92e9c420b2d081c8cd63c8441b324e49348360490d61e08a0908b830748cb';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e790dc7707417153227e1f3164db1c699e3b6b9f697d9e1c9c9142bc0e3d3409';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='bfac3d6409a7996301d948faedfd4c19920dbb667ba699b7fd4719188366be8b';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 04:23:06 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:fb668870d8a72b5d72a3b6d98ee626e00f9f7c29c6f4f7d3a63673d747dbffe7`  
		Last Modified: Fri, 09 Dec 2022 01:21:25 GMT  
		Size: 26.7 MB (26711459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8acae8945e830b26864e6f4dcccac1c0f41145f5792c80fa11241789b45ce0c0`  
		Last Modified: Fri, 09 Dec 2022 04:24:50 GMT  
		Size: 2.9 MB (2949577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418a294084d28a15701eab94ddac7b9b23dd9b9a965071887f43fbbb6d60c08b`  
		Last Modified: Fri, 09 Dec 2022 04:25:17 GMT  
		Size: 65.0 MB (65008860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; 386

```console
$ docker pull ibmjava@sha256:358a43ad8b9ac09544689fdc444d1bdf13a3287c54b9b530efd11c13376bf2bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94532127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b44bdfb616f53825307df86b887023a7ddf27e4f7157035e917597294465868e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Jan 2023 18:00:42 GMT
ADD file:dc76519390168deb6f9bb6052d08c6e7840908a831276d99bb19c6c245f8517b in / 
# Mon, 02 Jan 2023 18:00:43 GMT
CMD ["bash"]
# Mon, 02 Jan 2023 18:16:43 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Mon, 02 Jan 2023 18:17:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Mon, 02 Jan 2023 18:17:02 GMT
ENV JAVA_VERSION=8.0.7.20
# Mon, 02 Jan 2023 18:18:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bb548976980c436b15e59e0db7b4e99a7ed273df39e17db60047f950c2863c1b';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='768e6f8df5c9735d703f2dd5352b7c063949d59c6e15bc7d5c31d7ac667a241a';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='1ce92e9c420b2d081c8cd63c8441b324e49348360490d61e08a0908b830748cb';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e790dc7707417153227e1f3164db1c699e3b6b9f697d9e1c9c9142bc0e3d3409';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='bfac3d6409a7996301d948faedfd4c19920dbb667ba699b7fd4719188366be8b';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Mon, 02 Jan 2023 18:18:47 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1b284dbae22f155bfee2a25073c97c9758e66aa7129a455cb533d8e2cbc873f9`  
		Last Modified: Mon, 02 Jan 2023 18:01:17 GMT  
		Size: 27.2 MB (27165399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfed9768a70dc0ba56e7fd9969f79fa2ebac801784981b1c52ca8415df7ae55`  
		Last Modified: Mon, 02 Jan 2023 18:20:25 GMT  
		Size: 3.0 MB (2981625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97229bb82bc2a976df402be61e6622e55770c6ba9cf87bd06e661244bc3efc18`  
		Last Modified: Mon, 02 Jan 2023 18:21:02 GMT  
		Size: 64.4 MB (64385103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:510b44231e8c7dbd823a6352445fcdd82450b642e95e308f6d1f58fd2900fe2f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98807917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b92620008306b672c3411bc4acda1625ccd5e11316b97e694b202cd7d27cbe92`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:27:15 GMT
ADD file:05ec256cb279f6d94111b2413d31c85c4e1ff1365bce34d2fc4aa2788885fa06 in / 
# Fri, 09 Dec 2022 01:27:17 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:02:12 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 03:02:46 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 03:02:47 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 03:07:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bb548976980c436b15e59e0db7b4e99a7ed273df39e17db60047f950c2863c1b';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='768e6f8df5c9735d703f2dd5352b7c063949d59c6e15bc7d5c31d7ac667a241a';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='1ce92e9c420b2d081c8cd63c8441b324e49348360490d61e08a0908b830748cb';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e790dc7707417153227e1f3164db1c699e3b6b9f697d9e1c9c9142bc0e3d3409';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='bfac3d6409a7996301d948faedfd4c19920dbb667ba699b7fd4719188366be8b';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 03:07:09 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:29d5a8bf9800ea1d873fe104fc2b0b6d4efed1269ce0f9a80e4d65e96d3246e2`  
		Last Modified: Fri, 09 Dec 2022 01:29:45 GMT  
		Size: 30.4 MB (30442475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b911794ae1ce4902a6daaf989e919ecf0eec34798ddaf26f80408d03d5779c`  
		Last Modified: Fri, 09 Dec 2022 03:10:49 GMT  
		Size: 3.1 MB (3075733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6483ca4de227708018f79d4040e212e4afbf3a2960d20405e990569c6a62163`  
		Last Modified: Fri, 09 Dec 2022 03:11:38 GMT  
		Size: 65.3 MB (65289709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:5a1ceedf454081b9b5b04f6e129a05bc940ceb8afa9a9d81de7459698e08ff2a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94161761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9fe6165d115618482c50a742d945885d73ac35bedd8106e940e62dfde10dae`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:52:21 GMT
ADD file:c2fcdae7883d865c232dfc26d514c111189f6940ba74273c78067624cd02c962 in / 
# Fri, 09 Dec 2022 01:52:24 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:15:50 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 03:16:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 03:16:12 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 03:18:11 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bb548976980c436b15e59e0db7b4e99a7ed273df39e17db60047f950c2863c1b';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='768e6f8df5c9735d703f2dd5352b7c063949d59c6e15bc7d5c31d7ac667a241a';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='1ce92e9c420b2d081c8cd63c8441b324e49348360490d61e08a0908b830748cb';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e790dc7707417153227e1f3164db1c699e3b6b9f697d9e1c9c9142bc0e3d3409';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='bfac3d6409a7996301d948faedfd4c19920dbb667ba699b7fd4719188366be8b';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 03:18:14 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3fb013d46f2fda49d6c671f39f55c3330f927a4c55ae7e5096daf0a638dc38ec`  
		Last Modified: Fri, 09 Dec 2022 01:54:45 GMT  
		Size: 25.4 MB (25371298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49e7e6835b120e4486c693b4f03bdf01ba76a250b74306406b7bd9fbb2d737c`  
		Last Modified: Fri, 09 Dec 2022 03:20:23 GMT  
		Size: 2.7 MB (2667341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0cd8775a84894340cf7748f3238f0279db045c4e1d15c1256b87823a27951ad`  
		Last Modified: Fri, 09 Dec 2022 03:20:47 GMT  
		Size: 66.1 MB (66123122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

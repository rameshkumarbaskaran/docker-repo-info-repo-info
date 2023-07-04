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
$ docker pull ibmjava@sha256:f8f5a1e37868bb7516b86dcd506c0845fc4258f6e8a1dbe99889c7abc7535a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8` - linux; amd64

```console
$ docker pull ibmjava@sha256:b7da5671b83927331ab96a51daed1f4e279d32fe7c6b55dae603c9cf3a53fba6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (165995845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314e2dd39b80f7270acce9e70c948de5a2caf27f2b414e94ea4134c14da40461`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:57:15 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 16 Jun 2023 02:57:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 30 Jun 2023 23:23:48 GMT
ENV JAVA_VERSION=8.0.8.6
# Fri, 30 Jun 2023 23:24:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='2f173ec848303a99bcd38b0c13b1ddb2a70bb4ba9fa0e4ec5bd99268ff9987f8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc637ac2d65386079932d06a303c244daa39282e514ba376cdb7fd0128cd05a5';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e510a98c183248a9ebbec0093958c5fc2f1dc126c792878e0bc739b44eaad7cd';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='7bd82044da06a852d373c20bac462cc60bc85355ca57c850b9d5b513c7b93768';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 30 Jun 2023 23:24:48 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1aab967c9f4d601afc5e8b2023fa6a57cdb9f402102cbf9e941ffab60ec77b`  
		Last Modified: Fri, 16 Jun 2023 03:01:13 GMT  
		Size: 1.5 MB (1469042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4750ed8e2dee55c4ac7a03aed8efbf7e67419a502935599be8e5cf3ac67a427`  
		Last Modified: Fri, 30 Jun 2023 23:27:28 GMT  
		Size: 134.1 MB (134095764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:74dc42e03ea89dec60b00edb541588051efdd3f7cba4c075b20e483cce50c375
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171079912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795826c779222aa7fcb003db5523fcb1d1202da09acd89bacabca76cf73f8681`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:01:00 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:01:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:01:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:01:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:01:03 GMT
ADD file:00c4f44b35b683caef54d5b8b0e0b1e68872f45eae17dd7543adaf6c54512447 in / 
# Mon, 05 Jun 2023 17:01:04 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 01:32:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 16 Jun 2023 01:32:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 30 Jun 2023 23:34:08 GMT
ENV JAVA_VERSION=8.0.8.6
# Fri, 30 Jun 2023 23:36:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='2f173ec848303a99bcd38b0c13b1ddb2a70bb4ba9fa0e4ec5bd99268ff9987f8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc637ac2d65386079932d06a303c244daa39282e514ba376cdb7fd0128cd05a5';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e510a98c183248a9ebbec0093958c5fc2f1dc126c792878e0bc739b44eaad7cd';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='7bd82044da06a852d373c20bac462cc60bc85355ca57c850b9d5b513c7b93768';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 30 Jun 2023 23:36:35 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a02dd69d9a8a1e6f4fc2ccb509fb8efd6014b00ff932a757d23b4b012a2bec49`  
		Last Modified: Fri, 16 Jun 2023 00:44:52 GMT  
		Size: 35.7 MB (35711397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3831c1123275dd4d9043ad21bf2c9fb47b24b3ab61e99547e14106df60427380`  
		Last Modified: Fri, 16 Jun 2023 01:40:42 GMT  
		Size: 1.6 MB (1576481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2610129c267e9b676ec5feea35705fa96c12357775402d5f3f9222cd4e2f57f9`  
		Last Modified: Fri, 30 Jun 2023 23:42:53 GMT  
		Size: 133.8 MB (133792034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; s390x

```console
$ docker pull ibmjava@sha256:1ccc6c3a38bd38688a67ebe26e1e23a6f4af4a68f53681733c50f297e679b407
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160775676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00bb31a6736243cbb938a41bbd123587761628a6dd8263709cb31d393353e44`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:53:20 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:53:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:53:22 GMT
ADD file:fa0aef35be7808c8fd6751a52bdec4dd81057e2fcaa075c547a1db53640dae9a in / 
# Wed, 28 Jun 2023 08:53:22 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 16:51:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 04 Jul 2023 16:51:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 16:51:20 GMT
ENV JAVA_VERSION=8.0.8.6
# Tue, 04 Jul 2023 16:52:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='2f173ec848303a99bcd38b0c13b1ddb2a70bb4ba9fa0e4ec5bd99268ff9987f8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc637ac2d65386079932d06a303c244daa39282e514ba376cdb7fd0128cd05a5';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e510a98c183248a9ebbec0093958c5fc2f1dc126c792878e0bc739b44eaad7cd';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='7bd82044da06a852d373c20bac462cc60bc85355ca57c850b9d5b513c7b93768';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 04 Jul 2023 16:52:11 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:ce02ee0330980398d6a84a50abfa1a8c4d1cba27cbd7442b79f4aa1b1a14020d`  
		Last Modified: Tue, 04 Jul 2023 13:08:30 GMT  
		Size: 28.6 MB (28645696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bb008d160279336a7f69b2e2efa53fc36a1f7792039d4a7750f65556eb55fe`  
		Last Modified: Tue, 04 Jul 2023 16:54:25 GMT  
		Size: 1.5 MB (1477144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206261a99bf0b13e99750c033e68dcca3d6f76bafbf3f889ca8a88d31bd05e0b`  
		Last Modified: Tue, 04 Jul 2023 16:54:34 GMT  
		Size: 130.7 MB (130652836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:f8f5a1e37868bb7516b86dcd506c0845fc4258f6e8a1dbe99889c7abc7535a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:b7da5671b83927331ab96a51daed1f4e279d32fe7c6b55dae603c9cf3a53fba6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (165995845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314e2dd39b80f7270acce9e70c948de5a2caf27f2b414e94ea4134c14da40461`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:57:15 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 16 Jun 2023 02:57:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 30 Jun 2023 23:23:48 GMT
ENV JAVA_VERSION=8.0.8.6
# Fri, 30 Jun 2023 23:24:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='2f173ec848303a99bcd38b0c13b1ddb2a70bb4ba9fa0e4ec5bd99268ff9987f8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc637ac2d65386079932d06a303c244daa39282e514ba376cdb7fd0128cd05a5';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e510a98c183248a9ebbec0093958c5fc2f1dc126c792878e0bc739b44eaad7cd';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='7bd82044da06a852d373c20bac462cc60bc85355ca57c850b9d5b513c7b93768';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 30 Jun 2023 23:24:48 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1aab967c9f4d601afc5e8b2023fa6a57cdb9f402102cbf9e941ffab60ec77b`  
		Last Modified: Fri, 16 Jun 2023 03:01:13 GMT  
		Size: 1.5 MB (1469042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4750ed8e2dee55c4ac7a03aed8efbf7e67419a502935599be8e5cf3ac67a427`  
		Last Modified: Fri, 30 Jun 2023 23:27:28 GMT  
		Size: 134.1 MB (134095764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:74dc42e03ea89dec60b00edb541588051efdd3f7cba4c075b20e483cce50c375
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171079912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795826c779222aa7fcb003db5523fcb1d1202da09acd89bacabca76cf73f8681`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:01:00 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:01:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:01:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:01:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:01:03 GMT
ADD file:00c4f44b35b683caef54d5b8b0e0b1e68872f45eae17dd7543adaf6c54512447 in / 
# Mon, 05 Jun 2023 17:01:04 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 01:32:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 16 Jun 2023 01:32:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 30 Jun 2023 23:34:08 GMT
ENV JAVA_VERSION=8.0.8.6
# Fri, 30 Jun 2023 23:36:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='2f173ec848303a99bcd38b0c13b1ddb2a70bb4ba9fa0e4ec5bd99268ff9987f8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc637ac2d65386079932d06a303c244daa39282e514ba376cdb7fd0128cd05a5';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e510a98c183248a9ebbec0093958c5fc2f1dc126c792878e0bc739b44eaad7cd';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='7bd82044da06a852d373c20bac462cc60bc85355ca57c850b9d5b513c7b93768';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 30 Jun 2023 23:36:35 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a02dd69d9a8a1e6f4fc2ccb509fb8efd6014b00ff932a757d23b4b012a2bec49`  
		Last Modified: Fri, 16 Jun 2023 00:44:52 GMT  
		Size: 35.7 MB (35711397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3831c1123275dd4d9043ad21bf2c9fb47b24b3ab61e99547e14106df60427380`  
		Last Modified: Fri, 16 Jun 2023 01:40:42 GMT  
		Size: 1.6 MB (1576481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2610129c267e9b676ec5feea35705fa96c12357775402d5f3f9222cd4e2f57f9`  
		Last Modified: Fri, 30 Jun 2023 23:42:53 GMT  
		Size: 133.8 MB (133792034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:1ccc6c3a38bd38688a67ebe26e1e23a6f4af4a68f53681733c50f297e679b407
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160775676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00bb31a6736243cbb938a41bbd123587761628a6dd8263709cb31d393353e44`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:53:20 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:53:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:53:22 GMT
ADD file:fa0aef35be7808c8fd6751a52bdec4dd81057e2fcaa075c547a1db53640dae9a in / 
# Wed, 28 Jun 2023 08:53:22 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 16:51:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 04 Jul 2023 16:51:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 16:51:20 GMT
ENV JAVA_VERSION=8.0.8.6
# Tue, 04 Jul 2023 16:52:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='2f173ec848303a99bcd38b0c13b1ddb2a70bb4ba9fa0e4ec5bd99268ff9987f8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc637ac2d65386079932d06a303c244daa39282e514ba376cdb7fd0128cd05a5';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e510a98c183248a9ebbec0093958c5fc2f1dc126c792878e0bc739b44eaad7cd';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='7bd82044da06a852d373c20bac462cc60bc85355ca57c850b9d5b513c7b93768';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 04 Jul 2023 16:52:11 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:ce02ee0330980398d6a84a50abfa1a8c4d1cba27cbd7442b79f4aa1b1a14020d`  
		Last Modified: Tue, 04 Jul 2023 13:08:30 GMT  
		Size: 28.6 MB (28645696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bb008d160279336a7f69b2e2efa53fc36a1f7792039d4a7750f65556eb55fe`  
		Last Modified: Tue, 04 Jul 2023 16:54:25 GMT  
		Size: 1.5 MB (1477144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206261a99bf0b13e99750c033e68dcca3d6f76bafbf3f889ca8a88d31bd05e0b`  
		Last Modified: Tue, 04 Jul 2023 16:54:34 GMT  
		Size: 130.7 MB (130652836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:8ba02ac3a74d66c87fdfc68c37420a47ccb5ebf41976aab5ca08ec3d48a4e09c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:2df6f827f0cfceaec03e9cf8c73ee8d017539007c8cee30ac2f2756164c43c4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.1 MB (203149346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834035c2e83034222a843392ebbac922610690bcfe95e58f20830155ad242f7f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:57:15 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 16 Jun 2023 02:57:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 30 Jun 2023 23:23:48 GMT
ENV JAVA_VERSION=8.0.8.6
# Fri, 30 Jun 2023 23:26:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bd95ba315fa0752be3a18fd67c0dbda568313484f21420999766bc46c9af9191';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e159747a1fe64a03a24994887c8e4ab3aea06072f3a2ed99c3db31cec0c224de';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='7385da0c5ffde5b81f4830b95aa352db2a89b8380ccef25dcd77fdf5b0af3488';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='096edb7671f217d64ec9a6cf44b4d0e7f56184da1aa32e8d84eebe36c02c80d9';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 30 Jun 2023 23:26:58 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1aab967c9f4d601afc5e8b2023fa6a57cdb9f402102cbf9e941ffab60ec77b`  
		Last Modified: Fri, 16 Jun 2023 03:01:13 GMT  
		Size: 1.5 MB (1469042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3d721224099caff5dc158dbda3b69a0cbd9ba8ee0a5e406a8072f156dcce2d`  
		Last Modified: Fri, 30 Jun 2023 23:28:05 GMT  
		Size: 171.2 MB (171249265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:7748905c8e09c074f91b905db8a2887eea85954dc5c3befd79ae3f5312c42423
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.4 MB (208357736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e1b8ca0a9ddcaf0dc255e86adeb28a44405645bab8d4177eeae534efeacdd48`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:01:00 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:01:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:01:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:01:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:01:03 GMT
ADD file:00c4f44b35b683caef54d5b8b0e0b1e68872f45eae17dd7543adaf6c54512447 in / 
# Mon, 05 Jun 2023 17:01:04 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 01:32:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 16 Jun 2023 01:32:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 30 Jun 2023 23:34:08 GMT
ENV JAVA_VERSION=8.0.8.6
# Fri, 30 Jun 2023 23:42:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bd95ba315fa0752be3a18fd67c0dbda568313484f21420999766bc46c9af9191';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e159747a1fe64a03a24994887c8e4ab3aea06072f3a2ed99c3db31cec0c224de';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='7385da0c5ffde5b81f4830b95aa352db2a89b8380ccef25dcd77fdf5b0af3488';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='096edb7671f217d64ec9a6cf44b4d0e7f56184da1aa32e8d84eebe36c02c80d9';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 30 Jun 2023 23:42:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a02dd69d9a8a1e6f4fc2ccb509fb8efd6014b00ff932a757d23b4b012a2bec49`  
		Last Modified: Fri, 16 Jun 2023 00:44:52 GMT  
		Size: 35.7 MB (35711397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3831c1123275dd4d9043ad21bf2c9fb47b24b3ab61e99547e14106df60427380`  
		Last Modified: Fri, 16 Jun 2023 01:40:42 GMT  
		Size: 1.6 MB (1576481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188381b7aa74564ab295f4dd1a086683de39bb4d01038eebbd6818718b35c366`  
		Last Modified: Fri, 30 Jun 2023 23:43:51 GMT  
		Size: 171.1 MB (171069858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:b39f279112de98495d7f50eb628fc55312a612e262abe70e5f26d6dccd40bffb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191049154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c04147d478dacab93d2b427339df62bd556d0142da493aad64f80274abffcb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:53:20 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:53:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:53:22 GMT
ADD file:fa0aef35be7808c8fd6751a52bdec4dd81057e2fcaa075c547a1db53640dae9a in / 
# Wed, 28 Jun 2023 08:53:22 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 16:51:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 04 Jul 2023 16:51:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 16:51:20 GMT
ENV JAVA_VERSION=8.0.8.6
# Tue, 04 Jul 2023 16:54:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bd95ba315fa0752be3a18fd67c0dbda568313484f21420999766bc46c9af9191';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e159747a1fe64a03a24994887c8e4ab3aea06072f3a2ed99c3db31cec0c224de';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='7385da0c5ffde5b81f4830b95aa352db2a89b8380ccef25dcd77fdf5b0af3488';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='096edb7671f217d64ec9a6cf44b4d0e7f56184da1aa32e8d84eebe36c02c80d9';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 04 Jul 2023 16:54:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:ce02ee0330980398d6a84a50abfa1a8c4d1cba27cbd7442b79f4aa1b1a14020d`  
		Last Modified: Tue, 04 Jul 2023 13:08:30 GMT  
		Size: 28.6 MB (28645696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bb008d160279336a7f69b2e2efa53fc36a1f7792039d4a7750f65556eb55fe`  
		Last Modified: Tue, 04 Jul 2023 16:54:25 GMT  
		Size: 1.5 MB (1477144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe65be5a37cf879c019f55cf099ea231fdcf2302e8b6e79df9816d4798b1b04`  
		Last Modified: Tue, 04 Jul 2023 16:55:03 GMT  
		Size: 160.9 MB (160926314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:d207860a549402285fa7621766cb1a7b1aac7ec1d15b9c937fc83b2c6732f469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:4bbe6af9cb3a4775563b5fa63f502139f7691ac955ce648391da25b70244545d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101246913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de662ecabc02b88c7bf409f56d58de000d095da4cb4a8f5adcca9d1780598b21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:57:15 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 16 Jun 2023 02:57:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 30 Jun 2023 23:23:48 GMT
ENV JAVA_VERSION=8.0.8.6
# Fri, 30 Jun 2023 23:25:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='d795b429c31b76e28e96848ad66a2749314c498a2c744f41d1fa7bf032ccc495';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='75f234bd86768a7cd4aa0cf6b62f88f62f79a9d0455c3e49adf97cf363391170';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='3d2eceb6ff09b2663c312f0c11955372198cfd85dc693c4188875300aefae6ac';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='9e7f8f163eddd1d8c7781a11bc7e6a2d428063ac1d3054184227b172d95cef56';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 30 Jun 2023 23:25:39 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1aab967c9f4d601afc5e8b2023fa6a57cdb9f402102cbf9e941ffab60ec77b`  
		Last Modified: Fri, 16 Jun 2023 03:01:13 GMT  
		Size: 1.5 MB (1469042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba237cb7136dfa378f67671e23669e72053a5ef6ad375b959b271fb0619e5b3d`  
		Last Modified: Fri, 30 Jun 2023 23:27:46 GMT  
		Size: 69.3 MB (69346832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:1650a28505dc676d98f3bbbc58096134e9011c575352f69721c05fdec6af0c6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 MB (106974195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1924097623bf77029aecaa58d84153e693da57e69f27d7ef976bdc2b532dfc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:01:00 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:01:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:01:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:01:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:01:03 GMT
ADD file:00c4f44b35b683caef54d5b8b0e0b1e68872f45eae17dd7543adaf6c54512447 in / 
# Mon, 05 Jun 2023 17:01:04 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 01:32:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 16 Jun 2023 01:32:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 30 Jun 2023 23:34:08 GMT
ENV JAVA_VERSION=8.0.8.6
# Fri, 30 Jun 2023 23:38:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='d795b429c31b76e28e96848ad66a2749314c498a2c744f41d1fa7bf032ccc495';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='75f234bd86768a7cd4aa0cf6b62f88f62f79a9d0455c3e49adf97cf363391170';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='3d2eceb6ff09b2663c312f0c11955372198cfd85dc693c4188875300aefae6ac';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='9e7f8f163eddd1d8c7781a11bc7e6a2d428063ac1d3054184227b172d95cef56';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 30 Jun 2023 23:38:37 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a02dd69d9a8a1e6f4fc2ccb509fb8efd6014b00ff932a757d23b4b012a2bec49`  
		Last Modified: Fri, 16 Jun 2023 00:44:52 GMT  
		Size: 35.7 MB (35711397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3831c1123275dd4d9043ad21bf2c9fb47b24b3ab61e99547e14106df60427380`  
		Last Modified: Fri, 16 Jun 2023 01:40:42 GMT  
		Size: 1.6 MB (1576481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2d3c7a08e2e1bc10b40660ee85f5bfba8b45b54e0cdb2eb9f964db81f9dc63`  
		Last Modified: Fri, 30 Jun 2023 23:43:20 GMT  
		Size: 69.7 MB (69686317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:51d45c48d161b24b810410b3d10a1c5f0293282bacf266a47ee7e8c65061ec1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.0 MB (100042164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10e8a80e88c3c3542c8b59b6d6041874fe560481e4a53cd1a01fd2c630a2b2e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:53:20 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:53:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:53:22 GMT
ADD file:fa0aef35be7808c8fd6751a52bdec4dd81057e2fcaa075c547a1db53640dae9a in / 
# Wed, 28 Jun 2023 08:53:22 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 16:51:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 04 Jul 2023 16:51:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 16:51:20 GMT
ENV JAVA_VERSION=8.0.8.6
# Tue, 04 Jul 2023 16:52:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='d795b429c31b76e28e96848ad66a2749314c498a2c744f41d1fa7bf032ccc495';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='75f234bd86768a7cd4aa0cf6b62f88f62f79a9d0455c3e49adf97cf363391170';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='3d2eceb6ff09b2663c312f0c11955372198cfd85dc693c4188875300aefae6ac';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='9e7f8f163eddd1d8c7781a11bc7e6a2d428063ac1d3054184227b172d95cef56';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 04 Jul 2023 16:53:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:ce02ee0330980398d6a84a50abfa1a8c4d1cba27cbd7442b79f4aa1b1a14020d`  
		Last Modified: Tue, 04 Jul 2023 13:08:30 GMT  
		Size: 28.6 MB (28645696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bb008d160279336a7f69b2e2efa53fc36a1f7792039d4a7750f65556eb55fe`  
		Last Modified: Tue, 04 Jul 2023 16:54:25 GMT  
		Size: 1.5 MB (1477144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2752454753d34dd000abeba297879893b8cfca05dbd96759a7c65e6e9b80a8b9`  
		Last Modified: Tue, 04 Jul 2023 16:54:47 GMT  
		Size: 69.9 MB (69919324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:f8f5a1e37868bb7516b86dcd506c0845fc4258f6e8a1dbe99889c7abc7535a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:b7da5671b83927331ab96a51daed1f4e279d32fe7c6b55dae603c9cf3a53fba6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (165995845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314e2dd39b80f7270acce9e70c948de5a2caf27f2b414e94ea4134c14da40461`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:57:15 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 16 Jun 2023 02:57:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 30 Jun 2023 23:23:48 GMT
ENV JAVA_VERSION=8.0.8.6
# Fri, 30 Jun 2023 23:24:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='2f173ec848303a99bcd38b0c13b1ddb2a70bb4ba9fa0e4ec5bd99268ff9987f8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc637ac2d65386079932d06a303c244daa39282e514ba376cdb7fd0128cd05a5';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e510a98c183248a9ebbec0093958c5fc2f1dc126c792878e0bc739b44eaad7cd';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='7bd82044da06a852d373c20bac462cc60bc85355ca57c850b9d5b513c7b93768';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 30 Jun 2023 23:24:48 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1aab967c9f4d601afc5e8b2023fa6a57cdb9f402102cbf9e941ffab60ec77b`  
		Last Modified: Fri, 16 Jun 2023 03:01:13 GMT  
		Size: 1.5 MB (1469042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4750ed8e2dee55c4ac7a03aed8efbf7e67419a502935599be8e5cf3ac67a427`  
		Last Modified: Fri, 30 Jun 2023 23:27:28 GMT  
		Size: 134.1 MB (134095764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:74dc42e03ea89dec60b00edb541588051efdd3f7cba4c075b20e483cce50c375
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171079912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795826c779222aa7fcb003db5523fcb1d1202da09acd89bacabca76cf73f8681`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:01:00 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:01:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:01:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:01:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:01:03 GMT
ADD file:00c4f44b35b683caef54d5b8b0e0b1e68872f45eae17dd7543adaf6c54512447 in / 
# Mon, 05 Jun 2023 17:01:04 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 01:32:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 16 Jun 2023 01:32:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 30 Jun 2023 23:34:08 GMT
ENV JAVA_VERSION=8.0.8.6
# Fri, 30 Jun 2023 23:36:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='2f173ec848303a99bcd38b0c13b1ddb2a70bb4ba9fa0e4ec5bd99268ff9987f8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc637ac2d65386079932d06a303c244daa39282e514ba376cdb7fd0128cd05a5';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e510a98c183248a9ebbec0093958c5fc2f1dc126c792878e0bc739b44eaad7cd';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='7bd82044da06a852d373c20bac462cc60bc85355ca57c850b9d5b513c7b93768';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 30 Jun 2023 23:36:35 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a02dd69d9a8a1e6f4fc2ccb509fb8efd6014b00ff932a757d23b4b012a2bec49`  
		Last Modified: Fri, 16 Jun 2023 00:44:52 GMT  
		Size: 35.7 MB (35711397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3831c1123275dd4d9043ad21bf2c9fb47b24b3ab61e99547e14106df60427380`  
		Last Modified: Fri, 16 Jun 2023 01:40:42 GMT  
		Size: 1.6 MB (1576481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2610129c267e9b676ec5feea35705fa96c12357775402d5f3f9222cd4e2f57f9`  
		Last Modified: Fri, 30 Jun 2023 23:42:53 GMT  
		Size: 133.8 MB (133792034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:1ccc6c3a38bd38688a67ebe26e1e23a6f4af4a68f53681733c50f297e679b407
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160775676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00bb31a6736243cbb938a41bbd123587761628a6dd8263709cb31d393353e44`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:53:20 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:53:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:53:22 GMT
ADD file:fa0aef35be7808c8fd6751a52bdec4dd81057e2fcaa075c547a1db53640dae9a in / 
# Wed, 28 Jun 2023 08:53:22 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 16:51:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 04 Jul 2023 16:51:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 16:51:20 GMT
ENV JAVA_VERSION=8.0.8.6
# Tue, 04 Jul 2023 16:52:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='2f173ec848303a99bcd38b0c13b1ddb2a70bb4ba9fa0e4ec5bd99268ff9987f8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc637ac2d65386079932d06a303c244daa39282e514ba376cdb7fd0128cd05a5';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e510a98c183248a9ebbec0093958c5fc2f1dc126c792878e0bc739b44eaad7cd';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='7bd82044da06a852d373c20bac462cc60bc85355ca57c850b9d5b513c7b93768';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 04 Jul 2023 16:52:11 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:ce02ee0330980398d6a84a50abfa1a8c4d1cba27cbd7442b79f4aa1b1a14020d`  
		Last Modified: Tue, 04 Jul 2023 13:08:30 GMT  
		Size: 28.6 MB (28645696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bb008d160279336a7f69b2e2efa53fc36a1f7792039d4a7750f65556eb55fe`  
		Last Modified: Tue, 04 Jul 2023 16:54:25 GMT  
		Size: 1.5 MB (1477144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206261a99bf0b13e99750c033e68dcca3d6f76bafbf3f889ca8a88d31bd05e0b`  
		Last Modified: Tue, 04 Jul 2023 16:54:34 GMT  
		Size: 130.7 MB (130652836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:latest`

```console
$ docker pull ibmjava@sha256:f8f5a1e37868bb7516b86dcd506c0845fc4258f6e8a1dbe99889c7abc7535a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:latest` - linux; amd64

```console
$ docker pull ibmjava@sha256:b7da5671b83927331ab96a51daed1f4e279d32fe7c6b55dae603c9cf3a53fba6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (165995845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314e2dd39b80f7270acce9e70c948de5a2caf27f2b414e94ea4134c14da40461`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:57:15 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 16 Jun 2023 02:57:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 30 Jun 2023 23:23:48 GMT
ENV JAVA_VERSION=8.0.8.6
# Fri, 30 Jun 2023 23:24:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='2f173ec848303a99bcd38b0c13b1ddb2a70bb4ba9fa0e4ec5bd99268ff9987f8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc637ac2d65386079932d06a303c244daa39282e514ba376cdb7fd0128cd05a5';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e510a98c183248a9ebbec0093958c5fc2f1dc126c792878e0bc739b44eaad7cd';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='7bd82044da06a852d373c20bac462cc60bc85355ca57c850b9d5b513c7b93768';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 30 Jun 2023 23:24:48 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1aab967c9f4d601afc5e8b2023fa6a57cdb9f402102cbf9e941ffab60ec77b`  
		Last Modified: Fri, 16 Jun 2023 03:01:13 GMT  
		Size: 1.5 MB (1469042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4750ed8e2dee55c4ac7a03aed8efbf7e67419a502935599be8e5cf3ac67a427`  
		Last Modified: Fri, 30 Jun 2023 23:27:28 GMT  
		Size: 134.1 MB (134095764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:74dc42e03ea89dec60b00edb541588051efdd3f7cba4c075b20e483cce50c375
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171079912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795826c779222aa7fcb003db5523fcb1d1202da09acd89bacabca76cf73f8681`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:01:00 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:01:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:01:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:01:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:01:03 GMT
ADD file:00c4f44b35b683caef54d5b8b0e0b1e68872f45eae17dd7543adaf6c54512447 in / 
# Mon, 05 Jun 2023 17:01:04 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 01:32:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 16 Jun 2023 01:32:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 30 Jun 2023 23:34:08 GMT
ENV JAVA_VERSION=8.0.8.6
# Fri, 30 Jun 2023 23:36:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='2f173ec848303a99bcd38b0c13b1ddb2a70bb4ba9fa0e4ec5bd99268ff9987f8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc637ac2d65386079932d06a303c244daa39282e514ba376cdb7fd0128cd05a5';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e510a98c183248a9ebbec0093958c5fc2f1dc126c792878e0bc739b44eaad7cd';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='7bd82044da06a852d373c20bac462cc60bc85355ca57c850b9d5b513c7b93768';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 30 Jun 2023 23:36:35 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a02dd69d9a8a1e6f4fc2ccb509fb8efd6014b00ff932a757d23b4b012a2bec49`  
		Last Modified: Fri, 16 Jun 2023 00:44:52 GMT  
		Size: 35.7 MB (35711397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3831c1123275dd4d9043ad21bf2c9fb47b24b3ab61e99547e14106df60427380`  
		Last Modified: Fri, 16 Jun 2023 01:40:42 GMT  
		Size: 1.6 MB (1576481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2610129c267e9b676ec5feea35705fa96c12357775402d5f3f9222cd4e2f57f9`  
		Last Modified: Fri, 30 Jun 2023 23:42:53 GMT  
		Size: 133.8 MB (133792034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; s390x

```console
$ docker pull ibmjava@sha256:1ccc6c3a38bd38688a67ebe26e1e23a6f4af4a68f53681733c50f297e679b407
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160775676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00bb31a6736243cbb938a41bbd123587761628a6dd8263709cb31d393353e44`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:53:20 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:53:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:53:22 GMT
ADD file:fa0aef35be7808c8fd6751a52bdec4dd81057e2fcaa075c547a1db53640dae9a in / 
# Wed, 28 Jun 2023 08:53:22 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 16:51:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 04 Jul 2023 16:51:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 16:51:20 GMT
ENV JAVA_VERSION=8.0.8.6
# Tue, 04 Jul 2023 16:52:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='2f173ec848303a99bcd38b0c13b1ddb2a70bb4ba9fa0e4ec5bd99268ff9987f8';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cc637ac2d65386079932d06a303c244daa39282e514ba376cdb7fd0128cd05a5';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e510a98c183248a9ebbec0093958c5fc2f1dc126c792878e0bc739b44eaad7cd';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='7bd82044da06a852d373c20bac462cc60bc85355ca57c850b9d5b513c7b93768';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 04 Jul 2023 16:52:11 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:ce02ee0330980398d6a84a50abfa1a8c4d1cba27cbd7442b79f4aa1b1a14020d`  
		Last Modified: Tue, 04 Jul 2023 13:08:30 GMT  
		Size: 28.6 MB (28645696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bb008d160279336a7f69b2e2efa53fc36a1f7792039d4a7750f65556eb55fe`  
		Last Modified: Tue, 04 Jul 2023 16:54:25 GMT  
		Size: 1.5 MB (1477144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206261a99bf0b13e99750c033e68dcca3d6f76bafbf3f889ca8a88d31bd05e0b`  
		Last Modified: Tue, 04 Jul 2023 16:54:34 GMT  
		Size: 130.7 MB (130652836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:8ba02ac3a74d66c87fdfc68c37420a47ccb5ebf41976aab5ca08ec3d48a4e09c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:2df6f827f0cfceaec03e9cf8c73ee8d017539007c8cee30ac2f2756164c43c4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.1 MB (203149346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834035c2e83034222a843392ebbac922610690bcfe95e58f20830155ad242f7f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:57:15 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 16 Jun 2023 02:57:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 30 Jun 2023 23:23:48 GMT
ENV JAVA_VERSION=8.0.8.6
# Fri, 30 Jun 2023 23:26:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bd95ba315fa0752be3a18fd67c0dbda568313484f21420999766bc46c9af9191';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e159747a1fe64a03a24994887c8e4ab3aea06072f3a2ed99c3db31cec0c224de';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='7385da0c5ffde5b81f4830b95aa352db2a89b8380ccef25dcd77fdf5b0af3488';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='096edb7671f217d64ec9a6cf44b4d0e7f56184da1aa32e8d84eebe36c02c80d9';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 30 Jun 2023 23:26:58 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1aab967c9f4d601afc5e8b2023fa6a57cdb9f402102cbf9e941ffab60ec77b`  
		Last Modified: Fri, 16 Jun 2023 03:01:13 GMT  
		Size: 1.5 MB (1469042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3d721224099caff5dc158dbda3b69a0cbd9ba8ee0a5e406a8072f156dcce2d`  
		Last Modified: Fri, 30 Jun 2023 23:28:05 GMT  
		Size: 171.2 MB (171249265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:7748905c8e09c074f91b905db8a2887eea85954dc5c3befd79ae3f5312c42423
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.4 MB (208357736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e1b8ca0a9ddcaf0dc255e86adeb28a44405645bab8d4177eeae534efeacdd48`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:01:00 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:01:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:01:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:01:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:01:03 GMT
ADD file:00c4f44b35b683caef54d5b8b0e0b1e68872f45eae17dd7543adaf6c54512447 in / 
# Mon, 05 Jun 2023 17:01:04 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 01:32:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 16 Jun 2023 01:32:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 30 Jun 2023 23:34:08 GMT
ENV JAVA_VERSION=8.0.8.6
# Fri, 30 Jun 2023 23:42:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bd95ba315fa0752be3a18fd67c0dbda568313484f21420999766bc46c9af9191';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e159747a1fe64a03a24994887c8e4ab3aea06072f3a2ed99c3db31cec0c224de';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='7385da0c5ffde5b81f4830b95aa352db2a89b8380ccef25dcd77fdf5b0af3488';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='096edb7671f217d64ec9a6cf44b4d0e7f56184da1aa32e8d84eebe36c02c80d9';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 30 Jun 2023 23:42:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a02dd69d9a8a1e6f4fc2ccb509fb8efd6014b00ff932a757d23b4b012a2bec49`  
		Last Modified: Fri, 16 Jun 2023 00:44:52 GMT  
		Size: 35.7 MB (35711397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3831c1123275dd4d9043ad21bf2c9fb47b24b3ab61e99547e14106df60427380`  
		Last Modified: Fri, 16 Jun 2023 01:40:42 GMT  
		Size: 1.6 MB (1576481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188381b7aa74564ab295f4dd1a086683de39bb4d01038eebbd6818718b35c366`  
		Last Modified: Fri, 30 Jun 2023 23:43:51 GMT  
		Size: 171.1 MB (171069858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:b39f279112de98495d7f50eb628fc55312a612e262abe70e5f26d6dccd40bffb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191049154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c04147d478dacab93d2b427339df62bd556d0142da493aad64f80274abffcb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:53:20 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:53:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:53:22 GMT
ADD file:fa0aef35be7808c8fd6751a52bdec4dd81057e2fcaa075c547a1db53640dae9a in / 
# Wed, 28 Jun 2023 08:53:22 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 16:51:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 04 Jul 2023 16:51:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 16:51:20 GMT
ENV JAVA_VERSION=8.0.8.6
# Tue, 04 Jul 2023 16:54:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bd95ba315fa0752be3a18fd67c0dbda568313484f21420999766bc46c9af9191';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e159747a1fe64a03a24994887c8e4ab3aea06072f3a2ed99c3db31cec0c224de';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='7385da0c5ffde5b81f4830b95aa352db2a89b8380ccef25dcd77fdf5b0af3488';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='096edb7671f217d64ec9a6cf44b4d0e7f56184da1aa32e8d84eebe36c02c80d9';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 04 Jul 2023 16:54:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:ce02ee0330980398d6a84a50abfa1a8c4d1cba27cbd7442b79f4aa1b1a14020d`  
		Last Modified: Tue, 04 Jul 2023 13:08:30 GMT  
		Size: 28.6 MB (28645696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bb008d160279336a7f69b2e2efa53fc36a1f7792039d4a7750f65556eb55fe`  
		Last Modified: Tue, 04 Jul 2023 16:54:25 GMT  
		Size: 1.5 MB (1477144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe65be5a37cf879c019f55cf099ea231fdcf2302e8b6e79df9816d4798b1b04`  
		Last Modified: Tue, 04 Jul 2023 16:55:03 GMT  
		Size: 160.9 MB (160926314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:d207860a549402285fa7621766cb1a7b1aac7ec1d15b9c937fc83b2c6732f469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:4bbe6af9cb3a4775563b5fa63f502139f7691ac955ce648391da25b70244545d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101246913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de662ecabc02b88c7bf409f56d58de000d095da4cb4a8f5adcca9d1780598b21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:00:37 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:00:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:00:37 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:00:39 GMT
ADD file:0ad2ee2cfb186802f49c9bf4148674d1c6fc201f83478ec01ffaa7086d491323 in / 
# Mon, 05 Jun 2023 17:00:39 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 02:57:15 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 16 Jun 2023 02:57:21 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 30 Jun 2023 23:23:48 GMT
ENV JAVA_VERSION=8.0.8.6
# Fri, 30 Jun 2023 23:25:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='d795b429c31b76e28e96848ad66a2749314c498a2c744f41d1fa7bf032ccc495';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='75f234bd86768a7cd4aa0cf6b62f88f62f79a9d0455c3e49adf97cf363391170';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='3d2eceb6ff09b2663c312f0c11955372198cfd85dc693c4188875300aefae6ac';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='9e7f8f163eddd1d8c7781a11bc7e6a2d428063ac1d3054184227b172d95cef56';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 30 Jun 2023 23:25:39 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3f94e4e483ea634d7ab0b63649b8f72f8b721d4c626297fd0edae0abea1df9e9`  
		Last Modified: Tue, 06 Jun 2023 11:46:33 GMT  
		Size: 30.4 MB (30431039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1aab967c9f4d601afc5e8b2023fa6a57cdb9f402102cbf9e941ffab60ec77b`  
		Last Modified: Fri, 16 Jun 2023 03:01:13 GMT  
		Size: 1.5 MB (1469042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba237cb7136dfa378f67671e23669e72053a5ef6ad375b959b271fb0619e5b3d`  
		Last Modified: Fri, 30 Jun 2023 23:27:46 GMT  
		Size: 69.3 MB (69346832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:1650a28505dc676d98f3bbbc58096134e9011c575352f69721c05fdec6af0c6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.0 MB (106974195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1924097623bf77029aecaa58d84153e693da57e69f27d7ef976bdc2b532dfc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:01:00 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:01:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:01:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:01:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:01:03 GMT
ADD file:00c4f44b35b683caef54d5b8b0e0b1e68872f45eae17dd7543adaf6c54512447 in / 
# Mon, 05 Jun 2023 17:01:04 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 01:32:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 16 Jun 2023 01:32:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 30 Jun 2023 23:34:08 GMT
ENV JAVA_VERSION=8.0.8.6
# Fri, 30 Jun 2023 23:38:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='d795b429c31b76e28e96848ad66a2749314c498a2c744f41d1fa7bf032ccc495';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='75f234bd86768a7cd4aa0cf6b62f88f62f79a9d0455c3e49adf97cf363391170';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='3d2eceb6ff09b2663c312f0c11955372198cfd85dc693c4188875300aefae6ac';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='9e7f8f163eddd1d8c7781a11bc7e6a2d428063ac1d3054184227b172d95cef56';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 30 Jun 2023 23:38:37 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a02dd69d9a8a1e6f4fc2ccb509fb8efd6014b00ff932a757d23b4b012a2bec49`  
		Last Modified: Fri, 16 Jun 2023 00:44:52 GMT  
		Size: 35.7 MB (35711397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3831c1123275dd4d9043ad21bf2c9fb47b24b3ab61e99547e14106df60427380`  
		Last Modified: Fri, 16 Jun 2023 01:40:42 GMT  
		Size: 1.6 MB (1576481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2d3c7a08e2e1bc10b40660ee85f5bfba8b45b54e0cdb2eb9f964db81f9dc63`  
		Last Modified: Fri, 30 Jun 2023 23:43:20 GMT  
		Size: 69.7 MB (69686317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:51d45c48d161b24b810410b3d10a1c5f0293282bacf266a47ee7e8c65061ec1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.0 MB (100042164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10e8a80e88c3c3542c8b59b6d6041874fe560481e4a53cd1a01fd2c630a2b2e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 08:53:20 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:53:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:53:22 GMT
ADD file:fa0aef35be7808c8fd6751a52bdec4dd81057e2fcaa075c547a1db53640dae9a in / 
# Wed, 28 Jun 2023 08:53:22 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 16:51:16 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 04 Jul 2023 16:51:20 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 16:51:20 GMT
ENV JAVA_VERSION=8.0.8.6
# Tue, 04 Jul 2023 16:52:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='d795b429c31b76e28e96848ad66a2749314c498a2c744f41d1fa7bf032ccc495';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='75f234bd86768a7cd4aa0cf6b62f88f62f79a9d0455c3e49adf97cf363391170';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='3d2eceb6ff09b2663c312f0c11955372198cfd85dc693c4188875300aefae6ac';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='9e7f8f163eddd1d8c7781a11bc7e6a2d428063ac1d3054184227b172d95cef56';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 04 Jul 2023 16:53:00 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:ce02ee0330980398d6a84a50abfa1a8c4d1cba27cbd7442b79f4aa1b1a14020d`  
		Last Modified: Tue, 04 Jul 2023 13:08:30 GMT  
		Size: 28.6 MB (28645696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bb008d160279336a7f69b2e2efa53fc36a1f7792039d4a7750f65556eb55fe`  
		Last Modified: Tue, 04 Jul 2023 16:54:25 GMT  
		Size: 1.5 MB (1477144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2752454753d34dd000abeba297879893b8cfca05dbd96759a7c65e6e9b80a8b9`  
		Last Modified: Tue, 04 Jul 2023 16:54:47 GMT  
		Size: 69.9 MB (69919324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

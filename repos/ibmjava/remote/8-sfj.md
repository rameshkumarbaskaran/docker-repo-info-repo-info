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

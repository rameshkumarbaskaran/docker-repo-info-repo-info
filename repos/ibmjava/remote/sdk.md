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

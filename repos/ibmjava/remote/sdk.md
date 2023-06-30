## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:d46017bb0fa8b4e912280bbee42554044c0b43c15035b5c54f90699d47a5ca3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:17116380ad2d9405d9b4a6afa2e144f75a3a5a15ebbddd43889948a146c90c7c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.1 MB (203110231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d2ad258bf3c06b8f4ecdb92e776e619a7a1ccc9548d60382c4d26961104712`
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
# Fri, 16 Jun 2023 02:57:21 GMT
ENV JAVA_VERSION=8.0.8.5
# Fri, 16 Jun 2023 03:00:48 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a1b462fd16ae935c34523b761a08010120c074d10cd7ac339af213a9bed59f05';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='eac7923675423ef01db312a59ee68c96eb8ec474560630bda4d24807d4980dcf';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='9e14a91a5cd4aaafe5553b06364249cd7819d31edf187e1160ca6bec5ce3a82b';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='995373f2d4395484e8c784fe39062e98b5f6f6cb1a90ae6dd8931b7bfdc6cb14';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 16 Jun 2023 03:00:49 GMT
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
	-	`sha256:e999be3e47e84f8318ec04aa00141d2d30eb83aa56907132259042e6bb23864c`  
		Last Modified: Fri, 16 Jun 2023 03:01:58 GMT  
		Size: 171.2 MB (171210150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:9fde21dc9d9385920741619642d22573927c12e7bf6e3d85392bd4dbeee280c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208316682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f06cdb66966ad12065f3b9b694d5b2ea97688bbee08d492d5b3f760004d39a`
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
# Fri, 16 Jun 2023 01:32:19 GMT
ENV JAVA_VERSION=8.0.8.5
# Fri, 16 Jun 2023 01:40:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a1b462fd16ae935c34523b761a08010120c074d10cd7ac339af213a9bed59f05';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='eac7923675423ef01db312a59ee68c96eb8ec474560630bda4d24807d4980dcf';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='9e14a91a5cd4aaafe5553b06364249cd7819d31edf187e1160ca6bec5ce3a82b';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='995373f2d4395484e8c784fe39062e98b5f6f6cb1a90ae6dd8931b7bfdc6cb14';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 16 Jun 2023 01:40:20 GMT
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
	-	`sha256:260406cb1e7fd613b7e09eeaa2a51135d336a5e8cbec3975859139fa201c68a1`  
		Last Modified: Fri, 16 Jun 2023 01:41:49 GMT  
		Size: 171.0 MB (171028804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:6b10893c6777867c5bcd0dfc33e33df017ec4562fbf750255792725ab3c06855
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191047788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53f9130950dbc96bc73337680aad2a189635b68428e316adbcbaa7582e1d68c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 05 Jun 2023 17:01:02 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:01:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:01:04 GMT
ADD file:2d2f31ec110b9e7ec21a9d4824a430acdaabf0b4e9c1cdd337438992859b57ae in / 
# Mon, 05 Jun 2023 17:01:04 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 18:25:52 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 16 Jun 2023 18:25:56 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 30 Jun 2023 22:42:14 GMT
ENV JAVA_VERSION=8.0.8.6
# Fri, 30 Jun 2023 22:45:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bd95ba315fa0752be3a18fd67c0dbda568313484f21420999766bc46c9af9191';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e159747a1fe64a03a24994887c8e4ab3aea06072f3a2ed99c3db31cec0c224de';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='7385da0c5ffde5b81f4830b95aa352db2a89b8380ccef25dcd77fdf5b0af3488';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='096edb7671f217d64ec9a6cf44b4d0e7f56184da1aa32e8d84eebe36c02c80d9';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 30 Jun 2023 22:45:05 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:fab1a8aa44b00432834b7776a76fd4149ec2fee2336a3521bd5435428df7edc9`  
		Last Modified: Fri, 16 Jun 2023 18:23:35 GMT  
		Size: 28.6 MB (28644581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1521659225e331fd6923943db586c259687a2b65eab1dbc35fce49da80029f3`  
		Last Modified: Fri, 16 Jun 2023 18:37:39 GMT  
		Size: 1.5 MB (1477026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10d8e951ec17c9a3c7a70b7e137b59cb0af83aaba951a0c9ab3aa7b960887c9d`  
		Last Modified: Fri, 30 Jun 2023 22:46:04 GMT  
		Size: 160.9 MB (160926181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

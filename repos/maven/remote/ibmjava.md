## `maven:ibmjava`

```console
$ docker pull maven@sha256:f3bbd6878c93a6cb7444620263a3239b1fcebbc0cc2eeed3a9746a0b726de153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `maven:ibmjava` - linux; amd64

```console
$ docker pull maven@sha256:c2b0d4ebb2de8ecac1fb39dbea1d62030bf808d0c3391852d4995c10dd9be61a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235817932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951e9564690cc35ffefca1cd342092c0b1e9f5bcd344b2f196710ed185105dfc`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:36 GMT
ADD file:c6039a4f004b6b6c2e4c281a228d64d8410cb9fdf0c67776f84bb173d3522be1 in / 
# Wed, 02 Feb 2022 02:14:36 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:40:26 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 02 Feb 2022 03:40:35 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:40:35 GMT
ENV JAVA_VERSION=8.0.7.0
# Wed, 02 Feb 2022 03:42:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9fa9b9cb755667dd165d585d69da234536da1d5dfcaa430468e37e16cc650f9c';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='6e998d7152cf5816fc0759abb1f7f517788f7dbf38b8f2a71ebc3272cf940b53';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cde891855118977b203cf15833207f42a62da0902bad30462cdddcadc23ebfeb';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='18e71aaddc90197969e76cdbe9c23e9b8ff0960b88ba854e179bf80629bc740b';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ab843ee0b0e7e9765afb3a5081630eeb17b0372bc55b5c7dc37e8d03aa9c4d1a';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 02 Feb 2022 03:42:27 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 02 Feb 2022 12:05:54 GMT
ARG MAVEN_VERSION=3.8.4
# Wed, 02 Feb 2022 12:05:54 GMT
ARG USER_HOME_DIR=/root
# Wed, 02 Feb 2022 12:05:55 GMT
ARG SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8
# Wed, 02 Feb 2022 12:05:55 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries
# Wed, 02 Feb 2022 12:19:56 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN apt-get update && apt-get install -y curl   && mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 02 Feb 2022 12:19:56 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 02 Feb 2022 12:19:56 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 02 Feb 2022 12:19:57 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 02 Feb 2022 12:19:57 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 02 Feb 2022 12:19:57 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 02 Feb 2022 12:19:57 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:68e7bb398b9ff421236990bfeaf5c1feab26c590eed93489e245375c23551e2a`  
		Last Modified: Sat, 29 Jan 2022 14:35:20 GMT  
		Size: 26.7 MB (26708066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fb07417efc9ce7b84eb9ed465e87c936352af2a77456046d4e4c6f7f3e7a57`  
		Last Modified: Wed, 02 Feb 2022 03:42:54 GMT  
		Size: 3.0 MB (2959756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00c021bd04fb4af9c31814dc2a1f964d6aab3a4acd91312ed12f75815fbb8af`  
		Last Modified: Wed, 02 Feb 2022 03:43:45 GMT  
		Size: 165.9 MB (165859706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b0823c6ac0dfc8f3b7928a1b52ae1fabb4c8b6823973f0ec8c72dd08a8f106`  
		Last Modified: Wed, 02 Feb 2022 12:24:01 GMT  
		Size: 40.3 MB (40289194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f4eb5776325280d3effbd7f3ef0195540afd26ca0505e2f20617f377d20d3c`  
		Last Modified: Wed, 02 Feb 2022 12:23:57 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fa89bd08d8c724f1070f98c6a11c6739911680c2ddc0a4e9b19b7c1987255c`  
		Last Modified: Wed, 02 Feb 2022 12:23:57 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:ibmjava` - linux; 386

```console
$ docker pull maven@sha256:77350ba42060d4545f9ee3e399f7dd03cef70a14e02fbfecde474bd10ba8e308
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.2 MB (221173109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c7df2dd67a97b5eb8c55a2badcb3169e5437911ed595dc654ae2706760ca3b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 02 Feb 2022 01:39:15 GMT
ADD file:41a670fdf6e067377f3e555206d80e9dddb0d180cd7493802d3989acb2c1b573 in / 
# Wed, 02 Feb 2022 01:39:16 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 01:55:34 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 02 Feb 2022 01:56:00 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 01:56:00 GMT
ENV JAVA_VERSION=8.0.7.0
# Wed, 02 Feb 2022 01:58:05 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9fa9b9cb755667dd165d585d69da234536da1d5dfcaa430468e37e16cc650f9c';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='6e998d7152cf5816fc0759abb1f7f517788f7dbf38b8f2a71ebc3272cf940b53';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cde891855118977b203cf15833207f42a62da0902bad30462cdddcadc23ebfeb';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='18e71aaddc90197969e76cdbe9c23e9b8ff0960b88ba854e179bf80629bc740b';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ab843ee0b0e7e9765afb3a5081630eeb17b0372bc55b5c7dc37e8d03aa9c4d1a';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 02 Feb 2022 01:58:05 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Mon, 14 Feb 2022 19:39:22 GMT
RUN apt-get update && apt-get install -y curl
# Mon, 14 Feb 2022 19:39:22 GMT
ARG MAVEN_VERSION=3.8.4
# Mon, 14 Feb 2022 19:39:22 GMT
ARG USER_HOME_DIR=/root
# Mon, 14 Feb 2022 19:39:22 GMT
ARG SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8
# Mon, 14 Feb 2022 19:39:23 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries
# Mon, 14 Feb 2022 19:39:26 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 14 Feb 2022 19:39:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 14 Feb 2022 19:39:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 14 Feb 2022 19:39:26 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 14 Feb 2022 19:39:27 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 14 Feb 2022 19:39:27 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 14 Feb 2022 19:39:27 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:783703cdc79d2cd178a6be62b27388915bbc0dabf13db414d7ee577514c92adf`  
		Last Modified: Wed, 02 Feb 2022 01:40:03 GMT  
		Size: 27.2 MB (27161586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944419a0797263cb1168e0715821610315031f2aef101b1e93ceca4cafaa3636`  
		Last Modified: Wed, 02 Feb 2022 01:58:34 GMT  
		Size: 3.0 MB (2988866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72c2f179e33fedb5a20e4cdb81919a199efa3d9080f9ad71d72810e80b23e05`  
		Last Modified: Wed, 02 Feb 2022 01:59:35 GMT  
		Size: 154.0 MB (154038455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7400f3db250b5d018c481a1db9ccee5831071f12faa518a5c9b939e66477ccda`  
		Last Modified: Mon, 14 Feb 2022 19:39:56 GMT  
		Size: 27.9 MB (27873182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6ecf3ab1408628ec2b0f6aad73bc021c38ddd5a8b92e770c16dec058170071`  
		Last Modified: Mon, 14 Feb 2022 19:39:54 GMT  
		Size: 9.1 MB (9109806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4675aab0ecc396a06fe0538f4ab27a9d385420f9af500149e20e9df508d60d76`  
		Last Modified: Mon, 14 Feb 2022 19:39:53 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e2a1cf7e06369fd76a4b909175581d6fe0a883d66bf2d78f775923d762afad`  
		Last Modified: Mon, 14 Feb 2022 19:39:52 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:ibmjava` - linux; ppc64le

```console
$ docker pull maven@sha256:b9d4816333cbf002effcb6bd4e2394e1fedb434833d478ae738204d4a2ace701
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233306656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbee833e018221118640ebf69260e64b0fb081fd11ba744ee48321a01fdefb79`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 02 Feb 2022 03:49:58 GMT
ADD file:19b6b516bfde37805273abae0012aaceb45030dcc0c1dbc11828a4dfa6549c29 in / 
# Wed, 02 Feb 2022 03:50:03 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:01:20 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 02 Feb 2022 06:01:55 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:01:57 GMT
ENV JAVA_VERSION=8.0.7.0
# Wed, 02 Feb 2022 06:05:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9fa9b9cb755667dd165d585d69da234536da1d5dfcaa430468e37e16cc650f9c';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='6e998d7152cf5816fc0759abb1f7f517788f7dbf38b8f2a71ebc3272cf940b53';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cde891855118977b203cf15833207f42a62da0902bad30462cdddcadc23ebfeb';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='18e71aaddc90197969e76cdbe9c23e9b8ff0960b88ba854e179bf80629bc740b';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ab843ee0b0e7e9765afb3a5081630eeb17b0372bc55b5c7dc37e8d03aa9c4d1a';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 02 Feb 2022 06:05:26 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 02 Feb 2022 11:06:42 GMT
ARG MAVEN_VERSION=3.8.4
# Wed, 02 Feb 2022 11:06:43 GMT
ARG USER_HOME_DIR=/root
# Wed, 02 Feb 2022 11:06:44 GMT
ARG SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8
# Wed, 02 Feb 2022 11:06:45 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries
# Wed, 02 Feb 2022 15:00:48 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN apt-get update && apt-get install -y curl   && mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 02 Feb 2022 15:00:53 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 02 Feb 2022 15:00:57 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 02 Feb 2022 15:01:01 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 02 Feb 2022 15:01:03 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 02 Feb 2022 15:01:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 02 Feb 2022 15:01:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1dc99fe180768d17487534d27fca7d2aea3e7473c284314a65af7be77144eeaa`  
		Last Modified: Wed, 02 Feb 2022 03:52:51 GMT  
		Size: 30.4 MB (30437685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e519c40c78b488d71991dd0054bffe8260611286580cb61463ffb1d4b81bb2`  
		Last Modified: Wed, 02 Feb 2022 06:05:57 GMT  
		Size: 3.1 MB (3081867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6b2715a5412180411598c60963815f7c885b52210892ddc7520ae64803e981`  
		Last Modified: Wed, 02 Feb 2022 06:07:07 GMT  
		Size: 165.5 MB (165528328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7ee9c88877fc30157f0a48f934c6d1d126770f1b146efca7eb0c60aced8a32`  
		Last Modified: Wed, 02 Feb 2022 15:11:38 GMT  
		Size: 34.3 MB (34257560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba6f9ba8581155955f9ceafed9feb5f5a89fc2747ccadcaa583e96e970c371a`  
		Last Modified: Wed, 02 Feb 2022 15:11:31 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537670a95adacdfe9dd1208e1ec4f8742814e0488bbe4640c6e8cb0b7b06328b`  
		Last Modified: Wed, 02 Feb 2022 15:11:31 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:ibmjava` - linux; s390x

```console
$ docker pull maven@sha256:860ef0805b2e533f67f86a06680e65fa888a7b88bb61948496da36b89dc3a4d2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216328141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9193564302e667b263fd70915ba6a6c7de278a40673120fc0e8ee990dcb13d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 02 Feb 2022 01:42:03 GMT
ADD file:3fe2ce9d5d8932ed39dc2c73abff4b15e244fb1e7eb456de0a05df07ede3bf39 in / 
# Wed, 02 Feb 2022 01:42:07 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:39:28 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 02 Feb 2022 02:39:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:39:35 GMT
ENV JAVA_VERSION=8.0.7.0
# Wed, 02 Feb 2022 02:41:53 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9fa9b9cb755667dd165d585d69da234536da1d5dfcaa430468e37e16cc650f9c';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='6e998d7152cf5816fc0759abb1f7f517788f7dbf38b8f2a71ebc3272cf940b53';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cde891855118977b203cf15833207f42a62da0902bad30462cdddcadc23ebfeb';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='18e71aaddc90197969e76cdbe9c23e9b8ff0960b88ba854e179bf80629bc740b';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ab843ee0b0e7e9765afb3a5081630eeb17b0372bc55b5c7dc37e8d03aa9c4d1a';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 02 Feb 2022 02:41:58 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Mon, 14 Feb 2022 19:43:57 GMT
RUN apt-get update && apt-get install -y curl
# Mon, 14 Feb 2022 19:43:58 GMT
ARG MAVEN_VERSION=3.8.4
# Mon, 14 Feb 2022 19:43:58 GMT
ARG USER_HOME_DIR=/root
# Mon, 14 Feb 2022 19:43:58 GMT
ARG SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8
# Mon, 14 Feb 2022 19:43:58 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries
# Mon, 14 Feb 2022 19:44:12 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Mon, 14 Feb 2022 19:44:12 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 14 Feb 2022 19:44:12 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 14 Feb 2022 19:44:12 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Mon, 14 Feb 2022 19:44:12 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Mon, 14 Feb 2022 19:44:13 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 14 Feb 2022 19:44:13 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:cf002da3924024b39105dcc613288421b394e45e04d7a3c245ce5dcaf544dd98`  
		Last Modified: Wed, 02 Feb 2022 01:43:50 GMT  
		Size: 25.4 MB (25364307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4bcdb503991176c9486c76e56946053a4588fc20649c5465c056a465c592dee`  
		Last Modified: Wed, 02 Feb 2022 02:42:23 GMT  
		Size: 2.7 MB (2676856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36eac35f2d3f67c939de0ca1396ccaddaa663a009814cdc7ef48712d6295fac0`  
		Last Modified: Wed, 02 Feb 2022 02:43:14 GMT  
		Size: 156.0 MB (156013882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553c020e091abff94605bfcf3930cfcecd3e76ee658a70f80b8f0062016f106c`  
		Last Modified: Mon, 14 Feb 2022 19:47:18 GMT  
		Size: 23.2 MB (23162070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331788cd9d66fe3696ac38be45aa3e8ec677bcdc19b8e177e4a6e586b4cc1d20`  
		Last Modified: Mon, 14 Feb 2022 19:47:16 GMT  
		Size: 9.1 MB (9109811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41769d4df20684f87be6247210571a8dbe6d86384718987f4dfaa8eaf9533d3a`  
		Last Modified: Mon, 14 Feb 2022 19:47:16 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38eeefd24bcd059e11ee3fd6a9aca84c7c7cdd930042439b3004d5c6e4a7c980`  
		Last Modified: Mon, 14 Feb 2022 19:47:16 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

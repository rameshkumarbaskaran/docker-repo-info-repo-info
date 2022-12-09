## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:715bd6d00de3baec142aa3784a8c53844df91165a1cb454f19643a3d385cec72
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
$ docker pull ibmjava@sha256:f5238c588c331d383d4179ee7ae4d13fb94cec4679e24a1c0db0056d4267c499
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94532040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e58ffe09da66f708cb7b630ad6205e06b967f9db248e21862453cf253f56b110`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Dec 2022 01:38:59 GMT
ADD file:ab7098cc4395f87660bf4fef944711c4eae43c22aa2627b09681883a0aeab718 in / 
# Fri, 09 Dec 2022 01:38:59 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:03:42 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 09 Dec 2022 02:03:49 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 02:03:49 GMT
ENV JAVA_VERSION=8.0.7.20
# Fri, 09 Dec 2022 02:05:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bb548976980c436b15e59e0db7b4e99a7ed273df39e17db60047f950c2863c1b';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='768e6f8df5c9735d703f2dd5352b7c063949d59c6e15bc7d5c31d7ac667a241a';          YML_FILE='8.0/sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='1ce92e9c420b2d081c8cd63c8441b324e49348360490d61e08a0908b830748cb';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e790dc7707417153227e1f3164db1c699e3b6b9f697d9e1c9c9142bc0e3d3409';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='bfac3d6409a7996301d948faedfd4c19920dbb667ba699b7fd4719188366be8b';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 09 Dec 2022 02:05:33 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7e26b56c479a64877378342636b3b7f2659b9c6a8d68475ff70fb0ba3d5f3ca1`  
		Last Modified: Fri, 09 Dec 2022 01:39:36 GMT  
		Size: 27.2 MB (27165403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4197bc688d6f36137fa1f7308bd73f2c8de21e24f3cbb3801fda19600f2ead35`  
		Last Modified: Fri, 09 Dec 2022 02:07:12 GMT  
		Size: 3.0 MB (2981541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9776ecf1f95a1cf7fdba0a357e121ae38a4884aaf4c52a7f60cd1f80cced6c`  
		Last Modified: Fri, 09 Dec 2022 02:07:43 GMT  
		Size: 64.4 MB (64385096 bytes)  
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

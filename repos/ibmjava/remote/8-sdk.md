## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:dbd92f9209e07e63319599b800f7a1d1b6e815b5bc14eaea4382190a9d3316a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:fb989c9ebdf4d24b1bf83ff82865430e7a4e8267c42c63b5ff463f0ed9e153bd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195524960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70aea7e3097d6e192fe8cdd5db72e06068cf4042571d5aed38b349de7606c815`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:21 GMT
ADD file:2aa3e79e3cff3c048612744ac310cf86bc27de3433d420711bafc6612445befc in / 
# Fri, 07 Jan 2022 02:25:21 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:26:25 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 07 Jan 2022 03:26:32 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:26:33 GMT
ENV JAVA_VERSION=8.0.7.0
# Fri, 07 Jan 2022 03:28:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9fa9b9cb755667dd165d585d69da234536da1d5dfcaa430468e37e16cc650f9c';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='6e998d7152cf5816fc0759abb1f7f517788f7dbf38b8f2a71ebc3272cf940b53';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cde891855118977b203cf15833207f42a62da0902bad30462cdddcadc23ebfeb';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='18e71aaddc90197969e76cdbe9c23e9b8ff0960b88ba854e179bf80629bc740b';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ab843ee0b0e7e9765afb3a5081630eeb17b0372bc55b5c7dc37e8d03aa9c4d1a';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 07 Jan 2022 03:28:30 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:2f94e549220aea96f00cae7eb95f401e61b41a16cc5eb0b4ea592d0ce871930a`  
		Last Modified: Thu, 06 Jan 2022 23:50:21 GMT  
		Size: 26.7 MB (26705027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783c1a1f45083d49782e9c69cc2bb7cdc19bd099562f5f0aac114ad7bc7d8419`  
		Last Modified: Fri, 07 Jan 2022 03:28:57 GMT  
		Size: 3.0 MB (2960369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c65e59686ffd3451cbc3e0032e11c41fef7f2c9dce11cf390260ddb49477ea`  
		Last Modified: Fri, 07 Jan 2022 03:29:48 GMT  
		Size: 165.9 MB (165859564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; 386

```console
$ docker pull ibmjava@sha256:fee497612f6e441fbeee7530396e1b81e8e1bbe943dcc2c7f72c60f89eeab891
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184183974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7981c2079fb84c999214ed9e2621860654254a995c2c4fc7957db92c242805e6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:39:03 GMT
ADD file:4992040d291a9a6b53435279ff532c15e004fd7c7b35aa4783850a06ccff0694 in / 
# Fri, 07 Jan 2022 01:39:04 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 01:55:19 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 07 Jan 2022 01:55:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 01:55:38 GMT
ENV JAVA_VERSION=8.0.7.0
# Fri, 07 Jan 2022 01:57:45 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9fa9b9cb755667dd165d585d69da234536da1d5dfcaa430468e37e16cc650f9c';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='6e998d7152cf5816fc0759abb1f7f517788f7dbf38b8f2a71ebc3272cf940b53';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cde891855118977b203cf15833207f42a62da0902bad30462cdddcadc23ebfeb';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='18e71aaddc90197969e76cdbe9c23e9b8ff0960b88ba854e179bf80629bc740b';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ab843ee0b0e7e9765afb3a5081630eeb17b0372bc55b5c7dc37e8d03aa9c4d1a';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 07 Jan 2022 01:57:46 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:cd8c855b84a6297384d4a364fec672137f3aef84749b319ee5158b568545eb0f`  
		Last Modified: Fri, 07 Jan 2022 01:39:50 GMT  
		Size: 27.2 MB (27156435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2117a5cceef36b33a766d89032a5ed9031aa846b7f4aa20b30313c553fc2f481`  
		Last Modified: Fri, 07 Jan 2022 01:58:17 GMT  
		Size: 3.0 MB (2988908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707adec2205a56624665261e60b6cb0ee033e6343a2ce698c13166496136d934`  
		Last Modified: Fri, 07 Jan 2022 01:59:17 GMT  
		Size: 154.0 MB (154038631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:5500257801d584c063d8946e508baa2914fae2789f08d31644465bb4dc857730
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.0 MB (199042821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ea9b83fb01def7e0a85f11732784f8acd169e4909f801952286635964ffbae`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:19:52 GMT
ADD file:e29b7078eb9c78ec6f3931c4beea820e4b7fe5d0d02e02e220c083dcd603aad1 in / 
# Fri, 07 Jan 2022 02:19:55 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:28:44 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 07 Jan 2022 03:29:15 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:29:17 GMT
ENV JAVA_VERSION=8.0.7.0
# Fri, 07 Jan 2022 03:32:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9fa9b9cb755667dd165d585d69da234536da1d5dfcaa430468e37e16cc650f9c';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='6e998d7152cf5816fc0759abb1f7f517788f7dbf38b8f2a71ebc3272cf940b53';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cde891855118977b203cf15833207f42a62da0902bad30462cdddcadc23ebfeb';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='18e71aaddc90197969e76cdbe9c23e9b8ff0960b88ba854e179bf80629bc740b';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ab843ee0b0e7e9765afb3a5081630eeb17b0372bc55b5c7dc37e8d03aa9c4d1a';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 07 Jan 2022 03:32:18 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f130035f6453da800db2a1c34f617d35285297b1e549cc5fe138db9ecb704f0b`  
		Last Modified: Fri, 07 Jan 2022 02:22:21 GMT  
		Size: 30.4 MB (30432347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89db02523773279c64e3768c4c557e84eb48533e8cd88fa8b305a4631fe1620f`  
		Last Modified: Fri, 07 Jan 2022 03:32:43 GMT  
		Size: 3.1 MB (3081902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f8a8d82f45d97d9772077b279a46c7adc364f3c6ac8f3387991cd2252e18c8`  
		Last Modified: Fri, 07 Jan 2022 03:33:57 GMT  
		Size: 165.5 MB (165528572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:2a37a66bd92c6f4cf8d8cbccb9127e14680c7983dde77a82a480c010c224a433
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.1 MB (184052722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49dda0870047f2102ea05b4ce2561ae6628e9d8c0b386a546a9a0a33afec408`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:09 GMT
ADD file:caefb9be68fabe0b9b7dba683dabb869e5165a5a13534742d73a489a3712d9a9 in / 
# Fri, 07 Jan 2022 01:42:12 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:20:25 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 07 Jan 2022 02:20:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:20:32 GMT
ENV JAVA_VERSION=8.0.7.0
# Fri, 07 Jan 2022 02:22:43 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='9fa9b9cb755667dd165d585d69da234536da1d5dfcaa430468e37e16cc650f9c';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='6e998d7152cf5816fc0759abb1f7f517788f7dbf38b8f2a71ebc3272cf940b53';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='cde891855118977b203cf15833207f42a62da0902bad30462cdddcadc23ebfeb';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='18e71aaddc90197969e76cdbe9c23e9b8ff0960b88ba854e179bf80629bc740b';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='ab843ee0b0e7e9765afb3a5081630eeb17b0372bc55b5c7dc37e8d03aa9c4d1a';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 07 Jan 2022 02:22:45 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7587f9252eef493a02840102ba78c74de317d3d47f6d568af5602ff6c1c54a20`  
		Last Modified: Fri, 07 Jan 2022 01:43:57 GMT  
		Size: 25.4 MB (25362136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d5d9207d0f328849a5bf2aec9290cf52dbfa8a48e3d39b130fd1471f46a16e`  
		Last Modified: Fri, 07 Jan 2022 02:23:17 GMT  
		Size: 2.7 MB (2676903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:771b1270fd516faeef64cb76e3c095eef1db91189f69e9323bd0f5e1fe6cdf5f`  
		Last Modified: Fri, 07 Jan 2022 02:23:56 GMT  
		Size: 156.0 MB (156013683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

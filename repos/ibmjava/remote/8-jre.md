## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:2eec0cb4a1ea95a71a0d9bf3513d4ad02114983c8c9abb4dc58374a3f626937f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:8f502f586341ab0915e543524220fd69bc888551df7a5e4c05cda59b31dcaa20
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.4 MB (158392073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecd33fc84fe493b42f3dd21bf1ab8c86094431b9b1af8058c70a21bb58520c1`
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
# Fri, 07 Jan 2022 03:27:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='18d56640102a5e6b1326cc762dbf9ae19f00f81574f38ae1857d9f65761123ff';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='24af7fb9be209a68314dc341e5b62284d3625567872286f484cb296b9c551974';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='75ccfbaf6526ab854e193060110a9bef7878d186a95c3e0d57448ab96c09aa1a';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='200621b68eb39ae00ee875b31d6455bb2dcc5c8d050a4e4f8aa4fc7525a53d35';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='73f941590d60287d9d480884698120149bf2f9b8da04d2501b450f320a5be181';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 07 Jan 2022 03:27:07 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:33ee93795afea436bc51adcf292fea2b49d5a4051ff33ab0cc16357105957cea`  
		Last Modified: Fri, 07 Jan 2022 03:29:06 GMT  
		Size: 128.7 MB (128726677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; 386

```console
$ docker pull ibmjava@sha256:39702bdb2df40d46f05f2f96dcaafd0659326b33ce3e3abce31a1b6fb57ce1b9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147156762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db76404a02f291668782754055c23a227314dcafaa76d1130e1a5be5cbfcc757`
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
# Fri, 07 Jan 2022 01:56:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='18d56640102a5e6b1326cc762dbf9ae19f00f81574f38ae1857d9f65761123ff';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='24af7fb9be209a68314dc341e5b62284d3625567872286f484cb296b9c551974';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='75ccfbaf6526ab854e193060110a9bef7878d186a95c3e0d57448ab96c09aa1a';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='200621b68eb39ae00ee875b31d6455bb2dcc5c8d050a4e4f8aa4fc7525a53d35';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='73f941590d60287d9d480884698120149bf2f9b8da04d2501b450f320a5be181';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 07 Jan 2022 01:56:15 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:a16040488bf1a1a3787a90c167934d5a63118978dd076479c7d16f428a3f6a81`  
		Last Modified: Fri, 07 Jan 2022 01:58:27 GMT  
		Size: 117.0 MB (117011419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:269868c23629588bbdccc77a112d00116b568975c8686a903f4c3b2763d612be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.8 MB (161770422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca2cd6dc55b67013c1ac136463b4a40f96d412608622b97501d51a4dc5ee5b5`
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
# Fri, 07 Jan 2022 03:30:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='18d56640102a5e6b1326cc762dbf9ae19f00f81574f38ae1857d9f65761123ff';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='24af7fb9be209a68314dc341e5b62284d3625567872286f484cb296b9c551974';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='75ccfbaf6526ab854e193060110a9bef7878d186a95c3e0d57448ab96c09aa1a';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='200621b68eb39ae00ee875b31d6455bb2dcc5c8d050a4e4f8aa4fc7525a53d35';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='73f941590d60287d9d480884698120149bf2f9b8da04d2501b450f320a5be181';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 07 Jan 2022 03:30:11 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:8372d0c07db9ee4af75625eda00922334eb122c9730ed278ccf2668f02d09f82`  
		Last Modified: Fri, 07 Jan 2022 03:32:57 GMT  
		Size: 128.3 MB (128256173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:53d96c0e7c50d6e7f322299bd8da91c76d4aaf7a48c8821476d51faf6cfb66c4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.8 MB (153776376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cbf71042a76c21e2668fc10c7d2f960f04b7a9fbc90ca8e1e896451a29d2dfd`
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
# Fri, 07 Jan 2022 02:21:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='18d56640102a5e6b1326cc762dbf9ae19f00f81574f38ae1857d9f65761123ff';          YML_FILE='8.0/jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='24af7fb9be209a68314dc341e5b62284d3625567872286f484cb296b9c551974';          YML_FILE='8.0/jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='75ccfbaf6526ab854e193060110a9bef7878d186a95c3e0d57448ab96c09aa1a';          YML_FILE='8.0/jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='200621b68eb39ae00ee875b31d6455bb2dcc5c8d050a4e4f8aa4fc7525a53d35';          YML_FILE='8.0/jre/linux/s390/index.yml';          ;;        s390x)          ESUM='73f941590d60287d9d480884698120149bf2f9b8da04d2501b450f320a5be181';          YML_FILE='8.0/jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 07 Jan 2022 02:21:15 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
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
	-	`sha256:5948905ea3b7602d130be3b792486e9fa35aaf89ee11c6a87e63c7eabe5fdcf1`  
		Last Modified: Fri, 07 Jan 2022 02:23:25 GMT  
		Size: 125.7 MB (125737337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

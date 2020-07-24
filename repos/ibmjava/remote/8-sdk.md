## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:3226020572f49f573918d3c3e529b06f0ddb511bb3e8e9e9dd02f88a9b4a65f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:431e60c53a9ee1075ee961831b7e4c83a6c0ae8ae1d0d7c585cb0b0e8c02548b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.2 MB (197202515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ce57411be90bac0489c4cc69a683cb62382fbbc40261778e98c59a9572b08d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:08 GMT
ADD file:0b40d881e3e00d68de1f1df0a565385bb838144b83814df891c994f466e9efa2 in / 
# Mon, 06 Jul 2020 21:56:09 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:10 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:11 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:11 GMT
CMD ["/bin/bash"]
# Tue, 07 Jul 2020 00:12:33 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 07 Jul 2020 00:12:41 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:12:41 GMT
ENV JAVA_VERSION=1.8.0_sr6fp11
# Tue, 07 Jul 2020 00:15:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3bee7811d5beb382c4b08d1d1ca583613b88e79c4e631e47602baab4666b565b';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='543c7fbd0ee9f816026dd65933ba4e2ba885b5aa902e7866bab5bfa1911bd5bb';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d69ff7519e32e89db88a9a4d4d88d1881524073ac940f35d3860db2c6647be2e';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='898e741dcab49dd8aad35dd159f6909a32ae68ede442f5f56ac8ebdd47ad4183';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='560f41c60495b525fa70a4ec52f7061649b768b083b6577882ae5508b2e8653d';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 07 Jul 2020 00:15:11 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a1125296b23d78a3585a7910d649fbf0cc56284f9d2066e3243e8bc18f90b308`  
		Last Modified: Wed, 01 Jul 2020 12:21:40 GMT  
		Size: 26.7 MB (26696193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c742a4a0f38c95e690ad2dad8909c0cb232911418ac94a73da2a28becc7b734`  
		Last Modified: Mon, 06 Jul 2020 21:57:18 GMT  
		Size: 35.4 KB (35365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5ea3b329965bf7239f4e4f484915a444ec6d78b532ae12525934d4f6f7ac9a`  
		Last Modified: Mon, 06 Jul 2020 21:57:19 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4be91ead68299f53759fd80c135e0dde0eb797e91eb8fbc5a708a506e0c433`  
		Last Modified: Mon, 06 Jul 2020 21:57:19 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88deabb3b26fcc17ebbfec57f82d428134ba9ff9f281c1d085fb731c90238514`  
		Last Modified: Tue, 07 Jul 2020 00:15:28 GMT  
		Size: 3.0 MB (2957086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7770289d5b8cdb6dd2c11e0625f7ee6cca7322f3c7ef66c8ccecab2d34227b4`  
		Last Modified: Tue, 07 Jul 2020 00:16:09 GMT  
		Size: 167.5 MB (167512857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; 386

```console
$ docker pull ibmjava@sha256:4fb57524a082ff62f0fbde0f0b783b64d4561d254e51f760bc6abdc49ba45873
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185904704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12718c8304fcc4d3c1cf24e85af7114376a0ab339789ec5edc1e5ac9a98a34e2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jul 2020 14:40:18 GMT
ADD file:1041a59a13c0d49b1cb87f211694f68be4c9b76f2deb36e2d8955b77c4d2836f in / 
# Fri, 24 Jul 2020 14:40:19 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:40:20 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:40:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:40:21 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 14:56:28 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Jul 2020 14:56:40 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 14:56:40 GMT
ENV JAVA_VERSION=1.8.0_sr6fp11
# Fri, 24 Jul 2020 14:59:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3bee7811d5beb382c4b08d1d1ca583613b88e79c4e631e47602baab4666b565b';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='543c7fbd0ee9f816026dd65933ba4e2ba885b5aa902e7866bab5bfa1911bd5bb';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d69ff7519e32e89db88a9a4d4d88d1881524073ac940f35d3860db2c6647be2e';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='898e741dcab49dd8aad35dd159f6909a32ae68ede442f5f56ac8ebdd47ad4183';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='560f41c60495b525fa70a4ec52f7061649b768b083b6577882ae5508b2e8653d';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 24 Jul 2020 14:59:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:89823af3b784a3ef6d57a90159cbd5f28c863927aa03d4c43b44b6c37479fa1c`  
		Last Modified: Mon, 13 Jul 2020 15:46:56 GMT  
		Size: 27.1 MB (27123624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28677484c2569b014ecb876df3111b11e825c82629306b3af99a1c12f3b234e2`  
		Last Modified: Fri, 24 Jul 2020 14:40:50 GMT  
		Size: 34.6 KB (34611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c914b15d9c03339769ddd662b893654bbc371dbed4f8cdfa29ca1c57c0bb98e`  
		Last Modified: Fri, 24 Jul 2020 14:40:50 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dc7dbf6d65bca5959e6f7c892f468288c27e6a0ef07eec142d4497ee07e6cd`  
		Last Modified: Fri, 24 Jul 2020 14:40:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6390acddeaf0d5abd6917da9b4934d31bc7973be5b9dceb484774c00312c178`  
		Last Modified: Fri, 24 Jul 2020 14:59:13 GMT  
		Size: 3.0 MB (2982896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6b8c182f4e36476c58efa589521e3c26b58330d101d2a00a24e85e1c0930c5`  
		Last Modified: Fri, 24 Jul 2020 15:00:03 GMT  
		Size: 155.8 MB (155762562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:74b4ecd4a6768cd3df0b3e01b0bb9cb706dc7032fc3115ca0a3910639882d8e8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.6 MB (209621425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546485d08e5759cdbd83dbae76e3226965da3737815e676e42dfa2ac4e0a4c13`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 06 Jul 2020 22:11:55 GMT
ADD file:02f6904c1e662a7dcf6c813b0b166d2a793532babdd26486ccdf54c62e496d74 in / 
# Mon, 06 Jul 2020 22:12:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:12:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:12:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:12:39 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 23:15:15 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Mon, 06 Jul 2020 23:16:28 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 23:16:32 GMT
ENV JAVA_VERSION=1.8.0_sr6fp11
# Mon, 06 Jul 2020 23:20:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3bee7811d5beb382c4b08d1d1ca583613b88e79c4e631e47602baab4666b565b';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='543c7fbd0ee9f816026dd65933ba4e2ba885b5aa902e7866bab5bfa1911bd5bb';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d69ff7519e32e89db88a9a4d4d88d1881524073ac940f35d3860db2c6647be2e';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='898e741dcab49dd8aad35dd159f6909a32ae68ede442f5f56ac8ebdd47ad4183';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='560f41c60495b525fa70a4ec52f7061649b768b083b6577882ae5508b2e8653d';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Mon, 06 Jul 2020 23:21:11 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:9bf98a17426d75ff2afb0ce90ba51b39da3fbd14db0cbd75941ca79a027edf5b`  
		Last Modified: Mon, 06 Jul 2020 15:46:29 GMT  
		Size: 30.4 MB (30403476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0e6b7f1e0e442a73216c8f3a0be0d2541c137fd3387775bef4342bfb80c73d`  
		Last Modified: Mon, 06 Jul 2020 22:18:01 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2164204b75b39358091c51e041d91a70cee768036b72edaaa3c0a9d3b5f01bb4`  
		Last Modified: Mon, 06 Jul 2020 22:18:01 GMT  
		Size: 860.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8349a86bc0c340cfe9292a4a0743f0d20683515f048ac5b7a38bad559ebd5d`  
		Last Modified: Mon, 06 Jul 2020 22:18:01 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28d31b0685e687199f133a0499f1e0947877610faeaa561001d2ee14497d5a5`  
		Last Modified: Mon, 06 Jul 2020 23:21:34 GMT  
		Size: 3.1 MB (3075410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af89b8894688ba84738b0df5ebb18c9c9b6650b245f38d4cc0451f81e9919ee`  
		Last Modified: Mon, 06 Jul 2020 23:23:03 GMT  
		Size: 176.1 MB (176106291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:486a5bb7d55f34b589f0e92ed42ec7e40dd3e122f162034f7ba0ba56bcb36ecc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185933721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8c47e3d4ba0528bb8d768c488153412f35785ce7db78a7f1f63b3c22ca8732`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jul 2020 14:43:52 GMT
ADD file:03965719c666ec8be956f87c8fd8121313110d14fd14f25a85be1281e4ca000b in / 
# Fri, 24 Jul 2020 14:44:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:44:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:44:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:44:05 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 15:01:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Jul 2020 15:02:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 15:02:08 GMT
ENV JAVA_VERSION=1.8.0_sr6fp11
# Fri, 24 Jul 2020 15:05:17 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3bee7811d5beb382c4b08d1d1ca583613b88e79c4e631e47602baab4666b565b';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='543c7fbd0ee9f816026dd65933ba4e2ba885b5aa902e7866bab5bfa1911bd5bb';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='d69ff7519e32e89db88a9a4d4d88d1881524073ac940f35d3860db2c6647be2e';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='898e741dcab49dd8aad35dd159f6909a32ae68ede442f5f56ac8ebdd47ad4183';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='560f41c60495b525fa70a4ec52f7061649b768b083b6577882ae5508b2e8653d';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 24 Jul 2020 15:05:29 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:be08d3c199ef98c9593e956954bc77a9dbc438573a70702d7b3464d4e8d1ac41`  
		Last Modified: Mon, 13 Jul 2020 15:48:28 GMT  
		Size: 25.4 MB (25369527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d13cd4fc4b78e5f1f87dd7f9b563a260a4a858377937981e98c3246b6908cf`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 36.2 KB (36170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b49d28fc51a8e47b741fef4363cbf334000d3955d4bdef76622a0a5ba72a88`  
		Last Modified: Fri, 24 Jul 2020 14:45:31 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e784976bb1b84890c7c9256bdf2d9d634bc901a832f0724a5cf6d1e365e44f`  
		Last Modified: Fri, 24 Jul 2020 14:45:36 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a405adecbf26fa229b5a95f8e8bf05751335fb161fd163398048a3b477ee38`  
		Last Modified: Fri, 24 Jul 2020 15:05:54 GMT  
		Size: 2.7 MB (2672379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f1af58d0ebc2ce5e245b016dda803d889b52c3d40cf5153e48691718e39dbb`  
		Last Modified: Fri, 24 Jul 2020 15:06:48 GMT  
		Size: 157.9 MB (157854609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

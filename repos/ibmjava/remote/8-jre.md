## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:e70fdafd2f2e3c9540dab02af042a909629811e4b9b5ba2faa9f25d195ab5cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:ee19904bc8632b68559c37366b3c6a0482fe13e3c980af3ee21d81dcb7c3e116
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.5 MB (160463749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf6dd1557f8dd91fd993e90b298c0c79602268e406aa7464ffe6940ef9109aa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:22 GMT
ADD file:d7fa3c26651f9204a5629287a1a9a6e7dc6a0bc6eb499e82c433c0c8f67ff46b in / 
# Fri, 23 Apr 2021 22:21:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:25 GMT
CMD ["/bin/bash"]
# Sat, 24 Apr 2021 00:22:39 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Sat, 24 Apr 2021 00:22:49 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:22:49 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Sat, 24 Apr 2021 00:23:23 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Sat, 24 Apr 2021 00:23:24 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:01bf7da0a88c9e37ae418d17c0aeed0621524848d80ccb9e38c67e7ab8e11928`  
		Last Modified: Fri, 16 Apr 2021 15:20:23 GMT  
		Size: 26.7 MB (26697009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b4a5f15c7a0722b4f22e61b5387317eaf2602c27ffb2bceac9a25f19fbd156`  
		Last Modified: Fri, 23 Apr 2021 22:22:45 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ffbe87baa135002dddb7a7460082c5d6a352186e1be9464c5f31db81378824`  
		Last Modified: Fri, 23 Apr 2021 22:22:45 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efb27499fe25d5bffa55e2a37238fe3a0866fb1e210dba0ccff2fe5995b3ade`  
		Last Modified: Sat, 24 Apr 2021 00:25:17 GMT  
		Size: 3.0 MB (2959898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7050a00d84ec78029aa5162a487745608e888e27b3b9c4830582b322a52e7b62`  
		Last Modified: Sat, 24 Apr 2021 00:25:29 GMT  
		Size: 130.8 MB (130805802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; 386

```console
$ docker pull ibmjava@sha256:7f55127b9bfa584d8d3caaa2eb23949bae696786691c04ec131f1f97f9237475
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147717670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7322fbbb7b905ed4b19b233ce5aab725ccc4141e6aeff4fa24e60f9dbae013`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Apr 2021 22:39:49 GMT
ADD file:90725d5ecc587065bcac0f628d4fca740e70b473ad2304167c86a3929979ab6d in / 
# Fri, 23 Apr 2021 22:39:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:39:51 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:39:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:39:53 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 22:56:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 23 Apr 2021 22:56:57 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 18:39:02 GMT
ENV JAVA_VERSION=1.8.0_sr6fp30
# Wed, 19 May 2021 18:39:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='6a2e5fe690b38226e88cbba8ef6c1e9be4b0cdaa4c2321f9317833e892c01ffb';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='ce3d3fb3f9dd557724cb70af28b8f55819da610d56405c8212f5eecb7ad70b80';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='463138b32ef07140a8e6e3f3f3a92c802a1a945f992afa483d78888fde4bb41d';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='b9f1b1fc797ad14882c5dab32d6cb3f493cfa20b376031a88bd8577ef90f3293';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='f0ab1502ec69f76bbb9cf43aba71b6ad2e7a12fdedfbdcd943112c7eb9c77b35';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 May 2021 18:39:41 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:3ca505a8d0cb8bb3cbc0acdf7779f1042c7bdc466c7b025c91341342e5f91d11`  
		Last Modified: Fri, 23 Apr 2021 22:40:49 GMT  
		Size: 27.1 MB (27131171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d026bc940387371d3fe09319970ec5fb8b5412664a63d601a0b0d2ee6f932d`  
		Last Modified: Fri, 23 Apr 2021 22:40:43 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3c95f0f20e6979f6c17445cbb1ad51c1ad261f6a18edd64cc2cbe88fe56b7c`  
		Last Modified: Fri, 23 Apr 2021 22:40:43 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a16c08709439f10e0228f8ddd5aeee22678c1ffaf756f7c56377c229aeedcd2`  
		Last Modified: Fri, 23 Apr 2021 22:59:32 GMT  
		Size: 3.0 MB (2988497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c08bb6091d3da2336d713b2bde73e11cb589548834a3bae4160c6fbdbf42d4e`  
		Last Modified: Wed, 19 May 2021 18:42:39 GMT  
		Size: 117.6 MB (117596962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:075dc166cd683749093bac34517d565db03a2303cc37b2198c2127cee1a42ace
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.9 MB (163897744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cadf7d74cd84934f0a314a460a6bc1dc199eed589415b959af02ddeb10736a3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Apr 2021 22:30:25 GMT
ADD file:818f810cd30ef74fd4690c6265d80265647ba3353880cf8323500df6d2c48b69 in / 
# Fri, 23 Apr 2021 22:30:54 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:31:13 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:31:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:31:32 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:16:58 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 23 Apr 2021 23:17:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:17:43 GMT
ENV JAVA_VERSION=1.8.0_sr6fp26
# Fri, 23 Apr 2021 23:18:47 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='efa4b1b4f163133043eb99d1b276311201fc37bb60bfde051fd06c78cada038b';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='1f16f54b16bb978772c5ace5769a05233ba4a58de0e23d0542b0c0e55f95dd63';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='40b61a9bd4727d5dc1573ab69b1f973ffa14bf18f396a244f7263f7782173c98';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='4f52f3044658a232f2d8e77a275d1e95a6de90a6bf1e63a3ea6d7a87fa576d87';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='024b7c4691233016fff56bc9656e4979b283abbbe5751ddd98917944eaabdb10';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Fri, 23 Apr 2021 23:19:03 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:bb3095714506c08a64a49e29ab001d7000d94957d52e05db35361fd4a54c460c`  
		Last Modified: Fri, 23 Apr 2021 22:36:52 GMT  
		Size: 30.4 MB (30407300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd29acc6f7bfef8034eaca0bfb069f0d66e50351c84b062e224d6eae710afa79`  
		Last Modified: Fri, 23 Apr 2021 22:36:46 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7645fc50c9e70df51732b36ef7f8b21ebacd148c3bee4f1b29ca6dcba1bbb949`  
		Last Modified: Fri, 23 Apr 2021 22:36:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab6dc42492fe0eca98f1e563f3e8dabb70f122b45b752264bacb4ea14f59354`  
		Last Modified: Fri, 23 Apr 2021 23:22:26 GMT  
		Size: 3.1 MB (3082775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510992b332e039a7852bef411702a4b667a17ae9ef201c9118477ccc53172fa8`  
		Last Modified: Fri, 23 Apr 2021 23:22:40 GMT  
		Size: 130.4 MB (130406625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:b9944c5d401c9c0635bff71ce34bd2ee0d2587c2b91d944f658b35808fcc32a2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154571874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7963f562010cfabfc2ef80b31fa5a95ea8e503892947eea672b948b01d7a16ae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 23 Apr 2021 21:45:00 GMT
ADD file:5e61a5300d520d61a2130623465ba2e46da8e80dc2afa042473a42cbcd8d88d2 in / 
# Fri, 23 Apr 2021 21:45:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 21:45:05 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 21:45:07 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 21:45:07 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 22:25:02 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 23 Apr 2021 22:25:16 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 May 2021 18:41:40 GMT
ENV JAVA_VERSION=1.8.0_sr6fp30
# Wed, 19 May 2021 18:42:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='6a2e5fe690b38226e88cbba8ef6c1e9be4b0cdaa4c2321f9317833e892c01ffb';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='ce3d3fb3f9dd557724cb70af28b8f55819da610d56405c8212f5eecb7ad70b80';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='463138b32ef07140a8e6e3f3f3a92c802a1a945f992afa483d78888fde4bb41d';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='b9f1b1fc797ad14882c5dab32d6cb3f493cfa20b376031a88bd8577ef90f3293';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='f0ab1502ec69f76bbb9cf43aba71b6ad2e7a12fdedfbdcd943112c7eb9c77b35';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 May 2021 18:42:39 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:33ddddc4572ffe1f294f9f599ed989cc41eee5da4cdcf7db12d10700aa8c894e`  
		Last Modified: Fri, 23 Apr 2021 21:47:03 GMT  
		Size: 25.4 MB (25352756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4395f372a786db91b2f50dc8e43d8b7c3533eb4bd86f6728eb2a0c7108c077d2`  
		Last Modified: Fri, 23 Apr 2021 21:46:59 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e39753730df188282ca8193f14bbbb8cbe0b76ec02b34283a28449b1e41c05`  
		Last Modified: Fri, 23 Apr 2021 21:47:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e93b87da546ac7aa6705cd2f20bfe70cf04793ac73561e5dd8c579af88754aec`  
		Last Modified: Fri, 23 Apr 2021 22:28:41 GMT  
		Size: 2.7 MB (2676643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98c603bb7baabbba78bb559c62a8640d80fda2f790dea51bb7cfb2e968b1529`  
		Last Modified: Wed, 19 May 2021 18:45:16 GMT  
		Size: 126.5 MB (126541435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

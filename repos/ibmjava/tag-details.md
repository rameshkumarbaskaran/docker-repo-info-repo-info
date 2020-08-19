<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ibmjava`

-	[`ibmjava:8`](#ibmjava8)
-	[`ibmjava:8-jre`](#ibmjava8-jre)
-	[`ibmjava:8-jre-alpine`](#ibmjava8-jre-alpine)
-	[`ibmjava:8-sdk`](#ibmjava8-sdk)
-	[`ibmjava:8-sdk-alpine`](#ibmjava8-sdk-alpine)
-	[`ibmjava:8-sfj`](#ibmjava8-sfj)
-	[`ibmjava:8-sfj-alpine`](#ibmjava8-sfj-alpine)
-	[`ibmjava:jre`](#ibmjavajre)
-	[`ibmjava:jre-alpine`](#ibmjavajre-alpine)
-	[`ibmjava:latest`](#ibmjavalatest)
-	[`ibmjava:sdk`](#ibmjavasdk)
-	[`ibmjava:sdk-alpine`](#ibmjavasdk-alpine)
-	[`ibmjava:sfj`](#ibmjavasfj)
-	[`ibmjava:sfj-alpine`](#ibmjavasfj-alpine)

## `ibmjava:8`

```console
$ docker pull ibmjava@sha256:801fafdfd6b0d2692551ee5fcae8c22932370fb06f35dc0a47af40bb3d1f6ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8` - linux; amd64

```console
$ docker pull ibmjava@sha256:1f0f9320f40f3a719432c78b0dbf14b450a6cda1db913f9cf66d0dfdc02a327a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159913209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b67bdce293c9995d072bdf01f82459ab1b4abda93b43352fffac8045d7701f7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:19 GMT
ADD file:7d9bbf45a5b2510d44d3206a028cf6502757884d49e46d3d2e6356c3a92c4309 in / 
# Fri, 24 Jul 2020 14:38:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:22 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:11:53 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Jul 2020 16:12:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 22:19:53 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 05 Aug 2020 22:20:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b532b712f4f3cae2af0794d3f3859489b794e2bf1971f05b04098cdd4826672';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='dc70e8d2a9a1690a810352bf0993a6c32e323073938ff157381769e04d38d2be';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='8b1a383e7027b0783c07d736b3b5e31e26205e10e1b14d2ac942d4ee9a4b5d29';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='142bf26a6de087ad5edc4e673c38368b2fe00e3d00f35f9d7382f7a929b560d7';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9e30f6c9f98cfc64c10299627fe6158100ce63e2d2d299c8263c465e8f3138f9';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 05 Aug 2020 22:20:34 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7595c8c21622ea8a8b9778972e26dbbe063f7a1c4b0a28a80a34ebb3d343b586`  
		Last Modified: Mon, 13 Jul 2020 15:46:50 GMT  
		Size: 26.7 MB (26697127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af8ca898f36af68711cb67c345f65046a78ccd802453f4b129adf9205b1f8`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70799171ddba93a611490ba3557d782714b3f4da8963d49ac8726786ba8274a5`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c12202c5ef07dc9eb8f9d9e71407064684ed70f8c4040b62679b7d30200840`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3b48ae14e45cf7769bcc5ef96dd1a0d4389a21fd1de5c54169068b1730e569`  
		Last Modified: Fri, 24 Jul 2020 16:14:39 GMT  
		Size: 3.0 MB (2957372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ec5fdbe0e16348f4573b4d5009a350cf91b0507de9f6ee11165110da89b999`  
		Last Modified: Wed, 05 Aug 2020 22:24:59 GMT  
		Size: 130.2 MB (130222337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; 386

```console
$ docker pull ibmjava@sha256:f985e9b27c7895746c69e8ee336650254e6a9cf53c9b021f5f48f01122c2e063
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148691210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa00f05bb49b5a0ea57c2a58c6b2c1c02c66dcf6c4f61fdc83aa1cc95c5e033`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:47:40 GMT
ADD file:a2194fb1eb3c0e5832ad1c48e01faa517517697c7b45617fa0076fe1923711b1 in / 
# Wed, 19 Aug 2020 21:47:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:47:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:47:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:47:43 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:29:35 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 19 Aug 2020 22:29:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:29:44 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 19 Aug 2020 22:30:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b532b712f4f3cae2af0794d3f3859489b794e2bf1971f05b04098cdd4826672';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='dc70e8d2a9a1690a810352bf0993a6c32e323073938ff157381769e04d38d2be';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='8b1a383e7027b0783c07d736b3b5e31e26205e10e1b14d2ac942d4ee9a4b5d29';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='142bf26a6de087ad5edc4e673c38368b2fe00e3d00f35f9d7382f7a929b560d7';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9e30f6c9f98cfc64c10299627fe6158100ce63e2d2d299c8263c465e8f3138f9';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 Aug 2020 22:30:26 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:92ea639593649ab4b1d9a883cdee9a0c9ae490627a0a1e6b59d8962c94344d26`  
		Last Modified: Mon, 10 Aug 2020 14:27:54 GMT  
		Size: 27.1 MB (27124431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3de4f8866d6f8a7d6156f69d1684a0ffa16a4599d643cfb15061cf3eee5b2b6`  
		Last Modified: Wed, 19 Aug 2020 21:48:21 GMT  
		Size: 34.6 KB (34614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81cd73faed83d22ac56f653202675d246ace7921595d662985d5c6bf97668ad`  
		Last Modified: Wed, 19 Aug 2020 21:48:21 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d1af387dbe587e075a0fb09360f570e42daa62711aec6f26ad0c9c8d89b703`  
		Last Modified: Wed, 19 Aug 2020 21:48:21 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987ad5b9a08284cb8a30668b82cd354ea3c797c73b3a84645b8c2d16856b93db`  
		Last Modified: Wed, 19 Aug 2020 22:32:23 GMT  
		Size: 3.0 MB (2982729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20687db51cbd60eec816304bb11551919dd48ffd371ecec94b3b50bf3fd14a62`  
		Last Modified: Wed, 19 Aug 2020 22:32:35 GMT  
		Size: 118.5 MB (118548423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:bd87048f17e799c54e3f570e7de474cbc4602411645ef02f58232d2fa4f9607a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163310510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4153449699bd33da7767d00f6b222d6dd7b26d8ec12d5b08abd057ee8639129a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:14:04 GMT
ADD file:4954b2b03fa4bd48fabecbc1facd6d05808f55a143012aca45648ab2f767042a in / 
# Wed, 19 Aug 2020 21:14:14 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:14:22 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:14:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:14:32 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:50:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 19 Aug 2020 22:53:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:53:13 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 19 Aug 2020 22:54:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b532b712f4f3cae2af0794d3f3859489b794e2bf1971f05b04098cdd4826672';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='dc70e8d2a9a1690a810352bf0993a6c32e323073938ff157381769e04d38d2be';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='8b1a383e7027b0783c07d736b3b5e31e26205e10e1b14d2ac942d4ee9a4b5d29';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='142bf26a6de087ad5edc4e673c38368b2fe00e3d00f35f9d7382f7a929b560d7';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9e30f6c9f98cfc64c10299627fe6158100ce63e2d2d299c8263c465e8f3138f9';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 Aug 2020 22:54:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:23e4ce51557a90638716607f36b99292ea21b3e246ef66f83934e1eadb095632`  
		Last Modified: Mon, 10 Aug 2020 15:49:13 GMT  
		Size: 30.4 MB (30408877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b20479dd2a1972abd69e09a781025590f55fcbe8bef98a35b1067dceff85d60`  
		Last Modified: Wed, 19 Aug 2020 21:18:51 GMT  
		Size: 35.2 KB (35223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3107678818d326669afdd9fcce37d6b61613c2103e889ff7e019515b97ade1d`  
		Last Modified: Wed, 19 Aug 2020 21:18:51 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a571510b31b5805e20c811dcbb2413f66118e4be6a44a54c430826d8be670e7`  
		Last Modified: Wed, 19 Aug 2020 21:18:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9538a963d435f5fe1ba7326731a3fee312a667305ccdd70f519c5c40c2191d77`  
		Last Modified: Wed, 19 Aug 2020 22:57:56 GMT  
		Size: 3.1 MB (3075385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede11ddbd034b571963e94ea1a9d515b44d07dfafb6cc59988895ab675987187`  
		Last Modified: Wed, 19 Aug 2020 22:58:09 GMT  
		Size: 129.8 MB (129789980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8` - linux; s390x

```console
$ docker pull ibmjava@sha256:77041f0c019a7731275948ba4db3d16ea7cd24230d33e08a0ba9e9ddd402f353
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155547246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7246bd293e5b3ee65f71644f2a52459c2a179c7bcc44a1ed87884469821301a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:10:03 GMT
ADD file:1343b5ae7d875bd32e4eac552ae10c9631788fd97b99bcdeb9f6a9b85c230ba2 in / 
# Wed, 19 Aug 2020 21:10:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:10:05 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:10:06 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:10:06 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:08:24 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 19 Aug 2020 22:08:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:08:31 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 19 Aug 2020 22:09:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b532b712f4f3cae2af0794d3f3859489b794e2bf1971f05b04098cdd4826672';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='dc70e8d2a9a1690a810352bf0993a6c32e323073938ff157381769e04d38d2be';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='8b1a383e7027b0783c07d736b3b5e31e26205e10e1b14d2ac942d4ee9a4b5d29';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='142bf26a6de087ad5edc4e673c38368b2fe00e3d00f35f9d7382f7a929b560d7';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9e30f6c9f98cfc64c10299627fe6158100ce63e2d2d299c8263c465e8f3138f9';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 Aug 2020 22:09:15 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:25294e13856fd30261115dbfc6dd49e2d854414d32c9ead824b8183a83620e5c`  
		Last Modified: Mon, 10 Aug 2020 15:49:57 GMT  
		Size: 25.4 MB (25371147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e4b14541a6306ab7ffae9ed980e3ebac039f590869efecf63c6d745e1cde3c`  
		Last Modified: Wed, 19 Aug 2020 21:11:08 GMT  
		Size: 36.2 KB (36170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4164a02312fb3bccad51789030500218898a262ff17a962d62bb9849c9103d59`  
		Last Modified: Wed, 19 Aug 2020 21:11:08 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68677136804619b55f0437044d91d7bfe75e0b8013ca953c0d4db40c4d91d6b`  
		Last Modified: Wed, 19 Aug 2020 21:11:08 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2d7c1e4e8846aa212e0c088d2fa25dfc2856f64869c0721aaa4ef1499a7999`  
		Last Modified: Wed, 19 Aug 2020 22:11:12 GMT  
		Size: 2.7 MB (2672211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d120780fc389b1bd05d629730a20d12da94d18558bf4fe290f22dd0d97f379`  
		Last Modified: Wed, 19 Aug 2020 22:11:21 GMT  
		Size: 127.5 MB (127466682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-jre`

```console
$ docker pull ibmjava@sha256:801fafdfd6b0d2692551ee5fcae8c22932370fb06f35dc0a47af40bb3d1f6ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:1f0f9320f40f3a719432c78b0dbf14b450a6cda1db913f9cf66d0dfdc02a327a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159913209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b67bdce293c9995d072bdf01f82459ab1b4abda93b43352fffac8045d7701f7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:19 GMT
ADD file:7d9bbf45a5b2510d44d3206a028cf6502757884d49e46d3d2e6356c3a92c4309 in / 
# Fri, 24 Jul 2020 14:38:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:22 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:11:53 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Jul 2020 16:12:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 22:19:53 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 05 Aug 2020 22:20:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b532b712f4f3cae2af0794d3f3859489b794e2bf1971f05b04098cdd4826672';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='dc70e8d2a9a1690a810352bf0993a6c32e323073938ff157381769e04d38d2be';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='8b1a383e7027b0783c07d736b3b5e31e26205e10e1b14d2ac942d4ee9a4b5d29';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='142bf26a6de087ad5edc4e673c38368b2fe00e3d00f35f9d7382f7a929b560d7';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9e30f6c9f98cfc64c10299627fe6158100ce63e2d2d299c8263c465e8f3138f9';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 05 Aug 2020 22:20:34 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7595c8c21622ea8a8b9778972e26dbbe063f7a1c4b0a28a80a34ebb3d343b586`  
		Last Modified: Mon, 13 Jul 2020 15:46:50 GMT  
		Size: 26.7 MB (26697127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af8ca898f36af68711cb67c345f65046a78ccd802453f4b129adf9205b1f8`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70799171ddba93a611490ba3557d782714b3f4da8963d49ac8726786ba8274a5`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c12202c5ef07dc9eb8f9d9e71407064684ed70f8c4040b62679b7d30200840`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3b48ae14e45cf7769bcc5ef96dd1a0d4389a21fd1de5c54169068b1730e569`  
		Last Modified: Fri, 24 Jul 2020 16:14:39 GMT  
		Size: 3.0 MB (2957372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ec5fdbe0e16348f4573b4d5009a350cf91b0507de9f6ee11165110da89b999`  
		Last Modified: Wed, 05 Aug 2020 22:24:59 GMT  
		Size: 130.2 MB (130222337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; 386

```console
$ docker pull ibmjava@sha256:f985e9b27c7895746c69e8ee336650254e6a9cf53c9b021f5f48f01122c2e063
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148691210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa00f05bb49b5a0ea57c2a58c6b2c1c02c66dcf6c4f61fdc83aa1cc95c5e033`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:47:40 GMT
ADD file:a2194fb1eb3c0e5832ad1c48e01faa517517697c7b45617fa0076fe1923711b1 in / 
# Wed, 19 Aug 2020 21:47:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:47:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:47:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:47:43 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:29:35 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 19 Aug 2020 22:29:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:29:44 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 19 Aug 2020 22:30:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b532b712f4f3cae2af0794d3f3859489b794e2bf1971f05b04098cdd4826672';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='dc70e8d2a9a1690a810352bf0993a6c32e323073938ff157381769e04d38d2be';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='8b1a383e7027b0783c07d736b3b5e31e26205e10e1b14d2ac942d4ee9a4b5d29';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='142bf26a6de087ad5edc4e673c38368b2fe00e3d00f35f9d7382f7a929b560d7';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9e30f6c9f98cfc64c10299627fe6158100ce63e2d2d299c8263c465e8f3138f9';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 Aug 2020 22:30:26 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:92ea639593649ab4b1d9a883cdee9a0c9ae490627a0a1e6b59d8962c94344d26`  
		Last Modified: Mon, 10 Aug 2020 14:27:54 GMT  
		Size: 27.1 MB (27124431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3de4f8866d6f8a7d6156f69d1684a0ffa16a4599d643cfb15061cf3eee5b2b6`  
		Last Modified: Wed, 19 Aug 2020 21:48:21 GMT  
		Size: 34.6 KB (34614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81cd73faed83d22ac56f653202675d246ace7921595d662985d5c6bf97668ad`  
		Last Modified: Wed, 19 Aug 2020 21:48:21 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d1af387dbe587e075a0fb09360f570e42daa62711aec6f26ad0c9c8d89b703`  
		Last Modified: Wed, 19 Aug 2020 21:48:21 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987ad5b9a08284cb8a30668b82cd354ea3c797c73b3a84645b8c2d16856b93db`  
		Last Modified: Wed, 19 Aug 2020 22:32:23 GMT  
		Size: 3.0 MB (2982729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20687db51cbd60eec816304bb11551919dd48ffd371ecec94b3b50bf3fd14a62`  
		Last Modified: Wed, 19 Aug 2020 22:32:35 GMT  
		Size: 118.5 MB (118548423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:bd87048f17e799c54e3f570e7de474cbc4602411645ef02f58232d2fa4f9607a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163310510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4153449699bd33da7767d00f6b222d6dd7b26d8ec12d5b08abd057ee8639129a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:14:04 GMT
ADD file:4954b2b03fa4bd48fabecbc1facd6d05808f55a143012aca45648ab2f767042a in / 
# Wed, 19 Aug 2020 21:14:14 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:14:22 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:14:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:14:32 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:50:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 19 Aug 2020 22:53:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:53:13 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 19 Aug 2020 22:54:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b532b712f4f3cae2af0794d3f3859489b794e2bf1971f05b04098cdd4826672';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='dc70e8d2a9a1690a810352bf0993a6c32e323073938ff157381769e04d38d2be';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='8b1a383e7027b0783c07d736b3b5e31e26205e10e1b14d2ac942d4ee9a4b5d29';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='142bf26a6de087ad5edc4e673c38368b2fe00e3d00f35f9d7382f7a929b560d7';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9e30f6c9f98cfc64c10299627fe6158100ce63e2d2d299c8263c465e8f3138f9';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 Aug 2020 22:54:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:23e4ce51557a90638716607f36b99292ea21b3e246ef66f83934e1eadb095632`  
		Last Modified: Mon, 10 Aug 2020 15:49:13 GMT  
		Size: 30.4 MB (30408877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b20479dd2a1972abd69e09a781025590f55fcbe8bef98a35b1067dceff85d60`  
		Last Modified: Wed, 19 Aug 2020 21:18:51 GMT  
		Size: 35.2 KB (35223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3107678818d326669afdd9fcce37d6b61613c2103e889ff7e019515b97ade1d`  
		Last Modified: Wed, 19 Aug 2020 21:18:51 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a571510b31b5805e20c811dcbb2413f66118e4be6a44a54c430826d8be670e7`  
		Last Modified: Wed, 19 Aug 2020 21:18:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9538a963d435f5fe1ba7326731a3fee312a667305ccdd70f519c5c40c2191d77`  
		Last Modified: Wed, 19 Aug 2020 22:57:56 GMT  
		Size: 3.1 MB (3075385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede11ddbd034b571963e94ea1a9d515b44d07dfafb6cc59988895ab675987187`  
		Last Modified: Wed, 19 Aug 2020 22:58:09 GMT  
		Size: 129.8 MB (129789980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:77041f0c019a7731275948ba4db3d16ea7cd24230d33e08a0ba9e9ddd402f353
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155547246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7246bd293e5b3ee65f71644f2a52459c2a179c7bcc44a1ed87884469821301a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:10:03 GMT
ADD file:1343b5ae7d875bd32e4eac552ae10c9631788fd97b99bcdeb9f6a9b85c230ba2 in / 
# Wed, 19 Aug 2020 21:10:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:10:05 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:10:06 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:10:06 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:08:24 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 19 Aug 2020 22:08:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:08:31 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 19 Aug 2020 22:09:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b532b712f4f3cae2af0794d3f3859489b794e2bf1971f05b04098cdd4826672';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='dc70e8d2a9a1690a810352bf0993a6c32e323073938ff157381769e04d38d2be';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='8b1a383e7027b0783c07d736b3b5e31e26205e10e1b14d2ac942d4ee9a4b5d29';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='142bf26a6de087ad5edc4e673c38368b2fe00e3d00f35f9d7382f7a929b560d7';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9e30f6c9f98cfc64c10299627fe6158100ce63e2d2d299c8263c465e8f3138f9';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 Aug 2020 22:09:15 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:25294e13856fd30261115dbfc6dd49e2d854414d32c9ead824b8183a83620e5c`  
		Last Modified: Mon, 10 Aug 2020 15:49:57 GMT  
		Size: 25.4 MB (25371147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e4b14541a6306ab7ffae9ed980e3ebac039f590869efecf63c6d745e1cde3c`  
		Last Modified: Wed, 19 Aug 2020 21:11:08 GMT  
		Size: 36.2 KB (36170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4164a02312fb3bccad51789030500218898a262ff17a962d62bb9849c9103d59`  
		Last Modified: Wed, 19 Aug 2020 21:11:08 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68677136804619b55f0437044d91d7bfe75e0b8013ca953c0d4db40c4d91d6b`  
		Last Modified: Wed, 19 Aug 2020 21:11:08 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2d7c1e4e8846aa212e0c088d2fa25dfc2856f64869c0721aaa4ef1499a7999`  
		Last Modified: Wed, 19 Aug 2020 22:11:12 GMT  
		Size: 2.7 MB (2672211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d120780fc389b1bd05d629730a20d12da94d18558bf4fe290f22dd0d97f379`  
		Last Modified: Wed, 19 Aug 2020 22:11:21 GMT  
		Size: 127.5 MB (127466682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-jre-alpine`

```console
$ docker pull ibmjava@sha256:b0bab7ccc9dcd6fde9093789ffaf20cb283a0566d592c95de4b067c3e667f965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ibmjava:8-jre-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:46020f520ec3909e7950f847298cb74ce5b091ae592364acfa38e5c79512ff7e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138546090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedf54e322c9e103b7ed7c91bd48de5563270c8c166245d6a1fed84b6ac3a325`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2020 19:19:49 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 19 Jun 2020 19:19:50 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Fri, 19 Jun 2020 19:20:01 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Wed, 05 Aug 2020 22:20:40 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 05 Aug 2020 22:21:21 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b532b712f4f3cae2af0794d3f3859489b794e2bf1971f05b04098cdd4826672';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='dc70e8d2a9a1690a810352bf0993a6c32e323073938ff157381769e04d38d2be';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='8b1a383e7027b0783c07d736b3b5e31e26205e10e1b14d2ac942d4ee9a4b5d29';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='142bf26a6de087ad5edc4e673c38368b2fe00e3d00f35f9d7382f7a929b560d7';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9e30f6c9f98cfc64c10299627fe6158100ce63e2d2d299c8263c465e8f3138f9';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Wed, 05 Aug 2020 22:21:21 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54cb4ffe99c5f24fd5d9092d445c28497122a55355fd862f3431fe39b0069a3d`  
		Last Modified: Fri, 19 Jun 2020 19:22:30 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579fa70fe6805ba9995c002270c4bef412288205c0c631288438cdd962583a0d`  
		Last Modified: Fri, 19 Jun 2020 19:22:31 GMT  
		Size: 5.5 MB (5539665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c18a5b31bcf01d0017d5bc8d3006473719f9305ce3add67784617e801ee6131`  
		Last Modified: Wed, 05 Aug 2020 22:25:37 GMT  
		Size: 130.2 MB (130208339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sdk`

```console
$ docker pull ibmjava@sha256:04d6d89bc21e1d417e185eb035366b94f430a55995abb4c1db83d4b215f31616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:f9de30bff3d3529d6625c8da0369ce7d35f9063fd239c8a1adefc976d7ee8f43
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.1 MB (197080972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:191ab39d7fa77274554cc296db7802ec058a59d6d435b5ac11c7db8e4dc5a108`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:19 GMT
ADD file:7d9bbf45a5b2510d44d3206a028cf6502757884d49e46d3d2e6356c3a92c4309 in / 
# Fri, 24 Jul 2020 14:38:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:22 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:11:53 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Jul 2020 16:12:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 22:19:53 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 05 Aug 2020 22:23:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='1770fc44e0061a72ab9cfc47fb9a1934b17581fee77a3cc32e83b4bee0084256';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='00e56752a6c8206b7d4990d6a3f9d4456bd2ffcde7165b0c150b8084cb961df8';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2020c805a8019fbc903a2fb5d7e5cc5190c6c83ba92a93730b84ed33a06be9fc';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='a4a01a2372ca7f4cd039e72fa9826403300eb4867ab735760b99514a5c8b4908';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='7bd69fa987bad2b0681a474b6c2775a6466586c64e99535a9ba96ed0dccd69ea';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 05 Aug 2020 22:23:31 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7595c8c21622ea8a8b9778972e26dbbe063f7a1c4b0a28a80a34ebb3d343b586`  
		Last Modified: Mon, 13 Jul 2020 15:46:50 GMT  
		Size: 26.7 MB (26697127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af8ca898f36af68711cb67c345f65046a78ccd802453f4b129adf9205b1f8`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70799171ddba93a611490ba3557d782714b3f4da8963d49ac8726786ba8274a5`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c12202c5ef07dc9eb8f9d9e71407064684ed70f8c4040b62679b7d30200840`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3b48ae14e45cf7769bcc5ef96dd1a0d4389a21fd1de5c54169068b1730e569`  
		Last Modified: Fri, 24 Jul 2020 16:14:39 GMT  
		Size: 3.0 MB (2957372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68167569e9e6620bef5744d4ef36d4b69b2d7b92c9ca25b2f785561d207b3ff6`  
		Last Modified: Wed, 05 Aug 2020 22:26:25 GMT  
		Size: 167.4 MB (167390100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; 386

```console
$ docker pull ibmjava@sha256:62c2e177f7e670c64e1d730fcc30cd9ea4d208946096c55827cd56b67549be6b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.7 MB (185749351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8afc08b098d9dde268068d9e8955241b481a09a711efbd13dc4ae87e4d9daa5a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:47:40 GMT
ADD file:a2194fb1eb3c0e5832ad1c48e01faa517517697c7b45617fa0076fe1923711b1 in / 
# Wed, 19 Aug 2020 21:47:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:47:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:47:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:47:43 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:29:35 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 19 Aug 2020 22:29:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:29:44 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 19 Aug 2020 22:32:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='1770fc44e0061a72ab9cfc47fb9a1934b17581fee77a3cc32e83b4bee0084256';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='00e56752a6c8206b7d4990d6a3f9d4456bd2ffcde7165b0c150b8084cb961df8';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2020c805a8019fbc903a2fb5d7e5cc5190c6c83ba92a93730b84ed33a06be9fc';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='a4a01a2372ca7f4cd039e72fa9826403300eb4867ab735760b99514a5c8b4908';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='7bd69fa987bad2b0681a474b6c2775a6466586c64e99535a9ba96ed0dccd69ea';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 Aug 2020 22:32:10 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:92ea639593649ab4b1d9a883cdee9a0c9ae490627a0a1e6b59d8962c94344d26`  
		Last Modified: Mon, 10 Aug 2020 14:27:54 GMT  
		Size: 27.1 MB (27124431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3de4f8866d6f8a7d6156f69d1684a0ffa16a4599d643cfb15061cf3eee5b2b6`  
		Last Modified: Wed, 19 Aug 2020 21:48:21 GMT  
		Size: 34.6 KB (34614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81cd73faed83d22ac56f653202675d246ace7921595d662985d5c6bf97668ad`  
		Last Modified: Wed, 19 Aug 2020 21:48:21 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d1af387dbe587e075a0fb09360f570e42daa62711aec6f26ad0c9c8d89b703`  
		Last Modified: Wed, 19 Aug 2020 21:48:21 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987ad5b9a08284cb8a30668b82cd354ea3c797c73b3a84645b8c2d16856b93db`  
		Last Modified: Wed, 19 Aug 2020 22:32:23 GMT  
		Size: 3.0 MB (2982729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c449430090068659f9fffd3495633f9f08759364f27f4d1cf43eac45d7842faf`  
		Last Modified: Wed, 19 Aug 2020 22:33:14 GMT  
		Size: 155.6 MB (155606564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:c64ee4cec2a85b5ab5b25c72272f4a732737e6b2d948d5086fc9050105bfe56d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.6 MB (200600313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fb20779f8fcf88da7077d669a50945030ae85e1734672879ff859f063a3d7e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:14:04 GMT
ADD file:4954b2b03fa4bd48fabecbc1facd6d05808f55a143012aca45648ab2f767042a in / 
# Wed, 19 Aug 2020 21:14:14 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:14:22 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:14:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:14:32 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:50:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 19 Aug 2020 22:53:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:53:13 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 19 Aug 2020 22:57:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='1770fc44e0061a72ab9cfc47fb9a1934b17581fee77a3cc32e83b4bee0084256';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='00e56752a6c8206b7d4990d6a3f9d4456bd2ffcde7165b0c150b8084cb961df8';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2020c805a8019fbc903a2fb5d7e5cc5190c6c83ba92a93730b84ed33a06be9fc';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='a4a01a2372ca7f4cd039e72fa9826403300eb4867ab735760b99514a5c8b4908';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='7bd69fa987bad2b0681a474b6c2775a6466586c64e99535a9ba96ed0dccd69ea';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 Aug 2020 22:57:25 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:23e4ce51557a90638716607f36b99292ea21b3e246ef66f83934e1eadb095632`  
		Last Modified: Mon, 10 Aug 2020 15:49:13 GMT  
		Size: 30.4 MB (30408877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b20479dd2a1972abd69e09a781025590f55fcbe8bef98a35b1067dceff85d60`  
		Last Modified: Wed, 19 Aug 2020 21:18:51 GMT  
		Size: 35.2 KB (35223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3107678818d326669afdd9fcce37d6b61613c2103e889ff7e019515b97ade1d`  
		Last Modified: Wed, 19 Aug 2020 21:18:51 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a571510b31b5805e20c811dcbb2413f66118e4be6a44a54c430826d8be670e7`  
		Last Modified: Wed, 19 Aug 2020 21:18:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9538a963d435f5fe1ba7326731a3fee312a667305ccdd70f519c5c40c2191d77`  
		Last Modified: Wed, 19 Aug 2020 22:57:56 GMT  
		Size: 3.1 MB (3075385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3167be622de99c1fad74b9f24c68f72bf72550248db56df665841964581d327`  
		Last Modified: Wed, 19 Aug 2020 22:59:05 GMT  
		Size: 167.1 MB (167079783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:d8609d5288ce92f50dc06c9a679751176e8007d01309472e59218662ae341a48
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185799868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a66b1b1f370f7a037e68add3375b5faa7737af2cb44da53009815c440eec2b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:10:03 GMT
ADD file:1343b5ae7d875bd32e4eac552ae10c9631788fd97b99bcdeb9f6a9b85c230ba2 in / 
# Wed, 19 Aug 2020 21:10:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:10:05 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:10:06 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:10:06 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:08:24 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 19 Aug 2020 22:08:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:08:31 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 19 Aug 2020 22:10:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='1770fc44e0061a72ab9cfc47fb9a1934b17581fee77a3cc32e83b4bee0084256';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='00e56752a6c8206b7d4990d6a3f9d4456bd2ffcde7165b0c150b8084cb961df8';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2020c805a8019fbc903a2fb5d7e5cc5190c6c83ba92a93730b84ed33a06be9fc';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='a4a01a2372ca7f4cd039e72fa9826403300eb4867ab735760b99514a5c8b4908';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='7bd69fa987bad2b0681a474b6c2775a6466586c64e99535a9ba96ed0dccd69ea';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 Aug 2020 22:11:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:25294e13856fd30261115dbfc6dd49e2d854414d32c9ead824b8183a83620e5c`  
		Last Modified: Mon, 10 Aug 2020 15:49:57 GMT  
		Size: 25.4 MB (25371147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e4b14541a6306ab7ffae9ed980e3ebac039f590869efecf63c6d745e1cde3c`  
		Last Modified: Wed, 19 Aug 2020 21:11:08 GMT  
		Size: 36.2 KB (36170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4164a02312fb3bccad51789030500218898a262ff17a962d62bb9849c9103d59`  
		Last Modified: Wed, 19 Aug 2020 21:11:08 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68677136804619b55f0437044d91d7bfe75e0b8013ca953c0d4db40c4d91d6b`  
		Last Modified: Wed, 19 Aug 2020 21:11:08 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2d7c1e4e8846aa212e0c088d2fa25dfc2856f64869c0721aaa4ef1499a7999`  
		Last Modified: Wed, 19 Aug 2020 22:11:12 GMT  
		Size: 2.7 MB (2672211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b44d28c857b0538d6586c0e76fe1c491359c0e9a37a2a048a3f2941e0b11318`  
		Last Modified: Wed, 19 Aug 2020 22:11:53 GMT  
		Size: 157.7 MB (157719304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sdk-alpine`

```console
$ docker pull ibmjava@sha256:ef5aa44cbd90ebd3ee940ee987cf8d518838f6ccf6186fb150bb54f5bab73b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ibmjava:8-sdk-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:539cd8512aba5eb90993c75c8f4cf55714477f59787bfdac9fac5ad6dd5d1381
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.7 MB (175717764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893d437005de162d66f02b2e8d32d36eb28a91d4c7e5a698438697f58b1e1318`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2020 19:19:49 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 19 Jun 2020 19:19:50 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Fri, 19 Jun 2020 19:20:01 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Wed, 05 Aug 2020 22:20:40 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 05 Aug 2020 22:24:22 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='1770fc44e0061a72ab9cfc47fb9a1934b17581fee77a3cc32e83b4bee0084256';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='00e56752a6c8206b7d4990d6a3f9d4456bd2ffcde7165b0c150b8084cb961df8';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2020c805a8019fbc903a2fb5d7e5cc5190c6c83ba92a93730b84ed33a06be9fc';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='a4a01a2372ca7f4cd039e72fa9826403300eb4867ab735760b99514a5c8b4908';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='7bd69fa987bad2b0681a474b6c2775a6466586c64e99535a9ba96ed0dccd69ea';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Wed, 05 Aug 2020 22:24:22 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54cb4ffe99c5f24fd5d9092d445c28497122a55355fd862f3431fe39b0069a3d`  
		Last Modified: Fri, 19 Jun 2020 19:22:30 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579fa70fe6805ba9995c002270c4bef412288205c0c631288438cdd962583a0d`  
		Last Modified: Fri, 19 Jun 2020 19:22:31 GMT  
		Size: 5.5 MB (5539665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed831802ac3573cb821330d4d50b7d9f5982299b2160d17e860a0af5e13959ef`  
		Last Modified: Wed, 05 Aug 2020 22:26:57 GMT  
		Size: 167.4 MB (167380013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:b7a230eb8c4aa94f016e6e2a8accaf91c088e5219f8d1868b40ef55c91f7014d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:8-sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:28dc0e995c97a45c33f702aaf73b418dbe2b682a4afb404f15ec013e8bdeef0a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93171163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d137c5dba0334425e56c25734300c7b35dc5511a5d22500023d5ab101f6f5c78`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:19 GMT
ADD file:7d9bbf45a5b2510d44d3206a028cf6502757884d49e46d3d2e6356c3a92c4309 in / 
# Fri, 24 Jul 2020 14:38:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:22 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:11:53 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Jul 2020 16:12:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 22:19:53 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 05 Aug 2020 22:21:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='8a994f9fd1adefcbc35ba6db41a42b642f1e1b456028521ff4b4fc35db331b7f';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='8841d9a3beb8954c939ba1c9675561b5f5a8bf4593efe38b34cd340a8d8b84fc';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e5700d984127dff2ec050ee6d325626c10369c6cc0fa89cc790e35f38506361a';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='299b484ad1909f59f1d329d8c48792f65de3672a592a8cb7fd2ffdaa622c8b36';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='fc150ceedbb86e00f6b309ad5868df94397c5cadc5f5593044997c4b7f3188cb';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 05 Aug 2020 22:21:57 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7595c8c21622ea8a8b9778972e26dbbe063f7a1c4b0a28a80a34ebb3d343b586`  
		Last Modified: Mon, 13 Jul 2020 15:46:50 GMT  
		Size: 26.7 MB (26697127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af8ca898f36af68711cb67c345f65046a78ccd802453f4b129adf9205b1f8`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70799171ddba93a611490ba3557d782714b3f4da8963d49ac8726786ba8274a5`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c12202c5ef07dc9eb8f9d9e71407064684ed70f8c4040b62679b7d30200840`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3b48ae14e45cf7769bcc5ef96dd1a0d4389a21fd1de5c54169068b1730e569`  
		Last Modified: Fri, 24 Jul 2020 16:14:39 GMT  
		Size: 3.0 MB (2957372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e902f6fe0c3844b53e94a4b935305a7c679bdc8d35b78d91abe127bf59c765`  
		Last Modified: Wed, 05 Aug 2020 22:25:47 GMT  
		Size: 63.5 MB (63480291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; 386

```console
$ docker pull ibmjava@sha256:ca200e45f366ffe2bff3d6038b2099eea01cbf22cc486502ebd6ea0ec4cec84b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93049561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c36707821264333f5fa4bfcf0f688ef90b33c01519fd890627d4041cd58a29`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:47:40 GMT
ADD file:a2194fb1eb3c0e5832ad1c48e01faa517517697c7b45617fa0076fe1923711b1 in / 
# Wed, 19 Aug 2020 21:47:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:47:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:47:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:47:43 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:29:35 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 19 Aug 2020 22:29:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:29:44 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 19 Aug 2020 22:31:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='8a994f9fd1adefcbc35ba6db41a42b642f1e1b456028521ff4b4fc35db331b7f';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='8841d9a3beb8954c939ba1c9675561b5f5a8bf4593efe38b34cd340a8d8b84fc';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e5700d984127dff2ec050ee6d325626c10369c6cc0fa89cc790e35f38506361a';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='299b484ad1909f59f1d329d8c48792f65de3672a592a8cb7fd2ffdaa622c8b36';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='fc150ceedbb86e00f6b309ad5868df94397c5cadc5f5593044997c4b7f3188cb';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 Aug 2020 22:31:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:92ea639593649ab4b1d9a883cdee9a0c9ae490627a0a1e6b59d8962c94344d26`  
		Last Modified: Mon, 10 Aug 2020 14:27:54 GMT  
		Size: 27.1 MB (27124431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3de4f8866d6f8a7d6156f69d1684a0ffa16a4599d643cfb15061cf3eee5b2b6`  
		Last Modified: Wed, 19 Aug 2020 21:48:21 GMT  
		Size: 34.6 KB (34614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81cd73faed83d22ac56f653202675d246ace7921595d662985d5c6bf97668ad`  
		Last Modified: Wed, 19 Aug 2020 21:48:21 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d1af387dbe587e075a0fb09360f570e42daa62711aec6f26ad0c9c8d89b703`  
		Last Modified: Wed, 19 Aug 2020 21:48:21 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987ad5b9a08284cb8a30668b82cd354ea3c797c73b3a84645b8c2d16856b93db`  
		Last Modified: Wed, 19 Aug 2020 22:32:23 GMT  
		Size: 3.0 MB (2982729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e0dcff26d35f325fc80f0dc27604a0351495b0e9dfddcf775542646f43cc43`  
		Last Modified: Wed, 19 Aug 2020 22:32:50 GMT  
		Size: 62.9 MB (62906774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:0e9113943413f971561f855d5dce8fb726c9503e04cdc75486547bef476332ee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97218087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29987d85ab97128b74fc88a19cdbce4f1d3f8ea12715efa4b804e9ab93c4b0e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:14:04 GMT
ADD file:4954b2b03fa4bd48fabecbc1facd6d05808f55a143012aca45648ab2f767042a in / 
# Wed, 19 Aug 2020 21:14:14 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:14:22 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:14:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:14:32 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:50:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 19 Aug 2020 22:53:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:53:13 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 19 Aug 2020 22:55:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='8a994f9fd1adefcbc35ba6db41a42b642f1e1b456028521ff4b4fc35db331b7f';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='8841d9a3beb8954c939ba1c9675561b5f5a8bf4593efe38b34cd340a8d8b84fc';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e5700d984127dff2ec050ee6d325626c10369c6cc0fa89cc790e35f38506361a';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='299b484ad1909f59f1d329d8c48792f65de3672a592a8cb7fd2ffdaa622c8b36';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='fc150ceedbb86e00f6b309ad5868df94397c5cadc5f5593044997c4b7f3188cb';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 Aug 2020 22:55:57 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:23e4ce51557a90638716607f36b99292ea21b3e246ef66f83934e1eadb095632`  
		Last Modified: Mon, 10 Aug 2020 15:49:13 GMT  
		Size: 30.4 MB (30408877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b20479dd2a1972abd69e09a781025590f55fcbe8bef98a35b1067dceff85d60`  
		Last Modified: Wed, 19 Aug 2020 21:18:51 GMT  
		Size: 35.2 KB (35223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3107678818d326669afdd9fcce37d6b61613c2103e889ff7e019515b97ade1d`  
		Last Modified: Wed, 19 Aug 2020 21:18:51 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a571510b31b5805e20c811dcbb2413f66118e4be6a44a54c430826d8be670e7`  
		Last Modified: Wed, 19 Aug 2020 21:18:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9538a963d435f5fe1ba7326731a3fee312a667305ccdd70f519c5c40c2191d77`  
		Last Modified: Wed, 19 Aug 2020 22:57:56 GMT  
		Size: 3.1 MB (3075385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4213249081e4b2257b66ea99f3adcd00cf4a2c5f289368d4daa496e0e5fa6d74`  
		Last Modified: Wed, 19 Aug 2020 22:58:34 GMT  
		Size: 63.7 MB (63697557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:e4eeccf29fffb31f970762d4b5f50a8bc29fd647e8a9e0732f6761b5a8856cd9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92686296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9d289593b96b6fabb5456c53c86d7e8935988832908740b73acce39f75f60b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:10:03 GMT
ADD file:1343b5ae7d875bd32e4eac552ae10c9631788fd97b99bcdeb9f6a9b85c230ba2 in / 
# Wed, 19 Aug 2020 21:10:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:10:05 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:10:06 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:10:06 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:08:24 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 19 Aug 2020 22:08:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:08:31 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 19 Aug 2020 22:09:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='8a994f9fd1adefcbc35ba6db41a42b642f1e1b456028521ff4b4fc35db331b7f';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='8841d9a3beb8954c939ba1c9675561b5f5a8bf4593efe38b34cd340a8d8b84fc';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e5700d984127dff2ec050ee6d325626c10369c6cc0fa89cc790e35f38506361a';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='299b484ad1909f59f1d329d8c48792f65de3672a592a8cb7fd2ffdaa622c8b36';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='fc150ceedbb86e00f6b309ad5868df94397c5cadc5f5593044997c4b7f3188cb';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 Aug 2020 22:10:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:25294e13856fd30261115dbfc6dd49e2d854414d32c9ead824b8183a83620e5c`  
		Last Modified: Mon, 10 Aug 2020 15:49:57 GMT  
		Size: 25.4 MB (25371147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e4b14541a6306ab7ffae9ed980e3ebac039f590869efecf63c6d745e1cde3c`  
		Last Modified: Wed, 19 Aug 2020 21:11:08 GMT  
		Size: 36.2 KB (36170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4164a02312fb3bccad51789030500218898a262ff17a962d62bb9849c9103d59`  
		Last Modified: Wed, 19 Aug 2020 21:11:08 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68677136804619b55f0437044d91d7bfe75e0b8013ca953c0d4db40c4d91d6b`  
		Last Modified: Wed, 19 Aug 2020 21:11:08 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2d7c1e4e8846aa212e0c088d2fa25dfc2856f64869c0721aaa4ef1499a7999`  
		Last Modified: Wed, 19 Aug 2020 22:11:12 GMT  
		Size: 2.7 MB (2672211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe89329a51b9b166e85c5f7d24d30d8c209a1e786b42b555da6d79145d5876ae`  
		Last Modified: Wed, 19 Aug 2020 22:11:34 GMT  
		Size: 64.6 MB (64605732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:8-sfj-alpine`

```console
$ docker pull ibmjava@sha256:cbd2801fef988fe7f8eb3fcb1f021b2901cba6905c93a7db0b2bc263492677a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ibmjava:8-sfj-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:53d64d9ae0235913ec9bac9d8a66be157ffb2f48c90bf35b81b2455d0d632e2b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71830710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc2d6aa1d783c77157ca0045fd6e85aa02f8c6e70231bb1dd43e66fd79e5b5a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2020 19:19:49 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 19 Jun 2020 19:19:50 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Fri, 19 Jun 2020 19:20:01 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Wed, 05 Aug 2020 22:20:40 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 05 Aug 2020 22:22:35 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='8a994f9fd1adefcbc35ba6db41a42b642f1e1b456028521ff4b4fc35db331b7f';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='8841d9a3beb8954c939ba1c9675561b5f5a8bf4593efe38b34cd340a8d8b84fc';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e5700d984127dff2ec050ee6d325626c10369c6cc0fa89cc790e35f38506361a';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='299b484ad1909f59f1d329d8c48792f65de3672a592a8cb7fd2ffdaa622c8b36';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='fc150ceedbb86e00f6b309ad5868df94397c5cadc5f5593044997c4b7f3188cb';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Wed, 05 Aug 2020 22:22:35 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54cb4ffe99c5f24fd5d9092d445c28497122a55355fd862f3431fe39b0069a3d`  
		Last Modified: Fri, 19 Jun 2020 19:22:30 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579fa70fe6805ba9995c002270c4bef412288205c0c631288438cdd962583a0d`  
		Last Modified: Fri, 19 Jun 2020 19:22:31 GMT  
		Size: 5.5 MB (5539665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cdf7bf8e813f627a159b6fe67fe7b7e280a12bb5d812f651cff0f7c6efce08`  
		Last Modified: Wed, 05 Aug 2020 22:26:02 GMT  
		Size: 63.5 MB (63492959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:jre`

```console
$ docker pull ibmjava@sha256:801fafdfd6b0d2692551ee5fcae8c22932370fb06f35dc0a47af40bb3d1f6ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:jre` - linux; amd64

```console
$ docker pull ibmjava@sha256:1f0f9320f40f3a719432c78b0dbf14b450a6cda1db913f9cf66d0dfdc02a327a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159913209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b67bdce293c9995d072bdf01f82459ab1b4abda93b43352fffac8045d7701f7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:19 GMT
ADD file:7d9bbf45a5b2510d44d3206a028cf6502757884d49e46d3d2e6356c3a92c4309 in / 
# Fri, 24 Jul 2020 14:38:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:22 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:11:53 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Jul 2020 16:12:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 22:19:53 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 05 Aug 2020 22:20:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b532b712f4f3cae2af0794d3f3859489b794e2bf1971f05b04098cdd4826672';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='dc70e8d2a9a1690a810352bf0993a6c32e323073938ff157381769e04d38d2be';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='8b1a383e7027b0783c07d736b3b5e31e26205e10e1b14d2ac942d4ee9a4b5d29';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='142bf26a6de087ad5edc4e673c38368b2fe00e3d00f35f9d7382f7a929b560d7';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9e30f6c9f98cfc64c10299627fe6158100ce63e2d2d299c8263c465e8f3138f9';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 05 Aug 2020 22:20:34 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7595c8c21622ea8a8b9778972e26dbbe063f7a1c4b0a28a80a34ebb3d343b586`  
		Last Modified: Mon, 13 Jul 2020 15:46:50 GMT  
		Size: 26.7 MB (26697127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af8ca898f36af68711cb67c345f65046a78ccd802453f4b129adf9205b1f8`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70799171ddba93a611490ba3557d782714b3f4da8963d49ac8726786ba8274a5`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c12202c5ef07dc9eb8f9d9e71407064684ed70f8c4040b62679b7d30200840`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3b48ae14e45cf7769bcc5ef96dd1a0d4389a21fd1de5c54169068b1730e569`  
		Last Modified: Fri, 24 Jul 2020 16:14:39 GMT  
		Size: 3.0 MB (2957372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ec5fdbe0e16348f4573b4d5009a350cf91b0507de9f6ee11165110da89b999`  
		Last Modified: Wed, 05 Aug 2020 22:24:59 GMT  
		Size: 130.2 MB (130222337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; 386

```console
$ docker pull ibmjava@sha256:f985e9b27c7895746c69e8ee336650254e6a9cf53c9b021f5f48f01122c2e063
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148691210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa00f05bb49b5a0ea57c2a58c6b2c1c02c66dcf6c4f61fdc83aa1cc95c5e033`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:47:40 GMT
ADD file:a2194fb1eb3c0e5832ad1c48e01faa517517697c7b45617fa0076fe1923711b1 in / 
# Wed, 19 Aug 2020 21:47:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:47:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:47:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:47:43 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:29:35 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 19 Aug 2020 22:29:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:29:44 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 19 Aug 2020 22:30:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b532b712f4f3cae2af0794d3f3859489b794e2bf1971f05b04098cdd4826672';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='dc70e8d2a9a1690a810352bf0993a6c32e323073938ff157381769e04d38d2be';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='8b1a383e7027b0783c07d736b3b5e31e26205e10e1b14d2ac942d4ee9a4b5d29';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='142bf26a6de087ad5edc4e673c38368b2fe00e3d00f35f9d7382f7a929b560d7';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9e30f6c9f98cfc64c10299627fe6158100ce63e2d2d299c8263c465e8f3138f9';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 Aug 2020 22:30:26 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:92ea639593649ab4b1d9a883cdee9a0c9ae490627a0a1e6b59d8962c94344d26`  
		Last Modified: Mon, 10 Aug 2020 14:27:54 GMT  
		Size: 27.1 MB (27124431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3de4f8866d6f8a7d6156f69d1684a0ffa16a4599d643cfb15061cf3eee5b2b6`  
		Last Modified: Wed, 19 Aug 2020 21:48:21 GMT  
		Size: 34.6 KB (34614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81cd73faed83d22ac56f653202675d246ace7921595d662985d5c6bf97668ad`  
		Last Modified: Wed, 19 Aug 2020 21:48:21 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d1af387dbe587e075a0fb09360f570e42daa62711aec6f26ad0c9c8d89b703`  
		Last Modified: Wed, 19 Aug 2020 21:48:21 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987ad5b9a08284cb8a30668b82cd354ea3c797c73b3a84645b8c2d16856b93db`  
		Last Modified: Wed, 19 Aug 2020 22:32:23 GMT  
		Size: 3.0 MB (2982729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20687db51cbd60eec816304bb11551919dd48ffd371ecec94b3b50bf3fd14a62`  
		Last Modified: Wed, 19 Aug 2020 22:32:35 GMT  
		Size: 118.5 MB (118548423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:bd87048f17e799c54e3f570e7de474cbc4602411645ef02f58232d2fa4f9607a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163310510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4153449699bd33da7767d00f6b222d6dd7b26d8ec12d5b08abd057ee8639129a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:14:04 GMT
ADD file:4954b2b03fa4bd48fabecbc1facd6d05808f55a143012aca45648ab2f767042a in / 
# Wed, 19 Aug 2020 21:14:14 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:14:22 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:14:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:14:32 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:50:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 19 Aug 2020 22:53:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:53:13 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 19 Aug 2020 22:54:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b532b712f4f3cae2af0794d3f3859489b794e2bf1971f05b04098cdd4826672';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='dc70e8d2a9a1690a810352bf0993a6c32e323073938ff157381769e04d38d2be';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='8b1a383e7027b0783c07d736b3b5e31e26205e10e1b14d2ac942d4ee9a4b5d29';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='142bf26a6de087ad5edc4e673c38368b2fe00e3d00f35f9d7382f7a929b560d7';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9e30f6c9f98cfc64c10299627fe6158100ce63e2d2d299c8263c465e8f3138f9';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 Aug 2020 22:54:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:23e4ce51557a90638716607f36b99292ea21b3e246ef66f83934e1eadb095632`  
		Last Modified: Mon, 10 Aug 2020 15:49:13 GMT  
		Size: 30.4 MB (30408877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b20479dd2a1972abd69e09a781025590f55fcbe8bef98a35b1067dceff85d60`  
		Last Modified: Wed, 19 Aug 2020 21:18:51 GMT  
		Size: 35.2 KB (35223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3107678818d326669afdd9fcce37d6b61613c2103e889ff7e019515b97ade1d`  
		Last Modified: Wed, 19 Aug 2020 21:18:51 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a571510b31b5805e20c811dcbb2413f66118e4be6a44a54c430826d8be670e7`  
		Last Modified: Wed, 19 Aug 2020 21:18:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9538a963d435f5fe1ba7326731a3fee312a667305ccdd70f519c5c40c2191d77`  
		Last Modified: Wed, 19 Aug 2020 22:57:56 GMT  
		Size: 3.1 MB (3075385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede11ddbd034b571963e94ea1a9d515b44d07dfafb6cc59988895ab675987187`  
		Last Modified: Wed, 19 Aug 2020 22:58:09 GMT  
		Size: 129.8 MB (129789980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:jre` - linux; s390x

```console
$ docker pull ibmjava@sha256:77041f0c019a7731275948ba4db3d16ea7cd24230d33e08a0ba9e9ddd402f353
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155547246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7246bd293e5b3ee65f71644f2a52459c2a179c7bcc44a1ed87884469821301a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:10:03 GMT
ADD file:1343b5ae7d875bd32e4eac552ae10c9631788fd97b99bcdeb9f6a9b85c230ba2 in / 
# Wed, 19 Aug 2020 21:10:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:10:05 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:10:06 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:10:06 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:08:24 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 19 Aug 2020 22:08:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:08:31 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 19 Aug 2020 22:09:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b532b712f4f3cae2af0794d3f3859489b794e2bf1971f05b04098cdd4826672';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='dc70e8d2a9a1690a810352bf0993a6c32e323073938ff157381769e04d38d2be';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='8b1a383e7027b0783c07d736b3b5e31e26205e10e1b14d2ac942d4ee9a4b5d29';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='142bf26a6de087ad5edc4e673c38368b2fe00e3d00f35f9d7382f7a929b560d7';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9e30f6c9f98cfc64c10299627fe6158100ce63e2d2d299c8263c465e8f3138f9';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 Aug 2020 22:09:15 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:25294e13856fd30261115dbfc6dd49e2d854414d32c9ead824b8183a83620e5c`  
		Last Modified: Mon, 10 Aug 2020 15:49:57 GMT  
		Size: 25.4 MB (25371147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e4b14541a6306ab7ffae9ed980e3ebac039f590869efecf63c6d745e1cde3c`  
		Last Modified: Wed, 19 Aug 2020 21:11:08 GMT  
		Size: 36.2 KB (36170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4164a02312fb3bccad51789030500218898a262ff17a962d62bb9849c9103d59`  
		Last Modified: Wed, 19 Aug 2020 21:11:08 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68677136804619b55f0437044d91d7bfe75e0b8013ca953c0d4db40c4d91d6b`  
		Last Modified: Wed, 19 Aug 2020 21:11:08 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2d7c1e4e8846aa212e0c088d2fa25dfc2856f64869c0721aaa4ef1499a7999`  
		Last Modified: Wed, 19 Aug 2020 22:11:12 GMT  
		Size: 2.7 MB (2672211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d120780fc389b1bd05d629730a20d12da94d18558bf4fe290f22dd0d97f379`  
		Last Modified: Wed, 19 Aug 2020 22:11:21 GMT  
		Size: 127.5 MB (127466682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:jre-alpine`

```console
$ docker pull ibmjava@sha256:b0bab7ccc9dcd6fde9093789ffaf20cb283a0566d592c95de4b067c3e667f965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ibmjava:jre-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:46020f520ec3909e7950f847298cb74ce5b091ae592364acfa38e5c79512ff7e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138546090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedf54e322c9e103b7ed7c91bd48de5563270c8c166245d6a1fed84b6ac3a325`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2020 19:19:49 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 19 Jun 2020 19:19:50 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Fri, 19 Jun 2020 19:20:01 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Wed, 05 Aug 2020 22:20:40 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 05 Aug 2020 22:21:21 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b532b712f4f3cae2af0794d3f3859489b794e2bf1971f05b04098cdd4826672';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='dc70e8d2a9a1690a810352bf0993a6c32e323073938ff157381769e04d38d2be';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='8b1a383e7027b0783c07d736b3b5e31e26205e10e1b14d2ac942d4ee9a4b5d29';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='142bf26a6de087ad5edc4e673c38368b2fe00e3d00f35f9d7382f7a929b560d7';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9e30f6c9f98cfc64c10299627fe6158100ce63e2d2d299c8263c465e8f3138f9';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Wed, 05 Aug 2020 22:21:21 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54cb4ffe99c5f24fd5d9092d445c28497122a55355fd862f3431fe39b0069a3d`  
		Last Modified: Fri, 19 Jun 2020 19:22:30 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579fa70fe6805ba9995c002270c4bef412288205c0c631288438cdd962583a0d`  
		Last Modified: Fri, 19 Jun 2020 19:22:31 GMT  
		Size: 5.5 MB (5539665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c18a5b31bcf01d0017d5bc8d3006473719f9305ce3add67784617e801ee6131`  
		Last Modified: Wed, 05 Aug 2020 22:25:37 GMT  
		Size: 130.2 MB (130208339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:latest`

```console
$ docker pull ibmjava@sha256:801fafdfd6b0d2692551ee5fcae8c22932370fb06f35dc0a47af40bb3d1f6ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:latest` - linux; amd64

```console
$ docker pull ibmjava@sha256:1f0f9320f40f3a719432c78b0dbf14b450a6cda1db913f9cf66d0dfdc02a327a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159913209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b67bdce293c9995d072bdf01f82459ab1b4abda93b43352fffac8045d7701f7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:19 GMT
ADD file:7d9bbf45a5b2510d44d3206a028cf6502757884d49e46d3d2e6356c3a92c4309 in / 
# Fri, 24 Jul 2020 14:38:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:22 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:11:53 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Jul 2020 16:12:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 22:19:53 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 05 Aug 2020 22:20:34 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b532b712f4f3cae2af0794d3f3859489b794e2bf1971f05b04098cdd4826672';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='dc70e8d2a9a1690a810352bf0993a6c32e323073938ff157381769e04d38d2be';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='8b1a383e7027b0783c07d736b3b5e31e26205e10e1b14d2ac942d4ee9a4b5d29';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='142bf26a6de087ad5edc4e673c38368b2fe00e3d00f35f9d7382f7a929b560d7';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9e30f6c9f98cfc64c10299627fe6158100ce63e2d2d299c8263c465e8f3138f9';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 05 Aug 2020 22:20:34 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7595c8c21622ea8a8b9778972e26dbbe063f7a1c4b0a28a80a34ebb3d343b586`  
		Last Modified: Mon, 13 Jul 2020 15:46:50 GMT  
		Size: 26.7 MB (26697127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af8ca898f36af68711cb67c345f65046a78ccd802453f4b129adf9205b1f8`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70799171ddba93a611490ba3557d782714b3f4da8963d49ac8726786ba8274a5`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c12202c5ef07dc9eb8f9d9e71407064684ed70f8c4040b62679b7d30200840`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3b48ae14e45cf7769bcc5ef96dd1a0d4389a21fd1de5c54169068b1730e569`  
		Last Modified: Fri, 24 Jul 2020 16:14:39 GMT  
		Size: 3.0 MB (2957372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ec5fdbe0e16348f4573b4d5009a350cf91b0507de9f6ee11165110da89b999`  
		Last Modified: Wed, 05 Aug 2020 22:24:59 GMT  
		Size: 130.2 MB (130222337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; 386

```console
$ docker pull ibmjava@sha256:f985e9b27c7895746c69e8ee336650254e6a9cf53c9b021f5f48f01122c2e063
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148691210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa00f05bb49b5a0ea57c2a58c6b2c1c02c66dcf6c4f61fdc83aa1cc95c5e033`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:47:40 GMT
ADD file:a2194fb1eb3c0e5832ad1c48e01faa517517697c7b45617fa0076fe1923711b1 in / 
# Wed, 19 Aug 2020 21:47:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:47:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:47:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:47:43 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:29:35 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 19 Aug 2020 22:29:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:29:44 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 19 Aug 2020 22:30:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b532b712f4f3cae2af0794d3f3859489b794e2bf1971f05b04098cdd4826672';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='dc70e8d2a9a1690a810352bf0993a6c32e323073938ff157381769e04d38d2be';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='8b1a383e7027b0783c07d736b3b5e31e26205e10e1b14d2ac942d4ee9a4b5d29';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='142bf26a6de087ad5edc4e673c38368b2fe00e3d00f35f9d7382f7a929b560d7';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9e30f6c9f98cfc64c10299627fe6158100ce63e2d2d299c8263c465e8f3138f9';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 Aug 2020 22:30:26 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:92ea639593649ab4b1d9a883cdee9a0c9ae490627a0a1e6b59d8962c94344d26`  
		Last Modified: Mon, 10 Aug 2020 14:27:54 GMT  
		Size: 27.1 MB (27124431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3de4f8866d6f8a7d6156f69d1684a0ffa16a4599d643cfb15061cf3eee5b2b6`  
		Last Modified: Wed, 19 Aug 2020 21:48:21 GMT  
		Size: 34.6 KB (34614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81cd73faed83d22ac56f653202675d246ace7921595d662985d5c6bf97668ad`  
		Last Modified: Wed, 19 Aug 2020 21:48:21 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d1af387dbe587e075a0fb09360f570e42daa62711aec6f26ad0c9c8d89b703`  
		Last Modified: Wed, 19 Aug 2020 21:48:21 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987ad5b9a08284cb8a30668b82cd354ea3c797c73b3a84645b8c2d16856b93db`  
		Last Modified: Wed, 19 Aug 2020 22:32:23 GMT  
		Size: 3.0 MB (2982729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20687db51cbd60eec816304bb11551919dd48ffd371ecec94b3b50bf3fd14a62`  
		Last Modified: Wed, 19 Aug 2020 22:32:35 GMT  
		Size: 118.5 MB (118548423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:bd87048f17e799c54e3f570e7de474cbc4602411645ef02f58232d2fa4f9607a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163310510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4153449699bd33da7767d00f6b222d6dd7b26d8ec12d5b08abd057ee8639129a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:14:04 GMT
ADD file:4954b2b03fa4bd48fabecbc1facd6d05808f55a143012aca45648ab2f767042a in / 
# Wed, 19 Aug 2020 21:14:14 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:14:22 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:14:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:14:32 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:50:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 19 Aug 2020 22:53:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:53:13 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 19 Aug 2020 22:54:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b532b712f4f3cae2af0794d3f3859489b794e2bf1971f05b04098cdd4826672';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='dc70e8d2a9a1690a810352bf0993a6c32e323073938ff157381769e04d38d2be';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='8b1a383e7027b0783c07d736b3b5e31e26205e10e1b14d2ac942d4ee9a4b5d29';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='142bf26a6de087ad5edc4e673c38368b2fe00e3d00f35f9d7382f7a929b560d7';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9e30f6c9f98cfc64c10299627fe6158100ce63e2d2d299c8263c465e8f3138f9';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 Aug 2020 22:54:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:23e4ce51557a90638716607f36b99292ea21b3e246ef66f83934e1eadb095632`  
		Last Modified: Mon, 10 Aug 2020 15:49:13 GMT  
		Size: 30.4 MB (30408877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b20479dd2a1972abd69e09a781025590f55fcbe8bef98a35b1067dceff85d60`  
		Last Modified: Wed, 19 Aug 2020 21:18:51 GMT  
		Size: 35.2 KB (35223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3107678818d326669afdd9fcce37d6b61613c2103e889ff7e019515b97ade1d`  
		Last Modified: Wed, 19 Aug 2020 21:18:51 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a571510b31b5805e20c811dcbb2413f66118e4be6a44a54c430826d8be670e7`  
		Last Modified: Wed, 19 Aug 2020 21:18:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9538a963d435f5fe1ba7326731a3fee312a667305ccdd70f519c5c40c2191d77`  
		Last Modified: Wed, 19 Aug 2020 22:57:56 GMT  
		Size: 3.1 MB (3075385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede11ddbd034b571963e94ea1a9d515b44d07dfafb6cc59988895ab675987187`  
		Last Modified: Wed, 19 Aug 2020 22:58:09 GMT  
		Size: 129.8 MB (129789980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:latest` - linux; s390x

```console
$ docker pull ibmjava@sha256:77041f0c019a7731275948ba4db3d16ea7cd24230d33e08a0ba9e9ddd402f353
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155547246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7246bd293e5b3ee65f71644f2a52459c2a179c7bcc44a1ed87884469821301a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:10:03 GMT
ADD file:1343b5ae7d875bd32e4eac552ae10c9631788fd97b99bcdeb9f6a9b85c230ba2 in / 
# Wed, 19 Aug 2020 21:10:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:10:05 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:10:06 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:10:06 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:08:24 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 19 Aug 2020 22:08:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:08:31 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 19 Aug 2020 22:09:13 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3b532b712f4f3cae2af0794d3f3859489b794e2bf1971f05b04098cdd4826672';          YML_FILE='jre/linux/x86_64/index.yml';          ;;        i386)          ESUM='dc70e8d2a9a1690a810352bf0993a6c32e323073938ff157381769e04d38d2be';          YML_FILE='jre/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='8b1a383e7027b0783c07d736b3b5e31e26205e10e1b14d2ac942d4ee9a4b5d29';          YML_FILE='jre/linux/ppc64le/index.yml';          ;;        s390)          ESUM='142bf26a6de087ad5edc4e673c38368b2fe00e3d00f35f9d7382f7a929b560d7';          YML_FILE='jre/linux/s390/index.yml';          ;;        s390x)          ESUM='9e30f6c9f98cfc64c10299627fe6158100ce63e2d2d299c8263c465e8f3138f9';          YML_FILE='jre/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 Aug 2020 22:09:15 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:25294e13856fd30261115dbfc6dd49e2d854414d32c9ead824b8183a83620e5c`  
		Last Modified: Mon, 10 Aug 2020 15:49:57 GMT  
		Size: 25.4 MB (25371147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e4b14541a6306ab7ffae9ed980e3ebac039f590869efecf63c6d745e1cde3c`  
		Last Modified: Wed, 19 Aug 2020 21:11:08 GMT  
		Size: 36.2 KB (36170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4164a02312fb3bccad51789030500218898a262ff17a962d62bb9849c9103d59`  
		Last Modified: Wed, 19 Aug 2020 21:11:08 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68677136804619b55f0437044d91d7bfe75e0b8013ca953c0d4db40c4d91d6b`  
		Last Modified: Wed, 19 Aug 2020 21:11:08 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2d7c1e4e8846aa212e0c088d2fa25dfc2856f64869c0721aaa4ef1499a7999`  
		Last Modified: Wed, 19 Aug 2020 22:11:12 GMT  
		Size: 2.7 MB (2672211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d120780fc389b1bd05d629730a20d12da94d18558bf4fe290f22dd0d97f379`  
		Last Modified: Wed, 19 Aug 2020 22:11:21 GMT  
		Size: 127.5 MB (127466682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:04d6d89bc21e1d417e185eb035366b94f430a55995abb4c1db83d4b215f31616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:f9de30bff3d3529d6625c8da0369ce7d35f9063fd239c8a1adefc976d7ee8f43
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.1 MB (197080972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:191ab39d7fa77274554cc296db7802ec058a59d6d435b5ac11c7db8e4dc5a108`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:19 GMT
ADD file:7d9bbf45a5b2510d44d3206a028cf6502757884d49e46d3d2e6356c3a92c4309 in / 
# Fri, 24 Jul 2020 14:38:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:22 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:11:53 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Jul 2020 16:12:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 22:19:53 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 05 Aug 2020 22:23:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='1770fc44e0061a72ab9cfc47fb9a1934b17581fee77a3cc32e83b4bee0084256';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='00e56752a6c8206b7d4990d6a3f9d4456bd2ffcde7165b0c150b8084cb961df8';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2020c805a8019fbc903a2fb5d7e5cc5190c6c83ba92a93730b84ed33a06be9fc';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='a4a01a2372ca7f4cd039e72fa9826403300eb4867ab735760b99514a5c8b4908';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='7bd69fa987bad2b0681a474b6c2775a6466586c64e99535a9ba96ed0dccd69ea';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 05 Aug 2020 22:23:31 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7595c8c21622ea8a8b9778972e26dbbe063f7a1c4b0a28a80a34ebb3d343b586`  
		Last Modified: Mon, 13 Jul 2020 15:46:50 GMT  
		Size: 26.7 MB (26697127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af8ca898f36af68711cb67c345f65046a78ccd802453f4b129adf9205b1f8`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70799171ddba93a611490ba3557d782714b3f4da8963d49ac8726786ba8274a5`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c12202c5ef07dc9eb8f9d9e71407064684ed70f8c4040b62679b7d30200840`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3b48ae14e45cf7769bcc5ef96dd1a0d4389a21fd1de5c54169068b1730e569`  
		Last Modified: Fri, 24 Jul 2020 16:14:39 GMT  
		Size: 3.0 MB (2957372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68167569e9e6620bef5744d4ef36d4b69b2d7b92c9ca25b2f785561d207b3ff6`  
		Last Modified: Wed, 05 Aug 2020 22:26:25 GMT  
		Size: 167.4 MB (167390100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; 386

```console
$ docker pull ibmjava@sha256:62c2e177f7e670c64e1d730fcc30cd9ea4d208946096c55827cd56b67549be6b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.7 MB (185749351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8afc08b098d9dde268068d9e8955241b481a09a711efbd13dc4ae87e4d9daa5a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:47:40 GMT
ADD file:a2194fb1eb3c0e5832ad1c48e01faa517517697c7b45617fa0076fe1923711b1 in / 
# Wed, 19 Aug 2020 21:47:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:47:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:47:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:47:43 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:29:35 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 19 Aug 2020 22:29:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:29:44 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 19 Aug 2020 22:32:09 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='1770fc44e0061a72ab9cfc47fb9a1934b17581fee77a3cc32e83b4bee0084256';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='00e56752a6c8206b7d4990d6a3f9d4456bd2ffcde7165b0c150b8084cb961df8';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2020c805a8019fbc903a2fb5d7e5cc5190c6c83ba92a93730b84ed33a06be9fc';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='a4a01a2372ca7f4cd039e72fa9826403300eb4867ab735760b99514a5c8b4908';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='7bd69fa987bad2b0681a474b6c2775a6466586c64e99535a9ba96ed0dccd69ea';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 Aug 2020 22:32:10 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:92ea639593649ab4b1d9a883cdee9a0c9ae490627a0a1e6b59d8962c94344d26`  
		Last Modified: Mon, 10 Aug 2020 14:27:54 GMT  
		Size: 27.1 MB (27124431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3de4f8866d6f8a7d6156f69d1684a0ffa16a4599d643cfb15061cf3eee5b2b6`  
		Last Modified: Wed, 19 Aug 2020 21:48:21 GMT  
		Size: 34.6 KB (34614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81cd73faed83d22ac56f653202675d246ace7921595d662985d5c6bf97668ad`  
		Last Modified: Wed, 19 Aug 2020 21:48:21 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d1af387dbe587e075a0fb09360f570e42daa62711aec6f26ad0c9c8d89b703`  
		Last Modified: Wed, 19 Aug 2020 21:48:21 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987ad5b9a08284cb8a30668b82cd354ea3c797c73b3a84645b8c2d16856b93db`  
		Last Modified: Wed, 19 Aug 2020 22:32:23 GMT  
		Size: 3.0 MB (2982729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c449430090068659f9fffd3495633f9f08759364f27f4d1cf43eac45d7842faf`  
		Last Modified: Wed, 19 Aug 2020 22:33:14 GMT  
		Size: 155.6 MB (155606564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:c64ee4cec2a85b5ab5b25c72272f4a732737e6b2d948d5086fc9050105bfe56d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.6 MB (200600313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fb20779f8fcf88da7077d669a50945030ae85e1734672879ff859f063a3d7e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:14:04 GMT
ADD file:4954b2b03fa4bd48fabecbc1facd6d05808f55a143012aca45648ab2f767042a in / 
# Wed, 19 Aug 2020 21:14:14 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:14:22 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:14:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:14:32 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:50:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 19 Aug 2020 22:53:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:53:13 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 19 Aug 2020 22:57:19 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='1770fc44e0061a72ab9cfc47fb9a1934b17581fee77a3cc32e83b4bee0084256';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='00e56752a6c8206b7d4990d6a3f9d4456bd2ffcde7165b0c150b8084cb961df8';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2020c805a8019fbc903a2fb5d7e5cc5190c6c83ba92a93730b84ed33a06be9fc';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='a4a01a2372ca7f4cd039e72fa9826403300eb4867ab735760b99514a5c8b4908';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='7bd69fa987bad2b0681a474b6c2775a6466586c64e99535a9ba96ed0dccd69ea';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 Aug 2020 22:57:25 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:23e4ce51557a90638716607f36b99292ea21b3e246ef66f83934e1eadb095632`  
		Last Modified: Mon, 10 Aug 2020 15:49:13 GMT  
		Size: 30.4 MB (30408877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b20479dd2a1972abd69e09a781025590f55fcbe8bef98a35b1067dceff85d60`  
		Last Modified: Wed, 19 Aug 2020 21:18:51 GMT  
		Size: 35.2 KB (35223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3107678818d326669afdd9fcce37d6b61613c2103e889ff7e019515b97ade1d`  
		Last Modified: Wed, 19 Aug 2020 21:18:51 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a571510b31b5805e20c811dcbb2413f66118e4be6a44a54c430826d8be670e7`  
		Last Modified: Wed, 19 Aug 2020 21:18:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9538a963d435f5fe1ba7326731a3fee312a667305ccdd70f519c5c40c2191d77`  
		Last Modified: Wed, 19 Aug 2020 22:57:56 GMT  
		Size: 3.1 MB (3075385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3167be622de99c1fad74b9f24c68f72bf72550248db56df665841964581d327`  
		Last Modified: Wed, 19 Aug 2020 22:59:05 GMT  
		Size: 167.1 MB (167079783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:d8609d5288ce92f50dc06c9a679751176e8007d01309472e59218662ae341a48
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185799868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a66b1b1f370f7a037e68add3375b5faa7737af2cb44da53009815c440eec2b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:10:03 GMT
ADD file:1343b5ae7d875bd32e4eac552ae10c9631788fd97b99bcdeb9f6a9b85c230ba2 in / 
# Wed, 19 Aug 2020 21:10:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:10:05 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:10:06 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:10:06 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:08:24 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 19 Aug 2020 22:08:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:08:31 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 19 Aug 2020 22:10:58 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='1770fc44e0061a72ab9cfc47fb9a1934b17581fee77a3cc32e83b4bee0084256';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='00e56752a6c8206b7d4990d6a3f9d4456bd2ffcde7165b0c150b8084cb961df8';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2020c805a8019fbc903a2fb5d7e5cc5190c6c83ba92a93730b84ed33a06be9fc';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='a4a01a2372ca7f4cd039e72fa9826403300eb4867ab735760b99514a5c8b4908';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='7bd69fa987bad2b0681a474b6c2775a6466586c64e99535a9ba96ed0dccd69ea';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 Aug 2020 22:11:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:25294e13856fd30261115dbfc6dd49e2d854414d32c9ead824b8183a83620e5c`  
		Last Modified: Mon, 10 Aug 2020 15:49:57 GMT  
		Size: 25.4 MB (25371147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e4b14541a6306ab7ffae9ed980e3ebac039f590869efecf63c6d745e1cde3c`  
		Last Modified: Wed, 19 Aug 2020 21:11:08 GMT  
		Size: 36.2 KB (36170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4164a02312fb3bccad51789030500218898a262ff17a962d62bb9849c9103d59`  
		Last Modified: Wed, 19 Aug 2020 21:11:08 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68677136804619b55f0437044d91d7bfe75e0b8013ca953c0d4db40c4d91d6b`  
		Last Modified: Wed, 19 Aug 2020 21:11:08 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2d7c1e4e8846aa212e0c088d2fa25dfc2856f64869c0721aaa4ef1499a7999`  
		Last Modified: Wed, 19 Aug 2020 22:11:12 GMT  
		Size: 2.7 MB (2672211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b44d28c857b0538d6586c0e76fe1c491359c0e9a37a2a048a3f2941e0b11318`  
		Last Modified: Wed, 19 Aug 2020 22:11:53 GMT  
		Size: 157.7 MB (157719304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sdk-alpine`

```console
$ docker pull ibmjava@sha256:ef5aa44cbd90ebd3ee940ee987cf8d518838f6ccf6186fb150bb54f5bab73b4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ibmjava:sdk-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:539cd8512aba5eb90993c75c8f4cf55714477f59787bfdac9fac5ad6dd5d1381
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.7 MB (175717764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893d437005de162d66f02b2e8d32d36eb28a91d4c7e5a698438697f58b1e1318`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2020 19:19:49 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 19 Jun 2020 19:19:50 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Fri, 19 Jun 2020 19:20:01 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Wed, 05 Aug 2020 22:20:40 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 05 Aug 2020 22:24:22 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='1770fc44e0061a72ab9cfc47fb9a1934b17581fee77a3cc32e83b4bee0084256';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='00e56752a6c8206b7d4990d6a3f9d4456bd2ffcde7165b0c150b8084cb961df8';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='2020c805a8019fbc903a2fb5d7e5cc5190c6c83ba92a93730b84ed33a06be9fc';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='a4a01a2372ca7f4cd039e72fa9826403300eb4867ab735760b99514a5c8b4908';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='7bd69fa987bad2b0681a474b6c2775a6466586c64e99535a9ba96ed0dccd69ea';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Wed, 05 Aug 2020 22:24:22 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54cb4ffe99c5f24fd5d9092d445c28497122a55355fd862f3431fe39b0069a3d`  
		Last Modified: Fri, 19 Jun 2020 19:22:30 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579fa70fe6805ba9995c002270c4bef412288205c0c631288438cdd962583a0d`  
		Last Modified: Fri, 19 Jun 2020 19:22:31 GMT  
		Size: 5.5 MB (5539665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed831802ac3573cb821330d4d50b7d9f5982299b2160d17e860a0af5e13959ef`  
		Last Modified: Wed, 05 Aug 2020 22:26:57 GMT  
		Size: 167.4 MB (167380013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sfj`

```console
$ docker pull ibmjava@sha256:b7a230eb8c4aa94f016e6e2a8accaf91c088e5219f8d1868b40ef55c91f7014d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:28dc0e995c97a45c33f702aaf73b418dbe2b682a4afb404f15ec013e8bdeef0a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93171163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d137c5dba0334425e56c25734300c7b35dc5511a5d22500023d5ab101f6f5c78`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jul 2020 14:38:19 GMT
ADD file:7d9bbf45a5b2510d44d3206a028cf6502757884d49e46d3d2e6356c3a92c4309 in / 
# Fri, 24 Jul 2020 14:38:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 24 Jul 2020 14:38:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:38:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:38:22 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:11:53 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 24 Jul 2020 16:12:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 22:19:53 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 05 Aug 2020 22:21:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='8a994f9fd1adefcbc35ba6db41a42b642f1e1b456028521ff4b4fc35db331b7f';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='8841d9a3beb8954c939ba1c9675561b5f5a8bf4593efe38b34cd340a8d8b84fc';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e5700d984127dff2ec050ee6d325626c10369c6cc0fa89cc790e35f38506361a';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='299b484ad1909f59f1d329d8c48792f65de3672a592a8cb7fd2ffdaa622c8b36';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='fc150ceedbb86e00f6b309ad5868df94397c5cadc5f5593044997c4b7f3188cb';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 05 Aug 2020 22:21:57 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7595c8c21622ea8a8b9778972e26dbbe063f7a1c4b0a28a80a34ebb3d343b586`  
		Last Modified: Mon, 13 Jul 2020 15:46:50 GMT  
		Size: 26.7 MB (26697127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13af8ca898f36af68711cb67c345f65046a78ccd802453f4b129adf9205b1f8`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 35.4 KB (35364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70799171ddba93a611490ba3557d782714b3f4da8963d49ac8726786ba8274a5`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c12202c5ef07dc9eb8f9d9e71407064684ed70f8c4040b62679b7d30200840`  
		Last Modified: Fri, 24 Jul 2020 14:39:21 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3b48ae14e45cf7769bcc5ef96dd1a0d4389a21fd1de5c54169068b1730e569`  
		Last Modified: Fri, 24 Jul 2020 16:14:39 GMT  
		Size: 3.0 MB (2957372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e902f6fe0c3844b53e94a4b935305a7c679bdc8d35b78d91abe127bf59c765`  
		Last Modified: Wed, 05 Aug 2020 22:25:47 GMT  
		Size: 63.5 MB (63480291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; 386

```console
$ docker pull ibmjava@sha256:ca200e45f366ffe2bff3d6038b2099eea01cbf22cc486502ebd6ea0ec4cec84b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93049561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c36707821264333f5fa4bfcf0f688ef90b33c01519fd890627d4041cd58a29`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:47:40 GMT
ADD file:a2194fb1eb3c0e5832ad1c48e01faa517517697c7b45617fa0076fe1923711b1 in / 
# Wed, 19 Aug 2020 21:47:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:47:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:47:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:47:43 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:29:35 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 19 Aug 2020 22:29:44 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:29:44 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 19 Aug 2020 22:31:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='8a994f9fd1adefcbc35ba6db41a42b642f1e1b456028521ff4b4fc35db331b7f';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='8841d9a3beb8954c939ba1c9675561b5f5a8bf4593efe38b34cd340a8d8b84fc';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e5700d984127dff2ec050ee6d325626c10369c6cc0fa89cc790e35f38506361a';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='299b484ad1909f59f1d329d8c48792f65de3672a592a8cb7fd2ffdaa622c8b36';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='fc150ceedbb86e00f6b309ad5868df94397c5cadc5f5593044997c4b7f3188cb';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 Aug 2020 22:31:13 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:92ea639593649ab4b1d9a883cdee9a0c9ae490627a0a1e6b59d8962c94344d26`  
		Last Modified: Mon, 10 Aug 2020 14:27:54 GMT  
		Size: 27.1 MB (27124431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3de4f8866d6f8a7d6156f69d1684a0ffa16a4599d643cfb15061cf3eee5b2b6`  
		Last Modified: Wed, 19 Aug 2020 21:48:21 GMT  
		Size: 34.6 KB (34614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81cd73faed83d22ac56f653202675d246ace7921595d662985d5c6bf97668ad`  
		Last Modified: Wed, 19 Aug 2020 21:48:21 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d1af387dbe587e075a0fb09360f570e42daa62711aec6f26ad0c9c8d89b703`  
		Last Modified: Wed, 19 Aug 2020 21:48:21 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987ad5b9a08284cb8a30668b82cd354ea3c797c73b3a84645b8c2d16856b93db`  
		Last Modified: Wed, 19 Aug 2020 22:32:23 GMT  
		Size: 3.0 MB (2982729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e0dcff26d35f325fc80f0dc27604a0351495b0e9dfddcf775542646f43cc43`  
		Last Modified: Wed, 19 Aug 2020 22:32:50 GMT  
		Size: 62.9 MB (62906774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:0e9113943413f971561f855d5dce8fb726c9503e04cdc75486547bef476332ee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97218087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29987d85ab97128b74fc88a19cdbce4f1d3f8ea12715efa4b804e9ab93c4b0e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:14:04 GMT
ADD file:4954b2b03fa4bd48fabecbc1facd6d05808f55a143012aca45648ab2f767042a in / 
# Wed, 19 Aug 2020 21:14:14 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:14:22 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:14:29 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:14:32 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:50:51 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 19 Aug 2020 22:53:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:53:13 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 19 Aug 2020 22:55:50 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='8a994f9fd1adefcbc35ba6db41a42b642f1e1b456028521ff4b4fc35db331b7f';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='8841d9a3beb8954c939ba1c9675561b5f5a8bf4593efe38b34cd340a8d8b84fc';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e5700d984127dff2ec050ee6d325626c10369c6cc0fa89cc790e35f38506361a';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='299b484ad1909f59f1d329d8c48792f65de3672a592a8cb7fd2ffdaa622c8b36';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='fc150ceedbb86e00f6b309ad5868df94397c5cadc5f5593044997c4b7f3188cb';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 Aug 2020 22:55:57 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:23e4ce51557a90638716607f36b99292ea21b3e246ef66f83934e1eadb095632`  
		Last Modified: Mon, 10 Aug 2020 15:49:13 GMT  
		Size: 30.4 MB (30408877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b20479dd2a1972abd69e09a781025590f55fcbe8bef98a35b1067dceff85d60`  
		Last Modified: Wed, 19 Aug 2020 21:18:51 GMT  
		Size: 35.2 KB (35223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3107678818d326669afdd9fcce37d6b61613c2103e889ff7e019515b97ade1d`  
		Last Modified: Wed, 19 Aug 2020 21:18:51 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a571510b31b5805e20c811dcbb2413f66118e4be6a44a54c430826d8be670e7`  
		Last Modified: Wed, 19 Aug 2020 21:18:49 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9538a963d435f5fe1ba7326731a3fee312a667305ccdd70f519c5c40c2191d77`  
		Last Modified: Wed, 19 Aug 2020 22:57:56 GMT  
		Size: 3.1 MB (3075385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4213249081e4b2257b66ea99f3adcd00cf4a2c5f289368d4daa496e0e5fa6d74`  
		Last Modified: Wed, 19 Aug 2020 22:58:34 GMT  
		Size: 63.7 MB (63697557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:e4eeccf29fffb31f970762d4b5f50a8bc29fd647e8a9e0732f6761b5a8856cd9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92686296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9d289593b96b6fabb5456c53c86d7e8935988832908740b73acce39f75f60b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 19 Aug 2020 21:10:03 GMT
ADD file:1343b5ae7d875bd32e4eac552ae10c9631788fd97b99bcdeb9f6a9b85c230ba2 in / 
# Wed, 19 Aug 2020 21:10:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:10:05 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:10:06 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:10:06 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:08:24 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 19 Aug 2020 22:08:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:08:31 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 19 Aug 2020 22:09:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='8a994f9fd1adefcbc35ba6db41a42b642f1e1b456028521ff4b4fc35db331b7f';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='8841d9a3beb8954c939ba1c9675561b5f5a8bf4593efe38b34cd340a8d8b84fc';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e5700d984127dff2ec050ee6d325626c10369c6cc0fa89cc790e35f38506361a';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='299b484ad1909f59f1d329d8c48792f65de3672a592a8cb7fd2ffdaa622c8b36';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='fc150ceedbb86e00f6b309ad5868df94397c5cadc5f5593044997c4b7f3188cb';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 19 Aug 2020 22:10:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:25294e13856fd30261115dbfc6dd49e2d854414d32c9ead824b8183a83620e5c`  
		Last Modified: Mon, 10 Aug 2020 15:49:57 GMT  
		Size: 25.4 MB (25371147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e4b14541a6306ab7ffae9ed980e3ebac039f590869efecf63c6d745e1cde3c`  
		Last Modified: Wed, 19 Aug 2020 21:11:08 GMT  
		Size: 36.2 KB (36170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4164a02312fb3bccad51789030500218898a262ff17a962d62bb9849c9103d59`  
		Last Modified: Wed, 19 Aug 2020 21:11:08 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68677136804619b55f0437044d91d7bfe75e0b8013ca953c0d4db40c4d91d6b`  
		Last Modified: Wed, 19 Aug 2020 21:11:08 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2d7c1e4e8846aa212e0c088d2fa25dfc2856f64869c0721aaa4ef1499a7999`  
		Last Modified: Wed, 19 Aug 2020 22:11:12 GMT  
		Size: 2.7 MB (2672211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe89329a51b9b166e85c5f7d24d30d8c209a1e786b42b555da6d79145d5876ae`  
		Last Modified: Wed, 19 Aug 2020 22:11:34 GMT  
		Size: 64.6 MB (64605732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ibmjava:sfj-alpine`

```console
$ docker pull ibmjava@sha256:cbd2801fef988fe7f8eb3fcb1f021b2901cba6905c93a7db0b2bc263492677a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ibmjava:sfj-alpine` - linux; amd64

```console
$ docker pull ibmjava@sha256:53d64d9ae0235913ec9bac9d8a66be157ffb2f48c90bf35b81b2455d0d632e2b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71830710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bc2d6aa1d783c77157ca0045fd6e85aa02f8c6e70231bb1dd43e66fd79e5b5a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2020 19:19:49 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Fri, 19 Jun 2020 19:19:50 GMT
COPY file:3ca1cc706ceed4c671485bfc9a5f46a78571aaf829b0ab9fbb88c9d48e27ccd3 in /etc/apk/keys 
# Fri, 19 Jun 2020 19:20:01 GMT
RUN apk add --no-cache --virtual .build-deps curl binutils     && GLIBC_VER="2.30-r0"     && ALPINE_GLIBC_REPO="https://github.com/sgerrand/alpine-pkg-glibc/releases/download"     && GCC_LIBS_URL="https://archive.archlinux.org/packages/g/gcc-libs/gcc-libs-8.2.1%2B20180831-1-x86_64.pkg.tar.xz"     && GCC_LIBS_SHA256=e4b39fb1f5957c5aab5c2ce0c46e03d30426f3b94b9992b009d417ff2d56af4d     && curl -fLs https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub -o /tmp/sgerrand.rsa.pub     && cmp -s /etc/apk/keys/sgerrand.rsa.pub /tmp/sgerrand.rsa.pub     && curl -fLs ${ALPINE_GLIBC_REPO}/${GLIBC_VER}/glibc-${GLIBC_VER}.apk > /tmp/${GLIBC_VER}.apk     && apk add /tmp/${GLIBC_VER}.apk     && curl -fLs ${GCC_LIBS_URL} -o /tmp/gcc-libs.tar.xz     && echo "${GCC_LIBS_SHA256}  /tmp/gcc-libs.tar.xz" | sha256sum -c -     && mkdir /tmp/gcc     && tar -xf /tmp/gcc-libs.tar.xz -C /tmp/gcc     && mv /tmp/gcc/usr/lib/libgcc* /tmp/gcc/usr/lib/libstdc++* /usr/glibc-compat/lib     && strip /usr/glibc-compat/lib/libgcc_s.so.* /usr/glibc-compat/lib/libstdc++.so*     && apk del --purge .build-deps     && apk add --no-cache ca-certificates openssl     && rm -rf /tmp/${GLIBC_VER}.apk /tmp/gcc /tmp/gcc-libs.tar.xz /var/cache/apk/* /tmp/*.pub
# Wed, 05 Aug 2020 22:20:40 GMT
ENV JAVA_VERSION=1.8.0_sr6fp15
# Wed, 05 Aug 2020 22:22:35 GMT
RUN set -eux;     apk --no-cache add --virtual .build-deps wget;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='8a994f9fd1adefcbc35ba6db41a42b642f1e1b456028521ff4b4fc35db331b7f';          YML_FILE='sfj/linux/x86_64/index.yml';          ;;        i386)          ESUM='8841d9a3beb8954c939ba1c9675561b5f5a8bf4593efe38b34cd340a8d8b84fc';          YML_FILE='sfj/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='e5700d984127dff2ec050ee6d325626c10369c6cc0fa89cc790e35f38506361a';          YML_FILE='sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='299b484ad1909f59f1d329d8c48792f65de3672a592a8cb7fd2ffdaa622c8b36';          YML_FILE='sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='fc150ceedbb86e00f6b309ad5868df94397c5cadc5f5593044997c4b7f3188cb';          YML_FILE='sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;     apk del .build-deps;
# Wed, 05 Aug 2020 22:22:35 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54cb4ffe99c5f24fd5d9092d445c28497122a55355fd862f3431fe39b0069a3d`  
		Last Modified: Fri, 19 Jun 2020 19:22:30 GMT  
		Size: 545.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579fa70fe6805ba9995c002270c4bef412288205c0c631288438cdd962583a0d`  
		Last Modified: Fri, 19 Jun 2020 19:22:31 GMT  
		Size: 5.5 MB (5539665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cdf7bf8e813f627a159b6fe67fe7b7e280a12bb5d812f651cff0f7c6efce08`  
		Last Modified: Wed, 05 Aug 2020 22:26:02 GMT  
		Size: 63.5 MB (63492959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

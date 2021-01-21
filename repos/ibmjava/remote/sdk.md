## `ibmjava:sdk`

```console
$ docker pull ibmjava@sha256:30bd3315ee887bde3b8672e34bcecb1c44e4a72bc7add4673299c95adcbd5c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ibmjava:sdk` - linux; amd64

```console
$ docker pull ibmjava@sha256:2327cd5e5dec1ac285341b4ba2d20c815d99df96cc2b9116975139aae65c3080
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.2 MB (197182068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162249611eb653c8d474db0a56acac4f7e5bf2551130573ff392691a635c0267`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:25:13 GMT
ADD file:6ef542de9959c3061f2d0758adb031e226b221a1a2cd748ff59e6fc13216a1c0 in / 
# Wed, 25 Nov 2020 22:25:14 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:25:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:25:16 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:25:17 GMT
CMD ["/bin/bash"]
# Wed, 25 Nov 2020 23:12:02 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 25 Nov 2020 23:12:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 09 Dec 2020 04:08:58 GMT
ENV JAVA_VERSION=1.8.0_sr6fp20
# Wed, 09 Dec 2020 04:13:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='367a777afa71945eeaf623ff4f04d5dcd930eac2c1a234adbba4afe2d88926c1';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='a0e7eb3a68c2883e62b4a34e45c59c3f2880cfe57dbff09484c6b18fc2925e68';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4a7ac4712548d7630f2471a067406c94c3846fff75a0afc660682129dcf80e5b';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e6b476694cef95a2653a823dc5ed8e662ea08c975fe8564672385b5346ba29fe';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='17fad00b25231a85d15d681db2329f54d95cab48c1bab6bcd23b6306ad60d785';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 09 Dec 2020 04:13:27 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:f22ccc0b8772d8e1bcb40f137b373686bc27427a70c0e41dd22b38016e09e7e0`  
		Last Modified: Fri, 20 Nov 2020 13:21:30 GMT  
		Size: 26.7 MB (26708056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf8fb62ba5ffb221a2edb2208741346eb4d2d99a174138e4afbb69ce1fd9966`  
		Last Modified: Wed, 25 Nov 2020 22:26:30 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80c964ece6a3edf0db1cfc72ae0e6f0699fb776bbfcc92b708fbb945b0b9547`  
		Last Modified: Wed, 25 Nov 2020 22:26:30 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbbdc1b81f30dbbd36bce786a7db45a7e80384faea0379723165445aab33d793`  
		Last Modified: Wed, 25 Nov 2020 23:15:46 GMT  
		Size: 3.0 MB (2975364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a02c45f73adaa4512e533c811f3070666f904f9c12e14c5dec859e67f9cad3`  
		Last Modified: Wed, 09 Dec 2020 04:16:45 GMT  
		Size: 167.5 MB (167497636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; 386

```console
$ docker pull ibmjava@sha256:e0e7524592ad72d30db89499d28915843c942563e8b9ec0badb0994a9a2c5eb8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185844685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f085acd8562dbf11ab414f56accabb63c69456d35e99bdc75edc239fc0f673e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:44:18 GMT
ADD file:01b59ee8b65705b370ca0ae3515a429e8cbb9ab8fb22cce728108feff4ab182d in / 
# Thu, 21 Jan 2021 03:44:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:44:20 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 03:44:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:44:21 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 04:23:04 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 21 Jan 2021 04:23:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:23:13 GMT
ENV JAVA_VERSION=1.8.0_sr6fp20
# Thu, 21 Jan 2021 04:25:44 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='367a777afa71945eeaf623ff4f04d5dcd930eac2c1a234adbba4afe2d88926c1';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='a0e7eb3a68c2883e62b4a34e45c59c3f2880cfe57dbff09484c6b18fc2925e68';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4a7ac4712548d7630f2471a067406c94c3846fff75a0afc660682129dcf80e5b';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e6b476694cef95a2653a823dc5ed8e662ea08c975fe8564672385b5346ba29fe';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='17fad00b25231a85d15d681db2329f54d95cab48c1bab6bcd23b6306ad60d785';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 21 Jan 2021 04:25:44 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:a392d9ac4da4a6bfef8e4b1a5b3d67f0903ca47c0e6be7c0fa2d1207ea4ebc33`  
		Last Modified: Thu, 21 Jan 2021 03:45:04 GMT  
		Size: 27.1 MB (27137859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf47d4a0f4a9097aa0700057361f5bed24133938a630ee7fa36bef895bae976`  
		Last Modified: Thu, 21 Jan 2021 03:44:58 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d12f528b6dd5a2c96b3770017f558a77a79d82870a18293fc7d88afec2b52f`  
		Last Modified: Thu, 21 Jan 2021 03:44:58 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1145eae9404f424e7e41a234071086cd229f76465a493e0a5124e249263bfcd9`  
		Last Modified: Thu, 21 Jan 2021 04:26:13 GMT  
		Size: 3.0 MB (3002689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6e35b830b646f947977352877f2cacd333d84a05b6c9a08151542ff3407309`  
		Last Modified: Thu, 21 Jan 2021 04:27:10 GMT  
		Size: 155.7 MB (155703125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:33d3252c3055c42c43b7639cae857a0009880d46d161e431675e1f8dd5a9b4f6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.7 MB (200712588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503a6890ece81a8d261425ccace0e74ac799cbfe5c8eb09861d1cd10b1414694`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:21:42 GMT
ADD file:35026c42092857a1d20d4def6ac147d678e1e692decdc43f85d8f738ba889120 in / 
# Wed, 25 Nov 2020 22:22:02 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:22:15 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 25 Nov 2020 22:22:23 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:22:29 GMT
CMD ["/bin/bash"]
# Thu, 26 Nov 2020 01:42:24 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 26 Nov 2020 01:43:45 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 09 Dec 2020 05:00:41 GMT
ENV JAVA_VERSION=1.8.0_sr6fp20
# Wed, 09 Dec 2020 05:06:12 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='367a777afa71945eeaf623ff4f04d5dcd930eac2c1a234adbba4afe2d88926c1';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='a0e7eb3a68c2883e62b4a34e45c59c3f2880cfe57dbff09484c6b18fc2925e68';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4a7ac4712548d7630f2471a067406c94c3846fff75a0afc660682129dcf80e5b';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e6b476694cef95a2653a823dc5ed8e662ea08c975fe8564672385b5346ba29fe';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='17fad00b25231a85d15d681db2329f54d95cab48c1bab6bcd23b6306ad60d785';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 09 Dec 2020 05:06:34 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:83bc949c367f4f6e035dbcaa7d079a2e9f1e2e7a5db662f86772224750819827`  
		Last Modified: Mon, 23 Nov 2020 18:41:36 GMT  
		Size: 30.4 MB (30421462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4f6dea43dc0eb34aefcf5ef670e0bfbea3537a558b8760508df497341d5e637`  
		Last Modified: Wed, 25 Nov 2020 22:27:16 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913c73cb17025027afd384c5bd2b5f57add2dc2a5af20be1743da56431b9c5c0`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:104d224edb06f7b4b4a63e9416753dd0f3c8b15176441149bd2a8f53aa6935b1`  
		Last Modified: Thu, 26 Nov 2020 01:49:20 GMT  
		Size: 3.1 MB (3098476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bf3782aa45faf00c754d10c63ab6da53d248e1fde053a82eb08497d9678a41`  
		Last Modified: Wed, 09 Dec 2020 05:08:37 GMT  
		Size: 167.2 MB (167191604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ibmjava:sdk` - linux; s390x

```console
$ docker pull ibmjava@sha256:6c6f8734e9c1554a9271854aa2214a3a333adaa1dabe4dfb5b11bca5b7a39d44
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185909043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a0395e14c7459336e64e990d7e90a5356b4c3365936b2e79c5ab055bec80c2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 21 Jan 2021 04:00:45 GMT
ADD file:d443bbf06b974365e3cb2d99eea08d454059cf95b82a6023e4260fba5ead568e in / 
# Thu, 21 Jan 2021 04:00:51 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 04:00:53 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 21 Jan 2021 04:00:55 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 04:00:56 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 04:33:11 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Thu, 21 Jan 2021 04:33:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:33:25 GMT
ENV JAVA_VERSION=1.8.0_sr6fp20
# Thu, 21 Jan 2021 04:37:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='367a777afa71945eeaf623ff4f04d5dcd930eac2c1a234adbba4afe2d88926c1';          YML_FILE='sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='a0e7eb3a68c2883e62b4a34e45c59c3f2880cfe57dbff09484c6b18fc2925e68';          YML_FILE='sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='4a7ac4712548d7630f2471a067406c94c3846fff75a0afc660682129dcf80e5b';          YML_FILE='sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='e6b476694cef95a2653a823dc5ed8e662ea08c975fe8564672385b5346ba29fe';          YML_FILE='sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='17fad00b25231a85d15d681db2329f54d95cab48c1bab6bcd23b6306ad60d785';          YML_FILE='sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Thu, 21 Jan 2021 04:37:36 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:1a4e1c3f599543fe1043f321c3c5e14f5ca6073cba211f2144b569c5d0cff014`  
		Last Modified: Thu, 21 Jan 2021 04:03:17 GMT  
		Size: 25.4 MB (25381801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1202f2791a7390dbd7197d4cfde724e184be1b2f9d4791890fb64341336f889e`  
		Last Modified: Thu, 21 Jan 2021 04:03:13 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c44bad24828f92a8ff703d4d356f2969f0c1de9f6d852d3cec338a3aff6265`  
		Last Modified: Thu, 21 Jan 2021 04:03:13 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0790b1b850d834bc1ab5fc092fd86cfa28871f179c73453c07e80e721245333`  
		Last Modified: Thu, 21 Jan 2021 04:38:09 GMT  
		Size: 2.7 MB (2689532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9629f55b00870a71e2b04ea539d49dc3dd884375529869a0a127f6eb4de2b1`  
		Last Modified: Thu, 21 Jan 2021 04:39:07 GMT  
		Size: 157.8 MB (157836668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-6.5.1`

```console
$ docker pull couchbase@sha256:54448bed2c7272b5fc44a8a5d2e353eb0bcc38e584c0e47fbb898214b4cc43da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.5.1` - linux; amd64

```console
$ docker pull couchbase@sha256:c78017d81e17db52047b7adbba9636839b869ee608926e76ffd16cce5f61fb35
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **501.5 MB (501504321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1348e414e1386bc83366b8dae377e45135b22f3fef52a072e10cf505f95c4a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Thu, 17 Jun 2021 23:53:59 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 17 Jun 2021 23:54:38 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:54:40 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 17 Jun 2021 23:59:58 GMT
ARG CB_VERSION=6.5.1
# Thu, 17 Jun 2021 23:59:58 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1
# Thu, 17 Jun 2021 23:59:58 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu18.04_amd64.deb
# Thu, 17 Jun 2021 23:59:59 GMT
ARG CB_SHA256=992fc9aef85c210cc2d782a1726f2ef56ceb322fd67c2e95500e276ff106e6ff
# Thu, 17 Jun 2021 23:59:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 18 Jun 2021 00:00:00 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=992fc9aef85c210cc2d782a1726f2ef56ceb322fd67c2e95500e276ff106e6ff CB_VERSION=6.5.1
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 18 Jun 2021 00:00:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=992fc9aef85c210cc2d782a1726f2ef56ceb322fd67c2e95500e276ff106e6ff CB_VERSION=6.5.1
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 18 Jun 2021 00:01:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=992fc9aef85c210cc2d782a1726f2ef56ceb322fd67c2e95500e276ff106e6ff CB_VERSION=6.5.1
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 18 Jun 2021 00:01:03 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 18 Jun 2021 00:01:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=992fc9aef85c210cc2d782a1726f2ef56ceb322fd67c2e95500e276ff106e6ff CB_VERSION=6.5.1
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 18 Jun 2021 00:01:04 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:01:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=992fc9aef85c210cc2d782a1726f2ef56ceb322fd67c2e95500e276ff106e6ff CB_VERSION=6.5.1
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 18 Jun 2021 00:01:06 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=992fc9aef85c210cc2d782a1726f2ef56ceb322fd67c2e95500e276ff106e6ff CB_VERSION=6.5.1
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 18 Jun 2021 00:01:06 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 18 Jun 2021 00:01:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Jun 2021 00:01:06 GMT
CMD ["couchbase-server"]
# Fri, 18 Jun 2021 00:01:07 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 18 Jun 2021 00:01:07 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f23c2914264c712559d0bcc77a85377f94c9649ea3235072b3662e5d72a8cbe`  
		Last Modified: Fri, 18 Jun 2021 00:12:30 GMT  
		Size: 7.4 MB (7373851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5425c7cb0264c4c96e1eeef15ff71e54279d96b92737fbf84031243f93ba6d1`  
		Last Modified: Fri, 18 Jun 2021 00:12:25 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc1689f0a1796d5fc0fc626b7ac5288f0628efc3b89a7696da969b1a7704305`  
		Last Modified: Fri, 18 Jun 2021 00:16:46 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6061adc777fbd9280d52bc8d4b7fb60a18729e3d57a25f9bf05155af66ebd647`  
		Last Modified: Fri, 18 Jun 2021 00:17:41 GMT  
		Size: 467.3 MB (467307091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a378e24cad66949da0fda267cd3aa1ac96c6abfc70930f8c669c7d824249b3`  
		Last Modified: Fri, 18 Jun 2021 00:16:47 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a700db02f8ac0e6e8ec001a0581f7404788923c1505a94231dcd2a452d0339f8`  
		Last Modified: Fri, 18 Jun 2021 00:16:46 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977f4ece2efdf339ab77625b6827afd75ba3d6e5edb0fbb0cc7ae1e479e2cd57`  
		Last Modified: Fri, 18 Jun 2021 00:16:43 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d22e58b3b6f1ecb0d748d3aef99408fd764a2883a6975dbf5146171f5055a8`  
		Last Modified: Fri, 18 Jun 2021 00:16:43 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6727d2b48e171993775ede36ae1f9c85db386228f97f8e002fca83818c14bdc`  
		Last Modified: Fri, 18 Jun 2021 00:16:43 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4c6309e1120c41b9d412ab326fd26b78dcc6bbc2a08ee358c45f7e85f0c300`  
		Last Modified: Fri, 18 Jun 2021 00:16:44 GMT  
		Size: 118.2 KB (118190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e3ac5d9d49d697e429c79af1abccfc051fba84fcf83e029e7c91410d22d543`  
		Last Modified: Fri, 18 Jun 2021 00:16:43 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

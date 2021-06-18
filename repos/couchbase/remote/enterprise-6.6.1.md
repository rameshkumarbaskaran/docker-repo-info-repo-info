## `couchbase:enterprise-6.6.1`

```console
$ docker pull couchbase@sha256:0b13222ae52066763863ca35be3fb6b1d98b8b9dcb5b4725b98ced205490207b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.6.1` - linux; amd64

```console
$ docker pull couchbase@sha256:5a30ebba9b68c348218ff32169f91f1819d224f6d10f87782fa78d91ba30cd42
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **528.5 MB (528519982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff5dfd9354d6feb41256e35efabdb2ae86c6bd96d53231a74f13d7f831f97ca`
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
# Thu, 17 Jun 2021 23:57:20 GMT
ARG CB_VERSION=6.6.1
# Thu, 17 Jun 2021 23:57:21 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1
# Thu, 17 Jun 2021 23:57:21 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu18.04_amd64.deb
# Thu, 17 Jun 2021 23:57:21 GMT
ARG CB_SHA256=4bd8210458905a5801e98bda0663d1214f6743465843f49ef9a52212636b5e89
# Thu, 17 Jun 2021 23:57:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 17 Jun 2021 23:57:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=4bd8210458905a5801e98bda0663d1214f6743465843f49ef9a52212636b5e89 CB_VERSION=6.6.1
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 17 Jun 2021 23:58:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=4bd8210458905a5801e98bda0663d1214f6743465843f49ef9a52212636b5e89 CB_VERSION=6.6.1
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:58:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=4bd8210458905a5801e98bda0663d1214f6743465843f49ef9a52212636b5e89 CB_VERSION=6.6.1
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 17 Jun 2021 23:58:30 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 17 Jun 2021 23:58:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=4bd8210458905a5801e98bda0663d1214f6743465843f49ef9a52212636b5e89 CB_VERSION=6.6.1
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 17 Jun 2021 23:58:31 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 17 Jun 2021 23:58:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=4bd8210458905a5801e98bda0663d1214f6743465843f49ef9a52212636b5e89 CB_VERSION=6.6.1
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 17 Jun 2021 23:58:33 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.1 CB_SHA256=4bd8210458905a5801e98bda0663d1214f6743465843f49ef9a52212636b5e89 CB_VERSION=6.6.1
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 17 Jun 2021 23:58:33 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 17 Jun 2021 23:58:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Jun 2021 23:58:34 GMT
CMD ["couchbase-server"]
# Thu, 17 Jun 2021 23:58:34 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 17 Jun 2021 23:58:34 GMT
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
	-	`sha256:89787a3a9222b23a1a1113710da03a6a6519c85afba8c22201bade85b4d50bed`  
		Last Modified: Fri, 18 Jun 2021 00:14:20 GMT  
		Size: 2.0 KB (1964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2244ffe0af94a130953be2cc251e96791885663e82fbb0e61592ddefd97d8be`  
		Last Modified: Fri, 18 Jun 2021 00:15:16 GMT  
		Size: 494.3 MB (494322752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23c6b5c56afb70c77d0cd3e859b10375ce022a9ddf99d3d41faa064ffda60e9e`  
		Last Modified: Fri, 18 Jun 2021 00:14:20 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a5d4e8c19044b025fec8a29754cfce8526776aa119c1f829a404748588dc6f`  
		Last Modified: Fri, 18 Jun 2021 00:14:20 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87af809bfad4d754c234441ad5d36d94cbe0c50f14b27ddddc6629e0f16d549`  
		Last Modified: Fri, 18 Jun 2021 00:14:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d70ecccd457e718a64281676a2c63be88923a932e4174c1c1834ee2bc02bd0c`  
		Last Modified: Fri, 18 Jun 2021 00:14:18 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6cb1fd772a2632d64b17a56e98151a39b6e16dfce2da1cc6b15e2f25d8bd9d`  
		Last Modified: Fri, 18 Jun 2021 00:14:18 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f0e2ff2b687270332f3aa7e60ebee6cb94f7720960f3cbf8fcf2d83b7d38fbf`  
		Last Modified: Fri, 18 Jun 2021 00:14:18 GMT  
		Size: 118.2 KB (118191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cc0c073605dd0431c0c239ffffd0218f2553d42f1e794dcf5cd44088a7a7f5`  
		Last Modified: Fri, 18 Jun 2021 00:14:18 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

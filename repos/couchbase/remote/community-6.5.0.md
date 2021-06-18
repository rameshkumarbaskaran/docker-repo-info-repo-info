## `couchbase:community-6.5.0`

```console
$ docker pull couchbase@sha256:c3dc8c80238209fb5bf86df9bbbc1d7d8fc2f8675232f51c1ca0cd070f8fe5ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:community-6.5.0` - linux; amd64

```console
$ docker pull couchbase@sha256:ecbf1a70e4d4e97ec8cc5aeef3d9723162e0e193d6b3a08117930d5027637e71
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.6 MB (351608416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cfaaf6423b45cf9fedb1c9a2710385ff54fc536340c2e72874a5c8fa8fc1bde`
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
# Fri, 18 Jun 2021 00:07:10 GMT
ARG CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu18.04_amd64.deb
# Fri, 18 Jun 2021 00:07:10 GMT
ARG CB_SHA256=c4951cdab01759020444e4648023721ae3a333257591252475d34d5fc6ac8857
# Fri, 18 Jun 2021 00:07:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 18 Jun 2021 00:07:11 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=c4951cdab01759020444e4648023721ae3a333257591252475d34d5fc6ac8857 CB_VERSION=6.5.1
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 18 Jun 2021 00:07:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=c4951cdab01759020444e4648023721ae3a333257591252475d34d5fc6ac8857 CB_VERSION=6.5.1
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 18 Jun 2021 00:07:54 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=c4951cdab01759020444e4648023721ae3a333257591252475d34d5fc6ac8857 CB_VERSION=6.5.1
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 18 Jun 2021 00:07:55 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 18 Jun 2021 00:07:56 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=c4951cdab01759020444e4648023721ae3a333257591252475d34d5fc6ac8857 CB_VERSION=6.5.1
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 18 Jun 2021 00:07:56 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:07:57 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=c4951cdab01759020444e4648023721ae3a333257591252475d34d5fc6ac8857 CB_VERSION=6.5.1
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 18 Jun 2021 00:07:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=c4951cdab01759020444e4648023721ae3a333257591252475d34d5fc6ac8857 CB_VERSION=6.5.1
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 18 Jun 2021 00:07:58 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 18 Jun 2021 00:07:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Jun 2021 00:07:58 GMT
CMD ["couchbase-server"]
# Fri, 18 Jun 2021 00:07:59 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 18 Jun 2021 00:07:59 GMT
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
	-	`sha256:54c2836eeca2de7cbf1f1e43510077ab0895484b739665200582e48756300a22`  
		Last Modified: Fri, 18 Jun 2021 00:23:11 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623186f49f41a4e1cf8e6e7245301cefd8cd11568a05af39ecd8356644b28b84`  
		Last Modified: Fri, 18 Jun 2021 00:23:52 GMT  
		Size: 317.4 MB (317411183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6745a913839c7b4aaf1fdb41d9d3309915cb25f454ea93c91daf013077a4ad0`  
		Last Modified: Fri, 18 Jun 2021 00:23:11 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad045da201aa69e18ed31f273a9931cb26072795066fae210a7b0f9385f21ac`  
		Last Modified: Fri, 18 Jun 2021 00:23:11 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8e9bff8d13346accecf293094a36821f6f49f8419ed2ebf67325a39689fb3a`  
		Last Modified: Fri, 18 Jun 2021 00:23:08 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ea6816c2e6461b0aa848a1c46b90730d11fca2a9cbd65cbaa5826ea1f1bbb67`  
		Last Modified: Fri, 18 Jun 2021 00:23:08 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:815b3e6de6c2756fc414646fcbe57763fe64fadc97bd65e9e64f0769316de665`  
		Last Modified: Fri, 18 Jun 2021 00:23:08 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71726b059e33ec41762f4bb59470d86b5eaf69492eff3e656b07d9d385c40de1`  
		Last Modified: Fri, 18 Jun 2021 00:23:08 GMT  
		Size: 118.2 KB (118190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0432c730287be086e2eee3502b128e67dbe611010e7b59ecccbabc2a1380d6d6`  
		Last Modified: Fri, 18 Jun 2021 00:23:08 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchbase`

-	[`couchbase:6.0.5`](#couchbase605)
-	[`couchbase:6.6.5`](#couchbase665)
-	[`couchbase:7.0.3`](#couchbase703)
-	[`couchbase:community`](#couchbasecommunity)
-	[`couchbase:community-6.6.0`](#couchbasecommunity-660)
-	[`couchbase:community-7.0.2`](#couchbasecommunity-702)
-	[`couchbase:enterprise`](#couchbaseenterprise)
-	[`couchbase:enterprise-6.0.5`](#couchbaseenterprise-605)
-	[`couchbase:enterprise-6.6.5`](#couchbaseenterprise-665)
-	[`couchbase:enterprise-7.0.3`](#couchbaseenterprise-703)
-	[`couchbase:latest`](#couchbaselatest)

## `couchbase:6.0.5`

```console
$ docker pull couchbase@sha256:0ed512ce6de35ae7f30a4c4080b5f3e7deebba5f0a9d82926f1664a72471f962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:6.0.5` - linux; amd64

```console
$ docker pull couchbase@sha256:1dda6c80ec4974558f7ce738f13044651a7da8cafbd7aca5bdc4e98450c91e29
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.1 MB (466122331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a55fb4c69e2932cb6acea089d7e6edffc95fe4c9b1cbb2cc12cf3f3188d2b40`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:36 GMT
ADD file:c6039a4f004b6b6c2e4c281a228d64d8410cb9fdf0c67776f84bb173d3522be1 in / 
# Wed, 02 Feb 2022 02:14:36 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:48:15 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 02 Feb 2022 02:50:17 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:50:18 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Wed, 02 Feb 2022 02:50:18 GMT
ARG CB_VERSION=6.0.5
# Wed, 02 Feb 2022 02:50:18 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5
# Wed, 02 Feb 2022 02:50:19 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb
# Wed, 02 Feb 2022 02:50:19 GMT
ARG CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d
# Wed, 02 Feb 2022 02:50:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 02 Feb 2022 02:50:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 02 Feb 2022 02:51:18 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:51:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 02 Feb 2022 02:51:22 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Wed, 02 Feb 2022 02:51:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Wed, 02 Feb 2022 02:51:23 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:51:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 02 Feb 2022 02:51:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Wed, 02 Feb 2022 02:51:25 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Wed, 02 Feb 2022 02:51:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Feb 2022 02:51:25 GMT
CMD ["couchbase-server"]
# Wed, 02 Feb 2022 02:51:25 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Wed, 02 Feb 2022 02:51:25 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:68e7bb398b9ff421236990bfeaf5c1feab26c590eed93489e245375c23551e2a`  
		Last Modified: Sat, 29 Jan 2022 14:35:20 GMT  
		Size: 26.7 MB (26708066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba54da1fed646e55c6c4d1b71c4f317a4a5250a8ac092af6691767b311c7ae35`  
		Last Modified: Wed, 02 Feb 2022 02:56:23 GMT  
		Size: 15.9 MB (15921392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d794b9f33efe6d8977157d4ac5377b3685904a71c3620a022d30cd3e059b07ed`  
		Last Modified: Wed, 02 Feb 2022 02:56:18 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8254f789c1387cc82c2b32f9d6a9356eaf9e5d8999932f1b471dced2a078fa94`  
		Last Modified: Wed, 02 Feb 2022 02:56:17 GMT  
		Size: 2.0 KB (1963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfdad510c5f02d53ddc410fcccfb77fab84bc51a50cbdf5e24f7be3724e2b685`  
		Last Modified: Wed, 02 Feb 2022 02:56:59 GMT  
		Size: 423.4 MB (423362831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4796b56be115973358c0635c8b1be762dbbcf2d4b225c573225641b32a81aae`  
		Last Modified: Wed, 02 Feb 2022 02:56:18 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd03b499ec71f2b102b91141cec4b763425befd29b4ee24f7b374d2dd6a95043`  
		Last Modified: Wed, 02 Feb 2022 02:56:17 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5364de01f0c341dba16273b015af13a8e88f3c5029087aed1b3923206bd4266`  
		Last Modified: Wed, 02 Feb 2022 02:56:15 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18bedbedd446d1f57580fce54ad7fb3ee320dcd080f46f9ce2652189e284365b`  
		Last Modified: Wed, 02 Feb 2022 02:56:15 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21841c5a6eea70ad72241080650f562cd9f3f36e2b1447d01ef2d5bcb5f102ab`  
		Last Modified: Wed, 02 Feb 2022 02:56:15 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa680aa9b5725b96a7881310e69da0a945c655b4c1a88b4c81ba4712edb15ff`  
		Last Modified: Wed, 02 Feb 2022 02:56:15 GMT  
		Size: 125.6 KB (125557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2a5584c925ed99d4551dadaa0cf0d434e256638ca8927b726eeaf575f87ed4`  
		Last Modified: Wed, 02 Feb 2022 02:56:15 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:6.6.5`

```console
$ docker pull couchbase@sha256:3886eb23092c8e42c9113ae8b3c2913be8e323130a958739c783bc3e3cd7e9d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:6.6.5` - linux; amd64

```console
$ docker pull couchbase@sha256:02a08c0d00ee19dac6652145fd6f6afbb243fef8b4edea071ed39c99f68f0495
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.2 MB (541151121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c7bffdfe1ce5fd50c58e005901ba305dd06b5da3993bae9f5913eb9aea1ddd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:43:34 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 02 Feb 2022 02:46:36 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 02 Feb 2022 02:46:37 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:46:46 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Wed, 02 Feb 2022 02:46:46 GMT
ARG CB_VERSION=6.6.5
# Wed, 02 Feb 2022 02:46:46 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5
# Wed, 02 Feb 2022 02:46:46 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb
# Wed, 02 Feb 2022 02:46:47 GMT
ARG CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6
# Wed, 02 Feb 2022 02:46:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 02 Feb 2022 02:46:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_VERSION=6.6.5 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 02 Feb 2022 02:47:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_VERSION=6.6.5 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c -     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:47:50 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_VERSION=6.6.5 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 02 Feb 2022 02:47:50 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Wed, 02 Feb 2022 02:47:51 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_VERSION=6.6.5 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Wed, 02 Feb 2022 02:47:51 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:47:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_VERSION=6.6.5 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 02 Feb 2022 02:47:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_VERSION=6.6.5 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Wed, 02 Feb 2022 02:47:59 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Wed, 02 Feb 2022 02:48:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Feb 2022 02:48:00 GMT
CMD ["couchbase-server"]
# Wed, 02 Feb 2022 02:48:00 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Wed, 02 Feb 2022 02:48:00 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1754ce27a7ccb86d31d56d18a4e72ba9d67be285a916c8bd17248b727560a47d`  
		Last Modified: Wed, 02 Feb 2022 02:54:22 GMT  
		Size: 6.3 MB (6252084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5f7756f763ab2246a969908f94fa0b42406e43c41ad14c419d0ad54beb50d9`  
		Last Modified: Wed, 02 Feb 2022 02:54:20 GMT  
		Size: 1.8 KB (1828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbc09136fe05f40c619d016d0bba8dd53e94b083e1744226711ea3057fa8379`  
		Last Modified: Wed, 02 Feb 2022 02:55:16 GMT  
		Size: 505.9 MB (505890801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8fd0fde82ac5cd771ba6993145c59631f0e463809c2b727bd0056ad5f63665`  
		Last Modified: Wed, 02 Feb 2022 02:54:20 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8719c5cb0fb42529c032006f2414cd51e3ae277a9a9e8e322c4fd2f5d92e80`  
		Last Modified: Wed, 02 Feb 2022 02:54:20 GMT  
		Size: 743.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad063a0ccee34a72b08b383b143fd7c7f0069884c8a984966f56a6bd38c51f3d`  
		Last Modified: Wed, 02 Feb 2022 02:54:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1ec1e07f8149650f4c98a98a9259281d8fe9725da7995f86c9f57a58ec8dee`  
		Last Modified: Wed, 02 Feb 2022 02:54:18 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdb27013dd5b6ec10d9b8b8778d61a0573b2146537c7a716824bde5f3650be4`  
		Last Modified: Wed, 02 Feb 2022 02:54:18 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b151da713f459104635e6d2bee7174258be998280138a69ec849ad19260f6129`  
		Last Modified: Wed, 02 Feb 2022 02:54:18 GMT  
		Size: 439.8 KB (439771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fbf1915f342936bd4612edd42a845a199ff81e6bea379983490571b46ef6fd`  
		Last Modified: Wed, 02 Feb 2022 02:54:18 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:7.0.3`

```console
$ docker pull couchbase@sha256:b7fe37a8d08d4040b15e7697c3b1b35e34db207bad79a3d957d85eed570c6067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:7.0.3` - linux; amd64

```console
$ docker pull couchbase@sha256:3ee41d894fd019c7a00659b1c685e630250d09e85692cc4c590e458b398aaca7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.5 MB (677496418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff0aa38768b12da1562c06231cde38c8cc739b1ffa730b2a8fc91975a00656e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:43:34 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 02 Feb 2022 02:43:51 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:43:51 GMT
ARG CB_VERSION=7.0.3
# Wed, 02 Feb 2022 02:43:51 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3
# Wed, 02 Feb 2022 02:43:52 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb
# Wed, 02 Feb 2022 02:43:52 GMT
ARG CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c
# Wed, 02 Feb 2022 02:43:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 02 Feb 2022 02:43:53 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 02 Feb 2022 02:45:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:45:09 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 02 Feb 2022 02:45:09 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Wed, 02 Feb 2022 02:45:10 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Wed, 02 Feb 2022 02:45:10 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:45:11 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 02 Feb 2022 02:45:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             apt-get update;             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get purge -y chrpath;             apt-get autoremove;             apt-get clean;         fi
# Wed, 02 Feb 2022 02:45:19 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Wed, 02 Feb 2022 02:45:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Feb 2022 02:45:19 GMT
CMD ["couchbase-server"]
# Wed, 02 Feb 2022 02:45:19 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Wed, 02 Feb 2022 02:45:20 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847647b9360f9aad1f6c58fcacd59761db0751a4f43f49f443abe0ebfdd9a771`  
		Last Modified: Wed, 02 Feb 2022 02:51:53 GMT  
		Size: 6.3 MB (6252064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51893dafae15e810ea2b96978e5cf1a60b7655fc7edc928fdd581ecebcc3d62e`  
		Last Modified: Wed, 02 Feb 2022 02:51:49 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c61e05a235fb3653a6f011ad8f9c024efbf2a537dcac6bdd65740303c77a0e4`  
		Last Modified: Wed, 02 Feb 2022 02:52:59 GMT  
		Size: 618.3 MB (618297102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9805b55f10fe0fa41606c2befada0bf183362ca28845c3b6a1e6faefaf6e26`  
		Last Modified: Wed, 02 Feb 2022 02:51:49 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93fd98242510f7782081fdd0c9d61c233ac3252d771187088f003455508fe52e`  
		Last Modified: Wed, 02 Feb 2022 02:51:49 GMT  
		Size: 746.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc3831e2c2d11698c8304cdd17aec8c74f6109053d45a581abde33fffd3c40c`  
		Last Modified: Wed, 02 Feb 2022 02:51:47 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e51cc60ffa3e8305ff37b19af42e4e4888367b1cdc2a973f988a84b47e0ad8`  
		Last Modified: Wed, 02 Feb 2022 02:51:46 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b6d5f069c2d188607ba21063b88318c2fdcca45e6266591c93cd09381e2a23`  
		Last Modified: Wed, 02 Feb 2022 02:51:47 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193455409197bf87449315308de5d1d4412da4f31b1175f487bc4b1b5dd11d1e`  
		Last Modified: Wed, 02 Feb 2022 02:51:49 GMT  
		Size: 24.4 MB (24378774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa84c589b1b76bae8292a137b725ad2d70ee8385e591fe7794145831be66050`  
		Last Modified: Wed, 02 Feb 2022 02:51:46 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community`

```console
$ docker pull couchbase@sha256:4af91b8daeb91522d60dd6e1aa290769b2b2854b57715018c18016558097a6af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community` - linux; amd64

```console
$ docker pull couchbase@sha256:2cc2e66a841aa9a9a77b9d340b08d5d16d66f4a1925d4990d5887fb2fe0ae484
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.0 MB (429020776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4e2ad209fc8dda6a2fb8139b19a37d56b4f46a4354729c33e76fc11dcd8473`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:43:34 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 02 Feb 2022 02:45:37 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:45:38 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Wed, 02 Feb 2022 02:45:38 GMT
ARG CB_VERSION=7.0.2
# Wed, 02 Feb 2022 02:45:38 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2
# Wed, 02 Feb 2022 02:45:39 GMT
ARG CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb
# Wed, 02 Feb 2022 02:45:39 GMT
ARG CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
# Wed, 02 Feb 2022 02:45:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 02 Feb 2022 02:45:40 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 02 Feb 2022 02:46:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:46:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 02 Feb 2022 02:46:30 GMT
COPY file:cf9c7c8a9eda8a5fefcaa60d67181024b8a07b30eb318d4c9591b33a95ca6680 in /etc/service/couchbase-server/run 
# Wed, 02 Feb 2022 02:46:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Wed, 02 Feb 2022 02:46:31 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:46:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 02 Feb 2022 02:46:33 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Wed, 02 Feb 2022 02:46:33 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Wed, 02 Feb 2022 02:46:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Feb 2022 02:46:33 GMT
CMD ["couchbase-server"]
# Wed, 02 Feb 2022 02:46:34 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Wed, 02 Feb 2022 02:46:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c461decf964cb5352a497df5c119c5564ad59daaed0227372c08fd544a444891`  
		Last Modified: Wed, 02 Feb 2022 02:53:22 GMT  
		Size: 6.3 MB (6261170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ff820f8a414a224f1404ef28d239229484b22bc1cc1530bd463b3dc7827499`  
		Last Modified: Wed, 02 Feb 2022 02:53:20 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d2ed1b4e6b7adc74246f9b3afe009433c1a5d3206e7e82c3a8b7bccbecc87a`  
		Last Modified: Wed, 02 Feb 2022 02:53:19 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f943a9b83429b8a88e1c92f36612e6a47308dfce6ec02236bd04ee2269ab3b09`  
		Last Modified: Wed, 02 Feb 2022 02:54:08 GMT  
		Size: 394.1 MB (394061511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5013b5baeec032cb29e6ae47b1aa6d6420b85753fc7eb8db2660356c38f5d013`  
		Last Modified: Wed, 02 Feb 2022 02:53:19 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a018fd7f06ef974fd790efe050afd0f0b459bcced36277ce1b6f24167b9715`  
		Last Modified: Wed, 02 Feb 2022 02:53:18 GMT  
		Size: 603.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965dc3caaeeeaea7094dc482e0b8bcec416d75c52549e048b572ca3ade1dd229`  
		Last Modified: Wed, 02 Feb 2022 02:53:16 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48304fcbeddeb36b30a537ed61a1a16361832af670a50340eb7e096926697af`  
		Last Modified: Wed, 02 Feb 2022 02:53:17 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cff0acb92b06fbf82808aacb64e0429d9f0535bba10a9df3f61bcf640a1466f`  
		Last Modified: Wed, 02 Feb 2022 02:53:16 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac18fadba5138aaa641712af286a657bcedfc2789a9a012f54bdf1c87c01f3f`  
		Last Modified: Wed, 02 Feb 2022 02:53:17 GMT  
		Size: 129.5 KB (129514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae9073d19cc4e14ada0dd1ae4aa02c28fd01dcbc9a1d60f211a3a1019f2285c`  
		Last Modified: Wed, 02 Feb 2022 02:53:16 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-6.6.0`

```console
$ docker pull couchbase@sha256:fdd1d32c15ba32f2ede75472b17d2d46faa091b2dda3e7a332f985cdcc90162b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community-6.6.0` - linux; amd64

```console
$ docker pull couchbase@sha256:d201c08a35d3c387891b7db0f9b738729f3ca699c1e78bd3cffc97053314dc97
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.2 MB (354218743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc22a56175d8ceef0a6c9b673b56e89cfacb9872a41898a14e8cad76c3f1e9c1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:36 GMT
ADD file:c6039a4f004b6b6c2e4c281a228d64d8410cb9fdf0c67776f84bb173d3522be1 in / 
# Wed, 02 Feb 2022 02:14:36 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:48:15 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 02 Feb 2022 02:48:45 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:48:46 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Wed, 02 Feb 2022 02:48:46 GMT
ARG CB_VERSION=6.6.0
# Wed, 02 Feb 2022 02:48:46 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0
# Wed, 02 Feb 2022 02:48:47 GMT
ARG CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb
# Wed, 02 Feb 2022 02:48:47 GMT
ARG CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559
# Wed, 02 Feb 2022 02:48:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 02 Feb 2022 02:48:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 02 Feb 2022 02:49:34 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:49:35 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 02 Feb 2022 02:49:35 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Wed, 02 Feb 2022 02:49:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Wed, 02 Feb 2022 02:49:37 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:49:37 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 02 Feb 2022 02:49:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Wed, 02 Feb 2022 02:49:38 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Wed, 02 Feb 2022 02:49:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Feb 2022 02:49:39 GMT
CMD ["couchbase-server"]
# Wed, 02 Feb 2022 02:49:39 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Wed, 02 Feb 2022 02:49:39 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:68e7bb398b9ff421236990bfeaf5c1feab26c590eed93489e245375c23551e2a`  
		Last Modified: Sat, 29 Jan 2022 14:35:20 GMT  
		Size: 26.7 MB (26708066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e425b875a003fc3d1cb0261376c6c7b06f317ab62edc525973f364a81fa715b6`  
		Last Modified: Wed, 02 Feb 2022 02:55:33 GMT  
		Size: 7.4 MB (7369685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db3acdc189fe79683161c15fb20351332b6fa980f57cbbf2c14f9bc7a91839b1`  
		Last Modified: Wed, 02 Feb 2022 02:55:31 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216d4566df698875020ff56135b7c4b9ccec4f3ed1ac3bf3647dbe9236e6e44d`  
		Last Modified: Wed, 02 Feb 2022 02:55:30 GMT  
		Size: 2.0 KB (1962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a90fe8027662b5c454b3410922cf215003675074534f975f0fc8bfe298e55b`  
		Last Modified: Wed, 02 Feb 2022 02:56:08 GMT  
		Size: 320.0 MB (320018322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5181984dfb9361c67df2c5b5993c6cc4f3b6065bfcbf12064a6661a56f279da5`  
		Last Modified: Wed, 02 Feb 2022 02:55:29 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9dbdaf5435709bc5339630f695ff46a9380d7db3b17b9042c96d3e027fd13a`  
		Last Modified: Wed, 02 Feb 2022 02:55:29 GMT  
		Size: 473.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53a24c87a7220452e0949585ac9559d60825e6ef9e70e29411569fc08e95e2e`  
		Last Modified: Wed, 02 Feb 2022 02:55:27 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677095b029f2d6edf084c96e7c2cfa782c4450b6afa0fd39e253e8e0d62b2baf`  
		Last Modified: Wed, 02 Feb 2022 02:55:27 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ebc26fc42224cfbda435889d30e771ad96c02654c19e9fc3beb0e7f2eba22fe`  
		Last Modified: Wed, 02 Feb 2022 02:55:27 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aefcba46347e465d160a8620560e12acac13b728cfbb45fadb512c02ce03d94`  
		Last Modified: Wed, 02 Feb 2022 02:55:27 GMT  
		Size: 118.2 KB (118189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f556ceef96e57756240bf0d787fb91e7436f7630832ebb86197ffff68c7f143e`  
		Last Modified: Wed, 02 Feb 2022 02:55:27 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-7.0.2`

```console
$ docker pull couchbase@sha256:4af91b8daeb91522d60dd6e1aa290769b2b2854b57715018c18016558097a6af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community-7.0.2` - linux; amd64

```console
$ docker pull couchbase@sha256:2cc2e66a841aa9a9a77b9d340b08d5d16d66f4a1925d4990d5887fb2fe0ae484
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.0 MB (429020776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e4e2ad209fc8dda6a2fb8139b19a37d56b4f46a4354729c33e76fc11dcd8473`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:43:34 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 02 Feb 2022 02:45:37 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:45:38 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Wed, 02 Feb 2022 02:45:38 GMT
ARG CB_VERSION=7.0.2
# Wed, 02 Feb 2022 02:45:38 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2
# Wed, 02 Feb 2022 02:45:39 GMT
ARG CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb
# Wed, 02 Feb 2022 02:45:39 GMT
ARG CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
# Wed, 02 Feb 2022 02:45:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 02 Feb 2022 02:45:40 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 02 Feb 2022 02:46:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:46:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 02 Feb 2022 02:46:30 GMT
COPY file:cf9c7c8a9eda8a5fefcaa60d67181024b8a07b30eb318d4c9591b33a95ca6680 in /etc/service/couchbase-server/run 
# Wed, 02 Feb 2022 02:46:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Wed, 02 Feb 2022 02:46:31 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:46:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 02 Feb 2022 02:46:33 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Wed, 02 Feb 2022 02:46:33 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Wed, 02 Feb 2022 02:46:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Feb 2022 02:46:33 GMT
CMD ["couchbase-server"]
# Wed, 02 Feb 2022 02:46:34 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Wed, 02 Feb 2022 02:46:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c461decf964cb5352a497df5c119c5564ad59daaed0227372c08fd544a444891`  
		Last Modified: Wed, 02 Feb 2022 02:53:22 GMT  
		Size: 6.3 MB (6261170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ff820f8a414a224f1404ef28d239229484b22bc1cc1530bd463b3dc7827499`  
		Last Modified: Wed, 02 Feb 2022 02:53:20 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d2ed1b4e6b7adc74246f9b3afe009433c1a5d3206e7e82c3a8b7bccbecc87a`  
		Last Modified: Wed, 02 Feb 2022 02:53:19 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f943a9b83429b8a88e1c92f36612e6a47308dfce6ec02236bd04ee2269ab3b09`  
		Last Modified: Wed, 02 Feb 2022 02:54:08 GMT  
		Size: 394.1 MB (394061511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5013b5baeec032cb29e6ae47b1aa6d6420b85753fc7eb8db2660356c38f5d013`  
		Last Modified: Wed, 02 Feb 2022 02:53:19 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a018fd7f06ef974fd790efe050afd0f0b459bcced36277ce1b6f24167b9715`  
		Last Modified: Wed, 02 Feb 2022 02:53:18 GMT  
		Size: 603.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965dc3caaeeeaea7094dc482e0b8bcec416d75c52549e048b572ca3ade1dd229`  
		Last Modified: Wed, 02 Feb 2022 02:53:16 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48304fcbeddeb36b30a537ed61a1a16361832af670a50340eb7e096926697af`  
		Last Modified: Wed, 02 Feb 2022 02:53:17 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cff0acb92b06fbf82808aacb64e0429d9f0535bba10a9df3f61bcf640a1466f`  
		Last Modified: Wed, 02 Feb 2022 02:53:16 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac18fadba5138aaa641712af286a657bcedfc2789a9a012f54bdf1c87c01f3f`  
		Last Modified: Wed, 02 Feb 2022 02:53:17 GMT  
		Size: 129.5 KB (129514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae9073d19cc4e14ada0dd1ae4aa02c28fd01dcbc9a1d60f211a3a1019f2285c`  
		Last Modified: Wed, 02 Feb 2022 02:53:16 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise`

```console
$ docker pull couchbase@sha256:b7fe37a8d08d4040b15e7697c3b1b35e34db207bad79a3d957d85eed570c6067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise` - linux; amd64

```console
$ docker pull couchbase@sha256:3ee41d894fd019c7a00659b1c685e630250d09e85692cc4c590e458b398aaca7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.5 MB (677496418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff0aa38768b12da1562c06231cde38c8cc739b1ffa730b2a8fc91975a00656e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:43:34 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 02 Feb 2022 02:43:51 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:43:51 GMT
ARG CB_VERSION=7.0.3
# Wed, 02 Feb 2022 02:43:51 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3
# Wed, 02 Feb 2022 02:43:52 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb
# Wed, 02 Feb 2022 02:43:52 GMT
ARG CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c
# Wed, 02 Feb 2022 02:43:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 02 Feb 2022 02:43:53 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 02 Feb 2022 02:45:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:45:09 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 02 Feb 2022 02:45:09 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Wed, 02 Feb 2022 02:45:10 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Wed, 02 Feb 2022 02:45:10 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:45:11 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 02 Feb 2022 02:45:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             apt-get update;             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get purge -y chrpath;             apt-get autoremove;             apt-get clean;         fi
# Wed, 02 Feb 2022 02:45:19 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Wed, 02 Feb 2022 02:45:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Feb 2022 02:45:19 GMT
CMD ["couchbase-server"]
# Wed, 02 Feb 2022 02:45:19 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Wed, 02 Feb 2022 02:45:20 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847647b9360f9aad1f6c58fcacd59761db0751a4f43f49f443abe0ebfdd9a771`  
		Last Modified: Wed, 02 Feb 2022 02:51:53 GMT  
		Size: 6.3 MB (6252064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51893dafae15e810ea2b96978e5cf1a60b7655fc7edc928fdd581ecebcc3d62e`  
		Last Modified: Wed, 02 Feb 2022 02:51:49 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c61e05a235fb3653a6f011ad8f9c024efbf2a537dcac6bdd65740303c77a0e4`  
		Last Modified: Wed, 02 Feb 2022 02:52:59 GMT  
		Size: 618.3 MB (618297102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9805b55f10fe0fa41606c2befada0bf183362ca28845c3b6a1e6faefaf6e26`  
		Last Modified: Wed, 02 Feb 2022 02:51:49 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93fd98242510f7782081fdd0c9d61c233ac3252d771187088f003455508fe52e`  
		Last Modified: Wed, 02 Feb 2022 02:51:49 GMT  
		Size: 746.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc3831e2c2d11698c8304cdd17aec8c74f6109053d45a581abde33fffd3c40c`  
		Last Modified: Wed, 02 Feb 2022 02:51:47 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e51cc60ffa3e8305ff37b19af42e4e4888367b1cdc2a973f988a84b47e0ad8`  
		Last Modified: Wed, 02 Feb 2022 02:51:46 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b6d5f069c2d188607ba21063b88318c2fdcca45e6266591c93cd09381e2a23`  
		Last Modified: Wed, 02 Feb 2022 02:51:47 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193455409197bf87449315308de5d1d4412da4f31b1175f487bc4b1b5dd11d1e`  
		Last Modified: Wed, 02 Feb 2022 02:51:49 GMT  
		Size: 24.4 MB (24378774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa84c589b1b76bae8292a137b725ad2d70ee8385e591fe7794145831be66050`  
		Last Modified: Wed, 02 Feb 2022 02:51:46 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-6.0.5`

```console
$ docker pull couchbase@sha256:0ed512ce6de35ae7f30a4c4080b5f3e7deebba5f0a9d82926f1664a72471f962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise-6.0.5` - linux; amd64

```console
$ docker pull couchbase@sha256:1dda6c80ec4974558f7ce738f13044651a7da8cafbd7aca5bdc4e98450c91e29
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.1 MB (466122331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a55fb4c69e2932cb6acea089d7e6edffc95fe4c9b1cbb2cc12cf3f3188d2b40`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:36 GMT
ADD file:c6039a4f004b6b6c2e4c281a228d64d8410cb9fdf0c67776f84bb173d3522be1 in / 
# Wed, 02 Feb 2022 02:14:36 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:48:15 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 02 Feb 2022 02:50:17 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:50:18 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Wed, 02 Feb 2022 02:50:18 GMT
ARG CB_VERSION=6.0.5
# Wed, 02 Feb 2022 02:50:18 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5
# Wed, 02 Feb 2022 02:50:19 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb
# Wed, 02 Feb 2022 02:50:19 GMT
ARG CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d
# Wed, 02 Feb 2022 02:50:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 02 Feb 2022 02:50:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 02 Feb 2022 02:51:18 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:51:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 02 Feb 2022 02:51:22 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Wed, 02 Feb 2022 02:51:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Wed, 02 Feb 2022 02:51:23 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:51:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 02 Feb 2022 02:51:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Wed, 02 Feb 2022 02:51:25 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Wed, 02 Feb 2022 02:51:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Feb 2022 02:51:25 GMT
CMD ["couchbase-server"]
# Wed, 02 Feb 2022 02:51:25 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Wed, 02 Feb 2022 02:51:25 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:68e7bb398b9ff421236990bfeaf5c1feab26c590eed93489e245375c23551e2a`  
		Last Modified: Sat, 29 Jan 2022 14:35:20 GMT  
		Size: 26.7 MB (26708066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba54da1fed646e55c6c4d1b71c4f317a4a5250a8ac092af6691767b311c7ae35`  
		Last Modified: Wed, 02 Feb 2022 02:56:23 GMT  
		Size: 15.9 MB (15921392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d794b9f33efe6d8977157d4ac5377b3685904a71c3620a022d30cd3e059b07ed`  
		Last Modified: Wed, 02 Feb 2022 02:56:18 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8254f789c1387cc82c2b32f9d6a9356eaf9e5d8999932f1b471dced2a078fa94`  
		Last Modified: Wed, 02 Feb 2022 02:56:17 GMT  
		Size: 2.0 KB (1963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfdad510c5f02d53ddc410fcccfb77fab84bc51a50cbdf5e24f7be3724e2b685`  
		Last Modified: Wed, 02 Feb 2022 02:56:59 GMT  
		Size: 423.4 MB (423362831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4796b56be115973358c0635c8b1be762dbbcf2d4b225c573225641b32a81aae`  
		Last Modified: Wed, 02 Feb 2022 02:56:18 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd03b499ec71f2b102b91141cec4b763425befd29b4ee24f7b374d2dd6a95043`  
		Last Modified: Wed, 02 Feb 2022 02:56:17 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5364de01f0c341dba16273b015af13a8e88f3c5029087aed1b3923206bd4266`  
		Last Modified: Wed, 02 Feb 2022 02:56:15 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18bedbedd446d1f57580fce54ad7fb3ee320dcd080f46f9ce2652189e284365b`  
		Last Modified: Wed, 02 Feb 2022 02:56:15 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21841c5a6eea70ad72241080650f562cd9f3f36e2b1447d01ef2d5bcb5f102ab`  
		Last Modified: Wed, 02 Feb 2022 02:56:15 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa680aa9b5725b96a7881310e69da0a945c655b4c1a88b4c81ba4712edb15ff`  
		Last Modified: Wed, 02 Feb 2022 02:56:15 GMT  
		Size: 125.6 KB (125557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2a5584c925ed99d4551dadaa0cf0d434e256638ca8927b726eeaf575f87ed4`  
		Last Modified: Wed, 02 Feb 2022 02:56:15 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-6.6.5`

```console
$ docker pull couchbase@sha256:3886eb23092c8e42c9113ae8b3c2913be8e323130a958739c783bc3e3cd7e9d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise-6.6.5` - linux; amd64

```console
$ docker pull couchbase@sha256:02a08c0d00ee19dac6652145fd6f6afbb243fef8b4edea071ed39c99f68f0495
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **541.2 MB (541151121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c7bffdfe1ce5fd50c58e005901ba305dd06b5da3993bae9f5913eb9aea1ddd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:43:34 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 02 Feb 2022 02:46:36 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Wed, 02 Feb 2022 02:46:37 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:46:46 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Wed, 02 Feb 2022 02:46:46 GMT
ARG CB_VERSION=6.6.5
# Wed, 02 Feb 2022 02:46:46 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5
# Wed, 02 Feb 2022 02:46:46 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb
# Wed, 02 Feb 2022 02:46:47 GMT
ARG CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6
# Wed, 02 Feb 2022 02:46:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 02 Feb 2022 02:46:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_VERSION=6.6.5 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 02 Feb 2022 02:47:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_VERSION=6.6.5 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c -     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:47:50 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_VERSION=6.6.5 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 02 Feb 2022 02:47:50 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Wed, 02 Feb 2022 02:47:51 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_VERSION=6.6.5 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Wed, 02 Feb 2022 02:47:51 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:47:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_VERSION=6.6.5 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 02 Feb 2022 02:47:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.5-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.5 CB_SHA256=fb2da1880ea993dc7a5695c6fbe14cde62024d865a71a7d44ab653f0f633d4c6 CB_VERSION=6.6.5 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Wed, 02 Feb 2022 02:47:59 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Wed, 02 Feb 2022 02:48:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Feb 2022 02:48:00 GMT
CMD ["couchbase-server"]
# Wed, 02 Feb 2022 02:48:00 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Wed, 02 Feb 2022 02:48:00 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1754ce27a7ccb86d31d56d18a4e72ba9d67be285a916c8bd17248b727560a47d`  
		Last Modified: Wed, 02 Feb 2022 02:54:22 GMT  
		Size: 6.3 MB (6252084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5f7756f763ab2246a969908f94fa0b42406e43c41ad14c419d0ad54beb50d9`  
		Last Modified: Wed, 02 Feb 2022 02:54:20 GMT  
		Size: 1.8 KB (1828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbc09136fe05f40c619d016d0bba8dd53e94b083e1744226711ea3057fa8379`  
		Last Modified: Wed, 02 Feb 2022 02:55:16 GMT  
		Size: 505.9 MB (505890801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8fd0fde82ac5cd771ba6993145c59631f0e463809c2b727bd0056ad5f63665`  
		Last Modified: Wed, 02 Feb 2022 02:54:20 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8719c5cb0fb42529c032006f2414cd51e3ae277a9a9e8e322c4fd2f5d92e80`  
		Last Modified: Wed, 02 Feb 2022 02:54:20 GMT  
		Size: 743.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad063a0ccee34a72b08b383b143fd7c7f0069884c8a984966f56a6bd38c51f3d`  
		Last Modified: Wed, 02 Feb 2022 02:54:18 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1ec1e07f8149650f4c98a98a9259281d8fe9725da7995f86c9f57a58ec8dee`  
		Last Modified: Wed, 02 Feb 2022 02:54:18 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdb27013dd5b6ec10d9b8b8778d61a0573b2146537c7a716824bde5f3650be4`  
		Last Modified: Wed, 02 Feb 2022 02:54:18 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b151da713f459104635e6d2bee7174258be998280138a69ec849ad19260f6129`  
		Last Modified: Wed, 02 Feb 2022 02:54:18 GMT  
		Size: 439.8 KB (439771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fbf1915f342936bd4612edd42a845a199ff81e6bea379983490571b46ef6fd`  
		Last Modified: Wed, 02 Feb 2022 02:54:18 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-7.0.3`

```console
$ docker pull couchbase@sha256:b7fe37a8d08d4040b15e7697c3b1b35e34db207bad79a3d957d85eed570c6067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise-7.0.3` - linux; amd64

```console
$ docker pull couchbase@sha256:3ee41d894fd019c7a00659b1c685e630250d09e85692cc4c590e458b398aaca7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.5 MB (677496418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff0aa38768b12da1562c06231cde38c8cc739b1ffa730b2a8fc91975a00656e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:43:34 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 02 Feb 2022 02:43:51 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:43:51 GMT
ARG CB_VERSION=7.0.3
# Wed, 02 Feb 2022 02:43:51 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3
# Wed, 02 Feb 2022 02:43:52 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb
# Wed, 02 Feb 2022 02:43:52 GMT
ARG CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c
# Wed, 02 Feb 2022 02:43:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 02 Feb 2022 02:43:53 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 02 Feb 2022 02:45:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:45:09 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 02 Feb 2022 02:45:09 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Wed, 02 Feb 2022 02:45:10 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Wed, 02 Feb 2022 02:45:10 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:45:11 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 02 Feb 2022 02:45:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             apt-get update;             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get purge -y chrpath;             apt-get autoremove;             apt-get clean;         fi
# Wed, 02 Feb 2022 02:45:19 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Wed, 02 Feb 2022 02:45:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Feb 2022 02:45:19 GMT
CMD ["couchbase-server"]
# Wed, 02 Feb 2022 02:45:19 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Wed, 02 Feb 2022 02:45:20 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847647b9360f9aad1f6c58fcacd59761db0751a4f43f49f443abe0ebfdd9a771`  
		Last Modified: Wed, 02 Feb 2022 02:51:53 GMT  
		Size: 6.3 MB (6252064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51893dafae15e810ea2b96978e5cf1a60b7655fc7edc928fdd581ecebcc3d62e`  
		Last Modified: Wed, 02 Feb 2022 02:51:49 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c61e05a235fb3653a6f011ad8f9c024efbf2a537dcac6bdd65740303c77a0e4`  
		Last Modified: Wed, 02 Feb 2022 02:52:59 GMT  
		Size: 618.3 MB (618297102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9805b55f10fe0fa41606c2befada0bf183362ca28845c3b6a1e6faefaf6e26`  
		Last Modified: Wed, 02 Feb 2022 02:51:49 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93fd98242510f7782081fdd0c9d61c233ac3252d771187088f003455508fe52e`  
		Last Modified: Wed, 02 Feb 2022 02:51:49 GMT  
		Size: 746.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc3831e2c2d11698c8304cdd17aec8c74f6109053d45a581abde33fffd3c40c`  
		Last Modified: Wed, 02 Feb 2022 02:51:47 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e51cc60ffa3e8305ff37b19af42e4e4888367b1cdc2a973f988a84b47e0ad8`  
		Last Modified: Wed, 02 Feb 2022 02:51:46 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b6d5f069c2d188607ba21063b88318c2fdcca45e6266591c93cd09381e2a23`  
		Last Modified: Wed, 02 Feb 2022 02:51:47 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193455409197bf87449315308de5d1d4412da4f31b1175f487bc4b1b5dd11d1e`  
		Last Modified: Wed, 02 Feb 2022 02:51:49 GMT  
		Size: 24.4 MB (24378774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa84c589b1b76bae8292a137b725ad2d70ee8385e591fe7794145831be66050`  
		Last Modified: Wed, 02 Feb 2022 02:51:46 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:latest`

```console
$ docker pull couchbase@sha256:b7fe37a8d08d4040b15e7697c3b1b35e34db207bad79a3d957d85eed570c6067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:latest` - linux; amd64

```console
$ docker pull couchbase@sha256:3ee41d894fd019c7a00659b1c685e630250d09e85692cc4c590e458b398aaca7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.5 MB (677496418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff0aa38768b12da1562c06231cde38c8cc739b1ffa730b2a8fc91975a00656e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:43:34 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 02 Feb 2022 02:43:51 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:43:51 GMT
ARG CB_VERSION=7.0.3
# Wed, 02 Feb 2022 02:43:51 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3
# Wed, 02 Feb 2022 02:43:52 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb
# Wed, 02 Feb 2022 02:43:52 GMT
ARG CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c
# Wed, 02 Feb 2022 02:43:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 02 Feb 2022 02:43:53 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 02 Feb 2022 02:45:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 02 Feb 2022 02:45:09 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 02 Feb 2022 02:45:09 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Wed, 02 Feb 2022 02:45:10 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Wed, 02 Feb 2022 02:45:10 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:45:11 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 02 Feb 2022 02:45:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             apt-get update;             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get purge -y chrpath;             apt-get autoremove;             apt-get clean;         fi
# Wed, 02 Feb 2022 02:45:19 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Wed, 02 Feb 2022 02:45:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Feb 2022 02:45:19 GMT
CMD ["couchbase-server"]
# Wed, 02 Feb 2022 02:45:19 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Wed, 02 Feb 2022 02:45:20 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847647b9360f9aad1f6c58fcacd59761db0751a4f43f49f443abe0ebfdd9a771`  
		Last Modified: Wed, 02 Feb 2022 02:51:53 GMT  
		Size: 6.3 MB (6252064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51893dafae15e810ea2b96978e5cf1a60b7655fc7edc928fdd581ecebcc3d62e`  
		Last Modified: Wed, 02 Feb 2022 02:51:49 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c61e05a235fb3653a6f011ad8f9c024efbf2a537dcac6bdd65740303c77a0e4`  
		Last Modified: Wed, 02 Feb 2022 02:52:59 GMT  
		Size: 618.3 MB (618297102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9805b55f10fe0fa41606c2befada0bf183362ca28845c3b6a1e6faefaf6e26`  
		Last Modified: Wed, 02 Feb 2022 02:51:49 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93fd98242510f7782081fdd0c9d61c233ac3252d771187088f003455508fe52e`  
		Last Modified: Wed, 02 Feb 2022 02:51:49 GMT  
		Size: 746.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc3831e2c2d11698c8304cdd17aec8c74f6109053d45a581abde33fffd3c40c`  
		Last Modified: Wed, 02 Feb 2022 02:51:47 GMT  
		Size: 282.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e51cc60ffa3e8305ff37b19af42e4e4888367b1cdc2a973f988a84b47e0ad8`  
		Last Modified: Wed, 02 Feb 2022 02:51:46 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b6d5f069c2d188607ba21063b88318c2fdcca45e6266591c93cd09381e2a23`  
		Last Modified: Wed, 02 Feb 2022 02:51:47 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193455409197bf87449315308de5d1d4412da4f31b1175f487bc4b1b5dd11d1e`  
		Last Modified: Wed, 02 Feb 2022 02:51:49 GMT  
		Size: 24.4 MB (24378774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa84c589b1b76bae8292a137b725ad2d70ee8385e591fe7794145831be66050`  
		Last Modified: Wed, 02 Feb 2022 02:51:46 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

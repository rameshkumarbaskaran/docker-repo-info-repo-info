<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchbase`

-	[`couchbase:6.0.1`](#couchbase601)
-	[`couchbase:6.0.2`](#couchbase602)
-	[`couchbase:6.0.3`](#couchbase603)
-	[`couchbase:6.0.4`](#couchbase604)
-	[`couchbase:6.0.5`](#couchbase605)
-	[`couchbase:6.5.0`](#couchbase650)
-	[`couchbase:6.5.1`](#couchbase651)
-	[`couchbase:6.6.0`](#couchbase660)
-	[`couchbase:6.6.1`](#couchbase661)
-	[`couchbase:6.6.2`](#couchbase662)
-	[`couchbase:7.0.0-beta`](#couchbase700-beta)
-	[`couchbase:community`](#couchbasecommunity)
-	[`couchbase:community-6.5.0`](#couchbasecommunity-650)
-	[`couchbase:community-6.5.1`](#couchbasecommunity-651)
-	[`couchbase:community-6.6.0`](#couchbasecommunity-660)
-	[`couchbase:community-7.0.0-beta`](#couchbasecommunity-700-beta)
-	[`couchbase:enterprise`](#couchbaseenterprise)
-	[`couchbase:enterprise-6.0.1`](#couchbaseenterprise-601)
-	[`couchbase:enterprise-6.0.2`](#couchbaseenterprise-602)
-	[`couchbase:enterprise-6.0.3`](#couchbaseenterprise-603)
-	[`couchbase:enterprise-6.0.4`](#couchbaseenterprise-604)
-	[`couchbase:enterprise-6.0.5`](#couchbaseenterprise-605)
-	[`couchbase:enterprise-6.5.0`](#couchbaseenterprise-650)
-	[`couchbase:enterprise-6.5.1`](#couchbaseenterprise-651)
-	[`couchbase:enterprise-6.6.0`](#couchbaseenterprise-660)
-	[`couchbase:enterprise-6.6.1`](#couchbaseenterprise-661)
-	[`couchbase:enterprise-6.6.2`](#couchbaseenterprise-662)
-	[`couchbase:enterprise-7.0.0-beta`](#couchbaseenterprise-700-beta)
-	[`couchbase:latest`](#couchbaselatest)

## `couchbase:6.0.1`

```console
$ docker pull couchbase@sha256:fe1b56fb539ceb82334bd967c328b23b7cd8dce109b9e846f0e279432b570c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:6.0.1` - linux; amd64

```console
$ docker pull couchbase@sha256:dde19a8adbe3a3b0f4646c3fb3790e8f2e6d777488a9354f6dad9c6e214f9ba4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.2 MB (455207785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8061fc9cbad81be792ddc4baabb50b21d50a101dc1c64a6cd23739371981633`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Thu, 17 Jun 2021 23:53:59 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 17 Jun 2021 23:56:05 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:56:06 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 18 Jun 2021 00:05:58 GMT
ARG CB_VERSION=6.0.1
# Fri, 18 Jun 2021 00:05:58 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.1
# Fri, 18 Jun 2021 00:05:58 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.1-ubuntu18.04_amd64.deb
# Fri, 18 Jun 2021 00:05:58 GMT
ARG CB_SHA256=68deed9ba855e2a84500ae99a787c415fc85b4d4dc1140be28ae6f56662bafea
# Fri, 18 Jun 2021 00:05:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 18 Jun 2021 00:06:00 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.1 CB_SHA256=68deed9ba855e2a84500ae99a787c415fc85b4d4dc1140be28ae6f56662bafea CB_VERSION=6.0.1
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 18 Jun 2021 00:06:53 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.1 CB_SHA256=68deed9ba855e2a84500ae99a787c415fc85b4d4dc1140be28ae6f56662bafea CB_VERSION=6.0.1
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 18 Jun 2021 00:06:56 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.1 CB_SHA256=68deed9ba855e2a84500ae99a787c415fc85b4d4dc1140be28ae6f56662bafea CB_VERSION=6.0.1
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 18 Jun 2021 00:06:57 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 18 Jun 2021 00:06:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.1 CB_SHA256=68deed9ba855e2a84500ae99a787c415fc85b4d4dc1140be28ae6f56662bafea CB_VERSION=6.0.1
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 18 Jun 2021 00:06:58 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:06:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.1 CB_SHA256=68deed9ba855e2a84500ae99a787c415fc85b4d4dc1140be28ae6f56662bafea CB_VERSION=6.0.1
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 18 Jun 2021 00:07:00 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.1 CB_SHA256=68deed9ba855e2a84500ae99a787c415fc85b4d4dc1140be28ae6f56662bafea CB_VERSION=6.0.1
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 18 Jun 2021 00:07:00 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 18 Jun 2021 00:07:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Jun 2021 00:07:00 GMT
CMD ["couchbase-server"]
# Fri, 18 Jun 2021 00:07:00 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 18 Jun 2021 00:07:01 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bf3da53cf4b3f333e9356133c7830082e23c62dddddb71c4d2c08ea2915223`  
		Last Modified: Fri, 18 Jun 2021 00:13:27 GMT  
		Size: 15.9 MB (15923371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545dc5a4237ac749c5a107319df722d3d49b8cafcb548eede9190b28815c17e0`  
		Last Modified: Fri, 18 Jun 2021 00:13:20 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4247353f0bc85046a83a6cc2aad427553fbbec5f0b85ba8eee16b26da71d9ce0`  
		Last Modified: Fri, 18 Jun 2021 00:22:15 GMT  
		Size: 2.0 KB (1968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02bb17bb9093629862371fb12376e60d9478a01db74c9fc426c4bda1d0e0001e`  
		Last Modified: Fri, 18 Jun 2021 00:22:56 GMT  
		Size: 412.5 MB (412453654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034c7cb9e25b0ac592dc8b665885d3f6f76e1206678572370c0752c9ecf06481`  
		Last Modified: Fri, 18 Jun 2021 00:22:15 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02f16e49a1343c3a599156959420c59a131fbd06b7e99b0be14eb0b9952896ef`  
		Last Modified: Fri, 18 Jun 2021 00:22:15 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bd1e75e933c1a068f7a2cc9e7842713c664a70212b1dca6cee3f8e79bdb723`  
		Last Modified: Fri, 18 Jun 2021 00:22:13 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffde94834e60ef62b65cdcb28a92822fca9cda5013e3b669f6525b9534ee6e5`  
		Last Modified: Fri, 18 Jun 2021 00:22:13 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2c163249a75391387f01ce8911bf096e0134929731b176a3d7e27585b31f11`  
		Last Modified: Fri, 18 Jun 2021 00:22:13 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd99b4fba7d151e735fa15444042e6f01772f6763b6a1a2018a1eb8ec28a9d7e`  
		Last Modified: Fri, 18 Jun 2021 00:22:13 GMT  
		Size: 125.6 KB (125561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64dd53fbddeefbc0dbe648be59142805bde2d6c77b8476cb9edf24ee7dab4832`  
		Last Modified: Fri, 18 Jun 2021 00:22:13 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:6.0.2`

```console
$ docker pull couchbase@sha256:f14dc5a0682cf7a3d22cdf114cbc74aac02dfc25fd4394a2e84bc42d52febf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:6.0.2` - linux; amd64

```console
$ docker pull couchbase@sha256:f2753e9204daf3d6d1929812db4149d5bc1a3dbd7d1030f8418f6e7ffef53d18
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.4 MB (463377939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614fe6e4f61467fc368c3960ff074ad557a42091c396b4b1a5809597ec68faa1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Thu, 17 Jun 2021 23:53:59 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 17 Jun 2021 23:56:05 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:56:06 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 18 Jun 2021 00:04:46 GMT
ARG CB_VERSION=6.0.2
# Fri, 18 Jun 2021 00:04:46 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.2
# Fri, 18 Jun 2021 00:04:46 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.2-ubuntu18.04_amd64.deb
# Fri, 18 Jun 2021 00:04:46 GMT
ARG CB_SHA256=5410a56cefd7a9c624a2d64e474058b43a90e8d66c73fea6b2a8b16a4f6fe14d
# Fri, 18 Jun 2021 00:04:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 18 Jun 2021 00:04:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.2-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.2 CB_SHA256=5410a56cefd7a9c624a2d64e474058b43a90e8d66c73fea6b2a8b16a4f6fe14d CB_VERSION=6.0.2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 18 Jun 2021 00:05:41 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.2-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.2 CB_SHA256=5410a56cefd7a9c624a2d64e474058b43a90e8d66c73fea6b2a8b16a4f6fe14d CB_VERSION=6.0.2
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 18 Jun 2021 00:05:44 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.2-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.2 CB_SHA256=5410a56cefd7a9c624a2d64e474058b43a90e8d66c73fea6b2a8b16a4f6fe14d CB_VERSION=6.0.2
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 18 Jun 2021 00:05:44 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 18 Jun 2021 00:05:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.2-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.2 CB_SHA256=5410a56cefd7a9c624a2d64e474058b43a90e8d66c73fea6b2a8b16a4f6fe14d CB_VERSION=6.0.2
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 18 Jun 2021 00:05:45 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:05:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.2-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.2 CB_SHA256=5410a56cefd7a9c624a2d64e474058b43a90e8d66c73fea6b2a8b16a4f6fe14d CB_VERSION=6.0.2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 18 Jun 2021 00:05:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.2-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.2 CB_SHA256=5410a56cefd7a9c624a2d64e474058b43a90e8d66c73fea6b2a8b16a4f6fe14d CB_VERSION=6.0.2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 18 Jun 2021 00:05:48 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 18 Jun 2021 00:05:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Jun 2021 00:05:48 GMT
CMD ["couchbase-server"]
# Fri, 18 Jun 2021 00:05:48 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 18 Jun 2021 00:05:49 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bf3da53cf4b3f333e9356133c7830082e23c62dddddb71c4d2c08ea2915223`  
		Last Modified: Fri, 18 Jun 2021 00:13:27 GMT  
		Size: 15.9 MB (15923371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545dc5a4237ac749c5a107319df722d3d49b8cafcb548eede9190b28815c17e0`  
		Last Modified: Fri, 18 Jun 2021 00:13:20 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b1c2e053a5ec9ecd93a27aeeb1b32aaf0392ad1c33fe8f859078bb378be1b0`  
		Last Modified: Fri, 18 Jun 2021 00:21:19 GMT  
		Size: 2.0 KB (1968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b556c35a544d05c2ecfd95dd3b4d0edeb788664964f3e472f9fbf26babe221`  
		Last Modified: Fri, 18 Jun 2021 00:22:01 GMT  
		Size: 420.6 MB (420623807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4213e210b9d470e9b3e5c56908c34bd50bf8e4b79336e73e69057c058611e50`  
		Last Modified: Fri, 18 Jun 2021 00:21:18 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0246c4edda97f1d3586d842263d1a3b5ddaccc755b2729f1db02da3e76875420`  
		Last Modified: Fri, 18 Jun 2021 00:21:18 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b4b14d12afc0a09713ce5e3788f1fbb57df4d48fc47548c1ffedb8168bbe26e`  
		Last Modified: Fri, 18 Jun 2021 00:21:16 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3e98800a13b2af6203e88fa36e59ebcbf1557b1229b1c8fa38f93ad2424a8d`  
		Last Modified: Fri, 18 Jun 2021 00:21:16 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb38a623972beed70f2ad1e80d9e4250b2b098683fb993cdc6651edee54804f4`  
		Last Modified: Fri, 18 Jun 2021 00:21:16 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8637d65dcd664f6d6a04a691b6b17a19b64e52e1337ac13c7d450b77fc04d2d`  
		Last Modified: Fri, 18 Jun 2021 00:21:16 GMT  
		Size: 125.6 KB (125562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae85e8be4d0329da5496d8993ef0c4d3ff851336bb16111c7687ea3d077d6a2`  
		Last Modified: Fri, 18 Jun 2021 00:21:16 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:6.0.3`

```console
$ docker pull couchbase@sha256:6a5a77c25506213d95ed904831ee5673dd0de00f908347ee7b764da884c9bd63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:6.0.3` - linux; amd64

```console
$ docker pull couchbase@sha256:c2bd562e1899f2864037badfbb8448e75be5304e1c47ab4a10b6eae5007bc8f4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.9 MB (465902080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6001279031fc322a86ad8bcb7b885204e5582a90c0df3296d85f91a38603f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Thu, 17 Jun 2021 23:53:59 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 17 Jun 2021 23:56:05 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:56:06 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 18 Jun 2021 00:03:34 GMT
ARG CB_VERSION=6.0.3
# Fri, 18 Jun 2021 00:03:34 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3
# Fri, 18 Jun 2021 00:03:34 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu18.04_amd64.deb
# Fri, 18 Jun 2021 00:03:34 GMT
ARG CB_SHA256=8ee814ea8d99141de5493a6a24423c6a5dc4e01b8393dce87ca1639630315382
# Fri, 18 Jun 2021 00:03:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 18 Jun 2021 00:03:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=8ee814ea8d99141de5493a6a24423c6a5dc4e01b8393dce87ca1639630315382 CB_VERSION=6.0.3
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 18 Jun 2021 00:04:25 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=8ee814ea8d99141de5493a6a24423c6a5dc4e01b8393dce87ca1639630315382 CB_VERSION=6.0.3
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 18 Jun 2021 00:04:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=8ee814ea8d99141de5493a6a24423c6a5dc4e01b8393dce87ca1639630315382 CB_VERSION=6.0.3
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 18 Jun 2021 00:04:28 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 18 Jun 2021 00:04:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=8ee814ea8d99141de5493a6a24423c6a5dc4e01b8393dce87ca1639630315382 CB_VERSION=6.0.3
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 18 Jun 2021 00:04:30 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:04:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=8ee814ea8d99141de5493a6a24423c6a5dc4e01b8393dce87ca1639630315382 CB_VERSION=6.0.3
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 18 Jun 2021 00:04:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=8ee814ea8d99141de5493a6a24423c6a5dc4e01b8393dce87ca1639630315382 CB_VERSION=6.0.3
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 18 Jun 2021 00:04:32 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 18 Jun 2021 00:04:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Jun 2021 00:04:32 GMT
CMD ["couchbase-server"]
# Fri, 18 Jun 2021 00:04:32 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 18 Jun 2021 00:04:33 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bf3da53cf4b3f333e9356133c7830082e23c62dddddb71c4d2c08ea2915223`  
		Last Modified: Fri, 18 Jun 2021 00:13:27 GMT  
		Size: 15.9 MB (15923371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545dc5a4237ac749c5a107319df722d3d49b8cafcb548eede9190b28815c17e0`  
		Last Modified: Fri, 18 Jun 2021 00:13:20 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7140b47541859c7c1da04c3969a13a8d032439f6d6a2c9513bb22d30e9ec81a6`  
		Last Modified: Fri, 18 Jun 2021 00:20:16 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e0406848c935ddd75ff5f5d47fe98660f5a2e78fde07afcd8cd30f380ae7b9`  
		Last Modified: Fri, 18 Jun 2021 00:21:00 GMT  
		Size: 423.1 MB (423147946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9170b125c4dfadd1de7ff92e44c7003ff72668b698aa325186fff3449bff11`  
		Last Modified: Fri, 18 Jun 2021 00:20:16 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f29d7d6b7b107a076a04ba0af409db31ad694286c20909d062dfe0e7727c82`  
		Last Modified: Fri, 18 Jun 2021 00:20:16 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824042d8a830a420e0056c91ef62066d8c470cce68ef9188e0f6376d7f560336`  
		Last Modified: Fri, 18 Jun 2021 00:20:13 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72387d752334c7aed3331bb81c29ca85715a9339bc8b4a8cce570b09657614bf`  
		Last Modified: Fri, 18 Jun 2021 00:20:13 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e68c8a505ee1f4e68a60face6e5bf403fdf2668cef8c3a672ec04d1fbd3b67`  
		Last Modified: Fri, 18 Jun 2021 00:20:13 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c1c2d190ec7b3209221de5f1c091504f4974c599df4e28bf6ec1b889eb5d32`  
		Last Modified: Fri, 18 Jun 2021 00:20:14 GMT  
		Size: 125.6 KB (125562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf203913c66cafb3b670211298dfa44b94c5171a1546bea93e9a22508509994`  
		Last Modified: Fri, 18 Jun 2021 00:20:13 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:6.0.4`

```console
$ docker pull couchbase@sha256:768a0be972b295b8fd967c0ded61a278c1c2ef22e659c3892850f0760b12e784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:6.0.4` - linux; amd64

```console
$ docker pull couchbase@sha256:c298a4d6d5682be40e703c3c9cb7dbd110599ae51efe2ead4d58d52df1e1f42b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.2 MB (467168867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df402e941db862e70dfdf9b1886f9d34477c7ec8d6de82d33bc443cdbc89386`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Thu, 17 Jun 2021 23:53:59 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 17 Jun 2021 23:56:05 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:56:06 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 18 Jun 2021 00:02:22 GMT
ARG CB_VERSION=6.0.4
# Fri, 18 Jun 2021 00:02:22 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.4
# Fri, 18 Jun 2021 00:02:22 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.4-ubuntu18.04_amd64.deb
# Fri, 18 Jun 2021 00:02:23 GMT
ARG CB_SHA256=7dbe8dd074f9cabea69468ea488f9ffc19c04dab8fc2e98c937fa32704982aff
# Fri, 18 Jun 2021 00:02:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 18 Jun 2021 00:02:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.4-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.4 CB_SHA256=7dbe8dd074f9cabea69468ea488f9ffc19c04dab8fc2e98c937fa32704982aff CB_VERSION=6.0.4
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 18 Jun 2021 00:03:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.4-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.4 CB_SHA256=7dbe8dd074f9cabea69468ea488f9ffc19c04dab8fc2e98c937fa32704982aff CB_VERSION=6.0.4
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 18 Jun 2021 00:03:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.4-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.4 CB_SHA256=7dbe8dd074f9cabea69468ea488f9ffc19c04dab8fc2e98c937fa32704982aff CB_VERSION=6.0.4
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 18 Jun 2021 00:03:18 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 18 Jun 2021 00:03:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.4-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.4 CB_SHA256=7dbe8dd074f9cabea69468ea488f9ffc19c04dab8fc2e98c937fa32704982aff CB_VERSION=6.0.4
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 18 Jun 2021 00:03:19 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:03:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.4-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.4 CB_SHA256=7dbe8dd074f9cabea69468ea488f9ffc19c04dab8fc2e98c937fa32704982aff CB_VERSION=6.0.4
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 18 Jun 2021 00:03:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.4-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.4 CB_SHA256=7dbe8dd074f9cabea69468ea488f9ffc19c04dab8fc2e98c937fa32704982aff CB_VERSION=6.0.4
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 18 Jun 2021 00:03:21 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 18 Jun 2021 00:03:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Jun 2021 00:03:21 GMT
CMD ["couchbase-server"]
# Fri, 18 Jun 2021 00:03:21 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 18 Jun 2021 00:03:22 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bf3da53cf4b3f333e9356133c7830082e23c62dddddb71c4d2c08ea2915223`  
		Last Modified: Fri, 18 Jun 2021 00:13:27 GMT  
		Size: 15.9 MB (15923371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545dc5a4237ac749c5a107319df722d3d49b8cafcb548eede9190b28815c17e0`  
		Last Modified: Fri, 18 Jun 2021 00:13:20 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60fa8873fa27f508bb6dd4a45d6a6d2e3dd3df0352d427c3e8dbd1bdd7a44a02`  
		Last Modified: Fri, 18 Jun 2021 00:19:18 GMT  
		Size: 2.0 KB (1964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6be19648d35f5d96fc5b8658d54b3804b9876e56772f43613404cea6717d2f`  
		Last Modified: Fri, 18 Jun 2021 00:20:01 GMT  
		Size: 424.4 MB (424414734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe238b99720845cfe81c253f3ff30bc517923b0767087857f08e78015b6a8440`  
		Last Modified: Fri, 18 Jun 2021 00:19:18 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5f3795e56a5d2a85066a7952a266aefe1c67146108da953e73d1c1d6d186b6`  
		Last Modified: Fri, 18 Jun 2021 00:19:18 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528e93e00d13be7736369f280b2bf09ec30e5ae16c14b798e439353aff02a8bb`  
		Last Modified: Fri, 18 Jun 2021 00:19:16 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997293441b8ed4550205e79c87efd1f75a86ec47b8c71ef812c763610a140f2e`  
		Last Modified: Fri, 18 Jun 2021 00:19:16 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ab0ae57684cf9c26e565a4e49c80682898e7dbad4c7b870c6240fb61287022`  
		Last Modified: Fri, 18 Jun 2021 00:19:16 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c776ce0a278d5fbdfbd22508a2716779395f54ccc2a6d89eb2bb734c2967063`  
		Last Modified: Fri, 18 Jun 2021 00:19:16 GMT  
		Size: 125.6 KB (125564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49b5a158124ea31a3811965af11bd7b3b08fd14523cd846b8db56cf506ed97f`  
		Last Modified: Fri, 18 Jun 2021 00:19:16 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:6.0.5`

```console
$ docker pull couchbase@sha256:c01323a9d9957cd87b6929110951a5a618f1662ae616269827f507eb4eb1073f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:6.0.5` - linux; amd64

```console
$ docker pull couchbase@sha256:7c1f755f5f07e887dea165a97f226741611cd4ed0095531fa95114c5eeb0b38b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.1 MB (466117231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81c0474bf3d11d1efe347b4b57351ed149e20ea5f4291271dddeb0774ebd24f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Thu, 17 Jun 2021 23:53:59 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 17 Jun 2021 23:56:05 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:56:06 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 17 Jun 2021 23:56:06 GMT
ARG CB_VERSION=6.0.5
# Thu, 17 Jun 2021 23:56:06 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5
# Thu, 17 Jun 2021 23:56:06 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb
# Thu, 17 Jun 2021 23:56:06 GMT
ARG CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d
# Thu, 17 Jun 2021 23:56:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 17 Jun 2021 23:56:08 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 17 Jun 2021 23:57:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:57:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 17 Jun 2021 23:57:05 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 17 Jun 2021 23:57:06 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 17 Jun 2021 23:57:06 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 17 Jun 2021 23:57:07 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 17 Jun 2021 23:57:08 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 17 Jun 2021 23:57:09 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 17 Jun 2021 23:57:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Jun 2021 23:57:09 GMT
CMD ["couchbase-server"]
# Thu, 17 Jun 2021 23:57:09 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 17 Jun 2021 23:57:09 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bf3da53cf4b3f333e9356133c7830082e23c62dddddb71c4d2c08ea2915223`  
		Last Modified: Fri, 18 Jun 2021 00:13:27 GMT  
		Size: 15.9 MB (15923371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545dc5a4237ac749c5a107319df722d3d49b8cafcb548eede9190b28815c17e0`  
		Last Modified: Fri, 18 Jun 2021 00:13:20 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87889e99590a57a085f0ba827e2e71ce446e1a7f25644e6e8dece30666168683`  
		Last Modified: Fri, 18 Jun 2021 00:13:20 GMT  
		Size: 2.0 KB (1965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0564e1f57129e8716d24e67b4b2da2e87bd15ff09657998302ed32aa8ffc2e`  
		Last Modified: Fri, 18 Jun 2021 00:14:01 GMT  
		Size: 423.4 MB (423363109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe026f25a08cadf247eb0e3c071c316b77aaf96bd3285a8b0228737ade2a3b33`  
		Last Modified: Fri, 18 Jun 2021 00:13:20 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635016263f92d3a529516650e130c94d2bb254dbc01a542b29b1c3865ab70bf0`  
		Last Modified: Fri, 18 Jun 2021 00:13:20 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac6861274e63654ea9e7faef482e735dc9f967527284dc1fc0c2a16ca90b52b`  
		Last Modified: Fri, 18 Jun 2021 00:13:17 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe77e1429ab397b87e005aba082a0bc1642c611e3cca230b93c209047dc4fbc`  
		Last Modified: Fri, 18 Jun 2021 00:13:17 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4afd3c4adc77f24f67a05b779db5ecfa1428569910125e02f406244ecc9400e`  
		Last Modified: Fri, 18 Jun 2021 00:13:18 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051769b56ed3e3c77709dbbf85a5d2684be22f76488386c7dcd8de8a039992d6`  
		Last Modified: Fri, 18 Jun 2021 00:13:18 GMT  
		Size: 125.6 KB (125557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c685da4ede59d964d2de05bccc245bb082f20a1174ddafb4463a2eae4f9429`  
		Last Modified: Fri, 18 Jun 2021 00:13:17 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:6.5.0`

```console
$ docker pull couchbase@sha256:8668740169d3f677244cf33ab9f66449ba13a22fef4df3deaa854c13fbf8832e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:6.5.0` - linux; amd64

```console
$ docker pull couchbase@sha256:7e09cde3203b5dbb09655c7b7f2f79d3b2cf4002e5791dee99acb00734685e8d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.2 MB (542229518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78e79ee4baeea1779255fa4f44d8684f20d69ebe05a83758b60070c37fce4a9`
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
# Fri, 18 Jun 2021 00:01:10 GMT
ARG CB_VERSION=6.5.0
# Fri, 18 Jun 2021 00:01:10 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0
# Fri, 18 Jun 2021 00:01:11 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu18.04_amd64.deb
# Fri, 18 Jun 2021 00:01:11 GMT
ARG CB_SHA256=b4cafdc048b0caba85c24b90e6823e9ec2adc32061cafc527ddc99d706d6bc05
# Fri, 18 Jun 2021 00:01:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 18 Jun 2021 00:01:12 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=b4cafdc048b0caba85c24b90e6823e9ec2adc32061cafc527ddc99d706d6bc05 CB_VERSION=6.5.0
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 18 Jun 2021 00:02:10 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=b4cafdc048b0caba85c24b90e6823e9ec2adc32061cafc527ddc99d706d6bc05 CB_VERSION=6.5.0
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 18 Jun 2021 00:02:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=b4cafdc048b0caba85c24b90e6823e9ec2adc32061cafc527ddc99d706d6bc05 CB_VERSION=6.5.0
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 18 Jun 2021 00:02:14 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 18 Jun 2021 00:02:15 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=b4cafdc048b0caba85c24b90e6823e9ec2adc32061cafc527ddc99d706d6bc05 CB_VERSION=6.5.0
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 18 Jun 2021 00:02:16 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:02:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=b4cafdc048b0caba85c24b90e6823e9ec2adc32061cafc527ddc99d706d6bc05 CB_VERSION=6.5.0
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 18 Jun 2021 00:02:18 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=b4cafdc048b0caba85c24b90e6823e9ec2adc32061cafc527ddc99d706d6bc05 CB_VERSION=6.5.0
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 18 Jun 2021 00:02:18 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 18 Jun 2021 00:02:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Jun 2021 00:02:18 GMT
CMD ["couchbase-server"]
# Fri, 18 Jun 2021 00:02:18 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 18 Jun 2021 00:02:19 GMT
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
	-	`sha256:5c8b3ce17ef226f8fb59374def8431af1f97c6b514a9664f25af555db95764ab`  
		Last Modified: Fri, 18 Jun 2021 00:18:00 GMT  
		Size: 2.0 KB (1963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ee840ac8e386bc218ea5c82d18215f31ad473b116b6731784e9ded55bebd29`  
		Last Modified: Fri, 18 Jun 2021 00:18:59 GMT  
		Size: 508.0 MB (508032292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbc0745b9dbdb93ab65750133e34ed273878b35254871732432ea6dce088a1a`  
		Last Modified: Fri, 18 Jun 2021 00:18:00 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ca4ecc642dc8f43cd15dc8b912c10226d0d8710e85eaf3c597af0ad625adb3`  
		Last Modified: Fri, 18 Jun 2021 00:18:00 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5382b86490649b7f4bbc41f32ba2d9e945a61401ef1c8d6b44e8b43a6edca76`  
		Last Modified: Fri, 18 Jun 2021 00:17:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f17e72a9910f21de3af6497e53ac5b4b902ed6fa6c892f787931db3aaedc7ea`  
		Last Modified: Fri, 18 Jun 2021 00:17:58 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c7600b257287fb0c448acc4c774f68a91af7f772967bb094109376292d6563`  
		Last Modified: Fri, 18 Jun 2021 00:17:58 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd1cd0427c5b85482d11d43cfaa8d52ead6caeddf30e7f330d1a910d1de51b8`  
		Last Modified: Fri, 18 Jun 2021 00:17:58 GMT  
		Size: 118.2 KB (118188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72695b96ee7b4d421f03b5d494d03fa8eff4033a4d5a21edd800564ed86a312d`  
		Last Modified: Fri, 18 Jun 2021 00:17:58 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:6.5.1`

```console
$ docker pull couchbase@sha256:54448bed2c7272b5fc44a8a5d2e353eb0bcc38e584c0e47fbb898214b4cc43da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:6.5.1` - linux; amd64

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

## `couchbase:6.6.0`

```console
$ docker pull couchbase@sha256:79c4f1e0c4e9f79f8d6946c1b3cef60626223ad5a40b9c7bb2d30c6018f4620b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:6.6.0` - linux; amd64

```console
$ docker pull couchbase@sha256:f7cbf2222a070142576ebd839a053be6c156970667f0b65ee38cffe2deac5255
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.3 MB (527317903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620936063bcbda07dad2eb967daca0c3124e6cc0651a33853ad38ff84d87c46c`
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
# Thu, 17 Jun 2021 23:54:40 GMT
ARG CB_VERSION=6.6.0
# Thu, 17 Jun 2021 23:54:40 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0
# Thu, 17 Jun 2021 23:58:46 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.0-ubuntu18.04_amd64.deb
# Thu, 17 Jun 2021 23:58:46 GMT
ARG CB_SHA256=8e7fd5434537094be2fbdfedf3ab5005f0f7d5b9d0578f59ce540b424215b728
# Thu, 17 Jun 2021 23:58:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 17 Jun 2021 23:58:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=8e7fd5434537094be2fbdfedf3ab5005f0f7d5b9d0578f59ce540b424215b728 CB_VERSION=6.6.0
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 17 Jun 2021 23:59:42 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=8e7fd5434537094be2fbdfedf3ab5005f0f7d5b9d0578f59ce540b424215b728 CB_VERSION=6.6.0
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:59:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=8e7fd5434537094be2fbdfedf3ab5005f0f7d5b9d0578f59ce540b424215b728 CB_VERSION=6.6.0
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 17 Jun 2021 23:59:47 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 17 Jun 2021 23:59:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=8e7fd5434537094be2fbdfedf3ab5005f0f7d5b9d0578f59ce540b424215b728 CB_VERSION=6.6.0
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 17 Jun 2021 23:59:48 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 17 Jun 2021 23:59:49 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=8e7fd5434537094be2fbdfedf3ab5005f0f7d5b9d0578f59ce540b424215b728 CB_VERSION=6.6.0
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 17 Jun 2021 23:59:50 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=8e7fd5434537094be2fbdfedf3ab5005f0f7d5b9d0578f59ce540b424215b728 CB_VERSION=6.6.0
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 17 Jun 2021 23:59:50 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 17 Jun 2021 23:59:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Jun 2021 23:59:50 GMT
CMD ["couchbase-server"]
# Thu, 17 Jun 2021 23:59:51 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 17 Jun 2021 23:59:51 GMT
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
	-	`sha256:c473aa431222137a0c0c31086a7eed2d2ef3b44970d0edd9aa178f0cb6749fad`  
		Last Modified: Fri, 18 Jun 2021 00:15:32 GMT  
		Size: 2.0 KB (1964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b29e96ab7f88383ed71e42898311493724ecb11f4ac8bb2ac480f5fee2f945`  
		Last Modified: Fri, 18 Jun 2021 00:16:31 GMT  
		Size: 493.1 MB (493120683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead4ed436d77566312e872c28579ad4b0f6c1a60f23b22ee7bffa84344cb6dd5`  
		Last Modified: Fri, 18 Jun 2021 00:15:32 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff614568b5af842843683e3ec14347f4f78e3d51b6f536eca2779fcf53b24688`  
		Last Modified: Fri, 18 Jun 2021 00:15:32 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812cee8bf697619628847e394dde527001cd621075d30446fa41f6694a6dde31`  
		Last Modified: Fri, 18 Jun 2021 00:15:29 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1569987df52c8083e8cebcb3953ba11ec4e46861309a34158714c09578f0d5d9`  
		Last Modified: Fri, 18 Jun 2021 00:15:30 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4abb0766038a93cf47e1abc53d946272fe1634ce753eae46be98c4a6bffd5d2`  
		Last Modified: Fri, 18 Jun 2021 00:15:29 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7178ff9751618abb1f3fe07987c9631e5e8f9a3da9e4d9a8772faa8b945e225a`  
		Last Modified: Fri, 18 Jun 2021 00:15:30 GMT  
		Size: 118.2 KB (118186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18537c9ec688aac9d44245eef7385fe9aea862a27004c4fdce96aa1b7bf0357`  
		Last Modified: Fri, 18 Jun 2021 00:15:29 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:6.6.1`

```console
$ docker pull couchbase@sha256:0b13222ae52066763863ca35be3fb6b1d98b8b9dcb5b4725b98ced205490207b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:6.6.1` - linux; amd64

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

## `couchbase:6.6.2`

```console
$ docker pull couchbase@sha256:77b4d060590331a43f510cfc3cb7b15525ed5400101f0f59c4a2ec25a3dedf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:6.6.2` - linux; amd64

```console
$ docker pull couchbase@sha256:85324ba81b6690af2ffd0c4aca55e2f6cb33f30424436429ee3f2b36d04a3613
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.2 MB (533208069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80558d95cbe24b54ba3d59322dd53a7b6aea1020cf826bbdeccd7deb4245786e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Thu, 17 Jun 2021 23:49:37 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 17 Jun 2021 23:52:42 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:52:43 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 17 Jun 2021 23:52:43 GMT
ARG CB_VERSION=6.6.2
# Thu, 17 Jun 2021 23:52:43 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2
# Thu, 17 Jun 2021 23:52:44 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb
# Thu, 17 Jun 2021 23:52:44 GMT
ARG CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc
# Thu, 17 Jun 2021 23:52:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 17 Jun 2021 23:52:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc CB_VERSION=6.6.2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 17 Jun 2021 23:53:40 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc CB_VERSION=6.6.2
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:53:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc CB_VERSION=6.6.2
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 17 Jun 2021 23:53:45 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 17 Jun 2021 23:53:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc CB_VERSION=6.6.2
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 17 Jun 2021 23:53:46 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 17 Jun 2021 23:53:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc CB_VERSION=6.6.2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 17 Jun 2021 23:53:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc CB_VERSION=6.6.2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 17 Jun 2021 23:53:48 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 17 Jun 2021 23:53:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Jun 2021 23:53:49 GMT
CMD ["couchbase-server"]
# Thu, 17 Jun 2021 23:53:49 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 17 Jun 2021 23:53:49 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67da305d0dac6baad55e37f733b3f5ec3283b5e7fe1677249059934ab026954`  
		Last Modified: Fri, 18 Jun 2021 00:11:13 GMT  
		Size: 6.3 MB (6272494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40e53fb3184a126f904efe38e9d289a39a3c6e6e0db7d02eb0ccb2368f546b1`  
		Last Modified: Fri, 18 Jun 2021 00:11:08 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:becbd3f9883e16918ed323559857f13e851fba9f1b80dc1546031aa71bb06d6d`  
		Last Modified: Fri, 18 Jun 2021 00:11:08 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7efe1af36c3bc03cef8abc7cef78c0c54deca141871b2e0597d6777acbf0cb`  
		Last Modified: Fri, 18 Jun 2021 00:12:05 GMT  
		Size: 498.3 MB (498251631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808bd56cf902b650658fcbd42e47da54bcdccefb538bdf0b84fa588043f8a91f`  
		Last Modified: Fri, 18 Jun 2021 00:11:08 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99d7b5600a3cafd2ba74540ce1787dfa4c64a5bb3ee0825dd3825f59c17cae7`  
		Last Modified: Fri, 18 Jun 2021 00:11:08 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1aa30960f25d58cee9e0eeb1714d72572a9f8f39614653975ec656263e21e6`  
		Last Modified: Fri, 18 Jun 2021 00:11:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb32538178cf6cb9c326af0ce2e0b420a7de8608b1b3d7d20a4de041e72fc3c`  
		Last Modified: Fri, 18 Jun 2021 00:11:06 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3a42de62a16f39cb3473c06739fc64af6eebbf6f76d54ef93c738e9f0cd25a`  
		Last Modified: Fri, 18 Jun 2021 00:11:06 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41783a5d557fd27d6a0cfaa722255e28e50018a8a1a27e2609ca1ed4ea50d038`  
		Last Modified: Fri, 18 Jun 2021 00:11:06 GMT  
		Size: 125.9 KB (125892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07fb8ee2395d2c65d9f98bec783fc393c760c7283dce215e6d0b1d75ad2c754`  
		Last Modified: Fri, 18 Jun 2021 00:11:06 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:7.0.0-beta`

```console
$ docker pull couchbase@sha256:69db6d2cac0812e2e85f7f88c9df8f9008ac10296c4f356741c3767956ad1bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:7.0.0-beta` - linux; amd64

```console
$ docker pull couchbase@sha256:aeca39250c2452d98706e52aa74551223e508307f5a95476d9746379f7438aaa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.1 MB (628084604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a2faac4b4fa261d77e6a640b90fbc9719b163f7c784dd3b2f3eddfcb69e780`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Thu, 17 Jun 2021 23:49:37 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 17 Jun 2021 23:50:08 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:50:09 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 17 Jun 2021 23:50:09 GMT
ARG CB_VERSION=7.0.0-beta
# Thu, 17 Jun 2021 23:50:09 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta
# Thu, 17 Jun 2021 23:50:09 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb
# Thu, 17 Jun 2021 23:50:10 GMT
ARG CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6
# Thu, 17 Jun 2021 23:50:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 17 Jun 2021 23:50:11 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 17 Jun 2021 23:51:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:51:18 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 17 Jun 2021 23:51:18 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 17 Jun 2021 23:51:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 17 Jun 2021 23:51:19 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 17 Jun 2021 23:51:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 17 Jun 2021 23:51:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 17 Jun 2021 23:51:22 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 17 Jun 2021 23:51:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Jun 2021 23:51:22 GMT
CMD ["couchbase-server"]
# Thu, 17 Jun 2021 23:51:22 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 17 Jun 2021 23:51:22 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ea62ac22b460984a57032ad72ec95bf050b1340f4eb25afd54c1aed65b631c`  
		Last Modified: Fri, 18 Jun 2021 00:08:49 GMT  
		Size: 8.3 MB (8286917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c73cba5232eb8ed25020437adc96fd1779f00a5c2ed2ba2382b3ec228ab48b9`  
		Last Modified: Fri, 18 Jun 2021 00:08:44 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0f8937c6ee760ce96d311add15db77fd7fc154e09110970dcb7172b3326966`  
		Last Modified: Fri, 18 Jun 2021 00:08:44 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800fd1cd26a5a9021417137ad0466a01bf48dc5ce205a4c39155876f2a0a45a4`  
		Last Modified: Fri, 18 Jun 2021 00:09:50 GMT  
		Size: 591.1 MB (591113742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cddc4475e9d23b540d7ad7eadf0788c667591a0aebb68abca6873bebc9d25b10`  
		Last Modified: Fri, 18 Jun 2021 00:08:43 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b4c966359bd878649225d94e21bc5d9a041690083387bea49e1f48afb4e47a`  
		Last Modified: Fri, 18 Jun 2021 00:08:43 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f111047edbe8626b9ec5a73e4cf2bde9768f01fabf1d99c6a7265ed62ecfe2`  
		Last Modified: Fri, 18 Jun 2021 00:08:41 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d415610107ee18d1266a073f4bbaa2672ead83287c581bf64069f9f2c22cca38`  
		Last Modified: Fri, 18 Jun 2021 00:08:41 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfb2409bf2794a3ff6605a79670d95c5d84696691688d37c0ee391f4c15a6d3`  
		Last Modified: Fri, 18 Jun 2021 00:08:41 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696d6f9063781d2fe925e3429ea2732f1727d80c145e24869e826f72f0c8a6c0`  
		Last Modified: Fri, 18 Jun 2021 00:08:42 GMT  
		Size: 125.9 KB (125890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06d1f9385c1b8e646d10b4f38a834be1eaec775f14b3d29d9c6c9ba564a26e8`  
		Last Modified: Fri, 18 Jun 2021 00:08:41 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community`

```console
$ docker pull couchbase@sha256:7ff8a1c4c3966c242dfb1b25e51827daa45a519e45752d2d5d047b6a2d562747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:community` - linux; amd64

```console
$ docker pull couchbase@sha256:84cc0e242970c049bdb4ad28a496e86832bbc5e167ef7a228870dc11ed3f9d4c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.2 MB (354216257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f21f4a1de261e7410be63b65a7e067ff534b6713b30adc1ad8955db559d131d`
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
# Thu, 17 Jun 2021 23:54:40 GMT
ARG CB_VERSION=6.6.0
# Thu, 17 Jun 2021 23:54:40 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0
# Thu, 17 Jun 2021 23:54:40 GMT
ARG CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb
# Thu, 17 Jun 2021 23:54:40 GMT
ARG CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559
# Thu, 17 Jun 2021 23:54:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 17 Jun 2021 23:54:41 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 17 Jun 2021 23:55:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:55:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 17 Jun 2021 23:55:27 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 17 Jun 2021 23:55:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 17 Jun 2021 23:55:28 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 17 Jun 2021 23:55:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 17 Jun 2021 23:55:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 17 Jun 2021 23:55:30 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 17 Jun 2021 23:55:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Jun 2021 23:55:31 GMT
CMD ["couchbase-server"]
# Thu, 17 Jun 2021 23:55:31 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 17 Jun 2021 23:55:31 GMT
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
	-	`sha256:7816a394324c92ae04b5ecb7316d9ce0ac10c30ae870aec61cdd6069759057b5`  
		Last Modified: Fri, 18 Jun 2021 00:12:25 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8080359a8815393fab29fa5a07e7e7ebe8d26c810742894b6729ebcc36a16129`  
		Last Modified: Fri, 18 Jun 2021 00:13:06 GMT  
		Size: 320.0 MB (320019028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d1c2b131a1bfa5c76be9458c2e937947cfdc6d1d9011996e669dae556941b6`  
		Last Modified: Fri, 18 Jun 2021 00:12:25 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34da60ffac8de7d453621ecc9da63c195dd46698bd30b4a12cfcaca46d46355c`  
		Last Modified: Fri, 18 Jun 2021 00:12:25 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1fb489404dcc104a832e3da2f079001e173d9e53edd43e21b3cca163fa8d38`  
		Last Modified: Fri, 18 Jun 2021 00:12:23 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6b05fc253ccc66196345c2dc882b05b87a01aaa3109883d8c73feefad392e5`  
		Last Modified: Fri, 18 Jun 2021 00:12:23 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7482f6f57cc12c0c86053a2baae48f7290d04d65db8df10fff2fdca7a0f6b6a`  
		Last Modified: Fri, 18 Jun 2021 00:12:23 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5098852c08439d04dda14178a711651c2d91ed304032577dedf78ae7ddc2936b`  
		Last Modified: Fri, 18 Jun 2021 00:12:23 GMT  
		Size: 118.2 KB (118189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93a6036f460b49b331b2979c491e538851569264958459837275698f912b0c5`  
		Last Modified: Fri, 18 Jun 2021 00:12:23 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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

## `couchbase:community-6.5.1`

```console
$ docker pull couchbase@sha256:c3dc8c80238209fb5bf86df9bbbc1d7d8fc2f8675232f51c1ca0cd070f8fe5ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:community-6.5.1` - linux; amd64

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

## `couchbase:community-6.6.0`

```console
$ docker pull couchbase@sha256:7ff8a1c4c3966c242dfb1b25e51827daa45a519e45752d2d5d047b6a2d562747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:community-6.6.0` - linux; amd64

```console
$ docker pull couchbase@sha256:84cc0e242970c049bdb4ad28a496e86832bbc5e167ef7a228870dc11ed3f9d4c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.2 MB (354216257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f21f4a1de261e7410be63b65a7e067ff534b6713b30adc1ad8955db559d131d`
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
# Thu, 17 Jun 2021 23:54:40 GMT
ARG CB_VERSION=6.6.0
# Thu, 17 Jun 2021 23:54:40 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0
# Thu, 17 Jun 2021 23:54:40 GMT
ARG CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb
# Thu, 17 Jun 2021 23:54:40 GMT
ARG CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559
# Thu, 17 Jun 2021 23:54:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 17 Jun 2021 23:54:41 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 17 Jun 2021 23:55:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:55:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 17 Jun 2021 23:55:27 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 17 Jun 2021 23:55:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 17 Jun 2021 23:55:28 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 17 Jun 2021 23:55:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 17 Jun 2021 23:55:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 17 Jun 2021 23:55:30 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 17 Jun 2021 23:55:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Jun 2021 23:55:31 GMT
CMD ["couchbase-server"]
# Thu, 17 Jun 2021 23:55:31 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 17 Jun 2021 23:55:31 GMT
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
	-	`sha256:7816a394324c92ae04b5ecb7316d9ce0ac10c30ae870aec61cdd6069759057b5`  
		Last Modified: Fri, 18 Jun 2021 00:12:25 GMT  
		Size: 2.0 KB (1966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8080359a8815393fab29fa5a07e7e7ebe8d26c810742894b6729ebcc36a16129`  
		Last Modified: Fri, 18 Jun 2021 00:13:06 GMT  
		Size: 320.0 MB (320019028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d1c2b131a1bfa5c76be9458c2e937947cfdc6d1d9011996e669dae556941b6`  
		Last Modified: Fri, 18 Jun 2021 00:12:25 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34da60ffac8de7d453621ecc9da63c195dd46698bd30b4a12cfcaca46d46355c`  
		Last Modified: Fri, 18 Jun 2021 00:12:25 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1fb489404dcc104a832e3da2f079001e173d9e53edd43e21b3cca163fa8d38`  
		Last Modified: Fri, 18 Jun 2021 00:12:23 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6b05fc253ccc66196345c2dc882b05b87a01aaa3109883d8c73feefad392e5`  
		Last Modified: Fri, 18 Jun 2021 00:12:23 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7482f6f57cc12c0c86053a2baae48f7290d04d65db8df10fff2fdca7a0f6b6a`  
		Last Modified: Fri, 18 Jun 2021 00:12:23 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5098852c08439d04dda14178a711651c2d91ed304032577dedf78ae7ddc2936b`  
		Last Modified: Fri, 18 Jun 2021 00:12:23 GMT  
		Size: 118.2 KB (118189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93a6036f460b49b331b2979c491e538851569264958459837275698f912b0c5`  
		Last Modified: Fri, 18 Jun 2021 00:12:23 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-7.0.0-beta`

```console
$ docker pull couchbase@sha256:ecb06402401f015789433decb9b908d2dd0f15712f338d35d8bee703e70ce53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:community-7.0.0-beta` - linux; amd64

```console
$ docker pull couchbase@sha256:ca2694c29f07f570822c38cf750aa716188c4960f1da70baa7968a25b958fcc6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.0 MB (434020246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2202f600006447eb7eff9889506a0064b47271cdd0e9c4b34f9d4f8c4358c81`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Thu, 17 Jun 2021 23:49:37 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 17 Jun 2021 23:50:08 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:50:09 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 17 Jun 2021 23:50:09 GMT
ARG CB_VERSION=7.0.0-beta
# Thu, 17 Jun 2021 23:50:09 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta
# Thu, 17 Jun 2021 23:51:33 GMT
ARG CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb
# Thu, 17 Jun 2021 23:51:33 GMT
ARG CB_SHA256=51e843e9d2b5ef746353d79c044f17e4f9be0866673bd6fda01da27a0edf9fc9
# Thu, 17 Jun 2021 23:51:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 17 Jun 2021 23:51:34 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=51e843e9d2b5ef746353d79c044f17e4f9be0866673bd6fda01da27a0edf9fc9 CB_VERSION=7.0.0-beta
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 17 Jun 2021 23:52:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=51e843e9d2b5ef746353d79c044f17e4f9be0866673bd6fda01da27a0edf9fc9 CB_VERSION=7.0.0-beta
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:52:25 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=51e843e9d2b5ef746353d79c044f17e4f9be0866673bd6fda01da27a0edf9fc9 CB_VERSION=7.0.0-beta
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 17 Jun 2021 23:52:25 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 17 Jun 2021 23:52:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=51e843e9d2b5ef746353d79c044f17e4f9be0866673bd6fda01da27a0edf9fc9 CB_VERSION=7.0.0-beta
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 17 Jun 2021 23:52:26 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 17 Jun 2021 23:52:27 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=51e843e9d2b5ef746353d79c044f17e4f9be0866673bd6fda01da27a0edf9fc9 CB_VERSION=7.0.0-beta
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 17 Jun 2021 23:52:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=51e843e9d2b5ef746353d79c044f17e4f9be0866673bd6fda01da27a0edf9fc9 CB_VERSION=7.0.0-beta
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 17 Jun 2021 23:52:28 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 17 Jun 2021 23:52:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Jun 2021 23:52:29 GMT
CMD ["couchbase-server"]
# Thu, 17 Jun 2021 23:52:29 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 17 Jun 2021 23:52:29 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ea62ac22b460984a57032ad72ec95bf050b1340f4eb25afd54c1aed65b631c`  
		Last Modified: Fri, 18 Jun 2021 00:08:49 GMT  
		Size: 8.3 MB (8286917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c73cba5232eb8ed25020437adc96fd1779f00a5c2ed2ba2382b3ec228ab48b9`  
		Last Modified: Fri, 18 Jun 2021 00:08:44 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648b17c1a0c0f24fa08c90e46ccd713f200ca8874fb6a5e24cc7ec9d90c8990e`  
		Last Modified: Fri, 18 Jun 2021 00:10:04 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19447425f2103a5d80066002908e5929ef410f5884c8c15eb5a9d112b2b2e23`  
		Last Modified: Fri, 18 Jun 2021 00:10:55 GMT  
		Size: 397.0 MB (397049385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd092532cc7eb8b8c148addb3287f12d819f6d0ca2e3033777d46e90881ea7c`  
		Last Modified: Fri, 18 Jun 2021 00:10:04 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff075c4e2f27149008536623632e0158ae82b8d0caaae41c9932dd4b49c941b`  
		Last Modified: Fri, 18 Jun 2021 00:10:05 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9ad555891e4f1fcb7f7a28744d64713c94129d042c8ec8e79e45c2c5ad1fd1`  
		Last Modified: Fri, 18 Jun 2021 00:10:02 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f9e84330899867f4b19eae0e6c6380109035ae7c8f529ed804c5665542087a`  
		Last Modified: Fri, 18 Jun 2021 00:10:02 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a691eaba71b0afbfb5ed0e3ed59d87009b2aedd122c8a0540c8eb46f0d67ee1`  
		Last Modified: Fri, 18 Jun 2021 00:10:02 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f6a303eafb6f00a736f40a6be30432b7a94c51400d44f794fc4c15878a5fb2`  
		Last Modified: Fri, 18 Jun 2021 00:10:02 GMT  
		Size: 125.9 KB (125888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea45324b15654707f4be9202bca92c32b29c0995562555c191794a85c6b990b0`  
		Last Modified: Fri, 18 Jun 2021 00:10:02 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise`

```console
$ docker pull couchbase@sha256:77b4d060590331a43f510cfc3cb7b15525ed5400101f0f59c4a2ec25a3dedf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise` - linux; amd64

```console
$ docker pull couchbase@sha256:85324ba81b6690af2ffd0c4aca55e2f6cb33f30424436429ee3f2b36d04a3613
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.2 MB (533208069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80558d95cbe24b54ba3d59322dd53a7b6aea1020cf826bbdeccd7deb4245786e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Thu, 17 Jun 2021 23:49:37 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 17 Jun 2021 23:52:42 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:52:43 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 17 Jun 2021 23:52:43 GMT
ARG CB_VERSION=6.6.2
# Thu, 17 Jun 2021 23:52:43 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2
# Thu, 17 Jun 2021 23:52:44 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb
# Thu, 17 Jun 2021 23:52:44 GMT
ARG CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc
# Thu, 17 Jun 2021 23:52:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 17 Jun 2021 23:52:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc CB_VERSION=6.6.2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 17 Jun 2021 23:53:40 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc CB_VERSION=6.6.2
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:53:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc CB_VERSION=6.6.2
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 17 Jun 2021 23:53:45 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 17 Jun 2021 23:53:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc CB_VERSION=6.6.2
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 17 Jun 2021 23:53:46 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 17 Jun 2021 23:53:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc CB_VERSION=6.6.2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 17 Jun 2021 23:53:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc CB_VERSION=6.6.2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 17 Jun 2021 23:53:48 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 17 Jun 2021 23:53:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Jun 2021 23:53:49 GMT
CMD ["couchbase-server"]
# Thu, 17 Jun 2021 23:53:49 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 17 Jun 2021 23:53:49 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67da305d0dac6baad55e37f733b3f5ec3283b5e7fe1677249059934ab026954`  
		Last Modified: Fri, 18 Jun 2021 00:11:13 GMT  
		Size: 6.3 MB (6272494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40e53fb3184a126f904efe38e9d289a39a3c6e6e0db7d02eb0ccb2368f546b1`  
		Last Modified: Fri, 18 Jun 2021 00:11:08 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:becbd3f9883e16918ed323559857f13e851fba9f1b80dc1546031aa71bb06d6d`  
		Last Modified: Fri, 18 Jun 2021 00:11:08 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7efe1af36c3bc03cef8abc7cef78c0c54deca141871b2e0597d6777acbf0cb`  
		Last Modified: Fri, 18 Jun 2021 00:12:05 GMT  
		Size: 498.3 MB (498251631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808bd56cf902b650658fcbd42e47da54bcdccefb538bdf0b84fa588043f8a91f`  
		Last Modified: Fri, 18 Jun 2021 00:11:08 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99d7b5600a3cafd2ba74540ce1787dfa4c64a5bb3ee0825dd3825f59c17cae7`  
		Last Modified: Fri, 18 Jun 2021 00:11:08 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1aa30960f25d58cee9e0eeb1714d72572a9f8f39614653975ec656263e21e6`  
		Last Modified: Fri, 18 Jun 2021 00:11:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb32538178cf6cb9c326af0ce2e0b420a7de8608b1b3d7d20a4de041e72fc3c`  
		Last Modified: Fri, 18 Jun 2021 00:11:06 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3a42de62a16f39cb3473c06739fc64af6eebbf6f76d54ef93c738e9f0cd25a`  
		Last Modified: Fri, 18 Jun 2021 00:11:06 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41783a5d557fd27d6a0cfaa722255e28e50018a8a1a27e2609ca1ed4ea50d038`  
		Last Modified: Fri, 18 Jun 2021 00:11:06 GMT  
		Size: 125.9 KB (125892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07fb8ee2395d2c65d9f98bec783fc393c760c7283dce215e6d0b1d75ad2c754`  
		Last Modified: Fri, 18 Jun 2021 00:11:06 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-6.0.1`

```console
$ docker pull couchbase@sha256:fe1b56fb539ceb82334bd967c328b23b7cd8dce109b9e846f0e279432b570c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.0.1` - linux; amd64

```console
$ docker pull couchbase@sha256:dde19a8adbe3a3b0f4646c3fb3790e8f2e6d777488a9354f6dad9c6e214f9ba4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.2 MB (455207785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8061fc9cbad81be792ddc4baabb50b21d50a101dc1c64a6cd23739371981633`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Thu, 17 Jun 2021 23:53:59 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 17 Jun 2021 23:56:05 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:56:06 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 18 Jun 2021 00:05:58 GMT
ARG CB_VERSION=6.0.1
# Fri, 18 Jun 2021 00:05:58 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.1
# Fri, 18 Jun 2021 00:05:58 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.1-ubuntu18.04_amd64.deb
# Fri, 18 Jun 2021 00:05:58 GMT
ARG CB_SHA256=68deed9ba855e2a84500ae99a787c415fc85b4d4dc1140be28ae6f56662bafea
# Fri, 18 Jun 2021 00:05:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 18 Jun 2021 00:06:00 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.1 CB_SHA256=68deed9ba855e2a84500ae99a787c415fc85b4d4dc1140be28ae6f56662bafea CB_VERSION=6.0.1
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 18 Jun 2021 00:06:53 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.1 CB_SHA256=68deed9ba855e2a84500ae99a787c415fc85b4d4dc1140be28ae6f56662bafea CB_VERSION=6.0.1
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 18 Jun 2021 00:06:56 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.1 CB_SHA256=68deed9ba855e2a84500ae99a787c415fc85b4d4dc1140be28ae6f56662bafea CB_VERSION=6.0.1
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 18 Jun 2021 00:06:57 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 18 Jun 2021 00:06:58 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.1 CB_SHA256=68deed9ba855e2a84500ae99a787c415fc85b4d4dc1140be28ae6f56662bafea CB_VERSION=6.0.1
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 18 Jun 2021 00:06:58 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:06:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.1 CB_SHA256=68deed9ba855e2a84500ae99a787c415fc85b4d4dc1140be28ae6f56662bafea CB_VERSION=6.0.1
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 18 Jun 2021 00:07:00 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.1 CB_SHA256=68deed9ba855e2a84500ae99a787c415fc85b4d4dc1140be28ae6f56662bafea CB_VERSION=6.0.1
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 18 Jun 2021 00:07:00 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 18 Jun 2021 00:07:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Jun 2021 00:07:00 GMT
CMD ["couchbase-server"]
# Fri, 18 Jun 2021 00:07:00 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 18 Jun 2021 00:07:01 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bf3da53cf4b3f333e9356133c7830082e23c62dddddb71c4d2c08ea2915223`  
		Last Modified: Fri, 18 Jun 2021 00:13:27 GMT  
		Size: 15.9 MB (15923371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545dc5a4237ac749c5a107319df722d3d49b8cafcb548eede9190b28815c17e0`  
		Last Modified: Fri, 18 Jun 2021 00:13:20 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4247353f0bc85046a83a6cc2aad427553fbbec5f0b85ba8eee16b26da71d9ce0`  
		Last Modified: Fri, 18 Jun 2021 00:22:15 GMT  
		Size: 2.0 KB (1968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02bb17bb9093629862371fb12376e60d9478a01db74c9fc426c4bda1d0e0001e`  
		Last Modified: Fri, 18 Jun 2021 00:22:56 GMT  
		Size: 412.5 MB (412453654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034c7cb9e25b0ac592dc8b665885d3f6f76e1206678572370c0752c9ecf06481`  
		Last Modified: Fri, 18 Jun 2021 00:22:15 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02f16e49a1343c3a599156959420c59a131fbd06b7e99b0be14eb0b9952896ef`  
		Last Modified: Fri, 18 Jun 2021 00:22:15 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bd1e75e933c1a068f7a2cc9e7842713c664a70212b1dca6cee3f8e79bdb723`  
		Last Modified: Fri, 18 Jun 2021 00:22:13 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffde94834e60ef62b65cdcb28a92822fca9cda5013e3b669f6525b9534ee6e5`  
		Last Modified: Fri, 18 Jun 2021 00:22:13 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2c163249a75391387f01ce8911bf096e0134929731b176a3d7e27585b31f11`  
		Last Modified: Fri, 18 Jun 2021 00:22:13 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd99b4fba7d151e735fa15444042e6f01772f6763b6a1a2018a1eb8ec28a9d7e`  
		Last Modified: Fri, 18 Jun 2021 00:22:13 GMT  
		Size: 125.6 KB (125561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64dd53fbddeefbc0dbe648be59142805bde2d6c77b8476cb9edf24ee7dab4832`  
		Last Modified: Fri, 18 Jun 2021 00:22:13 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-6.0.2`

```console
$ docker pull couchbase@sha256:f14dc5a0682cf7a3d22cdf114cbc74aac02dfc25fd4394a2e84bc42d52febf54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.0.2` - linux; amd64

```console
$ docker pull couchbase@sha256:f2753e9204daf3d6d1929812db4149d5bc1a3dbd7d1030f8418f6e7ffef53d18
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.4 MB (463377939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614fe6e4f61467fc368c3960ff074ad557a42091c396b4b1a5809597ec68faa1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Thu, 17 Jun 2021 23:53:59 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 17 Jun 2021 23:56:05 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:56:06 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 18 Jun 2021 00:04:46 GMT
ARG CB_VERSION=6.0.2
# Fri, 18 Jun 2021 00:04:46 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.2
# Fri, 18 Jun 2021 00:04:46 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.2-ubuntu18.04_amd64.deb
# Fri, 18 Jun 2021 00:04:46 GMT
ARG CB_SHA256=5410a56cefd7a9c624a2d64e474058b43a90e8d66c73fea6b2a8b16a4f6fe14d
# Fri, 18 Jun 2021 00:04:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 18 Jun 2021 00:04:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.2-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.2 CB_SHA256=5410a56cefd7a9c624a2d64e474058b43a90e8d66c73fea6b2a8b16a4f6fe14d CB_VERSION=6.0.2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 18 Jun 2021 00:05:41 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.2-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.2 CB_SHA256=5410a56cefd7a9c624a2d64e474058b43a90e8d66c73fea6b2a8b16a4f6fe14d CB_VERSION=6.0.2
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 18 Jun 2021 00:05:44 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.2-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.2 CB_SHA256=5410a56cefd7a9c624a2d64e474058b43a90e8d66c73fea6b2a8b16a4f6fe14d CB_VERSION=6.0.2
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 18 Jun 2021 00:05:44 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 18 Jun 2021 00:05:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.2-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.2 CB_SHA256=5410a56cefd7a9c624a2d64e474058b43a90e8d66c73fea6b2a8b16a4f6fe14d CB_VERSION=6.0.2
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 18 Jun 2021 00:05:45 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:05:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.2-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.2 CB_SHA256=5410a56cefd7a9c624a2d64e474058b43a90e8d66c73fea6b2a8b16a4f6fe14d CB_VERSION=6.0.2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 18 Jun 2021 00:05:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.2-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.2 CB_SHA256=5410a56cefd7a9c624a2d64e474058b43a90e8d66c73fea6b2a8b16a4f6fe14d CB_VERSION=6.0.2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 18 Jun 2021 00:05:48 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 18 Jun 2021 00:05:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Jun 2021 00:05:48 GMT
CMD ["couchbase-server"]
# Fri, 18 Jun 2021 00:05:48 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 18 Jun 2021 00:05:49 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bf3da53cf4b3f333e9356133c7830082e23c62dddddb71c4d2c08ea2915223`  
		Last Modified: Fri, 18 Jun 2021 00:13:27 GMT  
		Size: 15.9 MB (15923371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545dc5a4237ac749c5a107319df722d3d49b8cafcb548eede9190b28815c17e0`  
		Last Modified: Fri, 18 Jun 2021 00:13:20 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b1c2e053a5ec9ecd93a27aeeb1b32aaf0392ad1c33fe8f859078bb378be1b0`  
		Last Modified: Fri, 18 Jun 2021 00:21:19 GMT  
		Size: 2.0 KB (1968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b556c35a544d05c2ecfd95dd3b4d0edeb788664964f3e472f9fbf26babe221`  
		Last Modified: Fri, 18 Jun 2021 00:22:01 GMT  
		Size: 420.6 MB (420623807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4213e210b9d470e9b3e5c56908c34bd50bf8e4b79336e73e69057c058611e50`  
		Last Modified: Fri, 18 Jun 2021 00:21:18 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0246c4edda97f1d3586d842263d1a3b5ddaccc755b2729f1db02da3e76875420`  
		Last Modified: Fri, 18 Jun 2021 00:21:18 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b4b14d12afc0a09713ce5e3788f1fbb57df4d48fc47548c1ffedb8168bbe26e`  
		Last Modified: Fri, 18 Jun 2021 00:21:16 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3e98800a13b2af6203e88fa36e59ebcbf1557b1229b1c8fa38f93ad2424a8d`  
		Last Modified: Fri, 18 Jun 2021 00:21:16 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb38a623972beed70f2ad1e80d9e4250b2b098683fb993cdc6651edee54804f4`  
		Last Modified: Fri, 18 Jun 2021 00:21:16 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8637d65dcd664f6d6a04a691b6b17a19b64e52e1337ac13c7d450b77fc04d2d`  
		Last Modified: Fri, 18 Jun 2021 00:21:16 GMT  
		Size: 125.6 KB (125562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae85e8be4d0329da5496d8993ef0c4d3ff851336bb16111c7687ea3d077d6a2`  
		Last Modified: Fri, 18 Jun 2021 00:21:16 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-6.0.3`

```console
$ docker pull couchbase@sha256:6a5a77c25506213d95ed904831ee5673dd0de00f908347ee7b764da884c9bd63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.0.3` - linux; amd64

```console
$ docker pull couchbase@sha256:c2bd562e1899f2864037badfbb8448e75be5304e1c47ab4a10b6eae5007bc8f4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.9 MB (465902080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6001279031fc322a86ad8bcb7b885204e5582a90c0df3296d85f91a38603f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Thu, 17 Jun 2021 23:53:59 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 17 Jun 2021 23:56:05 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:56:06 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 18 Jun 2021 00:03:34 GMT
ARG CB_VERSION=6.0.3
# Fri, 18 Jun 2021 00:03:34 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3
# Fri, 18 Jun 2021 00:03:34 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu18.04_amd64.deb
# Fri, 18 Jun 2021 00:03:34 GMT
ARG CB_SHA256=8ee814ea8d99141de5493a6a24423c6a5dc4e01b8393dce87ca1639630315382
# Fri, 18 Jun 2021 00:03:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 18 Jun 2021 00:03:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=8ee814ea8d99141de5493a6a24423c6a5dc4e01b8393dce87ca1639630315382 CB_VERSION=6.0.3
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 18 Jun 2021 00:04:25 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=8ee814ea8d99141de5493a6a24423c6a5dc4e01b8393dce87ca1639630315382 CB_VERSION=6.0.3
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 18 Jun 2021 00:04:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=8ee814ea8d99141de5493a6a24423c6a5dc4e01b8393dce87ca1639630315382 CB_VERSION=6.0.3
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 18 Jun 2021 00:04:28 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 18 Jun 2021 00:04:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=8ee814ea8d99141de5493a6a24423c6a5dc4e01b8393dce87ca1639630315382 CB_VERSION=6.0.3
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 18 Jun 2021 00:04:30 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:04:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=8ee814ea8d99141de5493a6a24423c6a5dc4e01b8393dce87ca1639630315382 CB_VERSION=6.0.3
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 18 Jun 2021 00:04:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=8ee814ea8d99141de5493a6a24423c6a5dc4e01b8393dce87ca1639630315382 CB_VERSION=6.0.3
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 18 Jun 2021 00:04:32 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 18 Jun 2021 00:04:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Jun 2021 00:04:32 GMT
CMD ["couchbase-server"]
# Fri, 18 Jun 2021 00:04:32 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 18 Jun 2021 00:04:33 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bf3da53cf4b3f333e9356133c7830082e23c62dddddb71c4d2c08ea2915223`  
		Last Modified: Fri, 18 Jun 2021 00:13:27 GMT  
		Size: 15.9 MB (15923371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545dc5a4237ac749c5a107319df722d3d49b8cafcb548eede9190b28815c17e0`  
		Last Modified: Fri, 18 Jun 2021 00:13:20 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7140b47541859c7c1da04c3969a13a8d032439f6d6a2c9513bb22d30e9ec81a6`  
		Last Modified: Fri, 18 Jun 2021 00:20:16 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e0406848c935ddd75ff5f5d47fe98660f5a2e78fde07afcd8cd30f380ae7b9`  
		Last Modified: Fri, 18 Jun 2021 00:21:00 GMT  
		Size: 423.1 MB (423147946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9170b125c4dfadd1de7ff92e44c7003ff72668b698aa325186fff3449bff11`  
		Last Modified: Fri, 18 Jun 2021 00:20:16 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f29d7d6b7b107a076a04ba0af409db31ad694286c20909d062dfe0e7727c82`  
		Last Modified: Fri, 18 Jun 2021 00:20:16 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:824042d8a830a420e0056c91ef62066d8c470cce68ef9188e0f6376d7f560336`  
		Last Modified: Fri, 18 Jun 2021 00:20:13 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72387d752334c7aed3331bb81c29ca85715a9339bc8b4a8cce570b09657614bf`  
		Last Modified: Fri, 18 Jun 2021 00:20:13 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e68c8a505ee1f4e68a60face6e5bf403fdf2668cef8c3a672ec04d1fbd3b67`  
		Last Modified: Fri, 18 Jun 2021 00:20:13 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c1c2d190ec7b3209221de5f1c091504f4974c599df4e28bf6ec1b889eb5d32`  
		Last Modified: Fri, 18 Jun 2021 00:20:14 GMT  
		Size: 125.6 KB (125562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf203913c66cafb3b670211298dfa44b94c5171a1546bea93e9a22508509994`  
		Last Modified: Fri, 18 Jun 2021 00:20:13 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-6.0.4`

```console
$ docker pull couchbase@sha256:768a0be972b295b8fd967c0ded61a278c1c2ef22e659c3892850f0760b12e784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.0.4` - linux; amd64

```console
$ docker pull couchbase@sha256:c298a4d6d5682be40e703c3c9cb7dbd110599ae51efe2ead4d58d52df1e1f42b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.2 MB (467168867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df402e941db862e70dfdf9b1886f9d34477c7ec8d6de82d33bc443cdbc89386`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Thu, 17 Jun 2021 23:53:59 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 17 Jun 2021 23:56:05 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:56:06 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 18 Jun 2021 00:02:22 GMT
ARG CB_VERSION=6.0.4
# Fri, 18 Jun 2021 00:02:22 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.4
# Fri, 18 Jun 2021 00:02:22 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.4-ubuntu18.04_amd64.deb
# Fri, 18 Jun 2021 00:02:23 GMT
ARG CB_SHA256=7dbe8dd074f9cabea69468ea488f9ffc19c04dab8fc2e98c937fa32704982aff
# Fri, 18 Jun 2021 00:02:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 18 Jun 2021 00:02:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.4-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.4 CB_SHA256=7dbe8dd074f9cabea69468ea488f9ffc19c04dab8fc2e98c937fa32704982aff CB_VERSION=6.0.4
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 18 Jun 2021 00:03:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.4-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.4 CB_SHA256=7dbe8dd074f9cabea69468ea488f9ffc19c04dab8fc2e98c937fa32704982aff CB_VERSION=6.0.4
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 18 Jun 2021 00:03:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.4-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.4 CB_SHA256=7dbe8dd074f9cabea69468ea488f9ffc19c04dab8fc2e98c937fa32704982aff CB_VERSION=6.0.4
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 18 Jun 2021 00:03:18 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 18 Jun 2021 00:03:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.4-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.4 CB_SHA256=7dbe8dd074f9cabea69468ea488f9ffc19c04dab8fc2e98c937fa32704982aff CB_VERSION=6.0.4
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 18 Jun 2021 00:03:19 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:03:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.4-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.4 CB_SHA256=7dbe8dd074f9cabea69468ea488f9ffc19c04dab8fc2e98c937fa32704982aff CB_VERSION=6.0.4
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 18 Jun 2021 00:03:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.4-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.4 CB_SHA256=7dbe8dd074f9cabea69468ea488f9ffc19c04dab8fc2e98c937fa32704982aff CB_VERSION=6.0.4
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 18 Jun 2021 00:03:21 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 18 Jun 2021 00:03:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Jun 2021 00:03:21 GMT
CMD ["couchbase-server"]
# Fri, 18 Jun 2021 00:03:21 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 18 Jun 2021 00:03:22 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bf3da53cf4b3f333e9356133c7830082e23c62dddddb71c4d2c08ea2915223`  
		Last Modified: Fri, 18 Jun 2021 00:13:27 GMT  
		Size: 15.9 MB (15923371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545dc5a4237ac749c5a107319df722d3d49b8cafcb548eede9190b28815c17e0`  
		Last Modified: Fri, 18 Jun 2021 00:13:20 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60fa8873fa27f508bb6dd4a45d6a6d2e3dd3df0352d427c3e8dbd1bdd7a44a02`  
		Last Modified: Fri, 18 Jun 2021 00:19:18 GMT  
		Size: 2.0 KB (1964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6be19648d35f5d96fc5b8658d54b3804b9876e56772f43613404cea6717d2f`  
		Last Modified: Fri, 18 Jun 2021 00:20:01 GMT  
		Size: 424.4 MB (424414734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe238b99720845cfe81c253f3ff30bc517923b0767087857f08e78015b6a8440`  
		Last Modified: Fri, 18 Jun 2021 00:19:18 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5f3795e56a5d2a85066a7952a266aefe1c67146108da953e73d1c1d6d186b6`  
		Last Modified: Fri, 18 Jun 2021 00:19:18 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528e93e00d13be7736369f280b2bf09ec30e5ae16c14b798e439353aff02a8bb`  
		Last Modified: Fri, 18 Jun 2021 00:19:16 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997293441b8ed4550205e79c87efd1f75a86ec47b8c71ef812c763610a140f2e`  
		Last Modified: Fri, 18 Jun 2021 00:19:16 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ab0ae57684cf9c26e565a4e49c80682898e7dbad4c7b870c6240fb61287022`  
		Last Modified: Fri, 18 Jun 2021 00:19:16 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c776ce0a278d5fbdfbd22508a2716779395f54ccc2a6d89eb2bb734c2967063`  
		Last Modified: Fri, 18 Jun 2021 00:19:16 GMT  
		Size: 125.6 KB (125564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49b5a158124ea31a3811965af11bd7b3b08fd14523cd846b8db56cf506ed97f`  
		Last Modified: Fri, 18 Jun 2021 00:19:16 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-6.0.5`

```console
$ docker pull couchbase@sha256:c01323a9d9957cd87b6929110951a5a618f1662ae616269827f507eb4eb1073f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.0.5` - linux; amd64

```console
$ docker pull couchbase@sha256:7c1f755f5f07e887dea165a97f226741611cd4ed0095531fa95114c5eeb0b38b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.1 MB (466117231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d81c0474bf3d11d1efe347b4b57351ed149e20ea5f4291271dddeb0774ebd24f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:22 GMT
ADD file:900f735ff138e5137cf25ddd85a32a01921ebec26d86704d24b5f12e73a832c2 in / 
# Thu, 17 Jun 2021 23:31:22 GMT
CMD ["bash"]
# Thu, 17 Jun 2021 23:53:59 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 17 Jun 2021 23:56:05 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:56:06 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 17 Jun 2021 23:56:06 GMT
ARG CB_VERSION=6.0.5
# Thu, 17 Jun 2021 23:56:06 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5
# Thu, 17 Jun 2021 23:56:06 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb
# Thu, 17 Jun 2021 23:56:06 GMT
ARG CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d
# Thu, 17 Jun 2021 23:56:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 17 Jun 2021 23:56:08 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 17 Jun 2021 23:57:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:57:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 17 Jun 2021 23:57:05 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 17 Jun 2021 23:57:06 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 17 Jun 2021 23:57:06 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 17 Jun 2021 23:57:07 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 17 Jun 2021 23:57:08 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 17 Jun 2021 23:57:09 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 17 Jun 2021 23:57:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Jun 2021 23:57:09 GMT
CMD ["couchbase-server"]
# Thu, 17 Jun 2021 23:57:09 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 17 Jun 2021 23:57:09 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:25fa05cd42bd8fabb25d2a6f3f8c9f7ab34637903d00fd2ed1c1d0fa980427dd`  
		Last Modified: Thu, 17 Jun 2021 23:32:41 GMT  
		Size: 26.7 MB (26700706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05bf3da53cf4b3f333e9356133c7830082e23c62dddddb71c4d2c08ea2915223`  
		Last Modified: Fri, 18 Jun 2021 00:13:27 GMT  
		Size: 15.9 MB (15923371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545dc5a4237ac749c5a107319df722d3d49b8cafcb548eede9190b28815c17e0`  
		Last Modified: Fri, 18 Jun 2021 00:13:20 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87889e99590a57a085f0ba827e2e71ce446e1a7f25644e6e8dece30666168683`  
		Last Modified: Fri, 18 Jun 2021 00:13:20 GMT  
		Size: 2.0 KB (1965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d0564e1f57129e8716d24e67b4b2da2e87bd15ff09657998302ed32aa8ffc2e`  
		Last Modified: Fri, 18 Jun 2021 00:14:01 GMT  
		Size: 423.4 MB (423363109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe026f25a08cadf247eb0e3c071c316b77aaf96bd3285a8b0228737ade2a3b33`  
		Last Modified: Fri, 18 Jun 2021 00:13:20 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635016263f92d3a529516650e130c94d2bb254dbc01a542b29b1c3865ab70bf0`  
		Last Modified: Fri, 18 Jun 2021 00:13:20 GMT  
		Size: 478.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac6861274e63654ea9e7faef482e735dc9f967527284dc1fc0c2a16ca90b52b`  
		Last Modified: Fri, 18 Jun 2021 00:13:17 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe77e1429ab397b87e005aba082a0bc1642c611e3cca230b93c209047dc4fbc`  
		Last Modified: Fri, 18 Jun 2021 00:13:17 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4afd3c4adc77f24f67a05b779db5ecfa1428569910125e02f406244ecc9400e`  
		Last Modified: Fri, 18 Jun 2021 00:13:18 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:051769b56ed3e3c77709dbbf85a5d2684be22f76488386c7dcd8de8a039992d6`  
		Last Modified: Fri, 18 Jun 2021 00:13:18 GMT  
		Size: 125.6 KB (125557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c685da4ede59d964d2de05bccc245bb082f20a1174ddafb4463a2eae4f9429`  
		Last Modified: Fri, 18 Jun 2021 00:13:17 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-6.5.0`

```console
$ docker pull couchbase@sha256:8668740169d3f677244cf33ab9f66449ba13a22fef4df3deaa854c13fbf8832e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.5.0` - linux; amd64

```console
$ docker pull couchbase@sha256:7e09cde3203b5dbb09655c7b7f2f79d3b2cf4002e5791dee99acb00734685e8d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.2 MB (542229518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78e79ee4baeea1779255fa4f44d8684f20d69ebe05a83758b60070c37fce4a9`
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
# Fri, 18 Jun 2021 00:01:10 GMT
ARG CB_VERSION=6.5.0
# Fri, 18 Jun 2021 00:01:10 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0
# Fri, 18 Jun 2021 00:01:11 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu18.04_amd64.deb
# Fri, 18 Jun 2021 00:01:11 GMT
ARG CB_SHA256=b4cafdc048b0caba85c24b90e6823e9ec2adc32061cafc527ddc99d706d6bc05
# Fri, 18 Jun 2021 00:01:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 18 Jun 2021 00:01:12 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=b4cafdc048b0caba85c24b90e6823e9ec2adc32061cafc527ddc99d706d6bc05 CB_VERSION=6.5.0
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 18 Jun 2021 00:02:10 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=b4cafdc048b0caba85c24b90e6823e9ec2adc32061cafc527ddc99d706d6bc05 CB_VERSION=6.5.0
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 18 Jun 2021 00:02:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=b4cafdc048b0caba85c24b90e6823e9ec2adc32061cafc527ddc99d706d6bc05 CB_VERSION=6.5.0
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 18 Jun 2021 00:02:14 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 18 Jun 2021 00:02:15 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=b4cafdc048b0caba85c24b90e6823e9ec2adc32061cafc527ddc99d706d6bc05 CB_VERSION=6.5.0
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 18 Jun 2021 00:02:16 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 18 Jun 2021 00:02:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=b4cafdc048b0caba85c24b90e6823e9ec2adc32061cafc527ddc99d706d6bc05 CB_VERSION=6.5.0
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 18 Jun 2021 00:02:18 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=b4cafdc048b0caba85c24b90e6823e9ec2adc32061cafc527ddc99d706d6bc05 CB_VERSION=6.5.0
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 18 Jun 2021 00:02:18 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 18 Jun 2021 00:02:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 18 Jun 2021 00:02:18 GMT
CMD ["couchbase-server"]
# Fri, 18 Jun 2021 00:02:18 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 18 Jun 2021 00:02:19 GMT
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
	-	`sha256:5c8b3ce17ef226f8fb59374def8431af1f97c6b514a9664f25af555db95764ab`  
		Last Modified: Fri, 18 Jun 2021 00:18:00 GMT  
		Size: 2.0 KB (1963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ee840ac8e386bc218ea5c82d18215f31ad473b116b6731784e9ded55bebd29`  
		Last Modified: Fri, 18 Jun 2021 00:18:59 GMT  
		Size: 508.0 MB (508032292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbc0745b9dbdb93ab65750133e34ed273878b35254871732432ea6dce088a1a`  
		Last Modified: Fri, 18 Jun 2021 00:18:00 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ca4ecc642dc8f43cd15dc8b912c10226d0d8710e85eaf3c597af0ad625adb3`  
		Last Modified: Fri, 18 Jun 2021 00:18:00 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5382b86490649b7f4bbc41f32ba2d9e945a61401ef1c8d6b44e8b43a6edca76`  
		Last Modified: Fri, 18 Jun 2021 00:17:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f17e72a9910f21de3af6497e53ac5b4b902ed6fa6c892f787931db3aaedc7ea`  
		Last Modified: Fri, 18 Jun 2021 00:17:58 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c7600b257287fb0c448acc4c774f68a91af7f772967bb094109376292d6563`  
		Last Modified: Fri, 18 Jun 2021 00:17:58 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd1cd0427c5b85482d11d43cfaa8d52ead6caeddf30e7f330d1a910d1de51b8`  
		Last Modified: Fri, 18 Jun 2021 00:17:58 GMT  
		Size: 118.2 KB (118188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72695b96ee7b4d421f03b5d494d03fa8eff4033a4d5a21edd800564ed86a312d`  
		Last Modified: Fri, 18 Jun 2021 00:17:58 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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

## `couchbase:enterprise-6.6.0`

```console
$ docker pull couchbase@sha256:79c4f1e0c4e9f79f8d6946c1b3cef60626223ad5a40b9c7bb2d30c6018f4620b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.6.0` - linux; amd64

```console
$ docker pull couchbase@sha256:f7cbf2222a070142576ebd839a053be6c156970667f0b65ee38cffe2deac5255
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.3 MB (527317903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620936063bcbda07dad2eb967daca0c3124e6cc0651a33853ad38ff84d87c46c`
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
# Thu, 17 Jun 2021 23:54:40 GMT
ARG CB_VERSION=6.6.0
# Thu, 17 Jun 2021 23:54:40 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0
# Thu, 17 Jun 2021 23:58:46 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.0-ubuntu18.04_amd64.deb
# Thu, 17 Jun 2021 23:58:46 GMT
ARG CB_SHA256=8e7fd5434537094be2fbdfedf3ab5005f0f7d5b9d0578f59ce540b424215b728
# Thu, 17 Jun 2021 23:58:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 17 Jun 2021 23:58:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=8e7fd5434537094be2fbdfedf3ab5005f0f7d5b9d0578f59ce540b424215b728 CB_VERSION=6.6.0
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 17 Jun 2021 23:59:42 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=8e7fd5434537094be2fbdfedf3ab5005f0f7d5b9d0578f59ce540b424215b728 CB_VERSION=6.6.0
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:59:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=8e7fd5434537094be2fbdfedf3ab5005f0f7d5b9d0578f59ce540b424215b728 CB_VERSION=6.6.0
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 17 Jun 2021 23:59:47 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 17 Jun 2021 23:59:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=8e7fd5434537094be2fbdfedf3ab5005f0f7d5b9d0578f59ce540b424215b728 CB_VERSION=6.6.0
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 17 Jun 2021 23:59:48 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 17 Jun 2021 23:59:49 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=8e7fd5434537094be2fbdfedf3ab5005f0f7d5b9d0578f59ce540b424215b728 CB_VERSION=6.6.0
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 17 Jun 2021 23:59:50 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=8e7fd5434537094be2fbdfedf3ab5005f0f7d5b9d0578f59ce540b424215b728 CB_VERSION=6.6.0
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 17 Jun 2021 23:59:50 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 17 Jun 2021 23:59:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Jun 2021 23:59:50 GMT
CMD ["couchbase-server"]
# Thu, 17 Jun 2021 23:59:51 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 17 Jun 2021 23:59:51 GMT
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
	-	`sha256:c473aa431222137a0c0c31086a7eed2d2ef3b44970d0edd9aa178f0cb6749fad`  
		Last Modified: Fri, 18 Jun 2021 00:15:32 GMT  
		Size: 2.0 KB (1964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b29e96ab7f88383ed71e42898311493724ecb11f4ac8bb2ac480f5fee2f945`  
		Last Modified: Fri, 18 Jun 2021 00:16:31 GMT  
		Size: 493.1 MB (493120683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead4ed436d77566312e872c28579ad4b0f6c1a60f23b22ee7bffa84344cb6dd5`  
		Last Modified: Fri, 18 Jun 2021 00:15:32 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff614568b5af842843683e3ec14347f4f78e3d51b6f536eca2779fcf53b24688`  
		Last Modified: Fri, 18 Jun 2021 00:15:32 GMT  
		Size: 475.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:812cee8bf697619628847e394dde527001cd621075d30446fa41f6694a6dde31`  
		Last Modified: Fri, 18 Jun 2021 00:15:29 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1569987df52c8083e8cebcb3953ba11ec4e46861309a34158714c09578f0d5d9`  
		Last Modified: Fri, 18 Jun 2021 00:15:30 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4abb0766038a93cf47e1abc53d946272fe1634ce753eae46be98c4a6bffd5d2`  
		Last Modified: Fri, 18 Jun 2021 00:15:29 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7178ff9751618abb1f3fe07987c9631e5e8f9a3da9e4d9a8772faa8b945e225a`  
		Last Modified: Fri, 18 Jun 2021 00:15:30 GMT  
		Size: 118.2 KB (118186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18537c9ec688aac9d44245eef7385fe9aea862a27004c4fdce96aa1b7bf0357`  
		Last Modified: Fri, 18 Jun 2021 00:15:29 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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

## `couchbase:enterprise-6.6.2`

```console
$ docker pull couchbase@sha256:77b4d060590331a43f510cfc3cb7b15525ed5400101f0f59c4a2ec25a3dedf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.6.2` - linux; amd64

```console
$ docker pull couchbase@sha256:85324ba81b6690af2ffd0c4aca55e2f6cb33f30424436429ee3f2b36d04a3613
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.2 MB (533208069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80558d95cbe24b54ba3d59322dd53a7b6aea1020cf826bbdeccd7deb4245786e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Thu, 17 Jun 2021 23:49:37 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 17 Jun 2021 23:52:42 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:52:43 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 17 Jun 2021 23:52:43 GMT
ARG CB_VERSION=6.6.2
# Thu, 17 Jun 2021 23:52:43 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2
# Thu, 17 Jun 2021 23:52:44 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb
# Thu, 17 Jun 2021 23:52:44 GMT
ARG CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc
# Thu, 17 Jun 2021 23:52:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 17 Jun 2021 23:52:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc CB_VERSION=6.6.2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 17 Jun 2021 23:53:40 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc CB_VERSION=6.6.2
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:53:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc CB_VERSION=6.6.2
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 17 Jun 2021 23:53:45 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 17 Jun 2021 23:53:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc CB_VERSION=6.6.2
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 17 Jun 2021 23:53:46 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 17 Jun 2021 23:53:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc CB_VERSION=6.6.2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 17 Jun 2021 23:53:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc CB_VERSION=6.6.2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 17 Jun 2021 23:53:48 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 17 Jun 2021 23:53:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Jun 2021 23:53:49 GMT
CMD ["couchbase-server"]
# Thu, 17 Jun 2021 23:53:49 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 17 Jun 2021 23:53:49 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67da305d0dac6baad55e37f733b3f5ec3283b5e7fe1677249059934ab026954`  
		Last Modified: Fri, 18 Jun 2021 00:11:13 GMT  
		Size: 6.3 MB (6272494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40e53fb3184a126f904efe38e9d289a39a3c6e6e0db7d02eb0ccb2368f546b1`  
		Last Modified: Fri, 18 Jun 2021 00:11:08 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:becbd3f9883e16918ed323559857f13e851fba9f1b80dc1546031aa71bb06d6d`  
		Last Modified: Fri, 18 Jun 2021 00:11:08 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7efe1af36c3bc03cef8abc7cef78c0c54deca141871b2e0597d6777acbf0cb`  
		Last Modified: Fri, 18 Jun 2021 00:12:05 GMT  
		Size: 498.3 MB (498251631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808bd56cf902b650658fcbd42e47da54bcdccefb538bdf0b84fa588043f8a91f`  
		Last Modified: Fri, 18 Jun 2021 00:11:08 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99d7b5600a3cafd2ba74540ce1787dfa4c64a5bb3ee0825dd3825f59c17cae7`  
		Last Modified: Fri, 18 Jun 2021 00:11:08 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1aa30960f25d58cee9e0eeb1714d72572a9f8f39614653975ec656263e21e6`  
		Last Modified: Fri, 18 Jun 2021 00:11:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb32538178cf6cb9c326af0ce2e0b420a7de8608b1b3d7d20a4de041e72fc3c`  
		Last Modified: Fri, 18 Jun 2021 00:11:06 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3a42de62a16f39cb3473c06739fc64af6eebbf6f76d54ef93c738e9f0cd25a`  
		Last Modified: Fri, 18 Jun 2021 00:11:06 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41783a5d557fd27d6a0cfaa722255e28e50018a8a1a27e2609ca1ed4ea50d038`  
		Last Modified: Fri, 18 Jun 2021 00:11:06 GMT  
		Size: 125.9 KB (125892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07fb8ee2395d2c65d9f98bec783fc393c760c7283dce215e6d0b1d75ad2c754`  
		Last Modified: Fri, 18 Jun 2021 00:11:06 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-7.0.0-beta`

```console
$ docker pull couchbase@sha256:69db6d2cac0812e2e85f7f88c9df8f9008ac10296c4f356741c3767956ad1bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-7.0.0-beta` - linux; amd64

```console
$ docker pull couchbase@sha256:aeca39250c2452d98706e52aa74551223e508307f5a95476d9746379f7438aaa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **628.1 MB (628084604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a2faac4b4fa261d77e6a640b90fbc9719b163f7c784dd3b2f3eddfcb69e780`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Thu, 17 Jun 2021 23:49:37 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 17 Jun 2021 23:50:08 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:50:09 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 17 Jun 2021 23:50:09 GMT
ARG CB_VERSION=7.0.0-beta
# Thu, 17 Jun 2021 23:50:09 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta
# Thu, 17 Jun 2021 23:50:09 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb
# Thu, 17 Jun 2021 23:50:10 GMT
ARG CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6
# Thu, 17 Jun 2021 23:50:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 17 Jun 2021 23:50:11 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 17 Jun 2021 23:51:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:51:18 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 17 Jun 2021 23:51:18 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 17 Jun 2021 23:51:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 17 Jun 2021 23:51:19 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 17 Jun 2021 23:51:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 17 Jun 2021 23:51:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 17 Jun 2021 23:51:22 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 17 Jun 2021 23:51:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Jun 2021 23:51:22 GMT
CMD ["couchbase-server"]
# Thu, 17 Jun 2021 23:51:22 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 17 Jun 2021 23:51:22 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ea62ac22b460984a57032ad72ec95bf050b1340f4eb25afd54c1aed65b631c`  
		Last Modified: Fri, 18 Jun 2021 00:08:49 GMT  
		Size: 8.3 MB (8286917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c73cba5232eb8ed25020437adc96fd1779f00a5c2ed2ba2382b3ec228ab48b9`  
		Last Modified: Fri, 18 Jun 2021 00:08:44 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0f8937c6ee760ce96d311add15db77fd7fc154e09110970dcb7172b3326966`  
		Last Modified: Fri, 18 Jun 2021 00:08:44 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800fd1cd26a5a9021417137ad0466a01bf48dc5ce205a4c39155876f2a0a45a4`  
		Last Modified: Fri, 18 Jun 2021 00:09:50 GMT  
		Size: 591.1 MB (591113742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cddc4475e9d23b540d7ad7eadf0788c667591a0aebb68abca6873bebc9d25b10`  
		Last Modified: Fri, 18 Jun 2021 00:08:43 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b4c966359bd878649225d94e21bc5d9a041690083387bea49e1f48afb4e47a`  
		Last Modified: Fri, 18 Jun 2021 00:08:43 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f111047edbe8626b9ec5a73e4cf2bde9768f01fabf1d99c6a7265ed62ecfe2`  
		Last Modified: Fri, 18 Jun 2021 00:08:41 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d415610107ee18d1266a073f4bbaa2672ead83287c581bf64069f9f2c22cca38`  
		Last Modified: Fri, 18 Jun 2021 00:08:41 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbfb2409bf2794a3ff6605a79670d95c5d84696691688d37c0ee391f4c15a6d3`  
		Last Modified: Fri, 18 Jun 2021 00:08:41 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696d6f9063781d2fe925e3429ea2732f1727d80c145e24869e826f72f0c8a6c0`  
		Last Modified: Fri, 18 Jun 2021 00:08:42 GMT  
		Size: 125.9 KB (125890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b06d1f9385c1b8e646d10b4f38a834be1eaec775f14b3d29d9c6c9ba564a26e8`  
		Last Modified: Fri, 18 Jun 2021 00:08:41 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:latest`

```console
$ docker pull couchbase@sha256:77b4d060590331a43f510cfc3cb7b15525ed5400101f0f59c4a2ec25a3dedf86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:latest` - linux; amd64

```console
$ docker pull couchbase@sha256:85324ba81b6690af2ffd0c4aca55e2f6cb33f30424436429ee3f2b36d04a3613
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **533.2 MB (533208069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80558d95cbe24b54ba3d59322dd53a7b6aea1020cf826bbdeccd7deb4245786e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 17 Jun 2021 23:31:29 GMT
ADD file:920cf788d1ba88f76c97e41e03e4dc2f3005b08d65b5e9da9dd1cbe20a74459b in / 
# Thu, 17 Jun 2021 23:31:29 GMT
CMD ["bash"]
# Thu, 17 Jun 2021 23:49:37 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 17 Jun 2021 23:52:42 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:52:43 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Thu, 17 Jun 2021 23:52:43 GMT
ARG CB_VERSION=6.6.2
# Thu, 17 Jun 2021 23:52:43 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2
# Thu, 17 Jun 2021 23:52:44 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb
# Thu, 17 Jun 2021 23:52:44 GMT
ARG CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc
# Thu, 17 Jun 2021 23:52:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 17 Jun 2021 23:52:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc CB_VERSION=6.6.2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 17 Jun 2021 23:53:40 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc CB_VERSION=6.6.2
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 17 Jun 2021 23:53:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc CB_VERSION=6.6.2
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Thu, 17 Jun 2021 23:53:45 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 17 Jun 2021 23:53:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc CB_VERSION=6.6.2
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Thu, 17 Jun 2021 23:53:46 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 17 Jun 2021 23:53:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc CB_VERSION=6.6.2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 17 Jun 2021 23:53:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.2 CB_SHA256=41c033e6c1e98b0844a5cb5768e3769e7012d8374a6bd235c86e10db33b17afc CB_VERSION=6.6.2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 17 Jun 2021 23:53:48 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 17 Jun 2021 23:53:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Jun 2021 23:53:49 GMT
CMD ["couchbase-server"]
# Thu, 17 Jun 2021 23:53:49 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 17 Jun 2021 23:53:49 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:c549ccf8d472c3bce9ce02e49c62b8f6cbc736ea2b8ba812a1ae9390c69d0b71`  
		Last Modified: Thu, 17 Jun 2021 23:32:58 GMT  
		Size: 28.6 MB (28553692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67da305d0dac6baad55e37f733b3f5ec3283b5e7fe1677249059934ab026954`  
		Last Modified: Fri, 18 Jun 2021 00:11:13 GMT  
		Size: 6.3 MB (6272494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40e53fb3184a126f904efe38e9d289a39a3c6e6e0db7d02eb0ccb2368f546b1`  
		Last Modified: Fri, 18 Jun 2021 00:11:08 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:becbd3f9883e16918ed323559857f13e851fba9f1b80dc1546031aa71bb06d6d`  
		Last Modified: Fri, 18 Jun 2021 00:11:08 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7efe1af36c3bc03cef8abc7cef78c0c54deca141871b2e0597d6777acbf0cb`  
		Last Modified: Fri, 18 Jun 2021 00:12:05 GMT  
		Size: 498.3 MB (498251631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808bd56cf902b650658fcbd42e47da54bcdccefb538bdf0b84fa588043f8a91f`  
		Last Modified: Fri, 18 Jun 2021 00:11:08 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99d7b5600a3cafd2ba74540ce1787dfa4c64a5bb3ee0825dd3825f59c17cae7`  
		Last Modified: Fri, 18 Jun 2021 00:11:08 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1aa30960f25d58cee9e0eeb1714d72572a9f8f39614653975ec656263e21e6`  
		Last Modified: Fri, 18 Jun 2021 00:11:05 GMT  
		Size: 279.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb32538178cf6cb9c326af0ce2e0b420a7de8608b1b3d7d20a4de041e72fc3c`  
		Last Modified: Fri, 18 Jun 2021 00:11:06 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3a42de62a16f39cb3473c06739fc64af6eebbf6f76d54ef93c738e9f0cd25a`  
		Last Modified: Fri, 18 Jun 2021 00:11:06 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41783a5d557fd27d6a0cfaa722255e28e50018a8a1a27e2609ca1ed4ea50d038`  
		Last Modified: Fri, 18 Jun 2021 00:11:06 GMT  
		Size: 125.9 KB (125892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07fb8ee2395d2c65d9f98bec783fc393c760c7283dce215e6d0b1d75ad2c754`  
		Last Modified: Fri, 18 Jun 2021 00:11:06 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

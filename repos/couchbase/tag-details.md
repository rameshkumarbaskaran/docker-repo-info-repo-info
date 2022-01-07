<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchbase`

-	[`couchbase:6.0.5`](#couchbase605)
-	[`couchbase:6.6.4`](#couchbase664)
-	[`couchbase:7.0.3`](#couchbase703)
-	[`couchbase:community`](#couchbasecommunity)
-	[`couchbase:community-6.6.0`](#couchbasecommunity-660)
-	[`couchbase:community-7.0.2`](#couchbasecommunity-702)
-	[`couchbase:enterprise`](#couchbaseenterprise)
-	[`couchbase:enterprise-6.0.5`](#couchbaseenterprise-605)
-	[`couchbase:enterprise-6.6.4`](#couchbaseenterprise-664)
-	[`couchbase:enterprise-7.0.3`](#couchbaseenterprise-703)
-	[`couchbase:latest`](#couchbaselatest)

## `couchbase:6.0.5`

```console
$ docker pull couchbase@sha256:be03f4a0eee07091c5e6b42d3a577c2794756db13ed7cc3119c0e8b72f6ee6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:6.0.5` - linux; amd64

```console
$ docker pull couchbase@sha256:5ebdf4939c5d46f6d32087c1bb28c0967184532eec5d7bedbeeae5486ff219e1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.1 MB (466119913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea3b97e3dcb95085a142f1dcadf201294bce16f8c819628d17e6296f013265f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:21 GMT
ADD file:2aa3e79e3cff3c048612744ac310cf86bc27de3433d420711bafc6612445befc in / 
# Fri, 07 Jan 2022 02:25:21 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:52:42 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 07 Jan 2022 02:54:44 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 07 Jan 2022 02:54:45 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 07 Jan 2022 02:54:45 GMT
ARG CB_VERSION=6.0.5
# Fri, 07 Jan 2022 02:54:45 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5
# Fri, 07 Jan 2022 02:54:46 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb
# Fri, 07 Jan 2022 02:54:46 GMT
ARG CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d
# Fri, 07 Jan 2022 02:54:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 07 Jan 2022 02:54:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 07 Jan 2022 02:55:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 07 Jan 2022 02:55:50 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 07 Jan 2022 02:55:50 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 07 Jan 2022 02:55:51 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 07 Jan 2022 02:55:51 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 07 Jan 2022 02:55:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 07 Jan 2022 02:55:53 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 07 Jan 2022 02:55:53 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 07 Jan 2022 02:55:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Jan 2022 02:55:53 GMT
CMD ["couchbase-server"]
# Fri, 07 Jan 2022 02:55:54 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 07 Jan 2022 02:55:54 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:2f94e549220aea96f00cae7eb95f401e61b41a16cc5eb0b4ea592d0ce871930a`  
		Last Modified: Thu, 06 Jan 2022 23:50:21 GMT  
		Size: 26.7 MB (26705027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e33bcc193d4c06563762ddad056028f9eb5a68bb14c96e48054bb7a57e3d6d`  
		Last Modified: Fri, 07 Jan 2022 03:00:45 GMT  
		Size: 15.9 MB (15921601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4965a86b9381cc2da611cf89bdd2522d66c112a05fe815e3929fadd00e8c612d`  
		Last Modified: Fri, 07 Jan 2022 03:00:41 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecdfa3eef7e95ac97bc3bab1c2995424ac3e24579983b4ebb63b056986687ca`  
		Last Modified: Fri, 07 Jan 2022 03:00:40 GMT  
		Size: 2.0 KB (1963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e20f3da4338b780536b19b01a18d9c8ff343c7a340c8d8b4ee19e986955bc96`  
		Last Modified: Fri, 07 Jan 2022 03:01:18 GMT  
		Size: 423.4 MB (423363242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7df65c056ca7bae77b6dfe98ebabe474056f98f19d08689b44ed726e3f7db4`  
		Last Modified: Fri, 07 Jan 2022 03:00:40 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3590d0bf2dfee04501dc388877a52f9160ad12772f6cde8c8795c260be178a95`  
		Last Modified: Fri, 07 Jan 2022 03:00:40 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3425ccc6efa0f744314c8c11e801cf580568ff3b43171758fad600df878b618`  
		Last Modified: Fri, 07 Jan 2022 03:00:38 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59e1549b0859bfa2fcdd3f82d6b78378b56fc634243673f6910bdd99a43331e`  
		Last Modified: Fri, 07 Jan 2022 03:00:38 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3cc87371a88370a2c16bfec6881f6cbafc4aa1bafa7a589fafb00f2291b601`  
		Last Modified: Fri, 07 Jan 2022 03:00:38 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ecdc492bbd4f515374a9cebf59bcca68fcd388198b541de59503853515f771`  
		Last Modified: Fri, 07 Jan 2022 03:00:38 GMT  
		Size: 125.6 KB (125563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3259321b9db1fb5dc44b85c70f69f436c24ea15b1bf47966e940ae5c560f4752`  
		Last Modified: Fri, 07 Jan 2022 03:00:38 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:6.6.4`

```console
$ docker pull couchbase@sha256:3775640593dd86e6682ff63de4a2e38941b7258753fc0f66d8db2ae0e0ebf707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:6.6.4` - linux; amd64

```console
$ docker pull couchbase@sha256:fdad5c35d221a25172dabeae1c9bcc613e10430817f2bd751ef0b1b384223d0f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.7 MB (561688730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820e0d5e5d4fd9cabdfce500318b7e20b77374619b596cd32cf3254cae0cec31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:47:48 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 07 Jan 2022 02:48:14 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 07 Jan 2022 02:51:19 GMT
ARG CB_VERSION=6.6.4
# Fri, 07 Jan 2022 02:51:20 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.4
# Fri, 07 Jan 2022 02:51:20 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.4-ubuntu20.04_amd64.deb
# Fri, 07 Jan 2022 02:51:20 GMT
ARG CB_SHA256=97cb0aec5a4f7e3d2c3e2017546ac0adb41478c6e5bc1dcefd06cc9f5926f6db
# Fri, 07 Jan 2022 02:51:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 07 Jan 2022 02:51:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.4-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.4 CB_SHA256=97cb0aec5a4f7e3d2c3e2017546ac0adb41478c6e5bc1dcefd06cc9f5926f6db CB_VERSION=6.6.4
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 07 Jan 2022 02:52:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.4-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.4 CB_SHA256=97cb0aec5a4f7e3d2c3e2017546ac0adb41478c6e5bc1dcefd06cc9f5926f6db CB_VERSION=6.6.4
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 07 Jan 2022 02:52:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.4-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.4 CB_SHA256=97cb0aec5a4f7e3d2c3e2017546ac0adb41478c6e5bc1dcefd06cc9f5926f6db CB_VERSION=6.6.4
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 07 Jan 2022 02:52:28 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Fri, 07 Jan 2022 02:52:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.4-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.4 CB_SHA256=97cb0aec5a4f7e3d2c3e2017546ac0adb41478c6e5bc1dcefd06cc9f5926f6db CB_VERSION=6.6.4
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 07 Jan 2022 02:52:29 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 07 Jan 2022 02:52:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.4-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.4 CB_SHA256=97cb0aec5a4f7e3d2c3e2017546ac0adb41478c6e5bc1dcefd06cc9f5926f6db CB_VERSION=6.6.4
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 07 Jan 2022 02:52:37 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.4-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.4 CB_SHA256=97cb0aec5a4f7e3d2c3e2017546ac0adb41478c6e5bc1dcefd06cc9f5926f6db CB_VERSION=6.6.4
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             apt-get update;             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get purge -y chrpath;             apt-get autoremove;             apt-get clean;         fi
# Fri, 07 Jan 2022 02:52:38 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Fri, 07 Jan 2022 02:52:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Jan 2022 02:52:38 GMT
CMD ["couchbase-server"]
# Fri, 07 Jan 2022 02:52:38 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 07 Jan 2022 02:52:39 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66cfcdf8838abf002a7e0a2b3f6a8a41688c07a1055f77fedce22a3c62c05b4`  
		Last Modified: Fri, 07 Jan 2022 02:56:20 GMT  
		Size: 6.3 MB (6252170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16199ea3a03efa6bc813742048c124777c44a880011c4f02f0ab2ed64655366`  
		Last Modified: Fri, 07 Jan 2022 02:58:50 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3335e980a3591f1d6a88a0e5987986c06e05d58c7b593480950e9e62c88131f`  
		Last Modified: Fri, 07 Jan 2022 02:59:42 GMT  
		Size: 503.0 MB (502991689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5eb14c1807736bf2b4ab827e9fd460dcaaabf182af700421592b7d13df3732`  
		Last Modified: Fri, 07 Jan 2022 02:58:50 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1d5b3d1205d51ec426512339929f89cf3f366b3730b33776992f14567234f10`  
		Last Modified: Fri, 07 Jan 2022 02:58:50 GMT  
		Size: 744.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2b217981de2a462d4dcc62538fc1a1f3c1cbf3b6f6729768fd39c08fb18c97`  
		Last Modified: Fri, 07 Jan 2022 02:58:48 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3235e9bac99058de6ff914ba35a22351a4a572b341552845bf65ec3abc12abde`  
		Last Modified: Fri, 07 Jan 2022 02:58:48 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc9220de1c0106fba54832851747dffad049287f03d3b12c7fa7ecff5461beb`  
		Last Modified: Fri, 07 Jan 2022 02:58:48 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4163898a45897dd974d3ae811621a9c97b0f6df6dfd4a13ad3e14f1ee967b9a6`  
		Last Modified: Fri, 07 Jan 2022 02:58:50 GMT  
		Size: 23.9 MB (23874079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719891fd4435444301cfc8b2b9cfa85be519b0014494181a0996b1f43600d323`  
		Last Modified: Fri, 07 Jan 2022 02:58:48 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:7.0.3`

```console
$ docker pull couchbase@sha256:47ed9b19ac85b202000e8875aa8ae507c81dac77c67f757b8367522d8f1f35d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:7.0.3` - linux; amd64

```console
$ docker pull couchbase@sha256:20251532870b6947b24c0249d8081652488af7ad45f221f015118dcd2df0db33
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.0 MB (676998066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb033a3df3d523bcf22def918aed04ea07ac0d1100bd60baf7cefec1943e6ee7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:47:48 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 07 Jan 2022 02:48:14 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 07 Jan 2022 02:48:14 GMT
ARG CB_VERSION=7.0.3
# Fri, 07 Jan 2022 02:48:15 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3
# Fri, 07 Jan 2022 02:48:15 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb
# Fri, 07 Jan 2022 02:48:15 GMT
ARG CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c
# Fri, 07 Jan 2022 02:48:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 07 Jan 2022 02:48:16 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 07 Jan 2022 02:49:34 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 07 Jan 2022 02:49:39 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 07 Jan 2022 02:49:39 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Fri, 07 Jan 2022 02:49:40 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 07 Jan 2022 02:49:41 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 07 Jan 2022 02:49:41 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 07 Jan 2022 02:49:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             apt-get update;             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get purge -y chrpath;             apt-get autoremove;             apt-get clean;         fi
# Fri, 07 Jan 2022 02:49:49 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Fri, 07 Jan 2022 02:49:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Jan 2022 02:49:49 GMT
CMD ["couchbase-server"]
# Fri, 07 Jan 2022 02:49:49 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 07 Jan 2022 02:49:50 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66cfcdf8838abf002a7e0a2b3f6a8a41688c07a1055f77fedce22a3c62c05b4`  
		Last Modified: Fri, 07 Jan 2022 02:56:20 GMT  
		Size: 6.3 MB (6252170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb4f8680ab88ed1d42054586110b2f7c88d44d1958461db8bc7768f41dbd77c`  
		Last Modified: Fri, 07 Jan 2022 02:56:17 GMT  
		Size: 1.8 KB (1829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1103d0911786914568c3da9a9a75f1af7bb0461c2ed7e70a18e2920a978e0bca`  
		Last Modified: Fri, 07 Jan 2022 02:57:27 GMT  
		Size: 618.3 MB (618296886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2110faa7a5b85b1938337de9103a54236c115e8e3eb81079716d9041b4003e05`  
		Last Modified: Fri, 07 Jan 2022 02:56:16 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fb9e05960f9a3f2f101ab8b046e9c1ec9e1ea75d558f014b3fa96b2110d4f8`  
		Last Modified: Fri, 07 Jan 2022 02:56:16 GMT  
		Size: 744.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4508c1d298c835756496e8819dd6a5eda3603f6598fffdb247bf6217bc698724`  
		Last Modified: Fri, 07 Jan 2022 02:56:14 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1496e727dd9652cc32a50f280e4a872cb12a0dcd8c36bfd63f4503a2a3c0aae`  
		Last Modified: Fri, 07 Jan 2022 02:56:14 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d91ce2b56d0558b11b0e82aef58a3a88a266d0e48acdb9c488593ff6f15377`  
		Last Modified: Fri, 07 Jan 2022 02:56:14 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc08238b4d72bda9a93053cd6b1dcb3dd9cc66f2a7a122fdd149f03bf1f50a4`  
		Last Modified: Fri, 07 Jan 2022 02:56:17 GMT  
		Size: 23.9 MB (23878221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2c81438f07aeea3dc1f64847b3c55fc43be24ea9d75c7bf33e92b0e758e980`  
		Last Modified: Fri, 07 Jan 2022 02:56:14 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community`

```console
$ docker pull couchbase@sha256:68de58c96248a30b4add89d892179430e29b62c1bbd0dcffee8a0265e8b02f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community` - linux; amd64

```console
$ docker pull couchbase@sha256:513adeddb3dac0587358c85f3711bf727e447e92f93652f72f8b1dac39065e26
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.0 MB (429023254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0820ad5c12ff1030870a5ae4f957641165d74ff97b54777dd68ff2a19840b05b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:47:48 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 07 Jan 2022 02:50:06 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 07 Jan 2022 02:50:07 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 07 Jan 2022 02:50:08 GMT
ARG CB_VERSION=7.0.2
# Fri, 07 Jan 2022 02:50:08 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2
# Fri, 07 Jan 2022 02:50:08 GMT
ARG CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb
# Fri, 07 Jan 2022 02:50:08 GMT
ARG CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
# Fri, 07 Jan 2022 02:50:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 07 Jan 2022 02:50:09 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 07 Jan 2022 02:50:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 07 Jan 2022 02:51:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 07 Jan 2022 02:51:03 GMT
COPY file:cf9c7c8a9eda8a5fefcaa60d67181024b8a07b30eb318d4c9591b33a95ca6680 in /etc/service/couchbase-server/run 
# Fri, 07 Jan 2022 02:51:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 07 Jan 2022 02:51:04 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 07 Jan 2022 02:51:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 07 Jan 2022 02:51:06 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 07 Jan 2022 02:51:06 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 07 Jan 2022 02:51:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Jan 2022 02:51:06 GMT
CMD ["couchbase-server"]
# Fri, 07 Jan 2022 02:51:07 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 07 Jan 2022 02:51:07 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:284122b04391b834f17a613aa23e44a4b0779b49c4ba9f6a3956cc60508f5c70`  
		Last Modified: Fri, 07 Jan 2022 02:57:51 GMT  
		Size: 6.3 MB (6261189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf01a5cc2a38f6a4074d276f4d169b403d8ad0c1940b429c62e188218d56103`  
		Last Modified: Fri, 07 Jan 2022 02:57:48 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b99cd90fc26a21733f1bb94cd0e2b9956607f9740913b5c6647b5323c82a4f`  
		Last Modified: Fri, 07 Jan 2022 02:57:48 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0879e222305ec3dc532151ff0a4e304e6576ce191dd1c8e48fb8964e3774379d`  
		Last Modified: Fri, 07 Jan 2022 02:58:37 GMT  
		Size: 394.1 MB (394061651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dc4149c320ffe22939dac147881a0ad3e3f99837c8f3f9ea40cc6c4a0c9fdd`  
		Last Modified: Fri, 07 Jan 2022 02:57:48 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270d7ca8583d0bf0615229eb25285df3e1f891ab7ad3d208e36c5be57f4807c9`  
		Last Modified: Fri, 07 Jan 2022 02:57:48 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e3b45dcc87a113571d0391bccd1724338906a8cf3b00353fe6540642416fbe`  
		Last Modified: Fri, 07 Jan 2022 02:57:46 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b272788b5f59d50d364138f28f046357d394fb1f2d49a2ca9874f0e1cd566d0`  
		Last Modified: Fri, 07 Jan 2022 02:57:46 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa25349832622183c7466dee90345f41343a80ef657290f102a0952375cf355b`  
		Last Modified: Fri, 07 Jan 2022 02:57:45 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed86d5d28263dfacb74f29cbfbf16e94448b3361c6cd7760ff1288173a5fb20`  
		Last Modified: Fri, 07 Jan 2022 02:57:46 GMT  
		Size: 129.5 KB (129512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9047bb95ecc6720389ad1355eebf785f9b9d373d388cbdcd05d431497416233f`  
		Last Modified: Fri, 07 Jan 2022 02:57:46 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-6.6.0`

```console
$ docker pull couchbase@sha256:0f868aafe8371855dd818cb3d6d5af327007688672559cf1542a0d60bda1342c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community-6.6.0` - linux; amd64

```console
$ docker pull couchbase@sha256:316dc8e50797b08a1bd6142b4a913efd831064e06ad2b22f74e647cb6fb37ded
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.2 MB (354216959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a9cb13ccaa7650c43e33282fd0cf4ab4b206560ee7e5da3e9e62515545c2bce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:21 GMT
ADD file:2aa3e79e3cff3c048612744ac310cf86bc27de3433d420711bafc6612445befc in / 
# Fri, 07 Jan 2022 02:25:21 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:52:42 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 07 Jan 2022 02:53:09 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 07 Jan 2022 02:53:10 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 07 Jan 2022 02:53:10 GMT
ARG CB_VERSION=6.6.0
# Fri, 07 Jan 2022 02:53:10 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0
# Fri, 07 Jan 2022 02:53:10 GMT
ARG CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb
# Fri, 07 Jan 2022 02:53:10 GMT
ARG CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559
# Fri, 07 Jan 2022 02:53:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 07 Jan 2022 02:53:12 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 07 Jan 2022 02:54:01 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 07 Jan 2022 02:54:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 07 Jan 2022 02:54:04 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 07 Jan 2022 02:54:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 07 Jan 2022 02:54:05 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 07 Jan 2022 02:54:06 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 07 Jan 2022 02:54:07 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.6.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.0 CB_SHA256=9b196cd7be81d7d6b179838e9d30164fdb7a1f27e96678e61e24e9fe5c93f559 CB_VERSION=6.6.0
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 07 Jan 2022 02:54:07 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 07 Jan 2022 02:54:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Jan 2022 02:54:08 GMT
CMD ["couchbase-server"]
# Fri, 07 Jan 2022 02:54:08 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 07 Jan 2022 02:54:08 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:2f94e549220aea96f00cae7eb95f401e61b41a16cc5eb0b4ea592d0ce871930a`  
		Last Modified: Thu, 06 Jan 2022 23:50:21 GMT  
		Size: 26.7 MB (26705027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39190a5f0bbb71c26d649db3ff358ae8ddfd7b3634d544103d0ac55f9779ceb3`  
		Last Modified: Fri, 07 Jan 2022 02:59:59 GMT  
		Size: 7.4 MB (7370433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97698cfedc7f7834b3b8cd5f209790a1af7a41516f26f1c86137ce5cc522f7c`  
		Last Modified: Fri, 07 Jan 2022 02:59:56 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ae42c413043afce4a580078a602b3dbe0ec0d6b628e051533a0f4e9544f96c`  
		Last Modified: Fri, 07 Jan 2022 02:59:55 GMT  
		Size: 2.0 KB (1960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94335ebfc3cc6fa1cbf69a1e8a56a4f2d4ce018f3b5d192d408dd583cfbe75e`  
		Last Modified: Fri, 07 Jan 2022 03:00:30 GMT  
		Size: 320.0 MB (320018825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bccdc9a88628503bf24d4b8282e1aa90c6bb7f890b0e5c5c4caa637fd8e9b6e`  
		Last Modified: Fri, 07 Jan 2022 02:59:55 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f8f0e3da910b950a44af23a03d2127e79764621d647adc1c84f55dd4eb51f7`  
		Last Modified: Fri, 07 Jan 2022 02:59:55 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8671096ee387705ca193e89b22c66c200aa0d98c8de7546799649af7246bae53`  
		Last Modified: Fri, 07 Jan 2022 02:59:53 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09bb6d49eed2a22a306b44672321920269f5780caf5c28bfef6d8a8ae356548`  
		Last Modified: Fri, 07 Jan 2022 02:59:53 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95eb5e43b610701fac9ce557c44f7b4c987b048d374614668d131aab82936d10`  
		Last Modified: Fri, 07 Jan 2022 02:59:53 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d66db0d11ed8c297b88b9ab962b59f81920374b6c893b73ae05c04e11e2f88c`  
		Last Modified: Fri, 07 Jan 2022 02:59:53 GMT  
		Size: 118.2 KB (118191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82838216793f2a205236d56ec93c6ded17bd1585b7f7255cce2d4ba31d1823e`  
		Last Modified: Fri, 07 Jan 2022 02:59:53 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-7.0.2`

```console
$ docker pull couchbase@sha256:68de58c96248a30b4add89d892179430e29b62c1bbd0dcffee8a0265e8b02f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:community-7.0.2` - linux; amd64

```console
$ docker pull couchbase@sha256:513adeddb3dac0587358c85f3711bf727e447e92f93652f72f8b1dac39065e26
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.0 MB (429023254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0820ad5c12ff1030870a5ae4f957641165d74ff97b54777dd68ff2a19840b05b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:47:48 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 07 Jan 2022 02:50:06 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 07 Jan 2022 02:50:07 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 07 Jan 2022 02:50:08 GMT
ARG CB_VERSION=7.0.2
# Fri, 07 Jan 2022 02:50:08 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2
# Fri, 07 Jan 2022 02:50:08 GMT
ARG CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb
# Fri, 07 Jan 2022 02:50:08 GMT
ARG CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e
# Fri, 07 Jan 2022 02:50:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 07 Jan 2022 02:50:09 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 07 Jan 2022 02:50:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 07 Jan 2022 02:51:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 07 Jan 2022 02:51:03 GMT
COPY file:cf9c7c8a9eda8a5fefcaa60d67181024b8a07b30eb318d4c9591b33a95ca6680 in /etc/service/couchbase-server/run 
# Fri, 07 Jan 2022 02:51:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 07 Jan 2022 02:51:04 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 07 Jan 2022 02:51:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 07 Jan 2022 02:51:06 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.2-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.2 CB_SHA256=f935dcad5c04b553a3c56d782c8d9cb782cbd1cf88878a425ba5f9d45d08120e CB_VERSION=7.0.2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 07 Jan 2022 02:51:06 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 07 Jan 2022 02:51:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Jan 2022 02:51:06 GMT
CMD ["couchbase-server"]
# Fri, 07 Jan 2022 02:51:07 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 07 Jan 2022 02:51:07 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:284122b04391b834f17a613aa23e44a4b0779b49c4ba9f6a3956cc60508f5c70`  
		Last Modified: Fri, 07 Jan 2022 02:57:51 GMT  
		Size: 6.3 MB (6261189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf01a5cc2a38f6a4074d276f4d169b403d8ad0c1940b429c62e188218d56103`  
		Last Modified: Fri, 07 Jan 2022 02:57:48 GMT  
		Size: 263.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b99cd90fc26a21733f1bb94cd0e2b9956607f9740913b5c6647b5323c82a4f`  
		Last Modified: Fri, 07 Jan 2022 02:57:48 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0879e222305ec3dc532151ff0a4e304e6576ce191dd1c8e48fb8964e3774379d`  
		Last Modified: Fri, 07 Jan 2022 02:58:37 GMT  
		Size: 394.1 MB (394061651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1dc4149c320ffe22939dac147881a0ad3e3f99837c8f3f9ea40cc6c4a0c9fdd`  
		Last Modified: Fri, 07 Jan 2022 02:57:48 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270d7ca8583d0bf0615229eb25285df3e1f891ab7ad3d208e36c5be57f4807c9`  
		Last Modified: Fri, 07 Jan 2022 02:57:48 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e3b45dcc87a113571d0391bccd1724338906a8cf3b00353fe6540642416fbe`  
		Last Modified: Fri, 07 Jan 2022 02:57:46 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b272788b5f59d50d364138f28f046357d394fb1f2d49a2ca9874f0e1cd566d0`  
		Last Modified: Fri, 07 Jan 2022 02:57:46 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa25349832622183c7466dee90345f41343a80ef657290f102a0952375cf355b`  
		Last Modified: Fri, 07 Jan 2022 02:57:45 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed86d5d28263dfacb74f29cbfbf16e94448b3361c6cd7760ff1288173a5fb20`  
		Last Modified: Fri, 07 Jan 2022 02:57:46 GMT  
		Size: 129.5 KB (129512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9047bb95ecc6720389ad1355eebf785f9b9d373d388cbdcd05d431497416233f`  
		Last Modified: Fri, 07 Jan 2022 02:57:46 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise`

```console
$ docker pull couchbase@sha256:47ed9b19ac85b202000e8875aa8ae507c81dac77c67f757b8367522d8f1f35d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise` - linux; amd64

```console
$ docker pull couchbase@sha256:20251532870b6947b24c0249d8081652488af7ad45f221f015118dcd2df0db33
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.0 MB (676998066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb033a3df3d523bcf22def918aed04ea07ac0d1100bd60baf7cefec1943e6ee7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:47:48 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 07 Jan 2022 02:48:14 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 07 Jan 2022 02:48:14 GMT
ARG CB_VERSION=7.0.3
# Fri, 07 Jan 2022 02:48:15 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3
# Fri, 07 Jan 2022 02:48:15 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb
# Fri, 07 Jan 2022 02:48:15 GMT
ARG CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c
# Fri, 07 Jan 2022 02:48:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 07 Jan 2022 02:48:16 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 07 Jan 2022 02:49:34 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 07 Jan 2022 02:49:39 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 07 Jan 2022 02:49:39 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Fri, 07 Jan 2022 02:49:40 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 07 Jan 2022 02:49:41 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 07 Jan 2022 02:49:41 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 07 Jan 2022 02:49:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             apt-get update;             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get purge -y chrpath;             apt-get autoremove;             apt-get clean;         fi
# Fri, 07 Jan 2022 02:49:49 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Fri, 07 Jan 2022 02:49:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Jan 2022 02:49:49 GMT
CMD ["couchbase-server"]
# Fri, 07 Jan 2022 02:49:49 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 07 Jan 2022 02:49:50 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66cfcdf8838abf002a7e0a2b3f6a8a41688c07a1055f77fedce22a3c62c05b4`  
		Last Modified: Fri, 07 Jan 2022 02:56:20 GMT  
		Size: 6.3 MB (6252170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb4f8680ab88ed1d42054586110b2f7c88d44d1958461db8bc7768f41dbd77c`  
		Last Modified: Fri, 07 Jan 2022 02:56:17 GMT  
		Size: 1.8 KB (1829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1103d0911786914568c3da9a9a75f1af7bb0461c2ed7e70a18e2920a978e0bca`  
		Last Modified: Fri, 07 Jan 2022 02:57:27 GMT  
		Size: 618.3 MB (618296886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2110faa7a5b85b1938337de9103a54236c115e8e3eb81079716d9041b4003e05`  
		Last Modified: Fri, 07 Jan 2022 02:56:16 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fb9e05960f9a3f2f101ab8b046e9c1ec9e1ea75d558f014b3fa96b2110d4f8`  
		Last Modified: Fri, 07 Jan 2022 02:56:16 GMT  
		Size: 744.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4508c1d298c835756496e8819dd6a5eda3603f6598fffdb247bf6217bc698724`  
		Last Modified: Fri, 07 Jan 2022 02:56:14 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1496e727dd9652cc32a50f280e4a872cb12a0dcd8c36bfd63f4503a2a3c0aae`  
		Last Modified: Fri, 07 Jan 2022 02:56:14 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d91ce2b56d0558b11b0e82aef58a3a88a266d0e48acdb9c488593ff6f15377`  
		Last Modified: Fri, 07 Jan 2022 02:56:14 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc08238b4d72bda9a93053cd6b1dcb3dd9cc66f2a7a122fdd149f03bf1f50a4`  
		Last Modified: Fri, 07 Jan 2022 02:56:17 GMT  
		Size: 23.9 MB (23878221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2c81438f07aeea3dc1f64847b3c55fc43be24ea9d75c7bf33e92b0e758e980`  
		Last Modified: Fri, 07 Jan 2022 02:56:14 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-6.0.5`

```console
$ docker pull couchbase@sha256:be03f4a0eee07091c5e6b42d3a577c2794756db13ed7cc3119c0e8b72f6ee6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise-6.0.5` - linux; amd64

```console
$ docker pull couchbase@sha256:5ebdf4939c5d46f6d32087c1bb28c0967184532eec5d7bedbeeae5486ff219e1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.1 MB (466119913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea3b97e3dcb95085a142f1dcadf201294bce16f8c819628d17e6296f013265f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:21 GMT
ADD file:2aa3e79e3cff3c048612744ac310cf86bc27de3433d420711bafc6612445befc in / 
# Fri, 07 Jan 2022 02:25:21 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:52:42 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 07 Jan 2022 02:54:44 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 07 Jan 2022 02:54:45 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 07 Jan 2022 02:54:45 GMT
ARG CB_VERSION=6.0.5
# Fri, 07 Jan 2022 02:54:45 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5
# Fri, 07 Jan 2022 02:54:46 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb
# Fri, 07 Jan 2022 02:54:46 GMT
ARG CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d
# Fri, 07 Jan 2022 02:54:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 07 Jan 2022 02:54:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 07 Jan 2022 02:55:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 07 Jan 2022 02:55:50 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 07 Jan 2022 02:55:50 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 07 Jan 2022 02:55:51 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 07 Jan 2022 02:55:51 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 07 Jan 2022 02:55:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 07 Jan 2022 02:55:53 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.5-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.5 CB_SHA256=6b152590867a58d771cffc22774d3cd66c916defcbeeeb339aca8d0a8e6d7f8d CB_VERSION=6.0.5
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 07 Jan 2022 02:55:53 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 07 Jan 2022 02:55:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Jan 2022 02:55:53 GMT
CMD ["couchbase-server"]
# Fri, 07 Jan 2022 02:55:54 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 07 Jan 2022 02:55:54 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:2f94e549220aea96f00cae7eb95f401e61b41a16cc5eb0b4ea592d0ce871930a`  
		Last Modified: Thu, 06 Jan 2022 23:50:21 GMT  
		Size: 26.7 MB (26705027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e33bcc193d4c06563762ddad056028f9eb5a68bb14c96e48054bb7a57e3d6d`  
		Last Modified: Fri, 07 Jan 2022 03:00:45 GMT  
		Size: 15.9 MB (15921601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4965a86b9381cc2da611cf89bdd2522d66c112a05fe815e3929fadd00e8c612d`  
		Last Modified: Fri, 07 Jan 2022 03:00:41 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecdfa3eef7e95ac97bc3bab1c2995424ac3e24579983b4ebb63b056986687ca`  
		Last Modified: Fri, 07 Jan 2022 03:00:40 GMT  
		Size: 2.0 KB (1963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e20f3da4338b780536b19b01a18d9c8ff343c7a340c8d8b4ee19e986955bc96`  
		Last Modified: Fri, 07 Jan 2022 03:01:18 GMT  
		Size: 423.4 MB (423363242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7df65c056ca7bae77b6dfe98ebabe474056f98f19d08689b44ed726e3f7db4`  
		Last Modified: Fri, 07 Jan 2022 03:00:40 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3590d0bf2dfee04501dc388877a52f9160ad12772f6cde8c8795c260be178a95`  
		Last Modified: Fri, 07 Jan 2022 03:00:40 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3425ccc6efa0f744314c8c11e801cf580568ff3b43171758fad600df878b618`  
		Last Modified: Fri, 07 Jan 2022 03:00:38 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59e1549b0859bfa2fcdd3f82d6b78378b56fc634243673f6910bdd99a43331e`  
		Last Modified: Fri, 07 Jan 2022 03:00:38 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3cc87371a88370a2c16bfec6881f6cbafc4aa1bafa7a589fafb00f2291b601`  
		Last Modified: Fri, 07 Jan 2022 03:00:38 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ecdc492bbd4f515374a9cebf59bcca68fcd388198b541de59503853515f771`  
		Last Modified: Fri, 07 Jan 2022 03:00:38 GMT  
		Size: 125.6 KB (125563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3259321b9db1fb5dc44b85c70f69f436c24ea15b1bf47966e940ae5c560f4752`  
		Last Modified: Fri, 07 Jan 2022 03:00:38 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-6.6.4`

```console
$ docker pull couchbase@sha256:3775640593dd86e6682ff63de4a2e38941b7258753fc0f66d8db2ae0e0ebf707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise-6.6.4` - linux; amd64

```console
$ docker pull couchbase@sha256:fdad5c35d221a25172dabeae1c9bcc613e10430817f2bd751ef0b1b384223d0f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **561.7 MB (561688730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820e0d5e5d4fd9cabdfce500318b7e20b77374619b596cd32cf3254cae0cec31`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:47:48 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 07 Jan 2022 02:48:14 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 07 Jan 2022 02:51:19 GMT
ARG CB_VERSION=6.6.4
# Fri, 07 Jan 2022 02:51:20 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.4
# Fri, 07 Jan 2022 02:51:20 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.6.4-ubuntu20.04_amd64.deb
# Fri, 07 Jan 2022 02:51:20 GMT
ARG CB_SHA256=97cb0aec5a4f7e3d2c3e2017546ac0adb41478c6e5bc1dcefd06cc9f5926f6db
# Fri, 07 Jan 2022 02:51:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 07 Jan 2022 02:51:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.4-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.4 CB_SHA256=97cb0aec5a4f7e3d2c3e2017546ac0adb41478c6e5bc1dcefd06cc9f5926f6db CB_VERSION=6.6.4
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 07 Jan 2022 02:52:26 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.4-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.4 CB_SHA256=97cb0aec5a4f7e3d2c3e2017546ac0adb41478c6e5bc1dcefd06cc9f5926f6db CB_VERSION=6.6.4
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 07 Jan 2022 02:52:28 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.4-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.4 CB_SHA256=97cb0aec5a4f7e3d2c3e2017546ac0adb41478c6e5bc1dcefd06cc9f5926f6db CB_VERSION=6.6.4
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 07 Jan 2022 02:52:28 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Fri, 07 Jan 2022 02:52:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.4-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.4 CB_SHA256=97cb0aec5a4f7e3d2c3e2017546ac0adb41478c6e5bc1dcefd06cc9f5926f6db CB_VERSION=6.6.4
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 07 Jan 2022 02:52:29 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 07 Jan 2022 02:52:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.4-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.4 CB_SHA256=97cb0aec5a4f7e3d2c3e2017546ac0adb41478c6e5bc1dcefd06cc9f5926f6db CB_VERSION=6.6.4
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 07 Jan 2022 02:52:37 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.6.4-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.6.4 CB_SHA256=97cb0aec5a4f7e3d2c3e2017546ac0adb41478c6e5bc1dcefd06cc9f5926f6db CB_VERSION=6.6.4
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             apt-get update;             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get purge -y chrpath;             apt-get autoremove;             apt-get clean;         fi
# Fri, 07 Jan 2022 02:52:38 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Fri, 07 Jan 2022 02:52:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Jan 2022 02:52:38 GMT
CMD ["couchbase-server"]
# Fri, 07 Jan 2022 02:52:38 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 07 Jan 2022 02:52:39 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66cfcdf8838abf002a7e0a2b3f6a8a41688c07a1055f77fedce22a3c62c05b4`  
		Last Modified: Fri, 07 Jan 2022 02:56:20 GMT  
		Size: 6.3 MB (6252170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a16199ea3a03efa6bc813742048c124777c44a880011c4f02f0ab2ed64655366`  
		Last Modified: Fri, 07 Jan 2022 02:58:50 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3335e980a3591f1d6a88a0e5987986c06e05d58c7b593480950e9e62c88131f`  
		Last Modified: Fri, 07 Jan 2022 02:59:42 GMT  
		Size: 503.0 MB (502991689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5eb14c1807736bf2b4ab827e9fd460dcaaabf182af700421592b7d13df3732`  
		Last Modified: Fri, 07 Jan 2022 02:58:50 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1d5b3d1205d51ec426512339929f89cf3f366b3730b33776992f14567234f10`  
		Last Modified: Fri, 07 Jan 2022 02:58:50 GMT  
		Size: 744.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2b217981de2a462d4dcc62538fc1a1f3c1cbf3b6f6729768fd39c08fb18c97`  
		Last Modified: Fri, 07 Jan 2022 02:58:48 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3235e9bac99058de6ff914ba35a22351a4a572b341552845bf65ec3abc12abde`  
		Last Modified: Fri, 07 Jan 2022 02:58:48 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc9220de1c0106fba54832851747dffad049287f03d3b12c7fa7ecff5461beb`  
		Last Modified: Fri, 07 Jan 2022 02:58:48 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4163898a45897dd974d3ae811621a9c97b0f6df6dfd4a13ad3e14f1ee967b9a6`  
		Last Modified: Fri, 07 Jan 2022 02:58:50 GMT  
		Size: 23.9 MB (23874079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719891fd4435444301cfc8b2b9cfa85be519b0014494181a0996b1f43600d323`  
		Last Modified: Fri, 07 Jan 2022 02:58:48 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-7.0.3`

```console
$ docker pull couchbase@sha256:47ed9b19ac85b202000e8875aa8ae507c81dac77c67f757b8367522d8f1f35d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise-7.0.3` - linux; amd64

```console
$ docker pull couchbase@sha256:20251532870b6947b24c0249d8081652488af7ad45f221f015118dcd2df0db33
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.0 MB (676998066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb033a3df3d523bcf22def918aed04ea07ac0d1100bd60baf7cefec1943e6ee7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:47:48 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 07 Jan 2022 02:48:14 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 07 Jan 2022 02:48:14 GMT
ARG CB_VERSION=7.0.3
# Fri, 07 Jan 2022 02:48:15 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3
# Fri, 07 Jan 2022 02:48:15 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb
# Fri, 07 Jan 2022 02:48:15 GMT
ARG CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c
# Fri, 07 Jan 2022 02:48:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 07 Jan 2022 02:48:16 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 07 Jan 2022 02:49:34 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 07 Jan 2022 02:49:39 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 07 Jan 2022 02:49:39 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Fri, 07 Jan 2022 02:49:40 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 07 Jan 2022 02:49:41 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 07 Jan 2022 02:49:41 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 07 Jan 2022 02:49:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             apt-get update;             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get purge -y chrpath;             apt-get autoremove;             apt-get clean;         fi
# Fri, 07 Jan 2022 02:49:49 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Fri, 07 Jan 2022 02:49:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Jan 2022 02:49:49 GMT
CMD ["couchbase-server"]
# Fri, 07 Jan 2022 02:49:49 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 07 Jan 2022 02:49:50 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66cfcdf8838abf002a7e0a2b3f6a8a41688c07a1055f77fedce22a3c62c05b4`  
		Last Modified: Fri, 07 Jan 2022 02:56:20 GMT  
		Size: 6.3 MB (6252170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb4f8680ab88ed1d42054586110b2f7c88d44d1958461db8bc7768f41dbd77c`  
		Last Modified: Fri, 07 Jan 2022 02:56:17 GMT  
		Size: 1.8 KB (1829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1103d0911786914568c3da9a9a75f1af7bb0461c2ed7e70a18e2920a978e0bca`  
		Last Modified: Fri, 07 Jan 2022 02:57:27 GMT  
		Size: 618.3 MB (618296886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2110faa7a5b85b1938337de9103a54236c115e8e3eb81079716d9041b4003e05`  
		Last Modified: Fri, 07 Jan 2022 02:56:16 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fb9e05960f9a3f2f101ab8b046e9c1ec9e1ea75d558f014b3fa96b2110d4f8`  
		Last Modified: Fri, 07 Jan 2022 02:56:16 GMT  
		Size: 744.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4508c1d298c835756496e8819dd6a5eda3603f6598fffdb247bf6217bc698724`  
		Last Modified: Fri, 07 Jan 2022 02:56:14 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1496e727dd9652cc32a50f280e4a872cb12a0dcd8c36bfd63f4503a2a3c0aae`  
		Last Modified: Fri, 07 Jan 2022 02:56:14 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d91ce2b56d0558b11b0e82aef58a3a88a266d0e48acdb9c488593ff6f15377`  
		Last Modified: Fri, 07 Jan 2022 02:56:14 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc08238b4d72bda9a93053cd6b1dcb3dd9cc66f2a7a122fdd149f03bf1f50a4`  
		Last Modified: Fri, 07 Jan 2022 02:56:17 GMT  
		Size: 23.9 MB (23878221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2c81438f07aeea3dc1f64847b3c55fc43be24ea9d75c7bf33e92b0e758e980`  
		Last Modified: Fri, 07 Jan 2022 02:56:14 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:latest`

```console
$ docker pull couchbase@sha256:47ed9b19ac85b202000e8875aa8ae507c81dac77c67f757b8367522d8f1f35d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:latest` - linux; amd64

```console
$ docker pull couchbase@sha256:20251532870b6947b24c0249d8081652488af7ad45f221f015118dcd2df0db33
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.0 MB (676998066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb033a3df3d523bcf22def918aed04ea07ac0d1100bd60baf7cefec1943e6ee7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:29 GMT
ADD file:122ad323412c2e70b3138d8eb62648c4692989de91be1ffb6b4bf086c8311b62 in / 
# Fri, 07 Jan 2022 02:25:30 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:47:48 GMT
LABEL maintainer=docker@couchbase.com
# Fri, 07 Jan 2022 02:48:14 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 07 Jan 2022 02:48:14 GMT
ARG CB_VERSION=7.0.3
# Fri, 07 Jan 2022 02:48:15 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3
# Fri, 07 Jan 2022 02:48:15 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb
# Fri, 07 Jan 2022 02:48:15 GMT
ARG CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c
# Fri, 07 Jan 2022 02:48:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 07 Jan 2022 02:48:16 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 07 Jan 2022 02:49:34 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 07 Jan 2022 02:49:39 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 07 Jan 2022 02:49:39 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Fri, 07 Jan 2022 02:49:40 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Fri, 07 Jan 2022 02:49:41 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 07 Jan 2022 02:49:41 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 07 Jan 2022 02:49:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.3-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.3 CB_SHA256=efacf9923a7203771fc342ec010d1baf9325c01f284b22c703b10e5dc9b38d2c CB_VERSION=7.0.3
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             apt-get update;             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get purge -y chrpath;             apt-get autoremove;             apt-get clean;         fi
# Fri, 07 Jan 2022 02:49:49 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Fri, 07 Jan 2022 02:49:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Jan 2022 02:49:49 GMT
CMD ["couchbase-server"]
# Fri, 07 Jan 2022 02:49:49 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 07 Jan 2022 02:49:50 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:ea362f368469f909a95f9a6e54ebe0121ce0a8e3c30583dd9c5fb35b14544dec`  
		Last Modified: Thu, 06 Jan 2022 15:07:12 GMT  
		Size: 28.6 MB (28566425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c66cfcdf8838abf002a7e0a2b3f6a8a41688c07a1055f77fedce22a3c62c05b4`  
		Last Modified: Fri, 07 Jan 2022 02:56:20 GMT  
		Size: 6.3 MB (6252170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb4f8680ab88ed1d42054586110b2f7c88d44d1958461db8bc7768f41dbd77c`  
		Last Modified: Fri, 07 Jan 2022 02:56:17 GMT  
		Size: 1.8 KB (1829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1103d0911786914568c3da9a9a75f1af7bb0461c2ed7e70a18e2920a978e0bca`  
		Last Modified: Fri, 07 Jan 2022 02:57:27 GMT  
		Size: 618.3 MB (618296886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2110faa7a5b85b1938337de9103a54236c115e8e3eb81079716d9041b4003e05`  
		Last Modified: Fri, 07 Jan 2022 02:56:16 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fb9e05960f9a3f2f101ab8b046e9c1ec9e1ea75d558f014b3fa96b2110d4f8`  
		Last Modified: Fri, 07 Jan 2022 02:56:16 GMT  
		Size: 744.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4508c1d298c835756496e8819dd6a5eda3603f6598fffdb247bf6217bc698724`  
		Last Modified: Fri, 07 Jan 2022 02:56:14 GMT  
		Size: 280.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1496e727dd9652cc32a50f280e4a872cb12a0dcd8c36bfd63f4503a2a3c0aae`  
		Last Modified: Fri, 07 Jan 2022 02:56:14 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d91ce2b56d0558b11b0e82aef58a3a88a266d0e48acdb9c488593ff6f15377`  
		Last Modified: Fri, 07 Jan 2022 02:56:14 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc08238b4d72bda9a93053cd6b1dcb3dd9cc66f2a7a122fdd149f03bf1f50a4`  
		Last Modified: Fri, 07 Jan 2022 02:56:17 GMT  
		Size: 23.9 MB (23878221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2c81438f07aeea3dc1f64847b3c55fc43be24ea9d75c7bf33e92b0e758e980`  
		Last Modified: Fri, 07 Jan 2022 02:56:14 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

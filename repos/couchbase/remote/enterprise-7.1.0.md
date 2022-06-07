## `couchbase:enterprise-7.1.0`

```console
$ docker pull couchbase@sha256:6ea8fc49bde775bb4999f59add71dc7e016c7ec6c00a286729c395a1948c0356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchbase:enterprise-7.1.0` - linux; amd64

```console
$ docker pull couchbase@sha256:7d39eec7f4b690434d612729e20696704b35af5c65a7452384f7f2ccb4e2e3cf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.3 MB (597284519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d89249226d96836b0a13f648400b9189386bc13965b7d75467689b363de3bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:11 GMT
ADD file:00dae10e79b05c4e1a3db053a1f85a4f38a39fe85cbbd88d74201a01a7dd59b5 in / 
# Mon, 06 Jun 2022 22:21:12 GMT
CMD ["bash"]
# Mon, 06 Jun 2022 23:57:21 GMT
LABEL maintainer=docker@couchbase.com
# Mon, 06 Jun 2022 23:57:21 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Mon, 06 Jun 2022 23:57:21 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Mon, 06 Jun 2022 23:57:42 GMT
# ARGS: CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2 runit     && ${CLEANUP_COMMAND}
# Mon, 06 Jun 2022 23:57:42 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0
# Mon, 06 Jun 2022 23:57:42 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb
# Mon, 06 Jun 2022 23:57:42 GMT
ARG CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987
# Mon, 06 Jun 2022 23:57:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Mon, 06 Jun 2022 23:57:43 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Mon, 06 Jun 2022 23:58:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && export INSTALL_DONT_START_SERVER=1     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c -     && ${UPDATE_COMMAND}     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/*
# Mon, 06 Jun 2022 23:58:43 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Mon, 06 Jun 2022 23:58:43 GMT
COPY file:018fa38d92aa0a4679f57c2d43b5c14547b2c603cab6ec7fd3240af5545472b5 in /etc/service/couchbase-server/run 
# Mon, 06 Jun 2022 23:58:43 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Mon, 06 Jun 2022 23:58:44 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Mon, 06 Jun 2022 23:58:44 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay
# Mon, 06 Jun 2022 23:58:45 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.1.0-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.1.0 CB_SHA256=5cefdbf8970a86b7869b3bc1f37bea2454e0d1f72733be39a1c20bb5c2641987 CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* UPDATE_COMMAND=apt-get update -y -q
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi
# Mon, 06 Jun 2022 23:58:45 GMT
COPY file:6e5292e89c7124e038a0d80ea3b942bff1ed578e67a07e764b041ea95b129aa3 in / 
# Mon, 06 Jun 2022 23:58:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 06 Jun 2022 23:58:45 GMT
CMD ["couchbase-server"]
# Mon, 06 Jun 2022 23:58:45 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Mon, 06 Jun 2022 23:58:45 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d7bfe07ed8476565a440c2113cc64d7c0409dba8ef761fb3ec019d7e6b5952df`  
		Last Modified: Wed, 01 Jun 2022 21:51:10 GMT  
		Size: 28.6 MB (28572632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b15b7718218cb8c8adc351f6e6d4b00e354a525046c18ec4d6f5bab108a1a66`  
		Last Modified: Tue, 07 Jun 2022 00:07:47 GMT  
		Size: 6.3 MB (6251734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a382f188a254365de856786d2674ede0de9879c8ccbb6afd090f339672983369`  
		Last Modified: Tue, 07 Jun 2022 00:07:46 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70907b514b578a504619d3d14792edbf0202a0f1f7758baffd0e5660ebad329`  
		Last Modified: Tue, 07 Jun 2022 00:08:45 GMT  
		Size: 562.5 MB (562455802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ef166d73a55b945bf9c1d80fad208364b8090aaad90081f952a5c865258e94`  
		Last Modified: Tue, 07 Jun 2022 00:07:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e437177da346d5fa18219c10d2749a25ef125f4de4b702b4fff7a14a5a31bccc`  
		Last Modified: Tue, 07 Jun 2022 00:07:43 GMT  
		Size: 738.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de991ce42e47127d35719b69d6eb8e7930f66ddc424d1fe6eefbf4f0712beed7`  
		Last Modified: Tue, 07 Jun 2022 00:07:44 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b527c1f51ff4a3db59ecb458830ad9722d0604474ac83ed472d002c4a37570`  
		Last Modified: Tue, 07 Jun 2022 00:07:43 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ebba9d2f225c927231971398e9dde38cb5280e95f5cd018b0db26c1dac7aa98`  
		Last Modified: Tue, 07 Jun 2022 00:07:44 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0d9f0e42e30d39153e6c61c707e551e1f90909cfc66bfa8ae986c3ac5ccb42`  
		Last Modified: Tue, 07 Jun 2022 00:07:44 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

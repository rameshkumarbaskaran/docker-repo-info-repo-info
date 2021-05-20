## `couchbase:community-6.5.1`

```console
$ docker pull couchbase@sha256:ba60dad501fa8c3428bb28ed55ce23ea8f2f13ae8ef5d066341464c97fea314e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:community-6.5.1` - linux; amd64

```console
$ docker pull couchbase@sha256:22c698310ff613b8555b27bef0b2bae0158e250f8efd7d9c94cdc821a9dcddc6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.6 MB (351605340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48190acfa65d8be9b49744f388be22121fb04ce97a698467e9860472f9861d49`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 19 May 2021 19:44:30 GMT
ADD file:e05689b5b0d51a2316f8a87b1a9d6cbf90d98b19a424dbb924ee3d0b1cc17bfc in / 
# Wed, 19 May 2021 19:44:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 May 2021 19:44:32 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 May 2021 19:44:33 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 May 2021 19:44:33 GMT
CMD ["/bin/bash"]
# Wed, 19 May 2021 20:37:24 GMT
LABEL maintainer=docker@couchbase.com
# Wed, 19 May 2021 20:37:47 GMT
RUN set -x &&     apt-get update &&     apt-get install -yq runit wget chrpath tzdata man     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 19 May 2021 20:37:48 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Wed, 19 May 2021 20:43:21 GMT
ARG CB_VERSION=6.5.1
# Wed, 19 May 2021 20:43:21 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1
# Wed, 19 May 2021 20:51:13 GMT
ARG CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu18.04_amd64.deb
# Wed, 19 May 2021 20:51:13 GMT
ARG CB_SHA256=c4951cdab01759020444e4648023721ae3a333257591252475d34d5fc6ac8857
# Wed, 19 May 2021 20:51:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 19 May 2021 20:51:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=c4951cdab01759020444e4648023721ae3a333257591252475d34d5fc6ac8857 CB_VERSION=6.5.1
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 19 May 2021 20:51:59 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=c4951cdab01759020444e4648023721ae3a333257591252475d34d5fc6ac8857 CB_VERSION=6.5.1
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 19 May 2021 20:52:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=c4951cdab01759020444e4648023721ae3a333257591252475d34d5fc6ac8857 CB_VERSION=6.5.1
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 19 May 2021 20:52:02 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Wed, 19 May 2021 20:52:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=c4951cdab01759020444e4648023721ae3a333257591252475d34d5fc6ac8857 CB_VERSION=6.5.1
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Wed, 19 May 2021 20:52:03 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 19 May 2021 20:52:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=c4951cdab01759020444e4648023721ae3a333257591252475d34d5fc6ac8857 CB_VERSION=6.5.1
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 19 May 2021 20:52:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.5.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=c4951cdab01759020444e4648023721ae3a333257591252475d34d5fc6ac8857 CB_VERSION=6.5.1
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Wed, 19 May 2021 20:52:06 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Wed, 19 May 2021 20:52:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 May 2021 20:52:06 GMT
CMD ["couchbase-server"]
# Wed, 19 May 2021 20:52:06 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Wed, 19 May 2021 20:52:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:4bbfd2c87b7524455f144a03bf387c88b6d4200e5e0df9139a9d5e79110f89ca`  
		Last Modified: Thu, 13 May 2021 14:54:04 GMT  
		Size: 26.7 MB (26696304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e110be24e168b42c1a2ddbc4a476a217b73cccdba69cdcb212b812a88f5726`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889a7173dcfeb409f9d88054a97ab2445f5a799a823f719a5573365ee3662b6f`  
		Last Modified: Wed, 19 May 2021 19:45:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8723b0ce09e00f93edd6ad638f58c72b0267b552fe98ea3b31a4992f7bb6505`  
		Last Modified: Wed, 19 May 2021 20:52:54 GMT  
		Size: 7.4 MB (7373972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad9d59e6d2171c21332ad46d9b8d83b66d0318da66b15cae4aff7bf21070166`  
		Last Modified: Wed, 19 May 2021 20:52:49 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1eb0d78d732eb1b88db19664e485bc4a32381add6a8ba4d1a141b2cd907f14`  
		Last Modified: Wed, 19 May 2021 21:03:44 GMT  
		Size: 2.0 KB (1969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c011a2ab659c24b6544581ea48bfe36d397c9765c88f62474652684804217c`  
		Last Modified: Wed, 19 May 2021 21:04:24 GMT  
		Size: 317.4 MB (317411344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbd5039a7718105f4b0f9f495aedc2e3f2ffd2b9b70c1e678962178c7d1e7cf`  
		Last Modified: Wed, 19 May 2021 21:03:44 GMT  
		Size: 190.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a45e36554a45e1f5449a7f9a90db23e8621f1d2d657abaee1f449295a41bd2`  
		Last Modified: Wed, 19 May 2021 21:03:44 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cae5ae9fea7b86c6698f3a5bb42a2b8e41ebc78da56f14f8459374153748784`  
		Last Modified: Wed, 19 May 2021 21:03:41 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b183face69e5290386221caf1e84316fe830a0ea8651207f638b92f3b90b8202`  
		Last Modified: Wed, 19 May 2021 21:03:41 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce70462c103d492ab10c7826d896a18f5ef595557bd74244c58b7ac30484d9d`  
		Last Modified: Wed, 19 May 2021 21:03:41 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60cbbf2e73b8e22fa3a2206e19a2cb00b974fd57f02f3ac6a2fc7954b3d452d3`  
		Last Modified: Wed, 19 May 2021 21:03:42 GMT  
		Size: 118.2 KB (118188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e160866ecf4bd0e37da0e8a8d33641dbd744db3e8d9d645229a2b46d21f5cbcc`  
		Last Modified: Wed, 19 May 2021 21:03:41 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

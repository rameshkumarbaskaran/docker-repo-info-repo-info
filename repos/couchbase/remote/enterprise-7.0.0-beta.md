## `couchbase:enterprise-7.0.0-beta`

```console
$ docker pull couchbase@sha256:aed5d206af89ea11245e4bf268b116bc2bf565e8afd2eafbf7df58fc7d1cf861
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-7.0.0-beta` - linux; amd64

```console
$ docker pull couchbase@sha256:1b6a19d2130ef5aa61c71bc9bed27e626237e0df166c7b68529f5ca0efa98517
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **625.8 MB (625802616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5ac5f99b3cfc54e9590951f971845df4a155f1391dbc7b8cdfed15eece26a3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:34 GMT
ADD file:5c44a80f547b7d68b550b0e64aef898b361666857abf9a5c8f3f8d0567b8e8e4 in / 
# Fri, 23 Apr 2021 22:21:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:37 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:09:02 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Fri, 23 Apr 2021 23:09:21 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Fri, 23 Apr 2021 23:09:22 GMT
RUN if [ ! -x /usr/sbin/runsvdir-start ]; then         cp -a /etc/runit/2 /usr/sbin/runsvdir-start;     fi
# Fri, 23 Apr 2021 23:09:22 GMT
ARG CB_VERSION=7.0.0-beta
# Fri, 23 Apr 2021 23:09:23 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta
# Fri, 23 Apr 2021 23:09:23 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb
# Fri, 23 Apr 2021 23:09:23 GMT
ARG CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6
# Fri, 23 Apr 2021 23:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 23 Apr 2021 23:09:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 23 Apr 2021 23:10:25 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Fri, 23 Apr 2021 23:10:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 23 Apr 2021 23:10:30 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 23 Apr 2021 23:10:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN chown -R couchbase:couchbase /etc/service
# Fri, 23 Apr 2021 23:10:31 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 23 Apr 2021 23:10:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 23 Apr 2021 23:10:33 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=e24be4f765eafbfbfdd5f7eddb780006084e3bd01cbcb3d3880dd9be48b955f6 CB_VERSION=7.0.0-beta
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 23 Apr 2021 23:10:34 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 23 Apr 2021 23:10:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 Apr 2021 23:10:34 GMT
CMD ["couchbase-server"]
# Fri, 23 Apr 2021 23:10:34 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 23 Apr 2021 23:10:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:345e3491a907bb7c6f1bdddcf4a94284b8b6ddd77eb7d93f09432b17b20f2bbe`  
		Last Modified: Fri, 16 Apr 2021 15:20:19 GMT  
		Size: 28.5 MB (28539626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57671312ef6fdbecf340e5fed0fb0863350cd806c92b1fdd7978adbd02afc5c3`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9250ddb7d0fa6d13302c7c3e6a0aa40390e42424caed1e5289077ee4054709`  
		Last Modified: Fri, 23 Apr 2021 22:23:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7936dfaada24f79bafe7aa3445a7d6cc71d2accb0dd3bc9edefb0fa557ebea99`  
		Last Modified: Fri, 23 Apr 2021 23:16:03 GMT  
		Size: 6.3 MB (6273226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa99224a9ececc210521261656e3641be6a69810d5fae3dc0e1d7ec28b3dfc34`  
		Last Modified: Fri, 23 Apr 2021 23:15:57 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4643d4da00876529596c8ef491faa1ecaaef06076d337327a42dcd469cfe26a`  
		Last Modified: Fri, 23 Apr 2021 23:15:57 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed03712a6d2286ba67f1ad6f3126f1c9cde5995d93ec20486bcfaa6b69773f4`  
		Last Modified: Fri, 23 Apr 2021 23:17:18 GMT  
		Size: 590.9 MB (590858600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100edec8d6dec14756fb5f17efb144b9722989552b47e08561a818f3aed7275d`  
		Last Modified: Fri, 23 Apr 2021 23:15:57 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a88af01b1d7cf6f40473508e357e6d593686d2f4f90d131707c493b8a4fe45a`  
		Last Modified: Fri, 23 Apr 2021 23:15:57 GMT  
		Size: 477.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030143abd5793c25bc4e60d5b2fd399c0f55e6e48979b76703ad7aaf97f48583`  
		Last Modified: Fri, 23 Apr 2021 23:15:54 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb1f4857061863a6cb3696690c7c5e7608ff350b957f1996ca6ad432fee196b`  
		Last Modified: Fri, 23 Apr 2021 23:15:54 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1f8d283e1c9bdf449cbcf3dd8dcbfa58f1c01a91dd34f01c56611fbe4fd502`  
		Last Modified: Fri, 23 Apr 2021 23:15:54 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b404b6274af16d841bb26a2a6fc508fa2a651895a548be86156a0ef0f597a18`  
		Last Modified: Fri, 23 Apr 2021 23:15:54 GMT  
		Size: 125.9 KB (125890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fddba050fadc5cc505c5536d6392b318385b12867bbefe7bd344926e58f19955`  
		Last Modified: Fri, 23 Apr 2021 23:15:54 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

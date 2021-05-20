## `couchbase:enterprise-6.5.0`

```console
$ docker pull couchbase@sha256:1b0ced22d7478a9739741d310e3733cbbbbe2bc612453417cba2bcc7df808475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.5.0` - linux; amd64

```console
$ docker pull couchbase@sha256:61a0d5079e2aa32f7d8c6f21f4213a48b01033b819a84df35a543a819a79c917
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.2 MB (542226744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce330b0e0756954bdf09bff98310adc9603190b6c7d12fae975efcd553df49d8`
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
# Wed, 19 May 2021 20:44:47 GMT
ARG CB_VERSION=6.5.0
# Wed, 19 May 2021 20:44:47 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0
# Wed, 19 May 2021 20:44:47 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu18.04_amd64.deb
# Wed, 19 May 2021 20:44:47 GMT
ARG CB_SHA256=b4cafdc048b0caba85c24b90e6823e9ec2adc32061cafc527ddc99d706d6bc05
# Wed, 19 May 2021 20:44:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 19 May 2021 20:44:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=b4cafdc048b0caba85c24b90e6823e9ec2adc32061cafc527ddc99d706d6bc05 CB_VERSION=6.5.0
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 19 May 2021 20:45:56 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=b4cafdc048b0caba85c24b90e6823e9ec2adc32061cafc527ddc99d706d6bc05 CB_VERSION=6.5.0
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 19 May 2021 20:46:00 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=b4cafdc048b0caba85c24b90e6823e9ec2adc32061cafc527ddc99d706d6bc05 CB_VERSION=6.5.0
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 19 May 2021 20:46:00 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Wed, 19 May 2021 20:46:01 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=b4cafdc048b0caba85c24b90e6823e9ec2adc32061cafc527ddc99d706d6bc05 CB_VERSION=6.5.0
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Wed, 19 May 2021 20:46:01 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 19 May 2021 20:46:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=b4cafdc048b0caba85c24b90e6823e9ec2adc32061cafc527ddc99d706d6bc05 CB_VERSION=6.5.0
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 19 May 2021 20:46:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0 CB_SHA256=b4cafdc048b0caba85c24b90e6823e9ec2adc32061cafc527ddc99d706d6bc05 CB_VERSION=6.5.0
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Wed, 19 May 2021 20:46:04 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Wed, 19 May 2021 20:46:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 May 2021 20:46:04 GMT
CMD ["couchbase-server"]
# Wed, 19 May 2021 20:46:04 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Wed, 19 May 2021 20:46:04 GMT
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
	-	`sha256:6c5f58794fc729fcf348afa2dcef108d12db268ea199cd0e6c3c4e4ad912de72`  
		Last Modified: Wed, 19 May 2021 20:58:34 GMT  
		Size: 2.0 KB (1967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f81fcfdbec31b03e4d3232ad53d1d33cb653ea8852d57279c9e2015402cbe2`  
		Last Modified: Wed, 19 May 2021 20:59:32 GMT  
		Size: 508.0 MB (508032741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8789570391e05fadb4f9bbfe3f607893b46e695c1ce57d2d1f97b24becfe9d11`  
		Last Modified: Wed, 19 May 2021 20:58:34 GMT  
		Size: 191.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf58fc1e41e79e49a402c487c92ae731fa3caf6708d73c2cfff531f49f553838`  
		Last Modified: Wed, 19 May 2021 20:58:34 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f63430d3051d5330149bfc6d249c96a64e427a7bd57ec997edacc690d0e71f5`  
		Last Modified: Wed, 19 May 2021 20:58:32 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2029d11a71345ea6a99284dfdbb4e3c3415df5de939142c5122450e743ff17c`  
		Last Modified: Wed, 19 May 2021 20:58:32 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df70b8b61453d0d8198d0e90be8e8773e96469959cd0743191e41c2ffc32f7f`  
		Last Modified: Wed, 19 May 2021 20:58:32 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c5ea54082367f17917662fd6a648a9316bed242b2563f933fe8f213ad06baf`  
		Last Modified: Wed, 19 May 2021 20:58:32 GMT  
		Size: 118.2 KB (118190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e23f3da773226d8427d9ac20974ad0377883a4bcaf1c1e5143889e53878823`  
		Last Modified: Wed, 19 May 2021 20:58:32 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

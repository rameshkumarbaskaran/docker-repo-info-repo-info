## `couchbase:enterprise-6.5.1`

```console
$ docker pull couchbase@sha256:e5a07ee624c264d3a8ebcc2ff0989ea710c5843f73b0d541b2e3ea2f476adc13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.5.1` - linux; amd64

```console
$ docker pull couchbase@sha256:2596eba7e35cd0ccd762fcaf0567fcb71e81671af09209a949c1421f66464e60
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **501.5 MB (501501160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbc773ff302a2271c286206d2f16058b9630a1f3eeab111dd453eb918eb05a12`
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
# Wed, 19 May 2021 20:43:21 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu18.04_amd64.deb
# Wed, 19 May 2021 20:43:22 GMT
ARG CB_SHA256=992fc9aef85c210cc2d782a1726f2ef56ceb322fd67c2e95500e276ff106e6ff
# Wed, 19 May 2021 20:43:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Wed, 19 May 2021 20:43:23 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=992fc9aef85c210cc2d782a1726f2ef56ceb322fd67c2e95500e276ff106e6ff CB_VERSION=6.5.1
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Wed, 19 May 2021 20:44:24 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=992fc9aef85c210cc2d782a1726f2ef56ceb322fd67c2e95500e276ff106e6ff CB_VERSION=6.5.1
RUN set -x &&     export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     apt-get update &&     apt-get install -y ./$CB_PACKAGE &&     rm -f ./$CB_PACKAGE &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 19 May 2021 20:44:29 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=992fc9aef85c210cc2d782a1726f2ef56ceb322fd67c2e95500e276ff106e6ff CB_VERSION=6.5.1
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Wed, 19 May 2021 20:44:29 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Wed, 19 May 2021 20:44:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=992fc9aef85c210cc2d782a1726f2ef56ceb322fd67c2e95500e276ff106e6ff CB_VERSION=6.5.1
RUN mkdir -p /etc/runit/runsvdir/default/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/runit/runsvdir/default/couchbase-server/supervise
# Wed, 19 May 2021 20:44:30 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Wed, 19 May 2021 20:44:31 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=992fc9aef85c210cc2d782a1726f2ef56ceb322fd67c2e95500e276ff106e6ff CB_VERSION=6.5.1
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Wed, 19 May 2021 20:44:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.1-ubuntu18.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.1 CB_SHA256=992fc9aef85c210cc2d782a1726f2ef56ceb322fd67c2e95500e276ff106e6ff CB_VERSION=6.5.1
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Wed, 19 May 2021 20:44:32 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Wed, 19 May 2021 20:44:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 May 2021 20:44:33 GMT
CMD ["couchbase-server"]
# Wed, 19 May 2021 20:44:33 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Wed, 19 May 2021 20:44:33 GMT
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
	-	`sha256:c0e7c36208414c632782ff3195cccf7d5c7bb6eda0dffbf707b775e7f5c56468`  
		Last Modified: Wed, 19 May 2021 20:57:20 GMT  
		Size: 2.0 KB (1970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fdc5964e843c9c13dab9c184abb20259a7da0119a6d6766d2fef5e18e81984f`  
		Last Modified: Wed, 19 May 2021 20:58:18 GMT  
		Size: 467.3 MB (467307165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64dc033078d33ddd7c93f8c9893f5fcb0204e33f1f5f0b0adbbd3c72d318d5f6`  
		Last Modified: Wed, 19 May 2021 20:57:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e62a708e1b485938810b795c6f97bd07162dc707443c94c04cd1f181226576`  
		Last Modified: Wed, 19 May 2021 20:57:20 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d83bb838adf886ddc78a7f9f7a4da236159da16da8b50b32a691e9be379ffdae`  
		Last Modified: Wed, 19 May 2021 20:57:17 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df885e4496a0d5f0d6eea5a9385b39c44778c4f9aed86041c66f07d8fbeb9a6`  
		Last Modified: Wed, 19 May 2021 20:57:17 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454dacb0c733f1912ac6c4eea8935a6851848d00233b7b4e157803c874ab6f6e`  
		Last Modified: Wed, 19 May 2021 20:57:18 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f3cfad73a73352fdcf7fba28fadded84066960c3b9ffd2efd8aeac46954003b`  
		Last Modified: Wed, 19 May 2021 20:57:17 GMT  
		Size: 118.2 KB (118188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c327bff855f6f98379f6d94052be1990d2ab4fca8a3485df525787ed890599fd`  
		Last Modified: Wed, 19 May 2021 20:57:17 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

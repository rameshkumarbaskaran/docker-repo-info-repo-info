## `couchbase:enterprise-6.0.4`

```console
$ docker pull couchbase@sha256:d945c477e401e4415e82af965b2b06cb670eafe30ae540c45d9e824ac3bb86a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.0.4` - linux; amd64

```console
$ docker pull couchbase@sha256:ffc05c1dda967f9f601a9e4d311d5dbf72705b88aefb2f71f62d697c0edabd30
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.6 MB (480557561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbb3397453bff79fae67132116712a4249191f1650c4f5519f3efe51955ee1fe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Wed, 19 Aug 2020 21:16:18 GMT
ADD file:144835a276ed2d8eaf6e893d5560444fe0d6a6f9b9bdadec1eb56e7bd9814427 in / 
# Wed, 19 Aug 2020 21:16:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 21:16:21 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:16:22 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:16:22 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:14:52 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Tue, 01 Sep 2020 23:33:59 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 01 Sep 2020 23:33:59 GMT
ARG CB_VERSION=6.0.4
# Tue, 01 Sep 2020 23:33:59 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.4
# Tue, 01 Sep 2020 23:33:59 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.4-ubuntu16.04_amd64.deb
# Tue, 01 Sep 2020 23:34:00 GMT
ARG CB_SHA256=a9144e41fdb62dc872e09be617f69157f23568cc6e1d425e7adaf580aeba9adf
# Tue, 01 Sep 2020 23:34:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Tue, 01 Sep 2020 23:34:01 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.4-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.4 CB_SHA256=a9144e41fdb62dc872e09be617f69157f23568cc6e1d425e7adaf580aeba9adf CB_VERSION=6.0.4
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Tue, 01 Sep 2020 23:34:46 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.4-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.4 CB_SHA256=a9144e41fdb62dc872e09be617f69157f23568cc6e1d425e7adaf580aeba9adf CB_VERSION=6.0.4
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Tue, 01 Sep 2020 23:34:46 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Tue, 01 Sep 2020 23:34:47 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.4-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.4 CB_SHA256=a9144e41fdb62dc872e09be617f69157f23568cc6e1d425e7adaf580aeba9adf CB_VERSION=6.0.4
RUN chown -R couchbase:couchbase /etc/service
# Tue, 01 Sep 2020 23:34:47 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Tue, 01 Sep 2020 23:34:48 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.4-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.4 CB_SHA256=a9144e41fdb62dc872e09be617f69157f23568cc6e1d425e7adaf580aeba9adf CB_VERSION=6.0.4
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Tue, 01 Sep 2020 23:34:49 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.4-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.4 CB_SHA256=a9144e41fdb62dc872e09be617f69157f23568cc6e1d425e7adaf580aeba9adf CB_VERSION=6.0.4
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Tue, 01 Sep 2020 23:34:49 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Tue, 01 Sep 2020 23:34:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Sep 2020 23:34:49 GMT
CMD ["couchbase-server"]
# Tue, 01 Sep 2020 23:34:49 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Tue, 01 Sep 2020 23:34:50 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:8e097b52bfb8e743e52ccd2dfbd5a0363e48a00b06cdd3728a6fd4d1f3a34280`  
		Last Modified: Sat, 08 Aug 2020 13:20:06 GMT  
		Size: 44.4 MB (44447543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a613a9b4553ca86fac22546f2f79e2ff3d17d8d6aeea8b97d67862a5a40ad8ec`  
		Last Modified: Wed, 19 Aug 2020 21:17:23 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc000f015361df35e770a910ce03d30691e35aa10d52f4a4f432f183a6c03db`  
		Last Modified: Wed, 19 Aug 2020 21:17:23 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73eef93b7466c41f22f32d28aae5eb87e1ebc0c4d232c5f5e68c955d0e798dca`  
		Last Modified: Wed, 19 Aug 2020 21:17:23 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed412374d487b41f73700633b4b7184d1420ff0ca8d34b44626295803d5e1b9`  
		Last Modified: Tue, 01 Sep 2020 23:35:52 GMT  
		Size: 14.3 MB (14285573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ff1f5a91c8ad68f983399dc667d74cabea6f2ce50c190cb004ca32550dfa65`  
		Last Modified: Tue, 01 Sep 2020 23:35:49 GMT  
		Size: 2.1 KB (2076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae2b09bf9514ca09275c0113ed5f7c97773f3666dc3618871d4617e607e741f`  
		Last Modified: Tue, 01 Sep 2020 23:36:33 GMT  
		Size: 421.7 MB (421698090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9377f97ac7ca65a33aba19a1f5796cdcb0367d651b7e0cfb58a1a500d494f215`  
		Last Modified: Tue, 01 Sep 2020 23:35:49 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2736ec3e9bbadc2da1bbdfb0ddf21eda2e75eefd48ae47d5ae35552d27c31f`  
		Last Modified: Tue, 01 Sep 2020 23:35:48 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a04e5b70dfa3e5566212474aaaf5ab94319810cc21df200fe133f66423497c`  
		Last Modified: Tue, 01 Sep 2020 23:35:48 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54226246d8c2e372052b8089b3d9071cc5329ab17a182e23b69358a9eb97e1c`  
		Last Modified: Tue, 01 Sep 2020 23:35:48 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0829d410b9f1ef825f1c6212f438e078cf3ae4d72a421b0c83dc220bc9d2901f`  
		Last Modified: Tue, 01 Sep 2020 23:35:48 GMT  
		Size: 120.6 KB (120597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7eacb9151b439000178fbd3fb7f69dc3fd235f3ec7bcf8e06766bd0bafe6eb`  
		Last Modified: Tue, 01 Sep 2020 23:35:48 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

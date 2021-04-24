## `couchbase:community-7.0.0-beta`

```console
$ docker pull couchbase@sha256:51991eb3d0683c616ccd0f851a24824172932593416f293c60d2fc4994295fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:community-7.0.0-beta` - linux; amd64

```console
$ docker pull couchbase@sha256:d389e970f8bacc02b0b5c4dbbab9fbdd27a84196599f1d9cfa5eae1dbcf604ee
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.7 MB (431739527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbbe9e529f7d187a702a9c03daa9272ab84311b7084813a176795682cd720ea5`
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
# Fri, 23 Apr 2021 23:10:43 GMT
ARG CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb
# Fri, 23 Apr 2021 23:10:43 GMT
ARG CB_SHA256=51e843e9d2b5ef746353d79c044f17e4f9be0866673bd6fda01da27a0edf9fc9
# Fri, 23 Apr 2021 23:10:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Fri, 23 Apr 2021 23:10:44 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=51e843e9d2b5ef746353d79c044f17e4f9be0866673bd6fda01da27a0edf9fc9 CB_VERSION=7.0.0-beta
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Fri, 23 Apr 2021 23:11:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=51e843e9d2b5ef746353d79c044f17e4f9be0866673bd6fda01da27a0edf9fc9 CB_VERSION=7.0.0-beta
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Fri, 23 Apr 2021 23:11:34 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=51e843e9d2b5ef746353d79c044f17e4f9be0866673bd6fda01da27a0edf9fc9 CB_VERSION=7.0.0-beta
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt
# Fri, 23 Apr 2021 23:11:34 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Fri, 23 Apr 2021 23:11:35 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=51e843e9d2b5ef746353d79c044f17e4f9be0866673bd6fda01da27a0edf9fc9 CB_VERSION=7.0.0-beta
RUN chown -R couchbase:couchbase /etc/service
# Fri, 23 Apr 2021 23:11:35 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Fri, 23 Apr 2021 23:11:36 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=51e843e9d2b5ef746353d79c044f17e4f9be0866673bd6fda01da27a0edf9fc9 CB_VERSION=7.0.0-beta
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Fri, 23 Apr 2021 23:11:37 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_7.0.0-beta-ubuntu20.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/7.0.0-beta CB_SHA256=51e843e9d2b5ef746353d79c044f17e4f9be0866673bd6fda01da27a0edf9fc9 CB_VERSION=7.0.0-beta
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Fri, 23 Apr 2021 23:11:37 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Fri, 23 Apr 2021 23:11:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 23 Apr 2021 23:11:38 GMT
CMD ["couchbase-server"]
# Fri, 23 Apr 2021 23:11:38 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Fri, 23 Apr 2021 23:11:38 GMT
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
	-	`sha256:6aaf535e1b8ae8e167aa59f1f99c1ea96b069b1139cf31ac6e27afddbb36e1c5`  
		Last Modified: Fri, 23 Apr 2021 23:17:35 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2ba326669bc73839ea36011c6df730e90bcda0da455e533d5bf14722d2d261`  
		Last Modified: Fri, 23 Apr 2021 23:18:29 GMT  
		Size: 396.8 MB (396795514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ec5675dff9faa3dffd9bbbafd2d94e308538bbe6f3d04d4707b1dc12b75be5`  
		Last Modified: Fri, 23 Apr 2021 23:17:35 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f9927c81ac34e46e91d14609af80e96753debb02fdf9967c9640e089bbf51e`  
		Last Modified: Fri, 23 Apr 2021 23:17:34 GMT  
		Size: 479.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec646a7b3dfde0e85b7beffa9f477615d7536bcdef316ebcbd5aa48d203145f4`  
		Last Modified: Fri, 23 Apr 2021 23:17:32 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1e3a06ddb8fefd5811e61fdb4e4bd5ef4ffd37826ff249dd2df76c8b19af6c`  
		Last Modified: Fri, 23 Apr 2021 23:17:32 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e047066a24290ea4238d6aba5f68a7e26bdf452c21b933d96ff60fa498faa16f`  
		Last Modified: Fri, 23 Apr 2021 23:17:32 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05638d1a9bc19353cfb6339c4ef687baf8bde544aa01a9ec1eeeeda9c41e872`  
		Last Modified: Fri, 23 Apr 2021 23:17:32 GMT  
		Size: 125.9 KB (125882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8419ec211353eb04cf844121e7ca1527d77807ca3d3ee1b83ababbb4f860bc`  
		Last Modified: Fri, 23 Apr 2021 23:17:32 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

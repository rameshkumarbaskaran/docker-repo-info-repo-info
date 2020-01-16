<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchbase`

-	[`couchbase:6.0.3`](#couchbase603)
-	[`couchbase:6.5.0-beta2`](#couchbase650-beta2)
-	[`couchbase:community`](#couchbasecommunity)
-	[`couchbase:community-6.0.0`](#couchbasecommunity-600)
-	[`couchbase:enterprise`](#couchbaseenterprise)
-	[`couchbase:enterprise-6.0.3`](#couchbaseenterprise-603)
-	[`couchbase:latest`](#couchbaselatest)

## `couchbase:6.0.3`

```console
$ docker pull couchbase@sha256:9e28e17f28b2e115bdcb0cd145542f18db98c2885af990e043a888fca1d49892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:6.0.3` - linux; amd64

```console
$ docker pull couchbase@sha256:f4c4caf91cab4ccd2ef4f43c6ddd1c143e5974057f7a3d2c807ae0903e54bdd0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **479.0 MB (479023380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6629f63789eed50a8aa3e2bbdda0d7a15f9659a9680abe2cf2edd9f8ec57caee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 16 Jan 2020 01:21:30 GMT
ADD file:4b2eb5cd0b37ca0154f3c5ad9212f5bc7244a35806395a9c76a96723d708b83a in / 
# Thu, 16 Jan 2020 01:21:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 01:21:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 01:21:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 01:21:32 GMT
CMD ["/bin/bash"]
# Thu, 16 Jan 2020 02:26:53 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Thu, 16 Jan 2020 02:27:14 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 16 Jan 2020 02:27:14 GMT
ARG CB_VERSION=6.0.3
# Thu, 16 Jan 2020 02:27:15 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3
# Thu, 16 Jan 2020 02:27:15 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb
# Thu, 16 Jan 2020 02:27:15 GMT
ARG CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8
# Thu, 16 Jan 2020 02:27:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 16 Jan 2020 02:27:16 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 16 Jan 2020 02:28:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Thu, 16 Jan 2020 02:28:03 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 16 Jan 2020 02:28:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN chown -R couchbase:couchbase /etc/service
# Thu, 16 Jan 2020 02:28:04 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 16 Jan 2020 02:28:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 16 Jan 2020 02:28:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 16 Jan 2020 02:28:05 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 16 Jan 2020 02:28:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Jan 2020 02:28:06 GMT
CMD ["couchbase-server"]
# Thu, 16 Jan 2020 02:28:06 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 16 Jan 2020 02:28:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0a01a72a686c389637334de1e2d0012da298960366f6d8f358b8e10dc3b5e330`  
		Last Modified: Wed, 15 Jan 2020 14:20:15 GMT  
		Size: 44.1 MB (44149770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc899a5544da1a6cfb970d2484d32c063f8df26a430d92f39c98e72261e226f2`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 525.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19197c55075519928dd2ff059745665a2c9b72f4e8af6f7a1ce662e696d339bd`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716d454e56b61d1343a01f3b1829574333e2e3df20e77d1958d7b0b939ea1b61`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeec66b303ebcb9fe75ec3336e7da7db4b0366b6cec4396763eb6ec62deccd0`  
		Last Modified: Thu, 16 Jan 2020 02:30:37 GMT  
		Size: 14.3 MB (14330706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdef4dea7c07f6715c5f3bc6ba6c356e96909d6977c48e70b6f9b2c8af77b805`  
		Last Modified: Thu, 16 Jan 2020 02:30:34 GMT  
		Size: 2.1 KB (2071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1736c7202653bfa7ba6b479c3da2c57d6455183afbf43ba12e42534f660d6a01`  
		Last Modified: Thu, 16 Jan 2020 02:31:18 GMT  
		Size: 420.4 MB (420416570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e3c6b40104ce8c9b4f51a46b09d88bb35395e8f3d29bb864fc06d4fe9b0c45`  
		Last Modified: Thu, 16 Jan 2020 02:30:33 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c240d6ace0e6512a5f307e3b3aa44f2ec783ed04d15d24c322c405f6cb7bbf36`  
		Last Modified: Thu, 16 Jan 2020 02:30:33 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b11af0ba1fd574829476204952339f1b81e5d026d751c36c3232c3654e27a6b`  
		Last Modified: Thu, 16 Jan 2020 02:30:33 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c83c24e35f281fb810eb8e6a27d5dc31126473a4c4c7b3c8a4d1010d2f7a4c7`  
		Last Modified: Thu, 16 Jan 2020 02:30:32 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e766c5af12cd402c160656bb8d6fb123e8447c46d25e5b94946cb52a7b7f17f`  
		Last Modified: Thu, 16 Jan 2020 02:30:32 GMT  
		Size: 120.6 KB (120597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782017be5f839a893287bb39d3ed172a7febf92a9b671dc677c2042a49cf665b`  
		Last Modified: Thu, 16 Jan 2020 02:30:33 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:6.5.0-beta2`

```console
$ docker pull couchbase@sha256:045b9a88b620a929b5c2ced93cfc4e1da8daad0b375354b5c39f2c04df1825cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:6.5.0-beta2` - linux; amd64

```console
$ docker pull couchbase@sha256:7072122fb879e816a102bec3eb24635777a9217d1c669fc9fbc590b92229b5e6
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.8 MB (512785850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9594086a48b5ea122a16324f328f8230b91340c132523f784e5c5e10b9a6479e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 16 Jan 2020 01:21:30 GMT
ADD file:4b2eb5cd0b37ca0154f3c5ad9212f5bc7244a35806395a9c76a96723d708b83a in / 
# Thu, 16 Jan 2020 01:21:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 01:21:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 01:21:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 01:21:32 GMT
CMD ["/bin/bash"]
# Thu, 16 Jan 2020 02:26:53 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Thu, 16 Jan 2020 02:28:34 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 16 Jan 2020 02:28:36 GMT
ARG CB_VERSION=6.5.0-beta2
# Thu, 16 Jan 2020 02:28:38 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0-beta2
# Thu, 16 Jan 2020 02:28:39 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.5.0-beta2-ubuntu16.04_amd64.deb
# Thu, 16 Jan 2020 02:28:39 GMT
ARG CB_SHA256=08aba6dfbacc6d4a217996753d47c852ca24a4a628eb2b073538fe3a3c9ccbc4
# Thu, 16 Jan 2020 02:28:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 16 Jan 2020 02:28:40 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-beta2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0-beta2 CB_SHA256=08aba6dfbacc6d4a217996753d47c852ca24a4a628eb2b073538fe3a3c9ccbc4 CB_VERSION=6.5.0-beta2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 16 Jan 2020 02:29:30 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-beta2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0-beta2 CB_SHA256=08aba6dfbacc6d4a217996753d47c852ca24a4a628eb2b073538fe3a3c9ccbc4 CB_VERSION=6.5.0-beta2
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Thu, 16 Jan 2020 02:29:31 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 16 Jan 2020 02:29:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-beta2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0-beta2 CB_SHA256=08aba6dfbacc6d4a217996753d47c852ca24a4a628eb2b073538fe3a3c9ccbc4 CB_VERSION=6.5.0-beta2
RUN chown -R couchbase:couchbase /etc/service
# Thu, 16 Jan 2020 02:29:32 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 16 Jan 2020 02:29:32 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-beta2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0-beta2 CB_SHA256=08aba6dfbacc6d4a217996753d47c852ca24a4a628eb2b073538fe3a3c9ccbc4 CB_VERSION=6.5.0-beta2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 16 Jan 2020 02:29:33 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-beta2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0-beta2 CB_SHA256=08aba6dfbacc6d4a217996753d47c852ca24a4a628eb2b073538fe3a3c9ccbc4 CB_VERSION=6.5.0-beta2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 16 Jan 2020 02:29:33 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 16 Jan 2020 02:29:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Jan 2020 02:29:34 GMT
CMD ["couchbase-server"]
# Thu, 16 Jan 2020 02:29:34 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 16 Jan 2020 02:29:34 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0a01a72a686c389637334de1e2d0012da298960366f6d8f358b8e10dc3b5e330`  
		Last Modified: Wed, 15 Jan 2020 14:20:15 GMT  
		Size: 44.1 MB (44149770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc899a5544da1a6cfb970d2484d32c063f8df26a430d92f39c98e72261e226f2`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 525.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19197c55075519928dd2ff059745665a2c9b72f4e8af6f7a1ce662e696d339bd`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716d454e56b61d1343a01f3b1829574333e2e3df20e77d1958d7b0b939ea1b61`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aaff9de0846739478518c7d79a7974ad65cdf813b6c0e4c54cf6eba9e5b1579`  
		Last Modified: Thu, 16 Jan 2020 02:31:37 GMT  
		Size: 5.9 MB (5853476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fb630e548dc498590e404466ad91066ebeb120f4e51c8bdf683e6ebc7c623f`  
		Last Modified: Thu, 16 Jan 2020 02:31:35 GMT  
		Size: 2.1 KB (2071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d913121cbb05b9e3d20ec1b42364fce05ec8550e766495a9a9a66daa95fa8668`  
		Last Modified: Thu, 16 Jan 2020 02:32:34 GMT  
		Size: 462.7 MB (462653204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c452aa5dd01d037bda87a275d8f7e32eb2c07f46322ef24c0cbf7fed38dc92b8`  
		Last Modified: Thu, 16 Jan 2020 02:31:35 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31dd9a03f4a5b4c1b48cccfcb389cc32a5d1d3d848c36339c441e58b862f9dac`  
		Last Modified: Thu, 16 Jan 2020 02:31:34 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2ad2478fac1830efd35a36e5c44c05ad5baf5b012e680b5bb0f912e7d77324`  
		Last Modified: Thu, 16 Jan 2020 02:31:34 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18eead3a89623f125dd81ccda204e5c4d6103975b44f638d9fd7ceaf57e8c870`  
		Last Modified: Thu, 16 Jan 2020 02:31:34 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc15d6a7a84af2176e5b134d1ed3b921c0343c1542cb4b02547f445b2d107c7`  
		Last Modified: Thu, 16 Jan 2020 02:31:35 GMT  
		Size: 123.7 KB (123664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8353a22ea4e8f6dc251cefee5dfbb2ec4fec8d1aad2c81c0c044c6519367f46c`  
		Last Modified: Thu, 16 Jan 2020 02:31:34 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community`

```console
$ docker pull couchbase@sha256:01377fa1847a7b3e0dabd5e50bffdc083e13fb8c7d2875c05e5f138634b528dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:community` - linux; amd64

```console
$ docker pull couchbase@sha256:2448438d8d3fc84ddd2afcdc43532f3e5a9d68e4b4f8f8db7bfeb64f41c59d5c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.5 MB (199494718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a430fc33753ba4282cac9a859e6bde079622ad021b4669b4adc79300ae8b55`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 16 Jan 2020 01:21:30 GMT
ADD file:4b2eb5cd0b37ca0154f3c5ad9212f5bc7244a35806395a9c76a96723d708b83a in / 
# Thu, 16 Jan 2020 01:21:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 01:21:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 01:21:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 01:21:32 GMT
CMD ["/bin/bash"]
# Thu, 16 Jan 2020 02:26:53 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Thu, 16 Jan 2020 02:27:14 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 16 Jan 2020 02:29:50 GMT
ARG CB_VERSION=6.0.0
# Thu, 16 Jan 2020 02:29:50 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0
# Thu, 16 Jan 2020 02:29:51 GMT
ARG CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb
# Thu, 16 Jan 2020 02:29:51 GMT
ARG CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece
# Thu, 16 Jan 2020 02:29:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 16 Jan 2020 02:29:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0 CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece CB_VERSION=6.0.0
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 16 Jan 2020 02:30:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0 CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece CB_VERSION=6.0.0
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Thu, 16 Jan 2020 02:30:18 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 16 Jan 2020 02:30:18 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0 CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece CB_VERSION=6.0.0
RUN chown -R couchbase:couchbase /etc/service
# Thu, 16 Jan 2020 02:30:19 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 16 Jan 2020 02:30:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0 CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece CB_VERSION=6.0.0
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 16 Jan 2020 02:30:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0 CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece CB_VERSION=6.0.0
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 16 Jan 2020 02:30:20 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 16 Jan 2020 02:30:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Jan 2020 02:30:20 GMT
CMD ["couchbase-server"]
# Thu, 16 Jan 2020 02:30:21 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 16 Jan 2020 02:30:21 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0a01a72a686c389637334de1e2d0012da298960366f6d8f358b8e10dc3b5e330`  
		Last Modified: Wed, 15 Jan 2020 14:20:15 GMT  
		Size: 44.1 MB (44149770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc899a5544da1a6cfb970d2484d32c063f8df26a430d92f39c98e72261e226f2`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 525.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19197c55075519928dd2ff059745665a2c9b72f4e8af6f7a1ce662e696d339bd`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716d454e56b61d1343a01f3b1829574333e2e3df20e77d1958d7b0b939ea1b61`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeec66b303ebcb9fe75ec3336e7da7db4b0366b6cec4396763eb6ec62deccd0`  
		Last Modified: Thu, 16 Jan 2020 02:30:37 GMT  
		Size: 14.3 MB (14330706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176f254ee9345fe905c7c1e5562f594d72666ebd2d1a15af046844aa8b0b54f7`  
		Last Modified: Thu, 16 Jan 2020 02:32:43 GMT  
		Size: 2.1 KB (2071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7c5aadb92a4f0eeda90ea89dacc92d7f523f1ed2544b4941d6f5a21d43f3fe`  
		Last Modified: Thu, 16 Jan 2020 02:33:04 GMT  
		Size: 140.9 MB (140887902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dffe3ed519790446d585636242e63c3eaed51f124d3dd46b4fcee21ce3f4ba6`  
		Last Modified: Thu, 16 Jan 2020 02:32:43 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1a3fbc445e8ed7306ba880bb7ada8e643e8bfd5f262781ef855dcbf153e892`  
		Last Modified: Thu, 16 Jan 2020 02:32:42 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a62305360ab2f2ee6ceec3989862d5c35914bc3f93113e30d7eb1636a666c6`  
		Last Modified: Thu, 16 Jan 2020 02:32:42 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f2322ac66384f08096647dbce267635153c869817ba8163be9f408d8dbb3e2`  
		Last Modified: Thu, 16 Jan 2020 02:32:41 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4abb7d11767aadd9e37de33a30014ae125c7f61fceede7a992c1236e072e4874`  
		Last Modified: Thu, 16 Jan 2020 02:32:42 GMT  
		Size: 120.6 KB (120598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcb9628b331895f85788deb5a107441a312adf2b8303b01cae2c90d527533d6`  
		Last Modified: Thu, 16 Jan 2020 02:32:42 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-6.0.0`

```console
$ docker pull couchbase@sha256:01377fa1847a7b3e0dabd5e50bffdc083e13fb8c7d2875c05e5f138634b528dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:community-6.0.0` - linux; amd64

```console
$ docker pull couchbase@sha256:2448438d8d3fc84ddd2afcdc43532f3e5a9d68e4b4f8f8db7bfeb64f41c59d5c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.5 MB (199494718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a430fc33753ba4282cac9a859e6bde079622ad021b4669b4adc79300ae8b55`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 16 Jan 2020 01:21:30 GMT
ADD file:4b2eb5cd0b37ca0154f3c5ad9212f5bc7244a35806395a9c76a96723d708b83a in / 
# Thu, 16 Jan 2020 01:21:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 01:21:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 01:21:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 01:21:32 GMT
CMD ["/bin/bash"]
# Thu, 16 Jan 2020 02:26:53 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Thu, 16 Jan 2020 02:27:14 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 16 Jan 2020 02:29:50 GMT
ARG CB_VERSION=6.0.0
# Thu, 16 Jan 2020 02:29:50 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0
# Thu, 16 Jan 2020 02:29:51 GMT
ARG CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb
# Thu, 16 Jan 2020 02:29:51 GMT
ARG CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece
# Thu, 16 Jan 2020 02:29:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 16 Jan 2020 02:29:52 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0 CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece CB_VERSION=6.0.0
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 16 Jan 2020 02:30:17 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0 CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece CB_VERSION=6.0.0
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Thu, 16 Jan 2020 02:30:18 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 16 Jan 2020 02:30:18 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0 CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece CB_VERSION=6.0.0
RUN chown -R couchbase:couchbase /etc/service
# Thu, 16 Jan 2020 02:30:19 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 16 Jan 2020 02:30:19 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0 CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece CB_VERSION=6.0.0
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 16 Jan 2020 02:30:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0 CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece CB_VERSION=6.0.0
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 16 Jan 2020 02:30:20 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 16 Jan 2020 02:30:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Jan 2020 02:30:20 GMT
CMD ["couchbase-server"]
# Thu, 16 Jan 2020 02:30:21 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 16 Jan 2020 02:30:21 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0a01a72a686c389637334de1e2d0012da298960366f6d8f358b8e10dc3b5e330`  
		Last Modified: Wed, 15 Jan 2020 14:20:15 GMT  
		Size: 44.1 MB (44149770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc899a5544da1a6cfb970d2484d32c063f8df26a430d92f39c98e72261e226f2`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 525.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19197c55075519928dd2ff059745665a2c9b72f4e8af6f7a1ce662e696d339bd`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716d454e56b61d1343a01f3b1829574333e2e3df20e77d1958d7b0b939ea1b61`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeec66b303ebcb9fe75ec3336e7da7db4b0366b6cec4396763eb6ec62deccd0`  
		Last Modified: Thu, 16 Jan 2020 02:30:37 GMT  
		Size: 14.3 MB (14330706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176f254ee9345fe905c7c1e5562f594d72666ebd2d1a15af046844aa8b0b54f7`  
		Last Modified: Thu, 16 Jan 2020 02:32:43 GMT  
		Size: 2.1 KB (2071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7c5aadb92a4f0eeda90ea89dacc92d7f523f1ed2544b4941d6f5a21d43f3fe`  
		Last Modified: Thu, 16 Jan 2020 02:33:04 GMT  
		Size: 140.9 MB (140887902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dffe3ed519790446d585636242e63c3eaed51f124d3dd46b4fcee21ce3f4ba6`  
		Last Modified: Thu, 16 Jan 2020 02:32:43 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1a3fbc445e8ed7306ba880bb7ada8e643e8bfd5f262781ef855dcbf153e892`  
		Last Modified: Thu, 16 Jan 2020 02:32:42 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a62305360ab2f2ee6ceec3989862d5c35914bc3f93113e30d7eb1636a666c6`  
		Last Modified: Thu, 16 Jan 2020 02:32:42 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f2322ac66384f08096647dbce267635153c869817ba8163be9f408d8dbb3e2`  
		Last Modified: Thu, 16 Jan 2020 02:32:41 GMT  
		Size: 216.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4abb7d11767aadd9e37de33a30014ae125c7f61fceede7a992c1236e072e4874`  
		Last Modified: Thu, 16 Jan 2020 02:32:42 GMT  
		Size: 120.6 KB (120598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcb9628b331895f85788deb5a107441a312adf2b8303b01cae2c90d527533d6`  
		Last Modified: Thu, 16 Jan 2020 02:32:42 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise`

```console
$ docker pull couchbase@sha256:9e28e17f28b2e115bdcb0cd145542f18db98c2885af990e043a888fca1d49892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise` - linux; amd64

```console
$ docker pull couchbase@sha256:f4c4caf91cab4ccd2ef4f43c6ddd1c143e5974057f7a3d2c807ae0903e54bdd0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **479.0 MB (479023380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6629f63789eed50a8aa3e2bbdda0d7a15f9659a9680abe2cf2edd9f8ec57caee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 16 Jan 2020 01:21:30 GMT
ADD file:4b2eb5cd0b37ca0154f3c5ad9212f5bc7244a35806395a9c76a96723d708b83a in / 
# Thu, 16 Jan 2020 01:21:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 01:21:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 01:21:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 01:21:32 GMT
CMD ["/bin/bash"]
# Thu, 16 Jan 2020 02:26:53 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Thu, 16 Jan 2020 02:27:14 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 16 Jan 2020 02:27:14 GMT
ARG CB_VERSION=6.0.3
# Thu, 16 Jan 2020 02:27:15 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3
# Thu, 16 Jan 2020 02:27:15 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb
# Thu, 16 Jan 2020 02:27:15 GMT
ARG CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8
# Thu, 16 Jan 2020 02:27:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 16 Jan 2020 02:27:16 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 16 Jan 2020 02:28:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Thu, 16 Jan 2020 02:28:03 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 16 Jan 2020 02:28:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN chown -R couchbase:couchbase /etc/service
# Thu, 16 Jan 2020 02:28:04 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 16 Jan 2020 02:28:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 16 Jan 2020 02:28:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 16 Jan 2020 02:28:05 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 16 Jan 2020 02:28:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Jan 2020 02:28:06 GMT
CMD ["couchbase-server"]
# Thu, 16 Jan 2020 02:28:06 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 16 Jan 2020 02:28:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0a01a72a686c389637334de1e2d0012da298960366f6d8f358b8e10dc3b5e330`  
		Last Modified: Wed, 15 Jan 2020 14:20:15 GMT  
		Size: 44.1 MB (44149770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc899a5544da1a6cfb970d2484d32c063f8df26a430d92f39c98e72261e226f2`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 525.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19197c55075519928dd2ff059745665a2c9b72f4e8af6f7a1ce662e696d339bd`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716d454e56b61d1343a01f3b1829574333e2e3df20e77d1958d7b0b939ea1b61`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeec66b303ebcb9fe75ec3336e7da7db4b0366b6cec4396763eb6ec62deccd0`  
		Last Modified: Thu, 16 Jan 2020 02:30:37 GMT  
		Size: 14.3 MB (14330706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdef4dea7c07f6715c5f3bc6ba6c356e96909d6977c48e70b6f9b2c8af77b805`  
		Last Modified: Thu, 16 Jan 2020 02:30:34 GMT  
		Size: 2.1 KB (2071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1736c7202653bfa7ba6b479c3da2c57d6455183afbf43ba12e42534f660d6a01`  
		Last Modified: Thu, 16 Jan 2020 02:31:18 GMT  
		Size: 420.4 MB (420416570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e3c6b40104ce8c9b4f51a46b09d88bb35395e8f3d29bb864fc06d4fe9b0c45`  
		Last Modified: Thu, 16 Jan 2020 02:30:33 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c240d6ace0e6512a5f307e3b3aa44f2ec783ed04d15d24c322c405f6cb7bbf36`  
		Last Modified: Thu, 16 Jan 2020 02:30:33 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b11af0ba1fd574829476204952339f1b81e5d026d751c36c3232c3654e27a6b`  
		Last Modified: Thu, 16 Jan 2020 02:30:33 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c83c24e35f281fb810eb8e6a27d5dc31126473a4c4c7b3c8a4d1010d2f7a4c7`  
		Last Modified: Thu, 16 Jan 2020 02:30:32 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e766c5af12cd402c160656bb8d6fb123e8447c46d25e5b94946cb52a7b7f17f`  
		Last Modified: Thu, 16 Jan 2020 02:30:32 GMT  
		Size: 120.6 KB (120597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782017be5f839a893287bb39d3ed172a7febf92a9b671dc677c2042a49cf665b`  
		Last Modified: Thu, 16 Jan 2020 02:30:33 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-6.0.3`

```console
$ docker pull couchbase@sha256:9e28e17f28b2e115bdcb0cd145542f18db98c2885af990e043a888fca1d49892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.0.3` - linux; amd64

```console
$ docker pull couchbase@sha256:f4c4caf91cab4ccd2ef4f43c6ddd1c143e5974057f7a3d2c807ae0903e54bdd0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **479.0 MB (479023380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6629f63789eed50a8aa3e2bbdda0d7a15f9659a9680abe2cf2edd9f8ec57caee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 16 Jan 2020 01:21:30 GMT
ADD file:4b2eb5cd0b37ca0154f3c5ad9212f5bc7244a35806395a9c76a96723d708b83a in / 
# Thu, 16 Jan 2020 01:21:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 01:21:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 01:21:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 01:21:32 GMT
CMD ["/bin/bash"]
# Thu, 16 Jan 2020 02:26:53 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Thu, 16 Jan 2020 02:27:14 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 16 Jan 2020 02:27:14 GMT
ARG CB_VERSION=6.0.3
# Thu, 16 Jan 2020 02:27:15 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3
# Thu, 16 Jan 2020 02:27:15 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb
# Thu, 16 Jan 2020 02:27:15 GMT
ARG CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8
# Thu, 16 Jan 2020 02:27:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 16 Jan 2020 02:27:16 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 16 Jan 2020 02:28:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Thu, 16 Jan 2020 02:28:03 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 16 Jan 2020 02:28:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN chown -R couchbase:couchbase /etc/service
# Thu, 16 Jan 2020 02:28:04 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 16 Jan 2020 02:28:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 16 Jan 2020 02:28:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 16 Jan 2020 02:28:05 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 16 Jan 2020 02:28:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Jan 2020 02:28:06 GMT
CMD ["couchbase-server"]
# Thu, 16 Jan 2020 02:28:06 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 16 Jan 2020 02:28:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0a01a72a686c389637334de1e2d0012da298960366f6d8f358b8e10dc3b5e330`  
		Last Modified: Wed, 15 Jan 2020 14:20:15 GMT  
		Size: 44.1 MB (44149770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc899a5544da1a6cfb970d2484d32c063f8df26a430d92f39c98e72261e226f2`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 525.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19197c55075519928dd2ff059745665a2c9b72f4e8af6f7a1ce662e696d339bd`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716d454e56b61d1343a01f3b1829574333e2e3df20e77d1958d7b0b939ea1b61`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeec66b303ebcb9fe75ec3336e7da7db4b0366b6cec4396763eb6ec62deccd0`  
		Last Modified: Thu, 16 Jan 2020 02:30:37 GMT  
		Size: 14.3 MB (14330706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdef4dea7c07f6715c5f3bc6ba6c356e96909d6977c48e70b6f9b2c8af77b805`  
		Last Modified: Thu, 16 Jan 2020 02:30:34 GMT  
		Size: 2.1 KB (2071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1736c7202653bfa7ba6b479c3da2c57d6455183afbf43ba12e42534f660d6a01`  
		Last Modified: Thu, 16 Jan 2020 02:31:18 GMT  
		Size: 420.4 MB (420416570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e3c6b40104ce8c9b4f51a46b09d88bb35395e8f3d29bb864fc06d4fe9b0c45`  
		Last Modified: Thu, 16 Jan 2020 02:30:33 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c240d6ace0e6512a5f307e3b3aa44f2ec783ed04d15d24c322c405f6cb7bbf36`  
		Last Modified: Thu, 16 Jan 2020 02:30:33 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b11af0ba1fd574829476204952339f1b81e5d026d751c36c3232c3654e27a6b`  
		Last Modified: Thu, 16 Jan 2020 02:30:33 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c83c24e35f281fb810eb8e6a27d5dc31126473a4c4c7b3c8a4d1010d2f7a4c7`  
		Last Modified: Thu, 16 Jan 2020 02:30:32 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e766c5af12cd402c160656bb8d6fb123e8447c46d25e5b94946cb52a7b7f17f`  
		Last Modified: Thu, 16 Jan 2020 02:30:32 GMT  
		Size: 120.6 KB (120597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782017be5f839a893287bb39d3ed172a7febf92a9b671dc677c2042a49cf665b`  
		Last Modified: Thu, 16 Jan 2020 02:30:33 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:latest`

```console
$ docker pull couchbase@sha256:9e28e17f28b2e115bdcb0cd145542f18db98c2885af990e043a888fca1d49892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:latest` - linux; amd64

```console
$ docker pull couchbase@sha256:f4c4caf91cab4ccd2ef4f43c6ddd1c143e5974057f7a3d2c807ae0903e54bdd0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **479.0 MB (479023380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6629f63789eed50a8aa3e2bbdda0d7a15f9659a9680abe2cf2edd9f8ec57caee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 16 Jan 2020 01:21:30 GMT
ADD file:4b2eb5cd0b37ca0154f3c5ad9212f5bc7244a35806395a9c76a96723d708b83a in / 
# Thu, 16 Jan 2020 01:21:31 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 16 Jan 2020 01:21:31 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 16 Jan 2020 01:21:32 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 16 Jan 2020 01:21:32 GMT
CMD ["/bin/bash"]
# Thu, 16 Jan 2020 02:26:53 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Thu, 16 Jan 2020 02:27:14 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 16 Jan 2020 02:27:14 GMT
ARG CB_VERSION=6.0.3
# Thu, 16 Jan 2020 02:27:15 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3
# Thu, 16 Jan 2020 02:27:15 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb
# Thu, 16 Jan 2020 02:27:15 GMT
ARG CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8
# Thu, 16 Jan 2020 02:27:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 16 Jan 2020 02:27:16 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 16 Jan 2020 02:28:02 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Thu, 16 Jan 2020 02:28:03 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 16 Jan 2020 02:28:03 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN chown -R couchbase:couchbase /etc/service
# Thu, 16 Jan 2020 02:28:04 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 16 Jan 2020 02:28:04 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 16 Jan 2020 02:28:05 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 16 Jan 2020 02:28:05 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 16 Jan 2020 02:28:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Jan 2020 02:28:06 GMT
CMD ["couchbase-server"]
# Thu, 16 Jan 2020 02:28:06 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 16 Jan 2020 02:28:06 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:0a01a72a686c389637334de1e2d0012da298960366f6d8f358b8e10dc3b5e330`  
		Last Modified: Wed, 15 Jan 2020 14:20:15 GMT  
		Size: 44.1 MB (44149770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc899a5544da1a6cfb970d2484d32c063f8df26a430d92f39c98e72261e226f2`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 525.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19197c55075519928dd2ff059745665a2c9b72f4e8af6f7a1ce662e696d339bd`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716d454e56b61d1343a01f3b1829574333e2e3df20e77d1958d7b0b939ea1b61`  
		Last Modified: Thu, 16 Jan 2020 01:22:24 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daeec66b303ebcb9fe75ec3336e7da7db4b0366b6cec4396763eb6ec62deccd0`  
		Last Modified: Thu, 16 Jan 2020 02:30:37 GMT  
		Size: 14.3 MB (14330706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdef4dea7c07f6715c5f3bc6ba6c356e96909d6977c48e70b6f9b2c8af77b805`  
		Last Modified: Thu, 16 Jan 2020 02:30:34 GMT  
		Size: 2.1 KB (2071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1736c7202653bfa7ba6b479c3da2c57d6455183afbf43ba12e42534f660d6a01`  
		Last Modified: Thu, 16 Jan 2020 02:31:18 GMT  
		Size: 420.4 MB (420416570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e3c6b40104ce8c9b4f51a46b09d88bb35395e8f3d29bb864fc06d4fe9b0c45`  
		Last Modified: Thu, 16 Jan 2020 02:30:33 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c240d6ace0e6512a5f307e3b3aa44f2ec783ed04d15d24c322c405f6cb7bbf36`  
		Last Modified: Thu, 16 Jan 2020 02:30:33 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b11af0ba1fd574829476204952339f1b81e5d026d751c36c3232c3654e27a6b`  
		Last Modified: Thu, 16 Jan 2020 02:30:33 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c83c24e35f281fb810eb8e6a27d5dc31126473a4c4c7b3c8a4d1010d2f7a4c7`  
		Last Modified: Thu, 16 Jan 2020 02:30:32 GMT  
		Size: 218.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e766c5af12cd402c160656bb8d6fb123e8447c46d25e5b94946cb52a7b7f17f`  
		Last Modified: Thu, 16 Jan 2020 02:30:32 GMT  
		Size: 120.6 KB (120597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782017be5f839a893287bb39d3ed172a7febf92a9b671dc677c2042a49cf665b`  
		Last Modified: Thu, 16 Jan 2020 02:30:33 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

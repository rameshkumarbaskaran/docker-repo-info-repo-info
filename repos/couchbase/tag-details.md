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
$ docker pull couchbase@sha256:dbe7ed71c3cff6a867cb40a350874469a8bf9b233a8f71c7b55244d184df9fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:6.0.3` - linux; amd64

```console
$ docker pull couchbase@sha256:4899eafc51a3e568e44fee276f5d7a640d1e719db01c12613427cfca6a7375f8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **479.0 MB (478997039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4deec10b265ebab6e829fe139078ee212977c3b7803716b30827e84507ebafbc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 19 Dec 2019 04:24:35 GMT
ADD file:f0b8eaa718bc3965b1e8395f5a6bea97c16651b50614e676bb3eaf31335a0045 in / 
# Thu, 19 Dec 2019 04:24:36 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 04:24:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:24:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:24:38 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:36:40 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Thu, 19 Dec 2019 06:37:19 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 19 Dec 2019 06:37:19 GMT
ARG CB_VERSION=6.0.3
# Thu, 19 Dec 2019 06:37:19 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3
# Thu, 19 Dec 2019 06:37:20 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb
# Thu, 19 Dec 2019 06:37:20 GMT
ARG CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8
# Thu, 19 Dec 2019 06:37:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 19 Dec 2019 06:37:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 19 Dec 2019 06:38:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Thu, 19 Dec 2019 06:38:13 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 19 Dec 2019 06:38:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN chown -R couchbase:couchbase /etc/service
# Thu, 19 Dec 2019 06:38:14 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 19 Dec 2019 06:38:15 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 19 Dec 2019 06:38:16 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 19 Dec 2019 06:38:16 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 19 Dec 2019 06:38:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Dec 2019 06:38:16 GMT
CMD ["couchbase-server"]
# Thu, 19 Dec 2019 06:38:16 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 19 Dec 2019 06:38:17 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:3386e6af03b043219225367632569465e5ecd47391d1f99a6d265e51bd463a83`  
		Last Modified: Thu, 12 Dec 2019 08:26:09 GMT  
		Size: 44.1 MB (44123254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ac0bbe6c8eeb959337b336ceaa5c3bbbae81e316025f9b94ede453540f2377`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1983a67e104e801fceb1850a375a71fe6b62636ba7a8403d9644f308a6a43f9`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0f3a523f04f61db942018321ae122f90d8e3303e243b005e8de9817daf7028`  
		Last Modified: Thu, 19 Dec 2019 04:25:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35cfbf2546f178acf65d54d00dea29c862a5aa1e13db5369ec2d40b471b6c54`  
		Last Modified: Thu, 19 Dec 2019 06:40:40 GMT  
		Size: 14.3 MB (14330783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccb057f4f3b006d1acc62ebfac34a161ecfb751d60d09392aae4c4c31e11551`  
		Last Modified: Thu, 19 Dec 2019 06:40:36 GMT  
		Size: 2.1 KB (2071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a73461e5e6fe075cfd4e3c2146911d543a051de1e03972ac7af476c0b93e41`  
		Last Modified: Thu, 19 Dec 2019 06:41:28 GMT  
		Size: 420.4 MB (420416653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982e4a808750196401527726d5b02c65f5380e9a6fbc20c50823f1f7c0498d45`  
		Last Modified: Thu, 19 Dec 2019 06:40:37 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b3d5ad6cd54004abaf14f21970fee97d6c4a68ffd92412650dab502b1358ae`  
		Last Modified: Thu, 19 Dec 2019 06:40:36 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b533d3803f7eaa89db560da41f0ac0fb805850ae1f24b959cd8811f9c1b77e6`  
		Last Modified: Thu, 19 Dec 2019 06:40:35 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae0dc830f7f9da77305035bec6c8ade79f6fe2f3ee27850e7b3953357a66bf9`  
		Last Modified: Thu, 19 Dec 2019 06:40:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9291ed8137ecc9a6cd8baa42c18b06c3c77c7fd7fda4bbb2bf04b514a4a70956`  
		Last Modified: Thu, 19 Dec 2019 06:40:35 GMT  
		Size: 120.6 KB (120597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6ceac673a197a02dedf6d6b48ec70174e2a03a700d309a3d536381dae7dace`  
		Last Modified: Thu, 19 Dec 2019 06:40:35 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:6.5.0-beta2`

```console
$ docker pull couchbase@sha256:8f68cfb612ec120c2f4dde63e8758b1eb141f7ad55caf8866228c53b40b6b1de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:6.5.0-beta2` - linux; amd64

```console
$ docker pull couchbase@sha256:9e03bbf9f23275a0541f90e87d76ee55f4af595442f2123b25292062901d47d8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **512.8 MB (512759075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35dcdee8c18c9d9b82fb29627f7370ccfd8dbbc28ff23a5ba04c805a8ff87fcc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 19 Dec 2019 04:24:35 GMT
ADD file:f0b8eaa718bc3965b1e8395f5a6bea97c16651b50614e676bb3eaf31335a0045 in / 
# Thu, 19 Dec 2019 04:24:36 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 04:24:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:24:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:24:38 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:36:40 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Thu, 19 Dec 2019 06:38:36 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl bzip2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 19 Dec 2019 06:38:37 GMT
ARG CB_VERSION=6.5.0-beta2
# Thu, 19 Dec 2019 06:38:37 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0-beta2
# Thu, 19 Dec 2019 06:38:37 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.5.0-beta2-ubuntu16.04_amd64.deb
# Thu, 19 Dec 2019 06:38:37 GMT
ARG CB_SHA256=08aba6dfbacc6d4a217996753d47c852ca24a4a628eb2b073538fe3a3c9ccbc4
# Thu, 19 Dec 2019 06:38:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 19 Dec 2019 06:38:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-beta2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0-beta2 CB_SHA256=08aba6dfbacc6d4a217996753d47c852ca24a4a628eb2b073538fe3a3c9ccbc4 CB_VERSION=6.5.0-beta2
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 19 Dec 2019 06:39:37 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-beta2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0-beta2 CB_SHA256=08aba6dfbacc6d4a217996753d47c852ca24a4a628eb2b073538fe3a3c9ccbc4 CB_VERSION=6.5.0-beta2
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Thu, 19 Dec 2019 06:39:37 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 19 Dec 2019 06:39:38 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-beta2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0-beta2 CB_SHA256=08aba6dfbacc6d4a217996753d47c852ca24a4a628eb2b073538fe3a3c9ccbc4 CB_VERSION=6.5.0-beta2
RUN chown -R couchbase:couchbase /etc/service
# Thu, 19 Dec 2019 06:39:39 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 19 Dec 2019 06:39:40 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-beta2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0-beta2 CB_SHA256=08aba6dfbacc6d4a217996753d47c852ca24a4a628eb2b073538fe3a3c9ccbc4 CB_VERSION=6.5.0-beta2
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 19 Dec 2019 06:39:41 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.5.0-beta2-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.5.0-beta2 CB_SHA256=08aba6dfbacc6d4a217996753d47c852ca24a4a628eb2b073538fe3a3c9ccbc4 CB_VERSION=6.5.0-beta2
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 19 Dec 2019 06:39:41 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 19 Dec 2019 06:39:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Dec 2019 06:39:41 GMT
CMD ["couchbase-server"]
# Thu, 19 Dec 2019 06:39:41 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 19 Dec 2019 06:39:42 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:3386e6af03b043219225367632569465e5ecd47391d1f99a6d265e51bd463a83`  
		Last Modified: Thu, 12 Dec 2019 08:26:09 GMT  
		Size: 44.1 MB (44123254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ac0bbe6c8eeb959337b336ceaa5c3bbbae81e316025f9b94ede453540f2377`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1983a67e104e801fceb1850a375a71fe6b62636ba7a8403d9644f308a6a43f9`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0f3a523f04f61db942018321ae122f90d8e3303e243b005e8de9817daf7028`  
		Last Modified: Thu, 19 Dec 2019 04:25:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d9de4d8a960826ad75e787f2d532b2390058005a0a957ba52ad5feeaaeef70`  
		Last Modified: Thu, 19 Dec 2019 06:41:36 GMT  
		Size: 5.9 MB (5853602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0727910867fb909efe0c387b6d71209c92624a95402ea6efa87ce9ae2f9b4b74`  
		Last Modified: Thu, 19 Dec 2019 06:41:35 GMT  
		Size: 2.1 KB (2074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2851a9b086680a19ba1a21c9fcca5cde2e2d82adbdb4eddef8a335916a1476f9`  
		Last Modified: Thu, 19 Dec 2019 06:42:42 GMT  
		Size: 462.7 MB (462652800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2fb2acc53c21cb2dd642e4791199fe4fd43c9ea53bead4bd1e52eebd7bc2e70`  
		Last Modified: Thu, 19 Dec 2019 06:41:35 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a1a0163c88fb3819b2df1b6bb6ba694653efe14f2a16a0b44ca5ab412de8b6`  
		Last Modified: Thu, 19 Dec 2019 06:41:34 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4569b941f3b2f9e7ee7701449097785e302afe1bdc62ee87c5824f894f4db3bf`  
		Last Modified: Thu, 19 Dec 2019 06:41:34 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c874d73ed5d7cd9a95c1ba870ac29252c7901403331cf2eccb80004eecd025e`  
		Last Modified: Thu, 19 Dec 2019 06:41:34 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f14a9ebe56cc0b4197e9bed29ac74060200e033c5be17b7594557ebcbc3050a`  
		Last Modified: Thu, 19 Dec 2019 06:41:34 GMT  
		Size: 123.7 KB (123664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7175fed4da05b3246041b81da833cfb2299fa684b3cc7e379027885d4e739d58`  
		Last Modified: Thu, 19 Dec 2019 06:41:34 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community`

```console
$ docker pull couchbase@sha256:ef03c8abc25a8fbc08c00a94acc73f6263124be33a482d5891790a1918b4503c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:community` - linux; amd64

```console
$ docker pull couchbase@sha256:117bb5abd494c81652affce51e6637a624db687fe85f471ea3f80f4b726331cd
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.5 MB (199468336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e508feb8c5fde2d369cf5c0509f83ec3401c09ba7b32f7b18c0b7501d6a87485`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 19 Dec 2019 04:24:35 GMT
ADD file:f0b8eaa718bc3965b1e8395f5a6bea97c16651b50614e676bb3eaf31335a0045 in / 
# Thu, 19 Dec 2019 04:24:36 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 04:24:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:24:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:24:38 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:36:40 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Thu, 19 Dec 2019 06:37:19 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 19 Dec 2019 06:39:53 GMT
ARG CB_VERSION=6.0.0
# Thu, 19 Dec 2019 06:39:53 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0
# Thu, 19 Dec 2019 06:39:53 GMT
ARG CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb
# Thu, 19 Dec 2019 06:39:53 GMT
ARG CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece
# Thu, 19 Dec 2019 06:39:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 19 Dec 2019 06:39:54 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0 CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece CB_VERSION=6.0.0
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 19 Dec 2019 06:40:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0 CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece CB_VERSION=6.0.0
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Thu, 19 Dec 2019 06:40:20 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 19 Dec 2019 06:40:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0 CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece CB_VERSION=6.0.0
RUN chown -R couchbase:couchbase /etc/service
# Thu, 19 Dec 2019 06:40:21 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 19 Dec 2019 06:40:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0 CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece CB_VERSION=6.0.0
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 19 Dec 2019 06:40:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0 CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece CB_VERSION=6.0.0
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 19 Dec 2019 06:40:23 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 19 Dec 2019 06:40:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Dec 2019 06:40:23 GMT
CMD ["couchbase-server"]
# Thu, 19 Dec 2019 06:40:23 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 19 Dec 2019 06:40:23 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:3386e6af03b043219225367632569465e5ecd47391d1f99a6d265e51bd463a83`  
		Last Modified: Thu, 12 Dec 2019 08:26:09 GMT  
		Size: 44.1 MB (44123254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ac0bbe6c8eeb959337b336ceaa5c3bbbae81e316025f9b94ede453540f2377`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1983a67e104e801fceb1850a375a71fe6b62636ba7a8403d9644f308a6a43f9`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0f3a523f04f61db942018321ae122f90d8e3303e243b005e8de9817daf7028`  
		Last Modified: Thu, 19 Dec 2019 04:25:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35cfbf2546f178acf65d54d00dea29c862a5aa1e13db5369ec2d40b471b6c54`  
		Last Modified: Thu, 19 Dec 2019 06:40:40 GMT  
		Size: 14.3 MB (14330783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dae530d69d4a12e6c0699565010595a4a5de7a53b335ad119985ad10c713ce`  
		Last Modified: Thu, 19 Dec 2019 06:42:49 GMT  
		Size: 2.1 KB (2075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ecaaae3a981119abe142b0d3d269226a30e92467e0cfeed4cd8fc18ba2fe5f9`  
		Last Modified: Thu, 19 Dec 2019 06:43:12 GMT  
		Size: 140.9 MB (140887945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27fb5a83fffaa82b9702184605283f83589ae68264da669c883d4ef96a09289a`  
		Last Modified: Thu, 19 Dec 2019 06:42:48 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554c574542d7c7b93d9187a88ca9247c40a90a63237f5f1b58da1b08ab79471c`  
		Last Modified: Thu, 19 Dec 2019 06:42:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f60c2c021044652e527645d4f3ee9b02c534fe8494bacfa50e566c3a476855f`  
		Last Modified: Thu, 19 Dec 2019 06:42:47 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef9c777ec4eb62d198feef0dde2f8505e537b3218b246d5d317c60f81bd1600`  
		Last Modified: Thu, 19 Dec 2019 06:42:48 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd21135c2641aab927ccd79e3257ee46c01b5ec66242964512efb210e958d0a2`  
		Last Modified: Thu, 19 Dec 2019 06:42:47 GMT  
		Size: 120.6 KB (120597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d69977d46e6e54ee73a24cf959e755e5961ba5df292de9ee38f0995474abaf1`  
		Last Modified: Thu, 19 Dec 2019 06:42:47 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:community-6.0.0`

```console
$ docker pull couchbase@sha256:ef03c8abc25a8fbc08c00a94acc73f6263124be33a482d5891790a1918b4503c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:community-6.0.0` - linux; amd64

```console
$ docker pull couchbase@sha256:117bb5abd494c81652affce51e6637a624db687fe85f471ea3f80f4b726331cd
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.5 MB (199468336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e508feb8c5fde2d369cf5c0509f83ec3401c09ba7b32f7b18c0b7501d6a87485`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 19 Dec 2019 04:24:35 GMT
ADD file:f0b8eaa718bc3965b1e8395f5a6bea97c16651b50614e676bb3eaf31335a0045 in / 
# Thu, 19 Dec 2019 04:24:36 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 04:24:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:24:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:24:38 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:36:40 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Thu, 19 Dec 2019 06:37:19 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 19 Dec 2019 06:39:53 GMT
ARG CB_VERSION=6.0.0
# Thu, 19 Dec 2019 06:39:53 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0
# Thu, 19 Dec 2019 06:39:53 GMT
ARG CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb
# Thu, 19 Dec 2019 06:39:53 GMT
ARG CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece
# Thu, 19 Dec 2019 06:39:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 19 Dec 2019 06:39:54 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0 CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece CB_VERSION=6.0.0
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 19 Dec 2019 06:40:20 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0 CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece CB_VERSION=6.0.0
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Thu, 19 Dec 2019 06:40:20 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 19 Dec 2019 06:40:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0 CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece CB_VERSION=6.0.0
RUN chown -R couchbase:couchbase /etc/service
# Thu, 19 Dec 2019 06:40:21 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 19 Dec 2019 06:40:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0 CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece CB_VERSION=6.0.0
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 19 Dec 2019 06:40:22 GMT
# ARGS: CB_PACKAGE=couchbase-server-community_6.0.0-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.0 CB_SHA256=949b1ded72776a557b9cd3ac89253a4fe6aed079966a4057c5aec41ae5a30ece CB_VERSION=6.0.0
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 19 Dec 2019 06:40:23 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 19 Dec 2019 06:40:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Dec 2019 06:40:23 GMT
CMD ["couchbase-server"]
# Thu, 19 Dec 2019 06:40:23 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 19 Dec 2019 06:40:23 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:3386e6af03b043219225367632569465e5ecd47391d1f99a6d265e51bd463a83`  
		Last Modified: Thu, 12 Dec 2019 08:26:09 GMT  
		Size: 44.1 MB (44123254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ac0bbe6c8eeb959337b336ceaa5c3bbbae81e316025f9b94ede453540f2377`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1983a67e104e801fceb1850a375a71fe6b62636ba7a8403d9644f308a6a43f9`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0f3a523f04f61db942018321ae122f90d8e3303e243b005e8de9817daf7028`  
		Last Modified: Thu, 19 Dec 2019 04:25:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35cfbf2546f178acf65d54d00dea29c862a5aa1e13db5369ec2d40b471b6c54`  
		Last Modified: Thu, 19 Dec 2019 06:40:40 GMT  
		Size: 14.3 MB (14330783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dae530d69d4a12e6c0699565010595a4a5de7a53b335ad119985ad10c713ce`  
		Last Modified: Thu, 19 Dec 2019 06:42:49 GMT  
		Size: 2.1 KB (2075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ecaaae3a981119abe142b0d3d269226a30e92467e0cfeed4cd8fc18ba2fe5f9`  
		Last Modified: Thu, 19 Dec 2019 06:43:12 GMT  
		Size: 140.9 MB (140887945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27fb5a83fffaa82b9702184605283f83589ae68264da669c883d4ef96a09289a`  
		Last Modified: Thu, 19 Dec 2019 06:42:48 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554c574542d7c7b93d9187a88ca9247c40a90a63237f5f1b58da1b08ab79471c`  
		Last Modified: Thu, 19 Dec 2019 06:42:47 GMT  
		Size: 410.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f60c2c021044652e527645d4f3ee9b02c534fe8494bacfa50e566c3a476855f`  
		Last Modified: Thu, 19 Dec 2019 06:42:47 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef9c777ec4eb62d198feef0dde2f8505e537b3218b246d5d317c60f81bd1600`  
		Last Modified: Thu, 19 Dec 2019 06:42:48 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd21135c2641aab927ccd79e3257ee46c01b5ec66242964512efb210e958d0a2`  
		Last Modified: Thu, 19 Dec 2019 06:42:47 GMT  
		Size: 120.6 KB (120597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d69977d46e6e54ee73a24cf959e755e5961ba5df292de9ee38f0995474abaf1`  
		Last Modified: Thu, 19 Dec 2019 06:42:47 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise`

```console
$ docker pull couchbase@sha256:dbe7ed71c3cff6a867cb40a350874469a8bf9b233a8f71c7b55244d184df9fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise` - linux; amd64

```console
$ docker pull couchbase@sha256:4899eafc51a3e568e44fee276f5d7a640d1e719db01c12613427cfca6a7375f8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **479.0 MB (478997039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4deec10b265ebab6e829fe139078ee212977c3b7803716b30827e84507ebafbc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 19 Dec 2019 04:24:35 GMT
ADD file:f0b8eaa718bc3965b1e8395f5a6bea97c16651b50614e676bb3eaf31335a0045 in / 
# Thu, 19 Dec 2019 04:24:36 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 04:24:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:24:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:24:38 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:36:40 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Thu, 19 Dec 2019 06:37:19 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 19 Dec 2019 06:37:19 GMT
ARG CB_VERSION=6.0.3
# Thu, 19 Dec 2019 06:37:19 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3
# Thu, 19 Dec 2019 06:37:20 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb
# Thu, 19 Dec 2019 06:37:20 GMT
ARG CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8
# Thu, 19 Dec 2019 06:37:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 19 Dec 2019 06:37:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 19 Dec 2019 06:38:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Thu, 19 Dec 2019 06:38:13 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 19 Dec 2019 06:38:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN chown -R couchbase:couchbase /etc/service
# Thu, 19 Dec 2019 06:38:14 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 19 Dec 2019 06:38:15 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 19 Dec 2019 06:38:16 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 19 Dec 2019 06:38:16 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 19 Dec 2019 06:38:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Dec 2019 06:38:16 GMT
CMD ["couchbase-server"]
# Thu, 19 Dec 2019 06:38:16 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 19 Dec 2019 06:38:17 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:3386e6af03b043219225367632569465e5ecd47391d1f99a6d265e51bd463a83`  
		Last Modified: Thu, 12 Dec 2019 08:26:09 GMT  
		Size: 44.1 MB (44123254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ac0bbe6c8eeb959337b336ceaa5c3bbbae81e316025f9b94ede453540f2377`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1983a67e104e801fceb1850a375a71fe6b62636ba7a8403d9644f308a6a43f9`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0f3a523f04f61db942018321ae122f90d8e3303e243b005e8de9817daf7028`  
		Last Modified: Thu, 19 Dec 2019 04:25:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35cfbf2546f178acf65d54d00dea29c862a5aa1e13db5369ec2d40b471b6c54`  
		Last Modified: Thu, 19 Dec 2019 06:40:40 GMT  
		Size: 14.3 MB (14330783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccb057f4f3b006d1acc62ebfac34a161ecfb751d60d09392aae4c4c31e11551`  
		Last Modified: Thu, 19 Dec 2019 06:40:36 GMT  
		Size: 2.1 KB (2071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a73461e5e6fe075cfd4e3c2146911d543a051de1e03972ac7af476c0b93e41`  
		Last Modified: Thu, 19 Dec 2019 06:41:28 GMT  
		Size: 420.4 MB (420416653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982e4a808750196401527726d5b02c65f5380e9a6fbc20c50823f1f7c0498d45`  
		Last Modified: Thu, 19 Dec 2019 06:40:37 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b3d5ad6cd54004abaf14f21970fee97d6c4a68ffd92412650dab502b1358ae`  
		Last Modified: Thu, 19 Dec 2019 06:40:36 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b533d3803f7eaa89db560da41f0ac0fb805850ae1f24b959cd8811f9c1b77e6`  
		Last Modified: Thu, 19 Dec 2019 06:40:35 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae0dc830f7f9da77305035bec6c8ade79f6fe2f3ee27850e7b3953357a66bf9`  
		Last Modified: Thu, 19 Dec 2019 06:40:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9291ed8137ecc9a6cd8baa42c18b06c3c77c7fd7fda4bbb2bf04b514a4a70956`  
		Last Modified: Thu, 19 Dec 2019 06:40:35 GMT  
		Size: 120.6 KB (120597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6ceac673a197a02dedf6d6b48ec70174e2a03a700d309a3d536381dae7dace`  
		Last Modified: Thu, 19 Dec 2019 06:40:35 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:enterprise-6.0.3`

```console
$ docker pull couchbase@sha256:dbe7ed71c3cff6a867cb40a350874469a8bf9b233a8f71c7b55244d184df9fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:enterprise-6.0.3` - linux; amd64

```console
$ docker pull couchbase@sha256:4899eafc51a3e568e44fee276f5d7a640d1e719db01c12613427cfca6a7375f8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **479.0 MB (478997039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4deec10b265ebab6e829fe139078ee212977c3b7803716b30827e84507ebafbc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 19 Dec 2019 04:24:35 GMT
ADD file:f0b8eaa718bc3965b1e8395f5a6bea97c16651b50614e676bb3eaf31335a0045 in / 
# Thu, 19 Dec 2019 04:24:36 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 04:24:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:24:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:24:38 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:36:40 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Thu, 19 Dec 2019 06:37:19 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 19 Dec 2019 06:37:19 GMT
ARG CB_VERSION=6.0.3
# Thu, 19 Dec 2019 06:37:19 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3
# Thu, 19 Dec 2019 06:37:20 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb
# Thu, 19 Dec 2019 06:37:20 GMT
ARG CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8
# Thu, 19 Dec 2019 06:37:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 19 Dec 2019 06:37:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 19 Dec 2019 06:38:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Thu, 19 Dec 2019 06:38:13 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 19 Dec 2019 06:38:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN chown -R couchbase:couchbase /etc/service
# Thu, 19 Dec 2019 06:38:14 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 19 Dec 2019 06:38:15 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 19 Dec 2019 06:38:16 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 19 Dec 2019 06:38:16 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 19 Dec 2019 06:38:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Dec 2019 06:38:16 GMT
CMD ["couchbase-server"]
# Thu, 19 Dec 2019 06:38:16 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 19 Dec 2019 06:38:17 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:3386e6af03b043219225367632569465e5ecd47391d1f99a6d265e51bd463a83`  
		Last Modified: Thu, 12 Dec 2019 08:26:09 GMT  
		Size: 44.1 MB (44123254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ac0bbe6c8eeb959337b336ceaa5c3bbbae81e316025f9b94ede453540f2377`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1983a67e104e801fceb1850a375a71fe6b62636ba7a8403d9644f308a6a43f9`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0f3a523f04f61db942018321ae122f90d8e3303e243b005e8de9817daf7028`  
		Last Modified: Thu, 19 Dec 2019 04:25:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35cfbf2546f178acf65d54d00dea29c862a5aa1e13db5369ec2d40b471b6c54`  
		Last Modified: Thu, 19 Dec 2019 06:40:40 GMT  
		Size: 14.3 MB (14330783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccb057f4f3b006d1acc62ebfac34a161ecfb751d60d09392aae4c4c31e11551`  
		Last Modified: Thu, 19 Dec 2019 06:40:36 GMT  
		Size: 2.1 KB (2071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a73461e5e6fe075cfd4e3c2146911d543a051de1e03972ac7af476c0b93e41`  
		Last Modified: Thu, 19 Dec 2019 06:41:28 GMT  
		Size: 420.4 MB (420416653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982e4a808750196401527726d5b02c65f5380e9a6fbc20c50823f1f7c0498d45`  
		Last Modified: Thu, 19 Dec 2019 06:40:37 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b3d5ad6cd54004abaf14f21970fee97d6c4a68ffd92412650dab502b1358ae`  
		Last Modified: Thu, 19 Dec 2019 06:40:36 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b533d3803f7eaa89db560da41f0ac0fb805850ae1f24b959cd8811f9c1b77e6`  
		Last Modified: Thu, 19 Dec 2019 06:40:35 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae0dc830f7f9da77305035bec6c8ade79f6fe2f3ee27850e7b3953357a66bf9`  
		Last Modified: Thu, 19 Dec 2019 06:40:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9291ed8137ecc9a6cd8baa42c18b06c3c77c7fd7fda4bbb2bf04b514a4a70956`  
		Last Modified: Thu, 19 Dec 2019 06:40:35 GMT  
		Size: 120.6 KB (120597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6ceac673a197a02dedf6d6b48ec70174e2a03a700d309a3d536381dae7dace`  
		Last Modified: Thu, 19 Dec 2019 06:40:35 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchbase:latest`

```console
$ docker pull couchbase@sha256:dbe7ed71c3cff6a867cb40a350874469a8bf9b233a8f71c7b55244d184df9fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `couchbase:latest` - linux; amd64

```console
$ docker pull couchbase@sha256:4899eafc51a3e568e44fee276f5d7a640d1e719db01c12613427cfca6a7375f8
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **479.0 MB (478997039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4deec10b265ebab6e829fe139078ee212977c3b7803716b30827e84507ebafbc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 19 Dec 2019 04:24:35 GMT
ADD file:f0b8eaa718bc3965b1e8395f5a6bea97c16651b50614e676bb3eaf31335a0045 in / 
# Thu, 19 Dec 2019 04:24:36 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 19 Dec 2019 04:24:37 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 19 Dec 2019 04:24:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 19 Dec 2019 04:24:38 GMT
CMD ["/bin/bash"]
# Thu, 19 Dec 2019 06:36:40 GMT
MAINTAINER Couchbase Docker Team <docker@couchbase.com>
# Thu, 19 Dec 2019 06:37:19 GMT
RUN apt-get update &&     apt-get install -yq runit wget chrpath tzdata     lsof lshw sysstat net-tools numactl python-httplib2 &&     apt-get autoremove && apt-get clean &&     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 19 Dec 2019 06:37:19 GMT
ARG CB_VERSION=6.0.3
# Thu, 19 Dec 2019 06:37:19 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3
# Thu, 19 Dec 2019 06:37:20 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb
# Thu, 19 Dec 2019 06:37:20 GMT
ARG CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8
# Thu, 19 Dec 2019 06:37:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 19 Dec 2019 06:37:21 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN groupadd -g 1000 couchbase && useradd couchbase -u 1000 -g couchbase -M
# Thu, 19 Dec 2019 06:38:13 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN export INSTALL_DONT_START_SERVER=1 &&     wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE &&     echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - &&     dpkg -i ./$CB_PACKAGE && rm -f ./$CB_PACKAGE
# Thu, 19 Dec 2019 06:38:13 GMT
COPY file:d6a307209223b2df102f46f07fd186e09fac7114db2c965bb54097d3b4d3b989 in /etc/service/couchbase-server/run 
# Thu, 19 Dec 2019 06:38:14 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN chown -R couchbase:couchbase /etc/service
# Thu, 19 Dec 2019 06:38:14 GMT
COPY file:1302333e9e56b11ae357341056dee0080efda9457b1ce3de1a1ecb6023e760ae in /usr/local/bin/ 
# Thu, 19 Dec 2019 06:38:15 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN ln -s dummy.sh /usr/local/bin/iptables-save &&     ln -s dummy.sh /usr/local/bin/lvdisplay &&     ln -s dummy.sh /usr/local/bin/vgdisplay &&     ln -s dummy.sh /usr/local/bin/pvdisplay
# Thu, 19 Dec 2019 06:38:16 GMT
# ARGS: CB_PACKAGE=couchbase-server-enterprise_6.0.3-ubuntu16.04_amd64.deb CB_RELEASE_URL=https://packages.couchbase.com/releases/6.0.3 CB_SHA256=bb8fe58b25d721833426ca5eeccc3bec41e793e7d961f1edac7f099f98345be8 CB_VERSION=6.0.3
RUN chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl
# Thu, 19 Dec 2019 06:38:16 GMT
COPY file:d816a67f62bfba76d2812cefbe92252afa13f3852775c3e68599df7741e90cb7 in / 
# Thu, 19 Dec 2019 06:38:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 19 Dec 2019 06:38:16 GMT
CMD ["couchbase-server"]
# Thu, 19 Dec 2019 06:38:16 GMT
EXPOSE 11207 11210 11211 18091 18092 18093 18094 18095 18096 8091 8092 8093 8094 8095 8096
# Thu, 19 Dec 2019 06:38:17 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:3386e6af03b043219225367632569465e5ecd47391d1f99a6d265e51bd463a83`  
		Last Modified: Thu, 12 Dec 2019 08:26:09 GMT  
		Size: 44.1 MB (44123254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ac0bbe6c8eeb959337b336ceaa5c3bbbae81e316025f9b94ede453540f2377`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1983a67e104e801fceb1850a375a71fe6b62636ba7a8403d9644f308a6a43f9`  
		Last Modified: Thu, 19 Dec 2019 04:26:00 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0f3a523f04f61db942018321ae122f90d8e3303e243b005e8de9817daf7028`  
		Last Modified: Thu, 19 Dec 2019 04:25:59 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35cfbf2546f178acf65d54d00dea29c862a5aa1e13db5369ec2d40b471b6c54`  
		Last Modified: Thu, 19 Dec 2019 06:40:40 GMT  
		Size: 14.3 MB (14330783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ccb057f4f3b006d1acc62ebfac34a161ecfb751d60d09392aae4c4c31e11551`  
		Last Modified: Thu, 19 Dec 2019 06:40:36 GMT  
		Size: 2.1 KB (2071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a73461e5e6fe075cfd4e3c2146911d543a051de1e03972ac7af476c0b93e41`  
		Last Modified: Thu, 19 Dec 2019 06:41:28 GMT  
		Size: 420.4 MB (420416653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982e4a808750196401527726d5b02c65f5380e9a6fbc20c50823f1f7c0498d45`  
		Last Modified: Thu, 19 Dec 2019 06:40:37 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2b3d5ad6cd54004abaf14f21970fee97d6c4a68ffd92412650dab502b1358ae`  
		Last Modified: Thu, 19 Dec 2019 06:40:36 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b533d3803f7eaa89db560da41f0ac0fb805850ae1f24b959cd8811f9c1b77e6`  
		Last Modified: Thu, 19 Dec 2019 06:40:35 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae0dc830f7f9da77305035bec6c8ade79f6fe2f3ee27850e7b3953357a66bf9`  
		Last Modified: Thu, 19 Dec 2019 06:40:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9291ed8137ecc9a6cd8baa42c18b06c3c77c7fd7fda4bbb2bf04b514a4a70956`  
		Last Modified: Thu, 19 Dec 2019 06:40:35 GMT  
		Size: 120.6 KB (120597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6ceac673a197a02dedf6d6b48ec70174e2a03a700d309a3d536381dae7dace`  
		Last Modified: Thu, 19 Dec 2019 06:40:35 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

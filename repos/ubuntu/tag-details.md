<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ubuntu`

-	[`ubuntu:14.04`](#ubuntu1404)
-	[`ubuntu:16.04`](#ubuntu1604)
-	[`ubuntu:18.04`](#ubuntu1804)
-	[`ubuntu:20.04`](#ubuntu2004)
-	[`ubuntu:20.10`](#ubuntu2010)
-	[`ubuntu:21.04`](#ubuntu2104)
-	[`ubuntu:21.10`](#ubuntu2110)
-	[`ubuntu:bionic`](#ubuntubionic)
-	[`ubuntu:bionic-20210702`](#ubuntubionic-20210702)
-	[`ubuntu:devel`](#ubuntudevel)
-	[`ubuntu:focal`](#ubuntufocal)
-	[`ubuntu:focal-20210713`](#ubuntufocal-20210713)
-	[`ubuntu:groovy`](#ubuntugroovy)
-	[`ubuntu:groovy-20210713`](#ubuntugroovy-20210713)
-	[`ubuntu:hirsute`](#ubuntuhirsute)
-	[`ubuntu:hirsute-20210711`](#ubuntuhirsute-20210711)
-	[`ubuntu:impish`](#ubuntuimpish)
-	[`ubuntu:impish-20210711`](#ubuntuimpish-20210711)
-	[`ubuntu:latest`](#ubuntulatest)
-	[`ubuntu:rolling`](#ubunturolling)
-	[`ubuntu:trusty`](#ubuntutrusty)
-	[`ubuntu:trusty-20191217`](#ubuntutrusty-20191217)
-	[`ubuntu:xenial`](#ubuntuxenial)
-	[`ubuntu:xenial-20210611`](#ubuntuxenial-20210611)

## `ubuntu:14.04`

```console
$ docker pull ubuntu@sha256:43cb19408de1e0ecf3ba5b5372ec98978963d6d0be42d0ad825e77a3bd16b5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `ubuntu:14.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:881afbae521c910f764f7187dbfbca3cc10c26f8bafa458c76dda009a901c29d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70764430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b66b487594a1f2b75396013bc05d29d9f527852d96c5577cc4f187559875d0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:40 GMT
ADD file:276b5d943a4d284f8a7b249176a31f93d95e852480c2b851de287e53ff622bba in / 
# Thu, 25 Mar 2021 22:33:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:43 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2e6e20c8e2e69fa5c3fcc310f419975cef5fbeb6f7f2fe1374071141281b6a06`  
		Last Modified: Wed, 18 Dec 2019 13:21:28 GMT  
		Size: 70.7 MB (70691577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0551a797c01db074ab0233ceb567e66b8ebdcb9de9a2e7baa36d57dfbca463a3`  
		Last Modified: Thu, 25 Mar 2021 22:35:39 GMT  
		Size: 72.7 KB (72664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512123a864da5e2a62949e65b67106292c5c704eff90cac2b949fc8d7ac1e58e`  
		Last Modified: Thu, 25 Mar 2021 22:35:39 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:14.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:534255069ef3adf1c7a555fd9f614845ab66c61ef9846e438d86e12ae8c89b88
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64700978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2cd03315989aa8326f2c276922d3969994c1304b1310d2e0d33a26d94dd68ea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:23:03 GMT
ADD file:e9d55e059869915743a8ca8e64582d23c48fe7e90e439daccd56d3e08e8673b4 in / 
# Tue, 13 Jul 2021 23:23:06 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 13 Jul 2021 23:23:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Tue, 13 Jul 2021 23:23:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 13 Jul 2021 23:23:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0db3a87a3d7959895fd860c8b924980adda6e77f5d315b6676a4ac0e12518978`  
		Last Modified: Thu, 19 Dec 2019 06:16:01 GMT  
		Size: 64.6 MB (64624015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c5cd1be699257153c2a6de85968c2d9c413d87470dc4f540c5c3decbca8e47`  
		Last Modified: Tue, 13 Jul 2021 23:28:27 GMT  
		Size: 76.8 KB (76774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbf1c32ebce749806713a088af6ff1cbf7c75a8132d310ff391948e3e611ef6`  
		Last Modified: Tue, 13 Jul 2021 23:28:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:14.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:0fe9a82e42e32a74cca83fc84d5ab80b2ef73b7b90b7bab661b00ef3d16bfad9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66525503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423c4ed354ff1af8b464f13e25792ddb5e0a2c6baa22b5af909e68b557062eec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 May 2021 12:30:34 GMT
ADD file:b0eb0db52e323748ea9b8d7f8aecbc523a747619cd08663bab0fe60ab59bc60e in / 
# Thu, 27 May 2021 12:30:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 27 May 2021 12:30:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 27 May 2021 12:30:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 27 May 2021 12:30:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d1a5a1e51f251c3431dec02e2cc8d157e92d1b46913708ce9e600747a6274977`  
		Last Modified: Thu, 19 Dec 2019 03:57:08 GMT  
		Size: 66.5 MB (66466219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e84a55d935eb29baa4a459e89f330e090e7f9db90fbdd96f6c47b89c614c671`  
		Last Modified: Thu, 27 May 2021 12:33:16 GMT  
		Size: 59.1 KB (59096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a9c88d39064b3377476bafe5b4a86f498750df033058cc4a61194f2ca5540b`  
		Last Modified: Thu, 27 May 2021 12:33:16 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:14.04` - linux; 386

```console
$ docker pull ubuntu@sha256:88152195106ff09bade23cb5aacfd26c381a8835c9d42124b4cba1dc3c2475e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68445499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f18ba408bae1426c4f394e045b16a140bc555e520d5eaacc97ac60ac5f298313`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:57:06 GMT
ADD file:e034601a525da53b0f39bb04d6e2264e2a592d0ae7c21e00697b9b62ca1efec9 in / 
# Thu, 25 Mar 2021 22:57:08 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:57:10 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:57:12 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:57:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:630712fe5783a35ad52a7026002143cb4f8fe65d34097dcaa4c4331b1b059a17`  
		Last Modified: Thu, 19 Dec 2019 04:44:02 GMT  
		Size: 68.4 MB (68380440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea2d50b5278097c6d027fc9fc0caf006649fcd94f094dde6ce578abe865ff21`  
		Last Modified: Thu, 25 Mar 2021 22:58:27 GMT  
		Size: 64.9 KB (64870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5795a499c24598e294527992a703053ab615879af048f3b809a3ad86141684d`  
		Last Modified: Thu, 25 Mar 2021 22:58:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:14.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:12d9fa858f255e4b70827aff83e8ce37b6fcaddaf6732276aa1f0763402f4fdc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73443156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02949c650aebaafb917ebe6bfd55a42505e22b38e8370878164051da4ae1bcc3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:24:04 GMT
ADD file:581665e92c72c8638b40fe509de6479dc1a5d7b5ffe8d6706006178c406e35e2 in / 
# Tue, 13 Jul 2021 23:24:24 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 13 Jul 2021 23:24:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Tue, 13 Jul 2021 23:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 13 Jul 2021 23:24:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bed4146d918c6c9a57bc3a8bf829e702975b0e53c7f25920fe9435b58ed6b64f`  
		Last Modified: Thu, 19 Dec 2019 04:26:52 GMT  
		Size: 73.4 MB (73379539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12aab203a69be44b1617f0da6b00b670e9016c3b00ab311b384ac3f859e86613`  
		Last Modified: Tue, 13 Jul 2021 23:29:07 GMT  
		Size: 63.4 KB (63430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1576c78d220b27404b5d0c3d635c36524229553e3ccf3b9a5ad4ca93c216c6c6`  
		Last Modified: Tue, 13 Jul 2021 23:29:07 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:16.04`

```console
$ docker pull ubuntu@sha256:286df18fa087cdccc0699f0db1ee60bcdae63874949e51de80d1fa4e88362126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:16.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:d388ba452d5f3f29399fc38c6928a65e4f28328a413c2edeee354569e7ab9bc9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46498913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b3fa4640d440e538e3d6fc4772c802c1a2d430e06c9a7920e654c7d7a601c9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:22:15 GMT
ADD file:a94a87e268e99c78143fae5148bd1200bf0da90c0e7f42bd8c168bb205ccb105 in / 
# Mon, 26 Jul 2021 21:22:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 26 Jul 2021 21:22:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 21:22:17 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 26 Jul 2021 21:22:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:52818491084148fa3469964bbcc3576686018a3b16b2e29be0407565c4c80b44`  
		Last Modified: Thu, 22 Jul 2021 16:25:00 GMT  
		Size: 46.5 MB (46497362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9df81d603d28f2a294b2f11b4f60d07b5b833b2ad7d6659a3f59b10cff2696`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636d9303bf663657be8e6796d720913bb985b5343da7949749ae1e72b54a88d8`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672b5bdcef61237567b311ad3d349f5eae18ba839ce2b204858a3083437a0a59`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:16.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:8e6989d7f12e1da4143c511fcca0ad11098b8601f0ca3e67d85706b525b717ba
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40313964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5956828c6af7649d7427fddc47a47e342afa0d4c7b391854d21157d4566eb5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:23:36 GMT
ADD file:ef24ce1c15acdd071b2d61cd27d2840f1fa5eda4937dfe8746997eb677b1451b in / 
# Tue, 13 Jul 2021 23:23:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 13 Jul 2021 23:23:41 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:23:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 13 Jul 2021 23:23:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bee35c084ef2789f844b87c031d55b07186255622024a15b526838f71500485a`  
		Last Modified: Thu, 17 Jun 2021 23:36:42 GMT  
		Size: 40.3 MB (40312433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82fe22c8ad83979c361a3c4d3e782f4a311856511042ff7a107356ea1e21e694`  
		Last Modified: Tue, 13 Jul 2021 23:29:28 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6b9c580e9f54a056423dc1ea3c0923d41d6f18b5abd11a5364db40a8f79fc7`  
		Last Modified: Tue, 13 Jul 2021 23:29:28 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f964743b5fd175c6240d9e2a4d592ff013029f4edea14efaec9813e6c65607e5`  
		Last Modified: Tue, 13 Jul 2021 23:29:28 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:16.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:1a7c76d63d768423a9908192ee61b5f25ecabf170dc009575db16a7b6f001896
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41240249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22d4e143f7d0bf20bc1d4618f63bab0ede51d173a71c32cad2045b87e616d1f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:49:35 GMT
ADD file:8d25df96ee02448d932dfa08341eceeb82da056f3ad8cbd1d8b24f44903e1891 in / 
# Mon, 26 Jul 2021 21:49:36 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 26 Jul 2021 21:49:37 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 21:49:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 26 Jul 2021 21:49:38 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2db5b739cd2a2fa296004e534a3fc4e7242f69130e59e1ff05a9e4ad4f7cd065`  
		Last Modified: Thu, 22 Jul 2021 16:25:06 GMT  
		Size: 41.2 MB (41238757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93da29956c4eb74ce61ad792d432dfe58787feb50bab77ef54679401df1ea22`  
		Last Modified: Mon, 26 Jul 2021 21:52:29 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3db33f994681db66c25858a525daaf3fde2cab655a638ab5f8e9adefcff34ff`  
		Last Modified: Mon, 26 Jul 2021 21:52:28 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ee9f14ba300ddf2ab6c21beb83fd70be989d93c2cb9de39ef70c61e3756041`  
		Last Modified: Mon, 26 Jul 2021 21:52:28 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:16.04` - linux; 386

```console
$ docker pull ubuntu@sha256:2acaf9eb4e50288bbb05b8238115b0cbf6f530985f2f9fc4c990224b8fa2b175
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45817296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26be9de5d32195fcef6cf4aa1cf46d5e86644d03ea1e905bfe051aa3e878e7e9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:19:12 GMT
ADD file:1b452fb9ede26959ad4e77cdde24fd29b55e6f0e25fc9e449602eec28f91a97f in / 
# Mon, 26 Jul 2021 21:19:13 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 26 Jul 2021 21:19:14 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 21:19:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 26 Jul 2021 21:19:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6002ee25903147b62d44ed293c693c455db05e98fd6ee23de5566fecd1b94976`  
		Last Modified: Sat, 24 Jul 2021 22:43:34 GMT  
		Size: 45.8 MB (45815767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebdd5137a750012174bcd408c7694f556d634de6d88eba053ea1865ec748809`  
		Last Modified: Mon, 26 Jul 2021 21:20:06 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e3facc8a281e63600ff451ccddd3e05b486726b9d9830b3de0726a8fefa074`  
		Last Modified: Mon, 26 Jul 2021 21:20:06 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7c8d8d34eaa9f414196f696ad2c62d1475973b2af07051c7e0eabac0ee86af`  
		Last Modified: Mon, 26 Jul 2021 21:20:06 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:16.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:412a6b8de102ebb781f558bcd5b66c96b0e6f9ee03fe30f566f09adf10480be0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47523790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4272e7d863f9da1994f2c32dfbb235c9284a7c5f923b0322c34f851eb4f08ab9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:25:11 GMT
ADD file:02f85c6f12364eaad4f80464effd781403b4c13c7732005ee3731d0d19a353c2 in / 
# Tue, 13 Jul 2021 23:25:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 13 Jul 2021 23:25:39 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:25:53 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 13 Jul 2021 23:25:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:77800700d823a40e3888379b1764dd49f1e6630a1848579e18e69c1dcc8f2558`  
		Last Modified: Thu, 17 Jun 2021 23:30:08 GMT  
		Size: 47.5 MB (47522284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0babf75a176b58db3a5df6096af29a306bf0ab34aed69816ecea017482b6ba6`  
		Last Modified: Tue, 13 Jul 2021 23:29:36 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aeb0805a3ad55f25fa2e52d341de43543d44705d05021e2d6a3ed9944915319`  
		Last Modified: Tue, 13 Jul 2021 23:29:36 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4421ae6a1a8096772ab2b5bb7d32cf300fbe5ffbe18cb6c742591febaf3bd7f`  
		Last Modified: Tue, 13 Jul 2021 23:29:36 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:16.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:13e9225a811698640577aef27c56f546d743519fd9301c9390d6ca1719f499a5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44089195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc5b5d39032a643edc9ae9b978586671c31c6bb5daa6a252ba6d8d7af7240b0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Jul 2021 20:55:52 GMT
ADD file:f5f56e2b2627da261a6178062e9bfac93ae66da8659cd0a443b6c9f6287084f8 in / 
# Mon, 26 Jul 2021 20:55:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 26 Jul 2021 20:55:56 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 20:55:57 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 26 Jul 2021 20:55:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0c85d52c5ad3f29826fe14cb11a9f94f5d0c766f47650e87720d614da0cba3c1`  
		Last Modified: Mon, 26 Jul 2021 20:58:05 GMT  
		Size: 44.1 MB (44087711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2a7580361ee0c51ed09eb59644c3edbca7639cdfee2ec4e3d921c8dd727339`  
		Last Modified: Mon, 26 Jul 2021 20:57:59 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56a77a0e6f8d9080c5c646f408f9a2aa52d5bacda38df1493fffaa4cd9b86fd`  
		Last Modified: Mon, 26 Jul 2021 20:57:59 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601f88d7e167a476b34623c363d7e5cc619faa8efa7e4f169093d342f1da402c`  
		Last Modified: Mon, 26 Jul 2021 20:57:59 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:18.04`

```console
$ docker pull ubuntu@sha256:a2c585c68506f7083ccebcf284576587be65e35886d3ee732c297c3e754942e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:18.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:07782849f2cff04e9bc29449c27d0fb2076e61e8bdb4475ec5dbc5386ed41a4f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26709039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a8cfeef17302cb7ce93cefe12368560fe62ef9d517808855f7bda79a1eb697`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:18.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:eb35905df1dad948847dc9d474b425eeb1c7a71e24a00df5f59bdbe611cf1c56
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22304073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1820aeca4d71cec52237d1c8ab6a7d534d55b9c905644491293eab8421e1bcf5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:20:43 GMT
ADD file:f065167f188d5bc319e42f0d3fb26520247ed8e38db629af17856b6f9e2f0cf0 in / 
# Tue, 13 Jul 2021 23:20:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:13c5fbe08fe2049e9effbe0d00319cfb1efa5d363e64f222a8bb747a01143fbd`  
		Last Modified: Tue, 13 Jul 2021 23:25:48 GMT  
		Size: 22.3 MB (22304073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:18.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:34ad5943b87b2e564daa9a339bb563589cff4779f82afa01d76cabf2b10a44e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23731597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0c6ae0b575322559fb80db1f422dc4d3e8063851a543f7f6bbb576899ce23e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:49 GMT
ADD file:e87e065765ef99e8db25307f469c7481ab480ac5fe6353ae4caf402766f14045 in / 
# Mon, 26 Jul 2021 21:48:50 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fda1cca7a3cc2b66c161597f27e151a9b1cab79d73c7c0c2706606813a3e58cf`  
		Last Modified: Mon, 26 Jul 2021 21:50:37 GMT  
		Size: 23.7 MB (23731597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:18.04` - linux; 386

```console
$ docker pull ubuntu@sha256:9fee49c70335d1f34cbf1c3d3371e2778eace8be62e629467000955f45dcfa0b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27162925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47caf860aa8ffdc2b9ac741b09b55a1ba183959a3bafa923178780853f1dc2f4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:18:53 GMT
ADD file:45b15f7ce91c2c05cc5e273dee6b36fade4217c3da1d407a6dc8e108f50e2b66 in / 
# Mon, 26 Jul 2021 21:18:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bc0a67b78038e09ba1732c1a7c63e6c8e924aca7029364acd54d64dd669b151f`  
		Last Modified: Mon, 26 Jul 2021 21:19:48 GMT  
		Size: 27.2 MB (27162925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:18.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:ff5e2c8fe5753c9761f77209e3611b7c42ba069205f0fe251434a2879d918bcb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30427987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfc8a230f662a3ef5262a60937cb7446f4c5328270929379cb41bb38654cd7b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:55 GMT
ADD file:45b627081344651e16f78f7bbb0da81c1dcc0300835ab0f4bdd6dd93621e461d in / 
# Tue, 13 Jul 2021 23:22:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b4e702a7ed6378fce702bcf7ca7d37185cd6d8387370cd090b9dc4bf5844f47c`  
		Last Modified: Tue, 13 Jul 2021 23:27:12 GMT  
		Size: 30.4 MB (30427987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:18.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:54207ae3982c4907825b6622fb38ac6b6fe72449d805b1d4cb0a02224bf6d88c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25367016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:140abc90d45b20c8fdb34e56ff2f4660ae86e8ce6f4c90cdd88905afb2a9e501`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 20:55:03 GMT
ADD file:edb1df135699bb6ca591e6493c0df55d2030d8990c3e0a3afa80442036f92e16 in / 
# Mon, 26 Jul 2021 20:55:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cb0153f85b121ce88ea3f3bebbb54c31f8547bed022bd201416974cd40c61f59`  
		Last Modified: Mon, 26 Jul 2021 20:56:50 GMT  
		Size: 25.4 MB (25367016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:20.04`

```console
$ docker pull ubuntu@sha256:ec361466a06c1ba246ae5f429fce6680d51b79f528660e299833b72a3c20ec14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:20.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:1e48201ccc2ab83afc435394b3bf70af0fa0055215c1e26a5da9b50a1ae367c9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28567944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1318b700e415001198d1bf66d260b07f67ca8a552b61b0da02b3832c778f221b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:20.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:8a2cbee49b50b0d08b01d4c31d70b72900f7668da53e8b4b9f1106a6443e4ca0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24062066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ce879b58c2cafb61a74c074b2e4339f8b97b15a7474e76315e809110937a05`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:08 GMT
ADD file:1ec1791cf8b61620293d0fdf83d76f3c07482a327aefef699a43e82e7c3aa0f0 in / 
# Tue, 13 Jul 2021 23:21:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5c5378967b4ed259bac71be5e1a9ea052469b5fe62bed34b19deb57d53dc63c0`  
		Last Modified: Tue, 13 Jul 2021 23:26:18 GMT  
		Size: 24.1 MB (24062066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:20.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:c0dd38485ed8b6e149d2fc935d1c61a3b750cda3b3eace0ad6df4abe33fa2b90
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27170255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58810d071ecb79ca0ce412597417260d4ae8cbe1a2896c55dce7f02f3d8f36ac`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:20.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:1030f108596afba03281f4c350466d74b900922c25e9881c7df6eefce6681080
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33287846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bb28c580f7164b6f79bebec70a9e67dbc1d62c92a17f72fe287267014f5e6a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:cdca4c00902f291c6bc305420b891f5149b6833b5f9892232ea690d38adfff3f in / 
# Tue, 13 Jul 2021 23:22:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:157ef43c951ca9b65226089aef70b09df64b81636884260390a329c24a3c614b`  
		Last Modified: Tue, 13 Jul 2021 23:27:34 GMT  
		Size: 33.3 MB (33287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:20.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:0f745a413c7886d6dc4f1e6a1d45a5cf5a9a85f72e6243b307e17d67e2e1fe10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27149898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14db5936efda0c6dd381ed7bb287bea8d5ccb027da8b97484564a85473f4dc77`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 20:55:12 GMT
ADD file:b8731edfdacfade2ec96757342f216962f3971b24077a9144da3f80003e6893e in / 
# Mon, 26 Jul 2021 20:55:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:38800a0044dea146ca3c3a08bc2c9c956396ad3241a3c343010775650298c379`  
		Last Modified: Mon, 26 Jul 2021 20:57:03 GMT  
		Size: 27.1 MB (27149898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:20.10`

```console
$ docker pull ubuntu@sha256:1caf59c068c2491671c8e143b4f0af5f6c7684395e367a3da0e2d6112b515077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:20.10` - linux; amd64

```console
$ docker pull ubuntu@sha256:754eb641a1ba98a8b483c3595a14164fa4ed7f4b457e1aa05f13ce06f8151723
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31342970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e508bd6d694ef622f1f5628104de30be6b58fc6c3c489f62e271b2d6f424a582`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:47 GMT
ADD file:23ff7ae476ddf97e5dbaf417c06418ae4d8d49a88acb92738bf03fb4a22eeca3 in / 
# Mon, 26 Jul 2021 21:21:47 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:32f3531c8415258308e8d8dda886004bc90cdf4793f9b97c6f33e7903036294f`  
		Last Modified: Mon, 26 Jul 2021 21:23:27 GMT  
		Size: 31.3 MB (31342970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:20.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:c6ecf83027c5771ed2f91b721fc693495117c700b11f5ed11af6fe7d1cb31870
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 MB (26312397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda5fc2153cc1581e00706b9ddcb3e07053538cb12bc1992ae869c9dc890e6dc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:33 GMT
ADD file:80b5f21ffac906a8416f39204cb526afaf64f15559123cb3a8fb311e312a703f in / 
# Tue, 13 Jul 2021 23:21:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7ad80ac50e31c20115b0366841c81a92d1916a7f2113255fe1125324250475e7`  
		Last Modified: Tue, 13 Jul 2021 23:26:54 GMT  
		Size: 26.3 MB (26312397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:20.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:5f999769760e67e5ebff9b4cdfba47909f695ee62f81fd2cbef6893b9763acad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.9 MB (29876744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f89080830426d542d290017420126adea752dcbdadd0378a4ad41fff580a59c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:49:05 GMT
ADD file:3a4e8fe51fe7ca76be749ef0b92043e9e9b241a7b6f196fbe2a8bcde49c5b3e7 in / 
# Mon, 26 Jul 2021 21:49:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:06dd9de3e7a96bf4bd49de5d681cb7062c5b3012c0f1b1bcd9d059380f55a1d2`  
		Last Modified: Mon, 26 Jul 2021 21:51:22 GMT  
		Size: 29.9 MB (29876744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:20.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:09ec5a4f8c30537574711fd78b0a91eb457c7df3c2fe9cc57201e8c7e2d3a336
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36562496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27089a136350a26e952f483854aa26d35d65fc26546c0d8192a1acf5ec9a07b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:45 GMT
ADD file:d810eebdcea73da6a0b9c4546fc356b13b60da24827c29923375b8e08f2195b4 in / 
# Tue, 13 Jul 2021 23:22:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97b0da8da7b9eb227e28852cb467ba3f76ac379708648200f035c072d3bbf4eb`  
		Last Modified: Tue, 13 Jul 2021 23:28:00 GMT  
		Size: 36.6 MB (36562496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:20.10` - linux; s390x

```console
$ docker pull ubuntu@sha256:78c188f0dfbcf09c68e00e316a7f0dc746286adb79cfe1bdee9a97466894b404
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31578338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366cbac6281e05c84836e160b41f2d677043d7a606c6552657dfa9529b586a9b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 20:55:22 GMT
ADD file:2f05dac9c72fd83b64830702accb3e1582661b82178055406f437be01591b038 in / 
# Mon, 26 Jul 2021 20:55:24 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6ebc30c62ba1234efc4428ed9d6d0f4f9b031ce916310c2d82b099cf9d02d1dc`  
		Last Modified: Mon, 26 Jul 2021 20:57:18 GMT  
		Size: 31.6 MB (31578338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:21.04`

```console
$ docker pull ubuntu@sha256:f734f5785fe15581fa062f65a9b64367d711d77ded6f5d94d3bebd842136ef48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:21.04` - linux; amd64

```console
$ docker pull ubuntu@sha256:ef8ee90cfa9cfc7c218586dea9daa6a8d1d191b3c73be143f4120fe140dae3d0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31837572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf70ebd2c444440ae068c5ccea80e2087906a825ff1019a9f6d6cbb229e33481`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:54 GMT
ADD file:6ae44786caae9af1c6b70dc9cc244e7d4e06fffc0696f68877527d69aa3fc735 in / 
# Mon, 26 Jul 2021 21:21:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4451f5c7eb7af74432585f5ebfbeb01bbfc87ec4a74dc93703bdd89330559cd1`  
		Last Modified: Mon, 26 Jul 2021 21:23:44 GMT  
		Size: 31.8 MB (31837572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:21.04` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:198eb162766bec2f17d3a0b63e108f0d3baa2777b2a57aae3cf5128d539f4518
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26853751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f456003eba6bf9ee07b68df86244805989efcd7b5087beb6bdfab6238485b1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:58 GMT
ADD file:5175798ab209bbc3941a05787751ecf9e7ba0b4e9cda31b044bd6d75e25976c8 in / 
# Tue, 13 Jul 2021 23:21:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fb746c2c12b45d26860f880a6e953018e4e9b83f9de17d11528fa484e1eb0f9f`  
		Last Modified: Tue, 13 Jul 2021 23:27:31 GMT  
		Size: 26.9 MB (26853751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:21.04` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:ca763e1a382a5b23f91abaf1c36a84be33da2d657f45746112f28ae010571041
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30299715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797e427e73c5159774c8eb88081f36b48516165ce1b20201afc4e6e54112c23f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:49:12 GMT
ADD file:878284607eb47bd96d58adc1bce14366656e20fede92cc0ff58787c14419cffe in / 
# Mon, 26 Jul 2021 21:49:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e34e08490be30f2dbe7ff29e0668c6e5aeba97f012896805dc1c38253e41bf42`  
		Last Modified: Mon, 26 Jul 2021 21:51:45 GMT  
		Size: 30.3 MB (30299715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:21.04` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:364af8f243780dc910f18d8bdb54cfd6df023d779fd8df6961a83051c07d2548
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37353027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b509d66002487ee099dd5b99b3b5efc26c925a3f5b746783cd9547b42c0521bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:23:07 GMT
ADD file:20ba7c85b0d967e38fdb53a91f37ff0266687978ecc0791861d4d1afb8c79899 in / 
# Tue, 13 Jul 2021 23:23:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2aeaf089064656dca36cf8480e9c7933a8c61fcc2a4c009ac61cbe442299cb68`  
		Last Modified: Tue, 13 Jul 2021 23:28:23 GMT  
		Size: 37.4 MB (37353027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:21.04` - linux; s390x

```console
$ docker pull ubuntu@sha256:13532df2f7a272c2c973268db5264059be5ba9882962d30db3d86ca38db3a737
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32624229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6607c9291374f45aab3fd1bdfefc6a6cd48c14aff62ffe96458dd03ce44e3de9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 20:55:31 GMT
ADD file:bdac50808129a68a89c50670c12a81b904aa091dbd47eddb391da90ab245345d in / 
# Mon, 26 Jul 2021 20:55:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0dde1b40c8bf5cce712bb8e104aa59e911b2c25d8aabe5075842cec6026b2bea`  
		Last Modified: Mon, 26 Jul 2021 20:57:32 GMT  
		Size: 32.6 MB (32624229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:21.10`

```console
$ docker pull ubuntu@sha256:5f8e6f156c9340b3742db9de27f51cba8a7cccc7dfab75817252887cc1511c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:21.10` - linux; amd64

```console
$ docker pull ubuntu@sha256:230c50db7d84d9a9ee76de505bd9405e043281a06e8398fb5efe086a8217bf40
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 MB (31519889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ecd4f42215a0a0851d38d400c65823b52bb27f957c78687bcd32f4cdec617a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:22:01 GMT
ADD file:aad4137373f37cc2272f1632b0fa50a91b4c0c878ca72ae8de8fee51ffa2f392 in / 
# Mon, 26 Jul 2021 21:22:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6c8d2949e37d3f87c8d42e502aebe8d287cc56bd1f5846a5265a2124c60cb49c`  
		Last Modified: Mon, 26 Jul 2021 21:24:04 GMT  
		Size: 31.5 MB (31519889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:21.10` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:873e7a4ea0af5861c11a9dad1caa7c88ecddb60358260397e35fc5fc0fb69f99
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26874823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b12f2dccadd333f3317db06e660ff070b5b16adc349e366a307ef901fca3d5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:2888fa0aa4baaaed5388c590baea27cba3d71017f1a390bf10191b18f123114c in / 
# Tue, 13 Jul 2021 23:22:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7fbf6def801b74c6b0c1bfed8350c986239cbb5ed41824f04074b3be99d3d8eb`  
		Last Modified: Tue, 13 Jul 2021 23:28:07 GMT  
		Size: 26.9 MB (26874823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:21.10` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:993294f9f183ba17a61857e31f589ddcda0e8f9636fc12d8fd34922f24539c36
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (29955429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a502550fdd23593fa879034f3635c637f2ef98e14eaf72bbb07bbc27c2163e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:49:21 GMT
ADD file:da87b88a910a756b9836fda56f61b491974f97e66462db711cde71ecfd6d28d8 in / 
# Mon, 26 Jul 2021 21:49:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:745e0e9e37f685fd5013fb72549992db744cf1eef9c1d0f35661c7fa8c1ebbda`  
		Last Modified: Mon, 26 Jul 2021 21:52:08 GMT  
		Size: 30.0 MB (29955429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:21.10` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:48f4289dcef78243d76861e5c7dc767f4d09c8b86c290835a9baa33034fe8d88
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37450815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369a2087639ab2667b4744b6c499a50611138db71cc72b09a00cc00afab2c4ac`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:23:30 GMT
ADD file:bd144e65c660dc138718837994b1fa3ea9593189413a61b63c8073bb1127532c in / 
# Tue, 13 Jul 2021 23:23:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:19f8a37977e3bfc6cc8d89c50cedc99d12151c43cd37c581e0fa522797296ca2`  
		Last Modified: Tue, 13 Jul 2021 23:28:48 GMT  
		Size: 37.5 MB (37450815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:21.10` - linux; s390x

```console
$ docker pull ubuntu@sha256:e4ef4355021c080c0e8c0d7d3b2feadf39aa35be77a176545acccb583bcefc86
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32489596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411d5c16e75a11c33d66b4bb7e2047820890af1c44bcdbf4f089ae6aa5cd50bd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 20:55:42 GMT
ADD file:b6ec59f7691777c81f8a8700ed1da1845eda3e628f2711f38e3c61e05d7a4135 in / 
# Mon, 26 Jul 2021 20:55:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:983c674c63ce4a2e843b63eb159ebc7a37998bed4be834de0311107fb837ffba`  
		Last Modified: Mon, 26 Jul 2021 20:57:48 GMT  
		Size: 32.5 MB (32489596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:bionic`

```console
$ docker pull ubuntu@sha256:a2c585c68506f7083ccebcf284576587be65e35886d3ee732c297c3e754942e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:bionic` - linux; amd64

```console
$ docker pull ubuntu@sha256:07782849f2cff04e9bc29449c27d0fb2076e61e8bdb4475ec5dbc5386ed41a4f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26709039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a8cfeef17302cb7ce93cefe12368560fe62ef9d517808855f7bda79a1eb697`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:eb35905df1dad948847dc9d474b425eeb1c7a71e24a00df5f59bdbe611cf1c56
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22304073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1820aeca4d71cec52237d1c8ab6a7d534d55b9c905644491293eab8421e1bcf5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:20:43 GMT
ADD file:f065167f188d5bc319e42f0d3fb26520247ed8e38db629af17856b6f9e2f0cf0 in / 
# Tue, 13 Jul 2021 23:20:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:13c5fbe08fe2049e9effbe0d00319cfb1efa5d363e64f222a8bb747a01143fbd`  
		Last Modified: Tue, 13 Jul 2021 23:25:48 GMT  
		Size: 22.3 MB (22304073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:34ad5943b87b2e564daa9a339bb563589cff4779f82afa01d76cabf2b10a44e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23731597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0c6ae0b575322559fb80db1f422dc4d3e8063851a543f7f6bbb576899ce23e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:49 GMT
ADD file:e87e065765ef99e8db25307f469c7481ab480ac5fe6353ae4caf402766f14045 in / 
# Mon, 26 Jul 2021 21:48:50 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fda1cca7a3cc2b66c161597f27e151a9b1cab79d73c7c0c2706606813a3e58cf`  
		Last Modified: Mon, 26 Jul 2021 21:50:37 GMT  
		Size: 23.7 MB (23731597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic` - linux; 386

```console
$ docker pull ubuntu@sha256:9fee49c70335d1f34cbf1c3d3371e2778eace8be62e629467000955f45dcfa0b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27162925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47caf860aa8ffdc2b9ac741b09b55a1ba183959a3bafa923178780853f1dc2f4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:18:53 GMT
ADD file:45b15f7ce91c2c05cc5e273dee6b36fade4217c3da1d407a6dc8e108f50e2b66 in / 
# Mon, 26 Jul 2021 21:18:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bc0a67b78038e09ba1732c1a7c63e6c8e924aca7029364acd54d64dd669b151f`  
		Last Modified: Mon, 26 Jul 2021 21:19:48 GMT  
		Size: 27.2 MB (27162925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:ff5e2c8fe5753c9761f77209e3611b7c42ba069205f0fe251434a2879d918bcb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30427987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfc8a230f662a3ef5262a60937cb7446f4c5328270929379cb41bb38654cd7b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:55 GMT
ADD file:45b627081344651e16f78f7bbb0da81c1dcc0300835ab0f4bdd6dd93621e461d in / 
# Tue, 13 Jul 2021 23:22:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b4e702a7ed6378fce702bcf7ca7d37185cd6d8387370cd090b9dc4bf5844f47c`  
		Last Modified: Tue, 13 Jul 2021 23:27:12 GMT  
		Size: 30.4 MB (30427987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic` - linux; s390x

```console
$ docker pull ubuntu@sha256:54207ae3982c4907825b6622fb38ac6b6fe72449d805b1d4cb0a02224bf6d88c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25367016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:140abc90d45b20c8fdb34e56ff2f4660ae86e8ce6f4c90cdd88905afb2a9e501`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 20:55:03 GMT
ADD file:edb1df135699bb6ca591e6493c0df55d2030d8990c3e0a3afa80442036f92e16 in / 
# Mon, 26 Jul 2021 20:55:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cb0153f85b121ce88ea3f3bebbb54c31f8547bed022bd201416974cd40c61f59`  
		Last Modified: Mon, 26 Jul 2021 20:56:50 GMT  
		Size: 25.4 MB (25367016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:bionic-20210702`

```console
$ docker pull ubuntu@sha256:3b8692dc4474d4f6043fae285676699361792ce1828e22b1b57367b5c05457e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:bionic-20210702` - linux; amd64

```console
$ docker pull ubuntu@sha256:c404618e908391e50953e1ead94fe05dbbddbf532bd5c89b935ef34a9ca130d3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26706145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbf60236a8e3dd08a08966064a8ac9f3943ecbffa6ae2ad9bc455974b956412c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic-20210702` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:eb35905df1dad948847dc9d474b425eeb1c7a71e24a00df5f59bdbe611cf1c56
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22304073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1820aeca4d71cec52237d1c8ab6a7d534d55b9c905644491293eab8421e1bcf5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:20:43 GMT
ADD file:f065167f188d5bc319e42f0d3fb26520247ed8e38db629af17856b6f9e2f0cf0 in / 
# Tue, 13 Jul 2021 23:20:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:13c5fbe08fe2049e9effbe0d00319cfb1efa5d363e64f222a8bb747a01143fbd`  
		Last Modified: Tue, 13 Jul 2021 23:25:48 GMT  
		Size: 22.3 MB (22304073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic-20210702` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:d12f1bfe5338cf7812b3e2241b7a2f6d2bcd9df9a054a16707e75355c5be3fda
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23729498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9033440523d58b7f09ef05522b56486bbcd930191dd2abb4d2aa338175fdbe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:09 GMT
ADD file:f5aca23bd8c77beda7e17bb71fc4df34d91662b6179de87029f24d21b9e799ad in / 
# Tue, 13 Jul 2021 23:01:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b9bb7af7248f30dd1b1f9807608f5f532133384e4db55caa6dbc69b9cf15ddcc`  
		Last Modified: Tue, 13 Jul 2021 23:03:17 GMT  
		Size: 23.7 MB (23729498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic-20210702` - linux; 386

```console
$ docker pull ubuntu@sha256:6b24223d4cefaddcc1eb58724271e5fc9600f6aa7eebec7e7a89e4eaf0e0a365
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27153547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a4435a5ea80c1fe38b39a002147fd612e35c1c6ab65fc050f36349b7d2a4ed`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:39:15 GMT
ADD file:2478887c0caae58ac755f71306211decbf5e69b832b9939974a93743e5c440f5 in / 
# Tue, 13 Jul 2021 22:39:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4c0067b0d84ac31443135f34e6bf8eacb1e1da0b388d042fbdd498858738047f`  
		Last Modified: Tue, 13 Jul 2021 22:40:10 GMT  
		Size: 27.2 MB (27153547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic-20210702` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:ff5e2c8fe5753c9761f77209e3611b7c42ba069205f0fe251434a2879d918bcb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 MB (30427987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfc8a230f662a3ef5262a60937cb7446f4c5328270929379cb41bb38654cd7b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:55 GMT
ADD file:45b627081344651e16f78f7bbb0da81c1dcc0300835ab0f4bdd6dd93621e461d in / 
# Tue, 13 Jul 2021 23:22:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b4e702a7ed6378fce702bcf7ca7d37185cd6d8387370cd090b9dc4bf5844f47c`  
		Last Modified: Tue, 13 Jul 2021 23:27:12 GMT  
		Size: 30.4 MB (30427987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:bionic-20210702` - linux; s390x

```console
$ docker pull ubuntu@sha256:53363cba7e786a7ea518ce5ec8b0230781695aee930de478bf615c62978854be
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25365649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16b0f8be5beb082c3bcbeb370035a585e7cd9da6e48a9689b3bcb228f6a7fa2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:22 GMT
ADD file:9e621b1dfa735f1a89553f154f2a2a6f669ff610236d92d6ebf37d1f378d8ec0 in / 
# Tue, 13 Jul 2021 22:53:24 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3287e09e36098b10234ccc1f8db0b48e2027ca7caa353a362d65f9b017ab802e`  
		Last Modified: Tue, 13 Jul 2021 22:55:34 GMT  
		Size: 25.4 MB (25365649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:devel`

```console
$ docker pull ubuntu@sha256:5f8e6f156c9340b3742db9de27f51cba8a7cccc7dfab75817252887cc1511c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:devel` - linux; amd64

```console
$ docker pull ubuntu@sha256:230c50db7d84d9a9ee76de505bd9405e043281a06e8398fb5efe086a8217bf40
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 MB (31519889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ecd4f42215a0a0851d38d400c65823b52bb27f957c78687bcd32f4cdec617a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:22:01 GMT
ADD file:aad4137373f37cc2272f1632b0fa50a91b4c0c878ca72ae8de8fee51ffa2f392 in / 
# Mon, 26 Jul 2021 21:22:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6c8d2949e37d3f87c8d42e502aebe8d287cc56bd1f5846a5265a2124c60cb49c`  
		Last Modified: Mon, 26 Jul 2021 21:24:04 GMT  
		Size: 31.5 MB (31519889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:devel` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:873e7a4ea0af5861c11a9dad1caa7c88ecddb60358260397e35fc5fc0fb69f99
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26874823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b12f2dccadd333f3317db06e660ff070b5b16adc349e366a307ef901fca3d5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:2888fa0aa4baaaed5388c590baea27cba3d71017f1a390bf10191b18f123114c in / 
# Tue, 13 Jul 2021 23:22:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7fbf6def801b74c6b0c1bfed8350c986239cbb5ed41824f04074b3be99d3d8eb`  
		Last Modified: Tue, 13 Jul 2021 23:28:07 GMT  
		Size: 26.9 MB (26874823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:devel` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:993294f9f183ba17a61857e31f589ddcda0e8f9636fc12d8fd34922f24539c36
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (29955429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a502550fdd23593fa879034f3635c637f2ef98e14eaf72bbb07bbc27c2163e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:49:21 GMT
ADD file:da87b88a910a756b9836fda56f61b491974f97e66462db711cde71ecfd6d28d8 in / 
# Mon, 26 Jul 2021 21:49:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:745e0e9e37f685fd5013fb72549992db744cf1eef9c1d0f35661c7fa8c1ebbda`  
		Last Modified: Mon, 26 Jul 2021 21:52:08 GMT  
		Size: 30.0 MB (29955429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:devel` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:48f4289dcef78243d76861e5c7dc767f4d09c8b86c290835a9baa33034fe8d88
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37450815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369a2087639ab2667b4744b6c499a50611138db71cc72b09a00cc00afab2c4ac`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:23:30 GMT
ADD file:bd144e65c660dc138718837994b1fa3ea9593189413a61b63c8073bb1127532c in / 
# Tue, 13 Jul 2021 23:23:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:19f8a37977e3bfc6cc8d89c50cedc99d12151c43cd37c581e0fa522797296ca2`  
		Last Modified: Tue, 13 Jul 2021 23:28:48 GMT  
		Size: 37.5 MB (37450815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:devel` - linux; s390x

```console
$ docker pull ubuntu@sha256:e4ef4355021c080c0e8c0d7d3b2feadf39aa35be77a176545acccb583bcefc86
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32489596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411d5c16e75a11c33d66b4bb7e2047820890af1c44bcdbf4f089ae6aa5cd50bd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 20:55:42 GMT
ADD file:b6ec59f7691777c81f8a8700ed1da1845eda3e628f2711f38e3c61e05d7a4135 in / 
# Mon, 26 Jul 2021 20:55:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:983c674c63ce4a2e843b63eb159ebc7a37998bed4be834de0311107fb837ffba`  
		Last Modified: Mon, 26 Jul 2021 20:57:48 GMT  
		Size: 32.5 MB (32489596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:focal`

```console
$ docker pull ubuntu@sha256:ec361466a06c1ba246ae5f429fce6680d51b79f528660e299833b72a3c20ec14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:focal` - linux; amd64

```console
$ docker pull ubuntu@sha256:1e48201ccc2ab83afc435394b3bf70af0fa0055215c1e26a5da9b50a1ae367c9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28567944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1318b700e415001198d1bf66d260b07f67ca8a552b61b0da02b3832c778f221b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:8a2cbee49b50b0d08b01d4c31d70b72900f7668da53e8b4b9f1106a6443e4ca0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24062066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ce879b58c2cafb61a74c074b2e4339f8b97b15a7474e76315e809110937a05`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:08 GMT
ADD file:1ec1791cf8b61620293d0fdf83d76f3c07482a327aefef699a43e82e7c3aa0f0 in / 
# Tue, 13 Jul 2021 23:21:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5c5378967b4ed259bac71be5e1a9ea052469b5fe62bed34b19deb57d53dc63c0`  
		Last Modified: Tue, 13 Jul 2021 23:26:18 GMT  
		Size: 24.1 MB (24062066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:c0dd38485ed8b6e149d2fc935d1c61a3b750cda3b3eace0ad6df4abe33fa2b90
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27170255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58810d071ecb79ca0ce412597417260d4ae8cbe1a2896c55dce7f02f3d8f36ac`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:1030f108596afba03281f4c350466d74b900922c25e9881c7df6eefce6681080
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33287846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bb28c580f7164b6f79bebec70a9e67dbc1d62c92a17f72fe287267014f5e6a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:cdca4c00902f291c6bc305420b891f5149b6833b5f9892232ea690d38adfff3f in / 
# Tue, 13 Jul 2021 23:22:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:157ef43c951ca9b65226089aef70b09df64b81636884260390a329c24a3c614b`  
		Last Modified: Tue, 13 Jul 2021 23:27:34 GMT  
		Size: 33.3 MB (33287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal` - linux; s390x

```console
$ docker pull ubuntu@sha256:0f745a413c7886d6dc4f1e6a1d45a5cf5a9a85f72e6243b307e17d67e2e1fe10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27149898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14db5936efda0c6dd381ed7bb287bea8d5ccb027da8b97484564a85473f4dc77`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 20:55:12 GMT
ADD file:b8731edfdacfade2ec96757342f216962f3971b24077a9144da3f80003e6893e in / 
# Mon, 26 Jul 2021 20:55:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:38800a0044dea146ca3c3a08bc2c9c956396ad3241a3c343010775650298c379`  
		Last Modified: Mon, 26 Jul 2021 20:57:03 GMT  
		Size: 27.1 MB (27149898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:focal-20210713`

```console
$ docker pull ubuntu@sha256:b3e2e47d016c08b3396b5ebe06ab0b711c34e7f37b98c9d37abe794b71cea0a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:focal-20210713` - linux; amd64

```console
$ docker pull ubuntu@sha256:778fdd9f62a6d7c0e53a97489ab3db17738bc5c1acf09a18738a2a674025eae6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28565863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29284518f497b8c5f49933e74e43ca5221e69c8251e780427f7d12f716625ff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal-20210713` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:8a2cbee49b50b0d08b01d4c31d70b72900f7668da53e8b4b9f1106a6443e4ca0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24062066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ce879b58c2cafb61a74c074b2e4339f8b97b15a7474e76315e809110937a05`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:08 GMT
ADD file:1ec1791cf8b61620293d0fdf83d76f3c07482a327aefef699a43e82e7c3aa0f0 in / 
# Tue, 13 Jul 2021 23:21:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5c5378967b4ed259bac71be5e1a9ea052469b5fe62bed34b19deb57d53dc63c0`  
		Last Modified: Tue, 13 Jul 2021 23:26:18 GMT  
		Size: 24.1 MB (24062066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal-20210713` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:cbab4168a24a0fe4697a807573b8fac2dad88ef797da97c651af11c97c33439f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27169081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdf4a30202f5cc2e986c25eee3cee725eb0017586b65a821dd9150e2ec2413b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:23 GMT
ADD file:4a34ac318ec122d2262279f4f06fd87cdf0383df4b0919cd46f3455b4fcb20a2 in / 
# Tue, 13 Jul 2021 23:01:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:99006dae3b24cf096633c9f0234ddeefee9042d4bede6ebc607d63a52bb79fb0`  
		Last Modified: Tue, 13 Jul 2021 23:03:36 GMT  
		Size: 27.2 MB (27169081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal-20210713` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:1030f108596afba03281f4c350466d74b900922c25e9881c7df6eefce6681080
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33287846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bb28c580f7164b6f79bebec70a9e67dbc1d62c92a17f72fe287267014f5e6a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:cdca4c00902f291c6bc305420b891f5149b6833b5f9892232ea690d38adfff3f in / 
# Tue, 13 Jul 2021 23:22:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:157ef43c951ca9b65226089aef70b09df64b81636884260390a329c24a3c614b`  
		Last Modified: Tue, 13 Jul 2021 23:27:34 GMT  
		Size: 33.3 MB (33287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:focal-20210713` - linux; s390x

```console
$ docker pull ubuntu@sha256:38711cd9d9eed84bda03811557cdb73acee3e3c0eef0769a93c3d7881e491ab8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27149318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd251e8b0998391f7503a207f9bacd6dbd30f68e964931ffddac1c69e76b08d0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:34 GMT
ADD file:ae5354f89d91eedd0614e3e97ee59fd6e23254923062c288d775e19b137dfd1c in / 
# Tue, 13 Jul 2021 22:53:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:761fa758059faa0c80b0b90fcbcc192fc7f573da055460d5b3f019e0faceeb7a`  
		Last Modified: Tue, 13 Jul 2021 22:55:47 GMT  
		Size: 27.1 MB (27149318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:groovy`

```console
$ docker pull ubuntu@sha256:1caf59c068c2491671c8e143b4f0af5f6c7684395e367a3da0e2d6112b515077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:groovy` - linux; amd64

```console
$ docker pull ubuntu@sha256:754eb641a1ba98a8b483c3595a14164fa4ed7f4b457e1aa05f13ce06f8151723
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31342970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e508bd6d694ef622f1f5628104de30be6b58fc6c3c489f62e271b2d6f424a582`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:47 GMT
ADD file:23ff7ae476ddf97e5dbaf417c06418ae4d8d49a88acb92738bf03fb4a22eeca3 in / 
# Mon, 26 Jul 2021 21:21:47 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:32f3531c8415258308e8d8dda886004bc90cdf4793f9b97c6f33e7903036294f`  
		Last Modified: Mon, 26 Jul 2021 21:23:27 GMT  
		Size: 31.3 MB (31342970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:groovy` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:c6ecf83027c5771ed2f91b721fc693495117c700b11f5ed11af6fe7d1cb31870
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 MB (26312397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda5fc2153cc1581e00706b9ddcb3e07053538cb12bc1992ae869c9dc890e6dc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:33 GMT
ADD file:80b5f21ffac906a8416f39204cb526afaf64f15559123cb3a8fb311e312a703f in / 
# Tue, 13 Jul 2021 23:21:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7ad80ac50e31c20115b0366841c81a92d1916a7f2113255fe1125324250475e7`  
		Last Modified: Tue, 13 Jul 2021 23:26:54 GMT  
		Size: 26.3 MB (26312397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:groovy` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:5f999769760e67e5ebff9b4cdfba47909f695ee62f81fd2cbef6893b9763acad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.9 MB (29876744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f89080830426d542d290017420126adea752dcbdadd0378a4ad41fff580a59c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:49:05 GMT
ADD file:3a4e8fe51fe7ca76be749ef0b92043e9e9b241a7b6f196fbe2a8bcde49c5b3e7 in / 
# Mon, 26 Jul 2021 21:49:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:06dd9de3e7a96bf4bd49de5d681cb7062c5b3012c0f1b1bcd9d059380f55a1d2`  
		Last Modified: Mon, 26 Jul 2021 21:51:22 GMT  
		Size: 29.9 MB (29876744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:groovy` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:09ec5a4f8c30537574711fd78b0a91eb457c7df3c2fe9cc57201e8c7e2d3a336
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36562496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27089a136350a26e952f483854aa26d35d65fc26546c0d8192a1acf5ec9a07b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:45 GMT
ADD file:d810eebdcea73da6a0b9c4546fc356b13b60da24827c29923375b8e08f2195b4 in / 
# Tue, 13 Jul 2021 23:22:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97b0da8da7b9eb227e28852cb467ba3f76ac379708648200f035c072d3bbf4eb`  
		Last Modified: Tue, 13 Jul 2021 23:28:00 GMT  
		Size: 36.6 MB (36562496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:groovy` - linux; s390x

```console
$ docker pull ubuntu@sha256:78c188f0dfbcf09c68e00e316a7f0dc746286adb79cfe1bdee9a97466894b404
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31578338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366cbac6281e05c84836e160b41f2d677043d7a606c6552657dfa9529b586a9b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 20:55:22 GMT
ADD file:2f05dac9c72fd83b64830702accb3e1582661b82178055406f437be01591b038 in / 
# Mon, 26 Jul 2021 20:55:24 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6ebc30c62ba1234efc4428ed9d6d0f4f9b031ce916310c2d82b099cf9d02d1dc`  
		Last Modified: Mon, 26 Jul 2021 20:57:18 GMT  
		Size: 31.6 MB (31578338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:groovy-20210713`

```console
$ docker pull ubuntu@sha256:39685c0f5c7e6a7cd463d0042d4a33a7d2e933e60cd8f5733ec2521a8e4892d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:groovy-20210713` - linux; amd64

```console
$ docker pull ubuntu@sha256:88d4432931e3e7757e6c7c565b58774b2925628b9bdffc86d4c906df8556c906
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 MB (31341566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7ae8e51e29fa6c2bc0bb507f66bffa5f7ea4f470990fa0aeed907020fa75bd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:45 GMT
ADD file:aa87e1d15a8d4e3640ec67e03ae6c4421158f4c64c838d701d82eb34722a2e3a in / 
# Tue, 13 Jul 2021 22:29:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:87103eef5146121c4b54992b41b2da8c9e671d21961ba24cfe5c1756737d5698`  
		Last Modified: Tue, 13 Jul 2021 22:31:40 GMT  
		Size: 31.3 MB (31341566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:groovy-20210713` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:c6ecf83027c5771ed2f91b721fc693495117c700b11f5ed11af6fe7d1cb31870
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 MB (26312397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda5fc2153cc1581e00706b9ddcb3e07053538cb12bc1992ae869c9dc890e6dc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:33 GMT
ADD file:80b5f21ffac906a8416f39204cb526afaf64f15559123cb3a8fb311e312a703f in / 
# Tue, 13 Jul 2021 23:21:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7ad80ac50e31c20115b0366841c81a92d1916a7f2113255fe1125324250475e7`  
		Last Modified: Tue, 13 Jul 2021 23:26:54 GMT  
		Size: 26.3 MB (26312397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:groovy-20210713` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:167cc98e855066af0974128227d79e541226ff042da708329f8be942c3a8dfa4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.9 MB (29877377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ae98f310882a1b43152644a1822429c8ca26b9f1640c34dcfffdb336739145`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:34 GMT
ADD file:8fe3c90118921d388c31ca28a21ff713dd718197e04654c6e0b7a09435f5287d in / 
# Tue, 13 Jul 2021 23:01:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3da8512ba050381848a454507530b9a467063e06b22a25eddc01311dbdf35301`  
		Last Modified: Tue, 13 Jul 2021 23:03:58 GMT  
		Size: 29.9 MB (29877377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:groovy-20210713` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:09ec5a4f8c30537574711fd78b0a91eb457c7df3c2fe9cc57201e8c7e2d3a336
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36562496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27089a136350a26e952f483854aa26d35d65fc26546c0d8192a1acf5ec9a07b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:45 GMT
ADD file:d810eebdcea73da6a0b9c4546fc356b13b60da24827c29923375b8e08f2195b4 in / 
# Tue, 13 Jul 2021 23:22:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97b0da8da7b9eb227e28852cb467ba3f76ac379708648200f035c072d3bbf4eb`  
		Last Modified: Tue, 13 Jul 2021 23:28:00 GMT  
		Size: 36.6 MB (36562496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:groovy-20210713` - linux; s390x

```console
$ docker pull ubuntu@sha256:9b64c14095739f23fdc3704f6cfb316eeb1d6d1b2438e3eda580c76757dc85d9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31577497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272b3c89ed1b8a558d5e1d9ba82c15855bce7c551d0ca034efeae4d079992769`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:46 GMT
ADD file:02a1c687ec9417cdf601518590b3a21fe31a0ebd2cdeb9bc63792512b95de989 in / 
# Tue, 13 Jul 2021 22:53:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:412af85569a706b682c00eeeaf32aeacbe1a5df158e5b67ddff07842b7ba3080`  
		Last Modified: Tue, 13 Jul 2021 22:56:02 GMT  
		Size: 31.6 MB (31577497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:hirsute`

```console
$ docker pull ubuntu@sha256:f734f5785fe15581fa062f65a9b64367d711d77ded6f5d94d3bebd842136ef48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:hirsute` - linux; amd64

```console
$ docker pull ubuntu@sha256:ef8ee90cfa9cfc7c218586dea9daa6a8d1d191b3c73be143f4120fe140dae3d0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31837572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf70ebd2c444440ae068c5ccea80e2087906a825ff1019a9f6d6cbb229e33481`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:54 GMT
ADD file:6ae44786caae9af1c6b70dc9cc244e7d4e06fffc0696f68877527d69aa3fc735 in / 
# Mon, 26 Jul 2021 21:21:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4451f5c7eb7af74432585f5ebfbeb01bbfc87ec4a74dc93703bdd89330559cd1`  
		Last Modified: Mon, 26 Jul 2021 21:23:44 GMT  
		Size: 31.8 MB (31837572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:hirsute` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:198eb162766bec2f17d3a0b63e108f0d3baa2777b2a57aae3cf5128d539f4518
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26853751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f456003eba6bf9ee07b68df86244805989efcd7b5087beb6bdfab6238485b1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:58 GMT
ADD file:5175798ab209bbc3941a05787751ecf9e7ba0b4e9cda31b044bd6d75e25976c8 in / 
# Tue, 13 Jul 2021 23:21:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fb746c2c12b45d26860f880a6e953018e4e9b83f9de17d11528fa484e1eb0f9f`  
		Last Modified: Tue, 13 Jul 2021 23:27:31 GMT  
		Size: 26.9 MB (26853751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:hirsute` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:ca763e1a382a5b23f91abaf1c36a84be33da2d657f45746112f28ae010571041
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30299715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797e427e73c5159774c8eb88081f36b48516165ce1b20201afc4e6e54112c23f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:49:12 GMT
ADD file:878284607eb47bd96d58adc1bce14366656e20fede92cc0ff58787c14419cffe in / 
# Mon, 26 Jul 2021 21:49:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e34e08490be30f2dbe7ff29e0668c6e5aeba97f012896805dc1c38253e41bf42`  
		Last Modified: Mon, 26 Jul 2021 21:51:45 GMT  
		Size: 30.3 MB (30299715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:hirsute` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:364af8f243780dc910f18d8bdb54cfd6df023d779fd8df6961a83051c07d2548
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37353027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b509d66002487ee099dd5b99b3b5efc26c925a3f5b746783cd9547b42c0521bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:23:07 GMT
ADD file:20ba7c85b0d967e38fdb53a91f37ff0266687978ecc0791861d4d1afb8c79899 in / 
# Tue, 13 Jul 2021 23:23:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2aeaf089064656dca36cf8480e9c7933a8c61fcc2a4c009ac61cbe442299cb68`  
		Last Modified: Tue, 13 Jul 2021 23:28:23 GMT  
		Size: 37.4 MB (37353027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:hirsute` - linux; s390x

```console
$ docker pull ubuntu@sha256:13532df2f7a272c2c973268db5264059be5ba9882962d30db3d86ca38db3a737
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32624229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6607c9291374f45aab3fd1bdfefc6a6cd48c14aff62ffe96458dd03ce44e3de9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 20:55:31 GMT
ADD file:bdac50808129a68a89c50670c12a81b904aa091dbd47eddb391da90ab245345d in / 
# Mon, 26 Jul 2021 20:55:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0dde1b40c8bf5cce712bb8e104aa59e911b2c25d8aabe5075842cec6026b2bea`  
		Last Modified: Mon, 26 Jul 2021 20:57:32 GMT  
		Size: 32.6 MB (32624229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:hirsute-20210711`

```console
$ docker pull ubuntu@sha256:20000a84ba67264b7f9a48f60b319a30d6898a41e1847ec809419f24fb40e634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:hirsute-20210711` - linux; amd64

```console
$ docker pull ubuntu@sha256:9aa325f4803f3d474c24f73211cbcc33c08d3956225fed1111591e1115d3d088
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31836858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f9a9836256862da05eacbb7d3d29eb267b03a0334cc72747ffc39d42b5703a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:57 GMT
ADD file:af305d3eb867f312743f97d1cbed14ee2a155fdfed4621c72a8e8cf25355660c in / 
# Tue, 13 Jul 2021 22:29:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:966b3c5c8637e41360eed39a59e6c16ee1e986f7f2b92244e4d39f7ca6669618`  
		Last Modified: Tue, 13 Jul 2021 22:31:57 GMT  
		Size: 31.8 MB (31836858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:hirsute-20210711` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:198eb162766bec2f17d3a0b63e108f0d3baa2777b2a57aae3cf5128d539f4518
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26853751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f456003eba6bf9ee07b68df86244805989efcd7b5087beb6bdfab6238485b1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:58 GMT
ADD file:5175798ab209bbc3941a05787751ecf9e7ba0b4e9cda31b044bd6d75e25976c8 in / 
# Tue, 13 Jul 2021 23:21:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fb746c2c12b45d26860f880a6e953018e4e9b83f9de17d11528fa484e1eb0f9f`  
		Last Modified: Tue, 13 Jul 2021 23:27:31 GMT  
		Size: 26.9 MB (26853751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:hirsute-20210711` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:b38344f77a057a937e8601487986798796375e45d058f0d6ef3cfb590acb8819
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30297903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ed560af6468524d70d787c18c8cb7ee425ffce3f04ca771a5ccd516d1f68df`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:46 GMT
ADD file:9e964afafcec670390a354fe9412da078ea83c247037612ce2b4c00c025cb4f1 in / 
# Tue, 13 Jul 2021 23:01:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cfe8b2632f122e3d77487867f2d08211ff277e78f8cb07a44832e91dd7c09ad7`  
		Last Modified: Tue, 13 Jul 2021 23:04:18 GMT  
		Size: 30.3 MB (30297903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:hirsute-20210711` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:364af8f243780dc910f18d8bdb54cfd6df023d779fd8df6961a83051c07d2548
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37353027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b509d66002487ee099dd5b99b3b5efc26c925a3f5b746783cd9547b42c0521bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:23:07 GMT
ADD file:20ba7c85b0d967e38fdb53a91f37ff0266687978ecc0791861d4d1afb8c79899 in / 
# Tue, 13 Jul 2021 23:23:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2aeaf089064656dca36cf8480e9c7933a8c61fcc2a4c009ac61cbe442299cb68`  
		Last Modified: Tue, 13 Jul 2021 23:28:23 GMT  
		Size: 37.4 MB (37353027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:hirsute-20210711` - linux; s390x

```console
$ docker pull ubuntu@sha256:d743dc5dbd73413eea8644d72b40dce08c9b44c6f0c5d72bc4c278dbb082ccd8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32623897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf0f5fa178a3cbac6f33d25b7745e5edc6e3e42f4bb7ea534d425f3500e0db1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:53:59 GMT
ADD file:3ee8a79599a2a708ba4baafd262055b8c2c472ee90e7dcc3275fe63e92944b8c in / 
# Tue, 13 Jul 2021 22:54:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a61bc2c77767fc8cabc22d8a497a56b3d5495549934b044350de2b9a1556ed4c`  
		Last Modified: Tue, 13 Jul 2021 22:56:16 GMT  
		Size: 32.6 MB (32623897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:impish`

```console
$ docker pull ubuntu@sha256:5f8e6f156c9340b3742db9de27f51cba8a7cccc7dfab75817252887cc1511c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:impish` - linux; amd64

```console
$ docker pull ubuntu@sha256:230c50db7d84d9a9ee76de505bd9405e043281a06e8398fb5efe086a8217bf40
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 MB (31519889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ecd4f42215a0a0851d38d400c65823b52bb27f957c78687bcd32f4cdec617a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:22:01 GMT
ADD file:aad4137373f37cc2272f1632b0fa50a91b4c0c878ca72ae8de8fee51ffa2f392 in / 
# Mon, 26 Jul 2021 21:22:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6c8d2949e37d3f87c8d42e502aebe8d287cc56bd1f5846a5265a2124c60cb49c`  
		Last Modified: Mon, 26 Jul 2021 21:24:04 GMT  
		Size: 31.5 MB (31519889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:impish` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:873e7a4ea0af5861c11a9dad1caa7c88ecddb60358260397e35fc5fc0fb69f99
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26874823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b12f2dccadd333f3317db06e660ff070b5b16adc349e366a307ef901fca3d5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:2888fa0aa4baaaed5388c590baea27cba3d71017f1a390bf10191b18f123114c in / 
# Tue, 13 Jul 2021 23:22:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7fbf6def801b74c6b0c1bfed8350c986239cbb5ed41824f04074b3be99d3d8eb`  
		Last Modified: Tue, 13 Jul 2021 23:28:07 GMT  
		Size: 26.9 MB (26874823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:impish` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:993294f9f183ba17a61857e31f589ddcda0e8f9636fc12d8fd34922f24539c36
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.0 MB (29955429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a502550fdd23593fa879034f3635c637f2ef98e14eaf72bbb07bbc27c2163e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:49:21 GMT
ADD file:da87b88a910a756b9836fda56f61b491974f97e66462db711cde71ecfd6d28d8 in / 
# Mon, 26 Jul 2021 21:49:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:745e0e9e37f685fd5013fb72549992db744cf1eef9c1d0f35661c7fa8c1ebbda`  
		Last Modified: Mon, 26 Jul 2021 21:52:08 GMT  
		Size: 30.0 MB (29955429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:impish` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:48f4289dcef78243d76861e5c7dc767f4d09c8b86c290835a9baa33034fe8d88
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37450815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369a2087639ab2667b4744b6c499a50611138db71cc72b09a00cc00afab2c4ac`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:23:30 GMT
ADD file:bd144e65c660dc138718837994b1fa3ea9593189413a61b63c8073bb1127532c in / 
# Tue, 13 Jul 2021 23:23:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:19f8a37977e3bfc6cc8d89c50cedc99d12151c43cd37c581e0fa522797296ca2`  
		Last Modified: Tue, 13 Jul 2021 23:28:48 GMT  
		Size: 37.5 MB (37450815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:impish` - linux; s390x

```console
$ docker pull ubuntu@sha256:e4ef4355021c080c0e8c0d7d3b2feadf39aa35be77a176545acccb583bcefc86
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.5 MB (32489596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411d5c16e75a11c33d66b4bb7e2047820890af1c44bcdbf4f089ae6aa5cd50bd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 20:55:42 GMT
ADD file:b6ec59f7691777c81f8a8700ed1da1845eda3e628f2711f38e3c61e05d7a4135 in / 
# Mon, 26 Jul 2021 20:55:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:983c674c63ce4a2e843b63eb159ebc7a37998bed4be834de0311107fb837ffba`  
		Last Modified: Mon, 26 Jul 2021 20:57:48 GMT  
		Size: 32.5 MB (32489596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:impish-20210711`

```console
$ docker pull ubuntu@sha256:4a6f8c3a917a830c22b2e41ad353e9c9b3e6710f36ed220a815f2a09cb3f7389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:impish-20210711` - linux; amd64

```console
$ docker pull ubuntu@sha256:a13f56ca6e8e420f14e520d3a9302356faf26fa29784bbc870a682cf2a62ea71
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31763760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722ec3d5541dcd1b429dcf41da7cd2eb58da388da6e656f07d8257d5e8e36c64`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:30:09 GMT
ADD file:fed31f525edbf4773d5c5dd77d89b40e3c4e2b018cd73ecdcfca8294b5daf963 in / 
# Tue, 13 Jul 2021 22:30:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a11e0c4b985a14790a9d1b7fc1c23c3e4534495df3ab94ab579474c7ed80abbb`  
		Last Modified: Tue, 13 Jul 2021 22:32:17 GMT  
		Size: 31.8 MB (31763760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:impish-20210711` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:873e7a4ea0af5861c11a9dad1caa7c88ecddb60358260397e35fc5fc0fb69f99
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26874823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b12f2dccadd333f3317db06e660ff070b5b16adc349e366a307ef901fca3d5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:2888fa0aa4baaaed5388c590baea27cba3d71017f1a390bf10191b18f123114c in / 
# Tue, 13 Jul 2021 23:22:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7fbf6def801b74c6b0c1bfed8350c986239cbb5ed41824f04074b3be99d3d8eb`  
		Last Modified: Tue, 13 Jul 2021 23:28:07 GMT  
		Size: 26.9 MB (26874823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:impish-20210711` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:3b32d8175be8b99f86a9f2aae3a423011aad12936088b06904ac7a809711c559
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 MB (30190328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518b847aad2ae444bc1a88aad4dbf09947e4e4a2dad7cbe3a80f5b47a3543096`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:01:57 GMT
ADD file:de726c8b286d17c655e46862c0d19a05b6322f245d12a64d4f081f86dbc50d57 in / 
# Tue, 13 Jul 2021 23:01:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b278a523c5f40181d31e0d016c0eb35135a9f686db2a8ded8ee3956984302028`  
		Last Modified: Tue, 13 Jul 2021 23:04:41 GMT  
		Size: 30.2 MB (30190328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:impish-20210711` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:48f4289dcef78243d76861e5c7dc767f4d09c8b86c290835a9baa33034fe8d88
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37450815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369a2087639ab2667b4744b6c499a50611138db71cc72b09a00cc00afab2c4ac`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:23:30 GMT
ADD file:bd144e65c660dc138718837994b1fa3ea9593189413a61b63c8073bb1127532c in / 
# Tue, 13 Jul 2021 23:23:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:19f8a37977e3bfc6cc8d89c50cedc99d12151c43cd37c581e0fa522797296ca2`  
		Last Modified: Tue, 13 Jul 2021 23:28:48 GMT  
		Size: 37.5 MB (37450815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:impish-20210711` - linux; s390x

```console
$ docker pull ubuntu@sha256:5c2f5d3d2de19cfd490ad801bc28594b41868854784cb7eb23b6b88aa35bec83
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32745092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c062c6069d01a0840ceb2cedc2e8986e1d32fe5f842a8afda35329a4a4c59309`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:54:13 GMT
ADD file:a30bdb91d78bd80aa66ed92daa416210251e82a5db9c5b47fde0ae75e6430cf0 in / 
# Tue, 13 Jul 2021 22:54:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3b3b22e2c6643e3694934a01b890529574080c32c43fd206b87f8e8de923a7e6`  
		Last Modified: Tue, 13 Jul 2021 22:56:31 GMT  
		Size: 32.7 MB (32745092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:latest`

```console
$ docker pull ubuntu@sha256:ec361466a06c1ba246ae5f429fce6680d51b79f528660e299833b72a3c20ec14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:latest` - linux; amd64

```console
$ docker pull ubuntu@sha256:1e48201ccc2ab83afc435394b3bf70af0fa0055215c1e26a5da9b50a1ae367c9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28567944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1318b700e415001198d1bf66d260b07f67ca8a552b61b0da02b3832c778f221b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:latest` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:8a2cbee49b50b0d08b01d4c31d70b72900f7668da53e8b4b9f1106a6443e4ca0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24062066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ce879b58c2cafb61a74c074b2e4339f8b97b15a7474e76315e809110937a05`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:08 GMT
ADD file:1ec1791cf8b61620293d0fdf83d76f3c07482a327aefef699a43e82e7c3aa0f0 in / 
# Tue, 13 Jul 2021 23:21:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5c5378967b4ed259bac71be5e1a9ea052469b5fe62bed34b19deb57d53dc63c0`  
		Last Modified: Tue, 13 Jul 2021 23:26:18 GMT  
		Size: 24.1 MB (24062066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:latest` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:c0dd38485ed8b6e149d2fc935d1c61a3b750cda3b3eace0ad6df4abe33fa2b90
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27170255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58810d071ecb79ca0ce412597417260d4ae8cbe1a2896c55dce7f02f3d8f36ac`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:latest` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:1030f108596afba03281f4c350466d74b900922c25e9881c7df6eefce6681080
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33287846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62bb28c580f7164b6f79bebec70a9e67dbc1d62c92a17f72fe287267014f5e6a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:cdca4c00902f291c6bc305420b891f5149b6833b5f9892232ea690d38adfff3f in / 
# Tue, 13 Jul 2021 23:22:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:157ef43c951ca9b65226089aef70b09df64b81636884260390a329c24a3c614b`  
		Last Modified: Tue, 13 Jul 2021 23:27:34 GMT  
		Size: 33.3 MB (33287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:latest` - linux; s390x

```console
$ docker pull ubuntu@sha256:0f745a413c7886d6dc4f1e6a1d45a5cf5a9a85f72e6243b307e17d67e2e1fe10
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27149898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14db5936efda0c6dd381ed7bb287bea8d5ccb027da8b97484564a85473f4dc77`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 20:55:12 GMT
ADD file:b8731edfdacfade2ec96757342f216962f3971b24077a9144da3f80003e6893e in / 
# Mon, 26 Jul 2021 20:55:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:38800a0044dea146ca3c3a08bc2c9c956396ad3241a3c343010775650298c379`  
		Last Modified: Mon, 26 Jul 2021 20:57:03 GMT  
		Size: 27.1 MB (27149898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:rolling`

```console
$ docker pull ubuntu@sha256:f734f5785fe15581fa062f65a9b64367d711d77ded6f5d94d3bebd842136ef48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:rolling` - linux; amd64

```console
$ docker pull ubuntu@sha256:ef8ee90cfa9cfc7c218586dea9daa6a8d1d191b3c73be143f4120fe140dae3d0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.8 MB (31837572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf70ebd2c444440ae068c5ccea80e2087906a825ff1019a9f6d6cbb229e33481`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:54 GMT
ADD file:6ae44786caae9af1c6b70dc9cc244e7d4e06fffc0696f68877527d69aa3fc735 in / 
# Mon, 26 Jul 2021 21:21:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4451f5c7eb7af74432585f5ebfbeb01bbfc87ec4a74dc93703bdd89330559cd1`  
		Last Modified: Mon, 26 Jul 2021 21:23:44 GMT  
		Size: 31.8 MB (31837572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:198eb162766bec2f17d3a0b63e108f0d3baa2777b2a57aae3cf5128d539f4518
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26853751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f456003eba6bf9ee07b68df86244805989efcd7b5087beb6bdfab6238485b1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:58 GMT
ADD file:5175798ab209bbc3941a05787751ecf9e7ba0b4e9cda31b044bd6d75e25976c8 in / 
# Tue, 13 Jul 2021 23:21:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fb746c2c12b45d26860f880a6e953018e4e9b83f9de17d11528fa484e1eb0f9f`  
		Last Modified: Tue, 13 Jul 2021 23:27:31 GMT  
		Size: 26.9 MB (26853751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:ca763e1a382a5b23f91abaf1c36a84be33da2d657f45746112f28ae010571041
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30299715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797e427e73c5159774c8eb88081f36b48516165ce1b20201afc4e6e54112c23f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:49:12 GMT
ADD file:878284607eb47bd96d58adc1bce14366656e20fede92cc0ff58787c14419cffe in / 
# Mon, 26 Jul 2021 21:49:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e34e08490be30f2dbe7ff29e0668c6e5aeba97f012896805dc1c38253e41bf42`  
		Last Modified: Mon, 26 Jul 2021 21:51:45 GMT  
		Size: 30.3 MB (30299715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:364af8f243780dc910f18d8bdb54cfd6df023d779fd8df6961a83051c07d2548
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37353027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b509d66002487ee099dd5b99b3b5efc26c925a3f5b746783cd9547b42c0521bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:23:07 GMT
ADD file:20ba7c85b0d967e38fdb53a91f37ff0266687978ecc0791861d4d1afb8c79899 in / 
# Tue, 13 Jul 2021 23:23:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2aeaf089064656dca36cf8480e9c7933a8c61fcc2a4c009ac61cbe442299cb68`  
		Last Modified: Tue, 13 Jul 2021 23:28:23 GMT  
		Size: 37.4 MB (37353027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:rolling` - linux; s390x

```console
$ docker pull ubuntu@sha256:13532df2f7a272c2c973268db5264059be5ba9882962d30db3d86ca38db3a737
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 MB (32624229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6607c9291374f45aab3fd1bdfefc6a6cd48c14aff62ffe96458dd03ce44e3de9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 26 Jul 2021 20:55:31 GMT
ADD file:bdac50808129a68a89c50670c12a81b904aa091dbd47eddb391da90ab245345d in / 
# Mon, 26 Jul 2021 20:55:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0dde1b40c8bf5cce712bb8e104aa59e911b2c25d8aabe5075842cec6026b2bea`  
		Last Modified: Mon, 26 Jul 2021 20:57:32 GMT  
		Size: 32.6 MB (32624229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:trusty`

```console
$ docker pull ubuntu@sha256:43cb19408de1e0ecf3ba5b5372ec98978963d6d0be42d0ad825e77a3bd16b5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `ubuntu:trusty` - linux; amd64

```console
$ docker pull ubuntu@sha256:881afbae521c910f764f7187dbfbca3cc10c26f8bafa458c76dda009a901c29d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70764430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b66b487594a1f2b75396013bc05d29d9f527852d96c5577cc4f187559875d0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:40 GMT
ADD file:276b5d943a4d284f8a7b249176a31f93d95e852480c2b851de287e53ff622bba in / 
# Thu, 25 Mar 2021 22:33:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:43 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2e6e20c8e2e69fa5c3fcc310f419975cef5fbeb6f7f2fe1374071141281b6a06`  
		Last Modified: Wed, 18 Dec 2019 13:21:28 GMT  
		Size: 70.7 MB (70691577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0551a797c01db074ab0233ceb567e66b8ebdcb9de9a2e7baa36d57dfbca463a3`  
		Last Modified: Thu, 25 Mar 2021 22:35:39 GMT  
		Size: 72.7 KB (72664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512123a864da5e2a62949e65b67106292c5c704eff90cac2b949fc8d7ac1e58e`  
		Last Modified: Thu, 25 Mar 2021 22:35:39 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:534255069ef3adf1c7a555fd9f614845ab66c61ef9846e438d86e12ae8c89b88
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64700978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2cd03315989aa8326f2c276922d3969994c1304b1310d2e0d33a26d94dd68ea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:23:03 GMT
ADD file:e9d55e059869915743a8ca8e64582d23c48fe7e90e439daccd56d3e08e8673b4 in / 
# Tue, 13 Jul 2021 23:23:06 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 13 Jul 2021 23:23:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Tue, 13 Jul 2021 23:23:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 13 Jul 2021 23:23:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0db3a87a3d7959895fd860c8b924980adda6e77f5d315b6676a4ac0e12518978`  
		Last Modified: Thu, 19 Dec 2019 06:16:01 GMT  
		Size: 64.6 MB (64624015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c5cd1be699257153c2a6de85968c2d9c413d87470dc4f540c5c3decbca8e47`  
		Last Modified: Tue, 13 Jul 2021 23:28:27 GMT  
		Size: 76.8 KB (76774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbf1c32ebce749806713a088af6ff1cbf7c75a8132d310ff391948e3e611ef6`  
		Last Modified: Tue, 13 Jul 2021 23:28:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:0fe9a82e42e32a74cca83fc84d5ab80b2ef73b7b90b7bab661b00ef3d16bfad9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66525503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423c4ed354ff1af8b464f13e25792ddb5e0a2c6baa22b5af909e68b557062eec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 May 2021 12:30:34 GMT
ADD file:b0eb0db52e323748ea9b8d7f8aecbc523a747619cd08663bab0fe60ab59bc60e in / 
# Thu, 27 May 2021 12:30:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 27 May 2021 12:30:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 27 May 2021 12:30:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 27 May 2021 12:30:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d1a5a1e51f251c3431dec02e2cc8d157e92d1b46913708ce9e600747a6274977`  
		Last Modified: Thu, 19 Dec 2019 03:57:08 GMT  
		Size: 66.5 MB (66466219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e84a55d935eb29baa4a459e89f330e090e7f9db90fbdd96f6c47b89c614c671`  
		Last Modified: Thu, 27 May 2021 12:33:16 GMT  
		Size: 59.1 KB (59096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a9c88d39064b3377476bafe5b4a86f498750df033058cc4a61194f2ca5540b`  
		Last Modified: Thu, 27 May 2021 12:33:16 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty` - linux; 386

```console
$ docker pull ubuntu@sha256:88152195106ff09bade23cb5aacfd26c381a8835c9d42124b4cba1dc3c2475e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68445499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f18ba408bae1426c4f394e045b16a140bc555e520d5eaacc97ac60ac5f298313`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:57:06 GMT
ADD file:e034601a525da53b0f39bb04d6e2264e2a592d0ae7c21e00697b9b62ca1efec9 in / 
# Thu, 25 Mar 2021 22:57:08 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:57:10 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:57:12 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:57:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:630712fe5783a35ad52a7026002143cb4f8fe65d34097dcaa4c4331b1b059a17`  
		Last Modified: Thu, 19 Dec 2019 04:44:02 GMT  
		Size: 68.4 MB (68380440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea2d50b5278097c6d027fc9fc0caf006649fcd94f094dde6ce578abe865ff21`  
		Last Modified: Thu, 25 Mar 2021 22:58:27 GMT  
		Size: 64.9 KB (64870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5795a499c24598e294527992a703053ab615879af048f3b809a3ad86141684d`  
		Last Modified: Thu, 25 Mar 2021 22:58:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:12d9fa858f255e4b70827aff83e8ce37b6fcaddaf6732276aa1f0763402f4fdc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73443156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02949c650aebaafb917ebe6bfd55a42505e22b38e8370878164051da4ae1bcc3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:24:04 GMT
ADD file:581665e92c72c8638b40fe509de6479dc1a5d7b5ffe8d6706006178c406e35e2 in / 
# Tue, 13 Jul 2021 23:24:24 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 13 Jul 2021 23:24:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Tue, 13 Jul 2021 23:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 13 Jul 2021 23:24:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bed4146d918c6c9a57bc3a8bf829e702975b0e53c7f25920fe9435b58ed6b64f`  
		Last Modified: Thu, 19 Dec 2019 04:26:52 GMT  
		Size: 73.4 MB (73379539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12aab203a69be44b1617f0da6b00b670e9016c3b00ab311b384ac3f859e86613`  
		Last Modified: Tue, 13 Jul 2021 23:29:07 GMT  
		Size: 63.4 KB (63430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1576c78d220b27404b5d0c3d635c36524229553e3ccf3b9a5ad4ca93c216c6c6`  
		Last Modified: Tue, 13 Jul 2021 23:29:07 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:trusty-20191217`

```console
$ docker pull ubuntu@sha256:43cb19408de1e0ecf3ba5b5372ec98978963d6d0be42d0ad825e77a3bd16b5f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `ubuntu:trusty-20191217` - linux; amd64

```console
$ docker pull ubuntu@sha256:881afbae521c910f764f7187dbfbca3cc10c26f8bafa458c76dda009a901c29d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70764430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b66b487594a1f2b75396013bc05d29d9f527852d96c5577cc4f187559875d0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:33:40 GMT
ADD file:276b5d943a4d284f8a7b249176a31f93d95e852480c2b851de287e53ff622bba in / 
# Thu, 25 Mar 2021 22:33:42 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:43 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:44 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2e6e20c8e2e69fa5c3fcc310f419975cef5fbeb6f7f2fe1374071141281b6a06`  
		Last Modified: Wed, 18 Dec 2019 13:21:28 GMT  
		Size: 70.7 MB (70691577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0551a797c01db074ab0233ceb567e66b8ebdcb9de9a2e7baa36d57dfbca463a3`  
		Last Modified: Thu, 25 Mar 2021 22:35:39 GMT  
		Size: 72.7 KB (72664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512123a864da5e2a62949e65b67106292c5c704eff90cac2b949fc8d7ac1e58e`  
		Last Modified: Thu, 25 Mar 2021 22:35:39 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty-20191217` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:534255069ef3adf1c7a555fd9f614845ab66c61ef9846e438d86e12ae8c89b88
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64700978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2cd03315989aa8326f2c276922d3969994c1304b1310d2e0d33a26d94dd68ea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:23:03 GMT
ADD file:e9d55e059869915743a8ca8e64582d23c48fe7e90e439daccd56d3e08e8673b4 in / 
# Tue, 13 Jul 2021 23:23:06 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 13 Jul 2021 23:23:07 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Tue, 13 Jul 2021 23:23:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 13 Jul 2021 23:23:10 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0db3a87a3d7959895fd860c8b924980adda6e77f5d315b6676a4ac0e12518978`  
		Last Modified: Thu, 19 Dec 2019 06:16:01 GMT  
		Size: 64.6 MB (64624015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c5cd1be699257153c2a6de85968c2d9c413d87470dc4f540c5c3decbca8e47`  
		Last Modified: Tue, 13 Jul 2021 23:28:27 GMT  
		Size: 76.8 KB (76774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbf1c32ebce749806713a088af6ff1cbf7c75a8132d310ff391948e3e611ef6`  
		Last Modified: Tue, 13 Jul 2021 23:28:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty-20191217` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:0fe9a82e42e32a74cca83fc84d5ab80b2ef73b7b90b7bab661b00ef3d16bfad9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66525503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423c4ed354ff1af8b464f13e25792ddb5e0a2c6baa22b5af909e68b557062eec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 May 2021 12:30:34 GMT
ADD file:b0eb0db52e323748ea9b8d7f8aecbc523a747619cd08663bab0fe60ab59bc60e in / 
# Thu, 27 May 2021 12:30:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 27 May 2021 12:30:36 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 27 May 2021 12:30:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 27 May 2021 12:30:37 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d1a5a1e51f251c3431dec02e2cc8d157e92d1b46913708ce9e600747a6274977`  
		Last Modified: Thu, 19 Dec 2019 03:57:08 GMT  
		Size: 66.5 MB (66466219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e84a55d935eb29baa4a459e89f330e090e7f9db90fbdd96f6c47b89c614c671`  
		Last Modified: Thu, 27 May 2021 12:33:16 GMT  
		Size: 59.1 KB (59096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a9c88d39064b3377476bafe5b4a86f498750df033058cc4a61194f2ca5540b`  
		Last Modified: Thu, 27 May 2021 12:33:16 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty-20191217` - linux; 386

```console
$ docker pull ubuntu@sha256:88152195106ff09bade23cb5aacfd26c381a8835c9d42124b4cba1dc3c2475e4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68445499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f18ba408bae1426c4f394e045b16a140bc555e520d5eaacc97ac60ac5f298313`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Mar 2021 22:57:06 GMT
ADD file:e034601a525da53b0f39bb04d6e2264e2a592d0ae7c21e00697b9b62ca1efec9 in / 
# Thu, 25 Mar 2021 22:57:08 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:57:10 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:57:12 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:57:12 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:630712fe5783a35ad52a7026002143cb4f8fe65d34097dcaa4c4331b1b059a17`  
		Last Modified: Thu, 19 Dec 2019 04:44:02 GMT  
		Size: 68.4 MB (68380440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea2d50b5278097c6d027fc9fc0caf006649fcd94f094dde6ce578abe865ff21`  
		Last Modified: Thu, 25 Mar 2021 22:58:27 GMT  
		Size: 64.9 KB (64870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5795a499c24598e294527992a703053ab615879af048f3b809a3ad86141684d`  
		Last Modified: Thu, 25 Mar 2021 22:58:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:trusty-20191217` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:12d9fa858f255e4b70827aff83e8ce37b6fcaddaf6732276aa1f0763402f4fdc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73443156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02949c650aebaafb917ebe6bfd55a42505e22b38e8370878164051da4ae1bcc3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:24:04 GMT
ADD file:581665e92c72c8638b40fe509de6479dc1a5d7b5ffe8d6706006178c406e35e2 in / 
# Tue, 13 Jul 2021 23:24:24 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 13 Jul 2021 23:24:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Tue, 13 Jul 2021 23:24:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 13 Jul 2021 23:24:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bed4146d918c6c9a57bc3a8bf829e702975b0e53c7f25920fe9435b58ed6b64f`  
		Last Modified: Thu, 19 Dec 2019 04:26:52 GMT  
		Size: 73.4 MB (73379539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12aab203a69be44b1617f0da6b00b670e9016c3b00ab311b384ac3f859e86613`  
		Last Modified: Tue, 13 Jul 2021 23:29:07 GMT  
		Size: 63.4 KB (63430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1576c78d220b27404b5d0c3d635c36524229553e3ccf3b9a5ad4ca93c216c6c6`  
		Last Modified: Tue, 13 Jul 2021 23:29:07 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:xenial`

```console
$ docker pull ubuntu@sha256:286df18fa087cdccc0699f0db1ee60bcdae63874949e51de80d1fa4e88362126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:xenial` - linux; amd64

```console
$ docker pull ubuntu@sha256:d388ba452d5f3f29399fc38c6928a65e4f28328a413c2edeee354569e7ab9bc9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46498913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b3fa4640d440e538e3d6fc4772c802c1a2d430e06c9a7920e654c7d7a601c9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:22:15 GMT
ADD file:a94a87e268e99c78143fae5148bd1200bf0da90c0e7f42bd8c168bb205ccb105 in / 
# Mon, 26 Jul 2021 21:22:16 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 26 Jul 2021 21:22:17 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 21:22:17 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 26 Jul 2021 21:22:18 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:52818491084148fa3469964bbcc3576686018a3b16b2e29be0407565c4c80b44`  
		Last Modified: Thu, 22 Jul 2021 16:25:00 GMT  
		Size: 46.5 MB (46497362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9df81d603d28f2a294b2f11b4f60d07b5b833b2ad7d6659a3f59b10cff2696`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636d9303bf663657be8e6796d720913bb985b5343da7949749ae1e72b54a88d8`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672b5bdcef61237567b311ad3d349f5eae18ba839ce2b204858a3083437a0a59`  
		Last Modified: Mon, 26 Jul 2021 21:24:20 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:8e6989d7f12e1da4143c511fcca0ad11098b8601f0ca3e67d85706b525b717ba
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40313964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5956828c6af7649d7427fddc47a47e342afa0d4c7b391854d21157d4566eb5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:23:36 GMT
ADD file:ef24ce1c15acdd071b2d61cd27d2840f1fa5eda4937dfe8746997eb677b1451b in / 
# Tue, 13 Jul 2021 23:23:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 13 Jul 2021 23:23:41 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:23:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 13 Jul 2021 23:23:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bee35c084ef2789f844b87c031d55b07186255622024a15b526838f71500485a`  
		Last Modified: Thu, 17 Jun 2021 23:36:42 GMT  
		Size: 40.3 MB (40312433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82fe22c8ad83979c361a3c4d3e782f4a311856511042ff7a107356ea1e21e694`  
		Last Modified: Tue, 13 Jul 2021 23:29:28 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6b9c580e9f54a056423dc1ea3c0923d41d6f18b5abd11a5364db40a8f79fc7`  
		Last Modified: Tue, 13 Jul 2021 23:29:28 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f964743b5fd175c6240d9e2a4d592ff013029f4edea14efaec9813e6c65607e5`  
		Last Modified: Tue, 13 Jul 2021 23:29:28 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:1a7c76d63d768423a9908192ee61b5f25ecabf170dc009575db16a7b6f001896
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41240249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22d4e143f7d0bf20bc1d4618f63bab0ede51d173a71c32cad2045b87e616d1f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:49:35 GMT
ADD file:8d25df96ee02448d932dfa08341eceeb82da056f3ad8cbd1d8b24f44903e1891 in / 
# Mon, 26 Jul 2021 21:49:36 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 26 Jul 2021 21:49:37 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 21:49:38 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 26 Jul 2021 21:49:38 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:2db5b739cd2a2fa296004e534a3fc4e7242f69130e59e1ff05a9e4ad4f7cd065`  
		Last Modified: Thu, 22 Jul 2021 16:25:06 GMT  
		Size: 41.2 MB (41238757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93da29956c4eb74ce61ad792d432dfe58787feb50bab77ef54679401df1ea22`  
		Last Modified: Mon, 26 Jul 2021 21:52:29 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3db33f994681db66c25858a525daaf3fde2cab655a638ab5f8e9adefcff34ff`  
		Last Modified: Mon, 26 Jul 2021 21:52:28 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ee9f14ba300ddf2ab6c21beb83fd70be989d93c2cb9de39ef70c61e3756041`  
		Last Modified: Mon, 26 Jul 2021 21:52:28 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial` - linux; 386

```console
$ docker pull ubuntu@sha256:2acaf9eb4e50288bbb05b8238115b0cbf6f530985f2f9fc4c990224b8fa2b175
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45817296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26be9de5d32195fcef6cf4aa1cf46d5e86644d03ea1e905bfe051aa3e878e7e9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Jul 2021 21:19:12 GMT
ADD file:1b452fb9ede26959ad4e77cdde24fd29b55e6f0e25fc9e449602eec28f91a97f in / 
# Mon, 26 Jul 2021 21:19:13 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 26 Jul 2021 21:19:14 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 21:19:15 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 26 Jul 2021 21:19:15 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6002ee25903147b62d44ed293c693c455db05e98fd6ee23de5566fecd1b94976`  
		Last Modified: Sat, 24 Jul 2021 22:43:34 GMT  
		Size: 45.8 MB (45815767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ebdd5137a750012174bcd408c7694f556d634de6d88eba053ea1865ec748809`  
		Last Modified: Mon, 26 Jul 2021 21:20:06 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e3facc8a281e63600ff451ccddd3e05b486726b9d9830b3de0726a8fefa074`  
		Last Modified: Mon, 26 Jul 2021 21:20:06 GMT  
		Size: 513.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7c8d8d34eaa9f414196f696ad2c62d1475973b2af07051c7e0eabac0ee86af`  
		Last Modified: Mon, 26 Jul 2021 21:20:06 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:412a6b8de102ebb781f558bcd5b66c96b0e6f9ee03fe30f566f09adf10480be0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47523790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4272e7d863f9da1994f2c32dfbb235c9284a7c5f923b0322c34f851eb4f08ab9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:25:11 GMT
ADD file:02f85c6f12364eaad4f80464effd781403b4c13c7732005ee3731d0d19a353c2 in / 
# Tue, 13 Jul 2021 23:25:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 13 Jul 2021 23:25:39 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:25:53 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 13 Jul 2021 23:25:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:77800700d823a40e3888379b1764dd49f1e6630a1848579e18e69c1dcc8f2558`  
		Last Modified: Thu, 17 Jun 2021 23:30:08 GMT  
		Size: 47.5 MB (47522284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0babf75a176b58db3a5df6096af29a306bf0ab34aed69816ecea017482b6ba6`  
		Last Modified: Tue, 13 Jul 2021 23:29:36 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aeb0805a3ad55f25fa2e52d341de43543d44705d05021e2d6a3ed9944915319`  
		Last Modified: Tue, 13 Jul 2021 23:29:36 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4421ae6a1a8096772ab2b5bb7d32cf300fbe5ffbe18cb6c742591febaf3bd7f`  
		Last Modified: Tue, 13 Jul 2021 23:29:36 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial` - linux; s390x

```console
$ docker pull ubuntu@sha256:13e9225a811698640577aef27c56f546d743519fd9301c9390d6ca1719f499a5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44089195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc5b5d39032a643edc9ae9b978586671c31c6bb5daa6a252ba6d8d7af7240b0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Jul 2021 20:55:52 GMT
ADD file:f5f56e2b2627da261a6178062e9bfac93ae66da8659cd0a443b6c9f6287084f8 in / 
# Mon, 26 Jul 2021 20:55:55 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 26 Jul 2021 20:55:56 GMT
RUN rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 20:55:57 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 26 Jul 2021 20:55:57 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0c85d52c5ad3f29826fe14cb11a9f94f5d0c766f47650e87720d614da0cba3c1`  
		Last Modified: Mon, 26 Jul 2021 20:58:05 GMT  
		Size: 44.1 MB (44087711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2a7580361ee0c51ed09eb59644c3edbca7639cdfee2ec4e3d921c8dd727339`  
		Last Modified: Mon, 26 Jul 2021 20:57:59 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56a77a0e6f8d9080c5c646f408f9a2aa52d5bacda38df1493fffaa4cd9b86fd`  
		Last Modified: Mon, 26 Jul 2021 20:57:59 GMT  
		Size: 467.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601f88d7e167a476b34623c363d7e5cc619faa8efa7e4f169093d342f1da402c`  
		Last Modified: Mon, 26 Jul 2021 20:57:59 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ubuntu:xenial-20210611`

```console
$ docker pull ubuntu@sha256:1b733ff6c7c7aac32101a35cb2c6399ca8c399a9f6de62a386abe26c65b59b9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ubuntu:xenial-20210611` - linux; amd64

```console
$ docker pull ubuntu@sha256:114bbce1997fa476da56c3958cb3ca13269a54b0a97dfd3667543c7778287bf2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46498331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065cf14a189c6220b58634f2d6d8952e52eeb02c1cd36070e4b48a65eff37251`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:32:06 GMT
ADD file:4dd75f16753c9c921fd05b1d0ed5b425d74d87405a76a0b3afcbf9723a50d1ce in / 
# Thu, 17 Jun 2021 23:32:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 17 Jun 2021 23:32:08 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 17 Jun 2021 23:32:09 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 17 Jun 2021 23:32:09 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:61e03ba1d4149ac4eb681c6bf75aef8ac4b3f0d6fbb08e9623c4089889396fc8`  
		Last Modified: Sat, 12 Jun 2021 00:25:16 GMT  
		Size: 46.5 MB (46496785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afb39f216bd4e336f9b78584bae0f6bcb77150107471d8d67d3b8abfbdea46a`  
		Last Modified: Thu, 17 Jun 2021 23:34:09 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e489abdc9f902f737bfef2c0c7ff5c35ca9b3ca11e73405a472f31a25f2dcc69`  
		Last Modified: Thu, 17 Jun 2021 23:34:08 GMT  
		Size: 528.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999fff7bcc2450fcf1210182802f3907e35cd7cf7569568bd2a179b9144d9c57`  
		Last Modified: Thu, 17 Jun 2021 23:34:08 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial-20210611` - linux; arm variant v7

```console
$ docker pull ubuntu@sha256:8e6989d7f12e1da4143c511fcca0ad11098b8601f0ca3e67d85706b525b717ba
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.3 MB (40313964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5956828c6af7649d7427fddc47a47e342afa0d4c7b391854d21157d4566eb5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:23:36 GMT
ADD file:ef24ce1c15acdd071b2d61cd27d2840f1fa5eda4937dfe8746997eb677b1451b in / 
# Tue, 13 Jul 2021 23:23:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 13 Jul 2021 23:23:41 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:23:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 13 Jul 2021 23:23:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:bee35c084ef2789f844b87c031d55b07186255622024a15b526838f71500485a`  
		Last Modified: Thu, 17 Jun 2021 23:36:42 GMT  
		Size: 40.3 MB (40312433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82fe22c8ad83979c361a3c4d3e782f4a311856511042ff7a107356ea1e21e694`  
		Last Modified: Tue, 13 Jul 2021 23:29:28 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6b9c580e9f54a056423dc1ea3c0923d41d6f18b5abd11a5364db40a8f79fc7`  
		Last Modified: Tue, 13 Jul 2021 23:29:28 GMT  
		Size: 511.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f964743b5fd175c6240d9e2a4d592ff013029f4edea14efaec9813e6c65607e5`  
		Last Modified: Tue, 13 Jul 2021 23:29:28 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial-20210611` - linux; arm64 variant v8

```console
$ docker pull ubuntu@sha256:8643d2dd3d66c303577420db92add571953f9e8ec96b132945739726cf038957
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41241394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef6fd310d3ea5e8f8b0ea361d9be4303696123c292d49911f42386bc1eafb31`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:54:40 GMT
ADD file:2675f90ace0ec88b2cdadc737d15d701b544bf2113480e898d0014a79dca13c7 in / 
# Thu, 17 Jun 2021 23:54:41 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 17 Jun 2021 23:54:42 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 17 Jun 2021 23:54:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 17 Jun 2021 23:54:43 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e2a24739a48e2c634f94c2cb69ead6b0ff1c84cedd9624eb29560b83c3eb6e0e`  
		Last Modified: Sat, 12 Jun 2021 00:25:19 GMT  
		Size: 41.2 MB (41239907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6732798425e9389fa6bd92caa59cd7de853b4cf01a7166724e26a430ec7211f`  
		Last Modified: Thu, 17 Jun 2021 23:57:28 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0af2bd04c3cb9d221318d494c05b29dd4b7c46886de97baee11fbd40723ab8`  
		Last Modified: Thu, 17 Jun 2021 23:57:28 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835469060484e7130eb258c8dfae8e4b1f8035c63bba23ab6e4f3e9b53a6cf1e`  
		Last Modified: Thu, 17 Jun 2021 23:57:28 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial-20210611` - linux; 386

```console
$ docker pull ubuntu@sha256:45415347f7e26415834d185cddbe8467b6c8af67452d16df8704f0ecdfea3c9a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45817159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac00878e8ff80d11ab497179500a31ba571485e18f34c716f63feb6b0f5d0428`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 17 Jun 2021 23:48:13 GMT
ADD file:405fb6ba2e4fcf060e027f7a0aad340b7aee637d50ec097aff59e15609bfc2c1 in / 
# Thu, 17 Jun 2021 23:48:14 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 17 Jun 2021 23:48:15 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 17 Jun 2021 23:48:16 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 17 Jun 2021 23:48:16 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:eca348360c85efd796e52ecf73e5add735eabf7e041356b47c87947e8a749e00`  
		Last Modified: Thu, 17 Jun 2021 23:49:12 GMT  
		Size: 45.8 MB (45815621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07150c0d356ea8abd3017d76adc6703dd76f0d1a9b03dfb86c9cb300b1a72d36`  
		Last Modified: Thu, 17 Jun 2021 23:49:03 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aaa5e08eb74cc48d87e687b4a660f7f9475de83f25661f2709740db81c41849`  
		Last Modified: Thu, 17 Jun 2021 23:49:03 GMT  
		Size: 517.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febb5fbfe0775e00dd59ff4f626d510952d83748697c62d0c6d18cd9bc8a256c`  
		Last Modified: Thu, 17 Jun 2021 23:49:03 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial-20210611` - linux; ppc64le

```console
$ docker pull ubuntu@sha256:412a6b8de102ebb781f558bcd5b66c96b0e6f9ee03fe30f566f09adf10480be0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47523790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4272e7d863f9da1994f2c32dfbb235c9284a7c5f923b0322c34f851eb4f08ab9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jul 2021 23:25:11 GMT
ADD file:02f85c6f12364eaad4f80464effd781403b4c13c7732005ee3731d0d19a353c2 in / 
# Tue, 13 Jul 2021 23:25:25 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 13 Jul 2021 23:25:39 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 23:25:53 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 13 Jul 2021 23:25:59 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:77800700d823a40e3888379b1764dd49f1e6630a1848579e18e69c1dcc8f2558`  
		Last Modified: Thu, 17 Jun 2021 23:30:08 GMT  
		Size: 47.5 MB (47522284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0babf75a176b58db3a5df6096af29a306bf0ab34aed69816ecea017482b6ba6`  
		Last Modified: Tue, 13 Jul 2021 23:29:36 GMT  
		Size: 859.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aeb0805a3ad55f25fa2e52d341de43543d44705d05021e2d6a3ed9944915319`  
		Last Modified: Tue, 13 Jul 2021 23:29:36 GMT  
		Size: 476.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4421ae6a1a8096772ab2b5bb7d32cf300fbe5ffbe18cb6c742591febaf3bd7f`  
		Last Modified: Tue, 13 Jul 2021 23:29:36 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ubuntu:xenial-20210611` - linux; s390x

```console
$ docker pull ubuntu@sha256:12b3037c258c44e4f4cb58f973da1061b3e0c4b77aee5bdfb8b1c1e9cbacf901
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44089617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc005875d9a3b856b5784b8c4606b4de9906a42ec455e4ab777f2faef2082062`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Jul 2021 22:54:28 GMT
ADD file:fe2f2172ef6c28729fe2906a3edd50a39e2ff612da510584327898429dd0b2c8 in / 
# Tue, 13 Jul 2021 22:54:32 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 13 Jul 2021 22:54:34 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 13 Jul 2021 22:54:36 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 13 Jul 2021 22:54:36 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5e94e6b2e2a61afc38e8c32f4b5cadc2ec32d2f223781d4ee4203e2e6b096a37`  
		Last Modified: Thu, 17 Jun 2021 23:46:23 GMT  
		Size: 44.1 MB (44088123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabfb1a7eacd3ce7cebc95a8e4a2552e56450e2ec1b036516b1bb09c4d22df48`  
		Last Modified: Tue, 13 Jul 2021 22:56:42 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c115486bffc8ae23d8bc9beb85e9cbd574b177de6a231bb437729902809aaf2`  
		Last Modified: Tue, 13 Jul 2021 22:56:42 GMT  
		Size: 470.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddfacfd07c012e416dfec6566c58456afbfad6dd84efd5d26b0339376edb6f1`  
		Last Modified: Tue, 13 Jul 2021 22:56:42 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

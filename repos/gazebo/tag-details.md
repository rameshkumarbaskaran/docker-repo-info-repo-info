<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `gazebo`

-	[`gazebo:gzserver11`](#gazebogzserver11)
-	[`gazebo:gzserver11-bionic`](#gazebogzserver11-bionic)
-	[`gazebo:gzserver11-focal`](#gazebogzserver11-focal)
-	[`gazebo:gzserver9`](#gazebogzserver9)
-	[`gazebo:gzserver9-bionic`](#gazebogzserver9-bionic)
-	[`gazebo:gzserver9-xenial`](#gazebogzserver9-xenial)
-	[`gazebo:latest`](#gazebolatest)
-	[`gazebo:libgazebo11`](#gazebolibgazebo11)
-	[`gazebo:libgazebo11-bionic`](#gazebolibgazebo11-bionic)
-	[`gazebo:libgazebo11-focal`](#gazebolibgazebo11-focal)
-	[`gazebo:libgazebo9`](#gazebolibgazebo9)
-	[`gazebo:libgazebo9-bionic`](#gazebolibgazebo9-bionic)
-	[`gazebo:libgazebo9-xenial`](#gazebolibgazebo9-xenial)

## `gazebo:gzserver11`

```console
$ docker pull gazebo@sha256:a88348012ee79d7a266771a8054e7c52cd0dc6d6bd71e191cf9c498d292b6ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver11` - linux; amd64

```console
$ docker pull gazebo@sha256:17217e15fbb50a0873f3745d4902ca47a4bba8cdb13d5db0764efa89717dbde5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318254000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4ebc9b8cc646a267b606a9085691cc7ece1005d2bcba8b8e33837c7e0f37d0`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

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
# Sat, 24 Apr 2021 00:05:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:06:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:06:02 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Sat, 24 Apr 2021 00:06:03 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Sat, 24 Apr 2021 00:09:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:09:43 GMT
EXPOSE 11345
# Sat, 24 Apr 2021 00:09:43 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Sat, 24 Apr 2021 00:09:43 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Sat, 24 Apr 2021 00:09:43 GMT
CMD ["gzserver"]
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
	-	`sha256:62f60c1e15de5890db12b66dcdc9fead43b285bea7d10d147a7baddfe0093488`  
		Last Modified: Sat, 24 Apr 2021 00:20:37 GMT  
		Size: 1.2 MB (1183512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a84e3d913f988af95e954537fcffb78eb9c9c3d5b91f5cdcf02a1f1c932a6d5`  
		Last Modified: Sat, 24 Apr 2021 00:20:37 GMT  
		Size: 16.2 MB (16150269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b47f933436cc57965cecdb865715bb01535d7aa664ecd5aaa38504b7d29a5a5`  
		Last Modified: Sat, 24 Apr 2021 00:20:34 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c28531c6ee3b84f26807ed129be1a1966692c7120ecfe5685853ca4d6a0873`  
		Last Modified: Sat, 24 Apr 2021 00:20:33 GMT  
		Size: 5.5 KB (5501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8ad6644768422c5ad05afb901373b192e8b3b226361adb1d3b00e49afe5901`  
		Last Modified: Sat, 24 Apr 2021 00:21:10 GMT  
		Size: 272.4 MB (272372428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d9815765b2ed56b325178f5b8015e18283270d5cce085d15a2ba4146a5df73c`  
		Last Modified: Sat, 24 Apr 2021 00:20:36 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:gzserver11-bionic`

```console
$ docker pull gazebo@sha256:86a966e20e6018d8f83567adbb7e9449b7ed9a04f4fec0c9617fc7264acd0ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver11-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:ce1e742f45097f89a7718bb33ceeaf31b0993b33df6c74d89c622979c5b9437e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 MB (277382489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32059d3e1e42ac338a293643cee49711138b41340ace5c1795697b45352f15c`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:22 GMT
ADD file:d7fa3c26651f9204a5629287a1a9a6e7dc6a0bc6eb499e82c433c0c8f67ff46b in / 
# Fri, 23 Apr 2021 22:21:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:25 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:54:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:54:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:54:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Fri, 23 Apr 2021 23:54:24 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Sat, 24 Apr 2021 00:03:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:03:50 GMT
EXPOSE 11345
# Sat, 24 Apr 2021 00:03:50 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Sat, 24 Apr 2021 00:03:51 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Sat, 24 Apr 2021 00:03:51 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:01bf7da0a88c9e37ae418d17c0aeed0621524848d80ccb9e38c67e7ab8e11928`  
		Last Modified: Fri, 16 Apr 2021 15:20:23 GMT  
		Size: 26.7 MB (26697009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b4a5f15c7a0722b4f22e61b5387317eaf2602c27ffb2bceac9a25f19fbd156`  
		Last Modified: Fri, 23 Apr 2021 22:22:45 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ffbe87baa135002dddb7a7460082c5d6a352186e1be9464c5f31db81378824`  
		Last Modified: Fri, 23 Apr 2021 22:22:45 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfad5d88235e65844b7c8944e2bd9a0cacde3a1ea196f87712547e7b0a19c3f`  
		Last Modified: Sat, 24 Apr 2021 00:17:26 GMT  
		Size: 841.6 KB (841642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b1efce7c1b75033060ddc06d651f1eed0c3b69c9a10650783d1338a8de16e7`  
		Last Modified: Sat, 24 Apr 2021 00:17:25 GMT  
		Size: 14.7 MB (14702594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2167b3eed350794a813a746a5221289779308d78aaa084b713ed9d9fe83250e`  
		Last Modified: Sat, 24 Apr 2021 00:17:22 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022f6080d75ae23a63af8b6f85496b1763e39be8adf414b532ba5c7c93d3ef5e`  
		Last Modified: Sat, 24 Apr 2021 00:17:22 GMT  
		Size: 5.5 KB (5462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f475d88930aab6fd2bc423304e95eb6f4986e4361e074070ba551f702f5ab2e`  
		Last Modified: Sat, 24 Apr 2021 00:19:31 GMT  
		Size: 235.1 MB (235133116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a928237d4f0f84c1e386b53ce4054080816dccd327881244f9bd349d49bc561`  
		Last Modified: Sat, 24 Apr 2021 00:19:00 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:gzserver11-focal`

```console
$ docker pull gazebo@sha256:a88348012ee79d7a266771a8054e7c52cd0dc6d6bd71e191cf9c498d292b6ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver11-focal` - linux; amd64

```console
$ docker pull gazebo@sha256:17217e15fbb50a0873f3745d4902ca47a4bba8cdb13d5db0764efa89717dbde5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318254000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4ebc9b8cc646a267b606a9085691cc7ece1005d2bcba8b8e33837c7e0f37d0`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

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
# Sat, 24 Apr 2021 00:05:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:06:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:06:02 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Sat, 24 Apr 2021 00:06:03 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Sat, 24 Apr 2021 00:09:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:09:43 GMT
EXPOSE 11345
# Sat, 24 Apr 2021 00:09:43 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Sat, 24 Apr 2021 00:09:43 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Sat, 24 Apr 2021 00:09:43 GMT
CMD ["gzserver"]
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
	-	`sha256:62f60c1e15de5890db12b66dcdc9fead43b285bea7d10d147a7baddfe0093488`  
		Last Modified: Sat, 24 Apr 2021 00:20:37 GMT  
		Size: 1.2 MB (1183512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a84e3d913f988af95e954537fcffb78eb9c9c3d5b91f5cdcf02a1f1c932a6d5`  
		Last Modified: Sat, 24 Apr 2021 00:20:37 GMT  
		Size: 16.2 MB (16150269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b47f933436cc57965cecdb865715bb01535d7aa664ecd5aaa38504b7d29a5a5`  
		Last Modified: Sat, 24 Apr 2021 00:20:34 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c28531c6ee3b84f26807ed129be1a1966692c7120ecfe5685853ca4d6a0873`  
		Last Modified: Sat, 24 Apr 2021 00:20:33 GMT  
		Size: 5.5 KB (5501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8ad6644768422c5ad05afb901373b192e8b3b226361adb1d3b00e49afe5901`  
		Last Modified: Sat, 24 Apr 2021 00:21:10 GMT  
		Size: 272.4 MB (272372428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d9815765b2ed56b325178f5b8015e18283270d5cce085d15a2ba4146a5df73c`  
		Last Modified: Sat, 24 Apr 2021 00:20:36 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:gzserver9`

```console
$ docker pull gazebo@sha256:907c8d757fc8fe7f591c805cf65a120564ab2cc7e6d0ba090862ae65f7df360f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver9` - linux; amd64

```console
$ docker pull gazebo@sha256:8470d88911667d5a6326b12a8e711d4925dc6441b48fffb605fe9bbe0e229fc6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.4 MB (268368878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00db7ed7799a0962bb245f29da1b23a2474410a5f45f1485d78b4a9f801ce632`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:22 GMT
ADD file:d7fa3c26651f9204a5629287a1a9a6e7dc6a0bc6eb499e82c433c0c8f67ff46b in / 
# Fri, 23 Apr 2021 22:21:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:25 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:54:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:54:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:54:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Fri, 23 Apr 2021 23:54:24 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Wed, 28 Apr 2021 19:13:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.17.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 28 Apr 2021 19:13:28 GMT
EXPOSE 11345
# Wed, 28 Apr 2021 19:13:29 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Wed, 28 Apr 2021 19:13:29 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Wed, 28 Apr 2021 19:13:29 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:01bf7da0a88c9e37ae418d17c0aeed0621524848d80ccb9e38c67e7ab8e11928`  
		Last Modified: Fri, 16 Apr 2021 15:20:23 GMT  
		Size: 26.7 MB (26697009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b4a5f15c7a0722b4f22e61b5387317eaf2602c27ffb2bceac9a25f19fbd156`  
		Last Modified: Fri, 23 Apr 2021 22:22:45 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ffbe87baa135002dddb7a7460082c5d6a352186e1be9464c5f31db81378824`  
		Last Modified: Fri, 23 Apr 2021 22:22:45 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfad5d88235e65844b7c8944e2bd9a0cacde3a1ea196f87712547e7b0a19c3f`  
		Last Modified: Sat, 24 Apr 2021 00:17:26 GMT  
		Size: 841.6 KB (841642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b1efce7c1b75033060ddc06d651f1eed0c3b69c9a10650783d1338a8de16e7`  
		Last Modified: Sat, 24 Apr 2021 00:17:25 GMT  
		Size: 14.7 MB (14702594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2167b3eed350794a813a746a5221289779308d78aaa084b713ed9d9fe83250e`  
		Last Modified: Sat, 24 Apr 2021 00:17:22 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022f6080d75ae23a63af8b6f85496b1763e39be8adf414b532ba5c7c93d3ef5e`  
		Last Modified: Sat, 24 Apr 2021 00:17:22 GMT  
		Size: 5.5 KB (5462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eabad2f1e30aa275f7020a73e7de0e8a97a32bc118f054bf82728eb193e2afc9`  
		Last Modified: Wed, 28 Apr 2021 19:19:44 GMT  
		Size: 226.1 MB (226119504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b5cb82b4c59623b5f8c6e65ecdc7c2ab0f5e9fa8867dfdd8241053f70b5110`  
		Last Modified: Wed, 28 Apr 2021 19:19:13 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:gzserver9-bionic`

```console
$ docker pull gazebo@sha256:907c8d757fc8fe7f591c805cf65a120564ab2cc7e6d0ba090862ae65f7df360f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver9-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:8470d88911667d5a6326b12a8e711d4925dc6441b48fffb605fe9bbe0e229fc6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.4 MB (268368878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00db7ed7799a0962bb245f29da1b23a2474410a5f45f1485d78b4a9f801ce632`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:22 GMT
ADD file:d7fa3c26651f9204a5629287a1a9a6e7dc6a0bc6eb499e82c433c0c8f67ff46b in / 
# Fri, 23 Apr 2021 22:21:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:25 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:54:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:54:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:54:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Fri, 23 Apr 2021 23:54:24 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Wed, 28 Apr 2021 19:13:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.17.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 28 Apr 2021 19:13:28 GMT
EXPOSE 11345
# Wed, 28 Apr 2021 19:13:29 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Wed, 28 Apr 2021 19:13:29 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Wed, 28 Apr 2021 19:13:29 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:01bf7da0a88c9e37ae418d17c0aeed0621524848d80ccb9e38c67e7ab8e11928`  
		Last Modified: Fri, 16 Apr 2021 15:20:23 GMT  
		Size: 26.7 MB (26697009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b4a5f15c7a0722b4f22e61b5387317eaf2602c27ffb2bceac9a25f19fbd156`  
		Last Modified: Fri, 23 Apr 2021 22:22:45 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ffbe87baa135002dddb7a7460082c5d6a352186e1be9464c5f31db81378824`  
		Last Modified: Fri, 23 Apr 2021 22:22:45 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfad5d88235e65844b7c8944e2bd9a0cacde3a1ea196f87712547e7b0a19c3f`  
		Last Modified: Sat, 24 Apr 2021 00:17:26 GMT  
		Size: 841.6 KB (841642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b1efce7c1b75033060ddc06d651f1eed0c3b69c9a10650783d1338a8de16e7`  
		Last Modified: Sat, 24 Apr 2021 00:17:25 GMT  
		Size: 14.7 MB (14702594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2167b3eed350794a813a746a5221289779308d78aaa084b713ed9d9fe83250e`  
		Last Modified: Sat, 24 Apr 2021 00:17:22 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022f6080d75ae23a63af8b6f85496b1763e39be8adf414b532ba5c7c93d3ef5e`  
		Last Modified: Sat, 24 Apr 2021 00:17:22 GMT  
		Size: 5.5 KB (5462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eabad2f1e30aa275f7020a73e7de0e8a97a32bc118f054bf82728eb193e2afc9`  
		Last Modified: Wed, 28 Apr 2021 19:19:44 GMT  
		Size: 226.1 MB (226119504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b5cb82b4c59623b5f8c6e65ecdc7c2ab0f5e9fa8867dfdd8241053f70b5110`  
		Last Modified: Wed, 28 Apr 2021 19:19:13 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:gzserver9-xenial`

```console
$ docker pull gazebo@sha256:f6c3e06f6180b1d60bfb70f29dad1a53a6086dcd2751c54a885b760306eab37f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:gzserver9-xenial` - linux; amd64

```console
$ docker pull gazebo@sha256:3d367ccf7a7514c0be9014bd75870a6cb161cba32efbe21abc9b5bde658af030
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.7 MB (270664130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6c3dfce853895158b2949fd885dc4aa1b8e5a7b2bc3e451ead67e7b9e67162`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 23 Apr 2021 22:22:16 GMT
ADD file:34f9c325bb2e6ad9f9a062ce9a0237fab0c04aea83f31b8548ea0ae532255be0 in / 
# Fri, 23 Apr 2021 22:22:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:22:18 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:22:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:22:19 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:48:31 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:48:33 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Fri, 23 Apr 2021 23:48:34 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Wed, 28 Apr 2021 19:05:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.17.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 28 Apr 2021 19:05:33 GMT
EXPOSE 11345
# Wed, 28 Apr 2021 19:05:33 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Wed, 28 Apr 2021 19:05:33 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Wed, 28 Apr 2021 19:05:34 GMT
CMD ["gzserver"]
```

-	Layers:
	-	`sha256:92473f7ef45574f608989888a6cfc8187d3a1425e3a63f974434acab03fed068`  
		Last Modified: Sat, 17 Apr 2021 15:20:07 GMT  
		Size: 46.3 MB (46254451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb52bde70123ac7f3a1b88fee95e74f4bdcdbd81917a91a35b56a52ec7671947`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64788f86be3fd71809b5de602deff9445f3de18d2f44a49d0a053dfc9a2008ae`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f6d5f2e001ababe3ddac4731d9c33121e1148ef32a87a83a5b470cb401abef`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340f215ec5582c3709c8edd826b45865536aee4a0e309b5eaf54bbae4ec4bf2f`  
		Last Modified: Sat, 24 Apr 2021 00:15:49 GMT  
		Size: 16.3 MB (16279968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9887fad184bfee18f93dc0728afcc29ef5a9413cc8e7dd66e94fb7a803959a87`  
		Last Modified: Sat, 24 Apr 2021 00:15:45 GMT  
		Size: 14.8 KB (14759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaaacc64da264322798a93c66aec28cfa0fea4a1cb0cebe2694cd18209fe74a8`  
		Last Modified: Sat, 24 Apr 2021 00:15:45 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5680ec8f99db4c4e5829e2d9d0fa07bbc48283956e97a4acf18748fcadb5903`  
		Last Modified: Wed, 28 Apr 2021 19:18:12 GMT  
		Size: 208.1 MB (208107667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc43beaaffbed249b82082f7a46abcf704a03fd57ec97d63722c0652a91f897`  
		Last Modified: Wed, 28 Apr 2021 19:17:45 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:latest`

```console
$ docker pull gazebo@sha256:ccf75e79db3de7e55bf113d4b96ae5d4db8840dc71a73d3ffaa5d0143d040623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:latest` - linux; amd64

```console
$ docker pull gazebo@sha256:504956d2050fe3ef5a1dbab5aeee02d89ffaca5604d275a701fc8952287c1b7d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.6 MB (598620455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1a4995df9bd0f7e8e8b1103d5c0d5f701e55bebcca0a327c1917e0b2513749`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

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
# Sat, 24 Apr 2021 00:05:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:06:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:06:02 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Sat, 24 Apr 2021 00:06:03 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Sat, 24 Apr 2021 00:09:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:09:43 GMT
EXPOSE 11345
# Sat, 24 Apr 2021 00:09:43 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Sat, 24 Apr 2021 00:09:43 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Sat, 24 Apr 2021 00:09:43 GMT
CMD ["gzserver"]
# Sat, 24 Apr 2021 00:15:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:62f60c1e15de5890db12b66dcdc9fead43b285bea7d10d147a7baddfe0093488`  
		Last Modified: Sat, 24 Apr 2021 00:20:37 GMT  
		Size: 1.2 MB (1183512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a84e3d913f988af95e954537fcffb78eb9c9c3d5b91f5cdcf02a1f1c932a6d5`  
		Last Modified: Sat, 24 Apr 2021 00:20:37 GMT  
		Size: 16.2 MB (16150269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b47f933436cc57965cecdb865715bb01535d7aa664ecd5aaa38504b7d29a5a5`  
		Last Modified: Sat, 24 Apr 2021 00:20:34 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c28531c6ee3b84f26807ed129be1a1966692c7120ecfe5685853ca4d6a0873`  
		Last Modified: Sat, 24 Apr 2021 00:20:33 GMT  
		Size: 5.5 KB (5501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8ad6644768422c5ad05afb901373b192e8b3b226361adb1d3b00e49afe5901`  
		Last Modified: Sat, 24 Apr 2021 00:21:10 GMT  
		Size: 272.4 MB (272372428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d9815765b2ed56b325178f5b8015e18283270d5cce085d15a2ba4146a5df73c`  
		Last Modified: Sat, 24 Apr 2021 00:20:36 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cabef54e475bc342b69668f5a78b6fc8a416325eb5b5be9c02584d2ead26d40`  
		Last Modified: Sat, 24 Apr 2021 00:22:17 GMT  
		Size: 280.4 MB (280366455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo11`

```console
$ docker pull gazebo@sha256:ccf75e79db3de7e55bf113d4b96ae5d4db8840dc71a73d3ffaa5d0143d040623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo11` - linux; amd64

```console
$ docker pull gazebo@sha256:504956d2050fe3ef5a1dbab5aeee02d89ffaca5604d275a701fc8952287c1b7d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.6 MB (598620455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1a4995df9bd0f7e8e8b1103d5c0d5f701e55bebcca0a327c1917e0b2513749`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

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
# Sat, 24 Apr 2021 00:05:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:06:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:06:02 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Sat, 24 Apr 2021 00:06:03 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Sat, 24 Apr 2021 00:09:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:09:43 GMT
EXPOSE 11345
# Sat, 24 Apr 2021 00:09:43 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Sat, 24 Apr 2021 00:09:43 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Sat, 24 Apr 2021 00:09:43 GMT
CMD ["gzserver"]
# Sat, 24 Apr 2021 00:15:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:62f60c1e15de5890db12b66dcdc9fead43b285bea7d10d147a7baddfe0093488`  
		Last Modified: Sat, 24 Apr 2021 00:20:37 GMT  
		Size: 1.2 MB (1183512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a84e3d913f988af95e954537fcffb78eb9c9c3d5b91f5cdcf02a1f1c932a6d5`  
		Last Modified: Sat, 24 Apr 2021 00:20:37 GMT  
		Size: 16.2 MB (16150269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b47f933436cc57965cecdb865715bb01535d7aa664ecd5aaa38504b7d29a5a5`  
		Last Modified: Sat, 24 Apr 2021 00:20:34 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c28531c6ee3b84f26807ed129be1a1966692c7120ecfe5685853ca4d6a0873`  
		Last Modified: Sat, 24 Apr 2021 00:20:33 GMT  
		Size: 5.5 KB (5501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8ad6644768422c5ad05afb901373b192e8b3b226361adb1d3b00e49afe5901`  
		Last Modified: Sat, 24 Apr 2021 00:21:10 GMT  
		Size: 272.4 MB (272372428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d9815765b2ed56b325178f5b8015e18283270d5cce085d15a2ba4146a5df73c`  
		Last Modified: Sat, 24 Apr 2021 00:20:36 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cabef54e475bc342b69668f5a78b6fc8a416325eb5b5be9c02584d2ead26d40`  
		Last Modified: Sat, 24 Apr 2021 00:22:17 GMT  
		Size: 280.4 MB (280366455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo11-bionic`

```console
$ docker pull gazebo@sha256:18bbd89d830184809fd9492381301acca9dcc7ecd3078d3b8c4b1b94ee43c694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo11-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:930424c2a01d59f52456a2678e529843529355c549067f30c6021b719becbed1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **546.7 MB (546662441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d139eb88f6cbb8bd25fbd4013c7522ce10453413cfc7b873a7f47dce9a1007a8`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:22 GMT
ADD file:d7fa3c26651f9204a5629287a1a9a6e7dc6a0bc6eb499e82c433c0c8f67ff46b in / 
# Fri, 23 Apr 2021 22:21:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:25 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:54:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:54:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:54:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Fri, 23 Apr 2021 23:54:24 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Sat, 24 Apr 2021 00:03:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:03:50 GMT
EXPOSE 11345
# Sat, 24 Apr 2021 00:03:50 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Sat, 24 Apr 2021 00:03:51 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Sat, 24 Apr 2021 00:03:51 GMT
CMD ["gzserver"]
# Sat, 24 Apr 2021 00:05:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:01bf7da0a88c9e37ae418d17c0aeed0621524848d80ccb9e38c67e7ab8e11928`  
		Last Modified: Fri, 16 Apr 2021 15:20:23 GMT  
		Size: 26.7 MB (26697009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b4a5f15c7a0722b4f22e61b5387317eaf2602c27ffb2bceac9a25f19fbd156`  
		Last Modified: Fri, 23 Apr 2021 22:22:45 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ffbe87baa135002dddb7a7460082c5d6a352186e1be9464c5f31db81378824`  
		Last Modified: Fri, 23 Apr 2021 22:22:45 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfad5d88235e65844b7c8944e2bd9a0cacde3a1ea196f87712547e7b0a19c3f`  
		Last Modified: Sat, 24 Apr 2021 00:17:26 GMT  
		Size: 841.6 KB (841642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b1efce7c1b75033060ddc06d651f1eed0c3b69c9a10650783d1338a8de16e7`  
		Last Modified: Sat, 24 Apr 2021 00:17:25 GMT  
		Size: 14.7 MB (14702594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2167b3eed350794a813a746a5221289779308d78aaa084b713ed9d9fe83250e`  
		Last Modified: Sat, 24 Apr 2021 00:17:22 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022f6080d75ae23a63af8b6f85496b1763e39be8adf414b532ba5c7c93d3ef5e`  
		Last Modified: Sat, 24 Apr 2021 00:17:22 GMT  
		Size: 5.5 KB (5462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f475d88930aab6fd2bc423304e95eb6f4986e4361e074070ba551f702f5ab2e`  
		Last Modified: Sat, 24 Apr 2021 00:19:31 GMT  
		Size: 235.1 MB (235133116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a928237d4f0f84c1e386b53ce4054080816dccd327881244f9bd349d49bc561`  
		Last Modified: Sat, 24 Apr 2021 00:19:00 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f17aac8491b5c3994de1bbc49604367bfc06912bb576e3ce5ba5665f5db38a`  
		Last Modified: Sat, 24 Apr 2021 00:20:23 GMT  
		Size: 269.3 MB (269279952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo11-focal`

```console
$ docker pull gazebo@sha256:ccf75e79db3de7e55bf113d4b96ae5d4db8840dc71a73d3ffaa5d0143d040623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo11-focal` - linux; amd64

```console
$ docker pull gazebo@sha256:504956d2050fe3ef5a1dbab5aeee02d89ffaca5604d275a701fc8952287c1b7d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.6 MB (598620455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1a4995df9bd0f7e8e8b1103d5c0d5f701e55bebcca0a327c1917e0b2513749`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

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
# Sat, 24 Apr 2021 00:05:34 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:06:01 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:06:02 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Sat, 24 Apr 2021 00:06:03 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Sat, 24 Apr 2021 00:09:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo11=11.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Sat, 24 Apr 2021 00:09:43 GMT
EXPOSE 11345
# Sat, 24 Apr 2021 00:09:43 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Sat, 24 Apr 2021 00:09:43 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Sat, 24 Apr 2021 00:09:43 GMT
CMD ["gzserver"]
# Sat, 24 Apr 2021 00:15:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo11-dev=11.5.0-1*     && rm -rf /var/lib/apt/lists/*
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
	-	`sha256:62f60c1e15de5890db12b66dcdc9fead43b285bea7d10d147a7baddfe0093488`  
		Last Modified: Sat, 24 Apr 2021 00:20:37 GMT  
		Size: 1.2 MB (1183512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a84e3d913f988af95e954537fcffb78eb9c9c3d5b91f5cdcf02a1f1c932a6d5`  
		Last Modified: Sat, 24 Apr 2021 00:20:37 GMT  
		Size: 16.2 MB (16150269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b47f933436cc57965cecdb865715bb01535d7aa664ecd5aaa38504b7d29a5a5`  
		Last Modified: Sat, 24 Apr 2021 00:20:34 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c28531c6ee3b84f26807ed129be1a1966692c7120ecfe5685853ca4d6a0873`  
		Last Modified: Sat, 24 Apr 2021 00:20:33 GMT  
		Size: 5.5 KB (5501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8ad6644768422c5ad05afb901373b192e8b3b226361adb1d3b00e49afe5901`  
		Last Modified: Sat, 24 Apr 2021 00:21:10 GMT  
		Size: 272.4 MB (272372428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d9815765b2ed56b325178f5b8015e18283270d5cce085d15a2ba4146a5df73c`  
		Last Modified: Sat, 24 Apr 2021 00:20:36 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cabef54e475bc342b69668f5a78b6fc8a416325eb5b5be9c02584d2ead26d40`  
		Last Modified: Sat, 24 Apr 2021 00:22:17 GMT  
		Size: 280.4 MB (280366455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo9`

```console
$ docker pull gazebo@sha256:7287a8929e72d0f10a52886c4434e25bd3ecf9d682622a6f9a20d8f64bc58e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo9` - linux; amd64

```console
$ docker pull gazebo@sha256:70efc8f21b3df88198e62011f415d601386b34cc691c9646d00c1147e3dbead2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.6 MB (413575482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcad5fb2d713712ceb2fd8f96459bcd6db27beadc9bb686a2893a2efc2bfe9b8`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:22 GMT
ADD file:d7fa3c26651f9204a5629287a1a9a6e7dc6a0bc6eb499e82c433c0c8f67ff46b in / 
# Fri, 23 Apr 2021 22:21:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:25 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:54:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:54:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:54:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Fri, 23 Apr 2021 23:54:24 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Wed, 28 Apr 2021 19:13:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.17.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 28 Apr 2021 19:13:28 GMT
EXPOSE 11345
# Wed, 28 Apr 2021 19:13:29 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Wed, 28 Apr 2021 19:13:29 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Wed, 28 Apr 2021 19:13:29 GMT
CMD ["gzserver"]
# Wed, 28 Apr 2021 19:16:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo9-dev=9.17.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:01bf7da0a88c9e37ae418d17c0aeed0621524848d80ccb9e38c67e7ab8e11928`  
		Last Modified: Fri, 16 Apr 2021 15:20:23 GMT  
		Size: 26.7 MB (26697009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b4a5f15c7a0722b4f22e61b5387317eaf2602c27ffb2bceac9a25f19fbd156`  
		Last Modified: Fri, 23 Apr 2021 22:22:45 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ffbe87baa135002dddb7a7460082c5d6a352186e1be9464c5f31db81378824`  
		Last Modified: Fri, 23 Apr 2021 22:22:45 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfad5d88235e65844b7c8944e2bd9a0cacde3a1ea196f87712547e7b0a19c3f`  
		Last Modified: Sat, 24 Apr 2021 00:17:26 GMT  
		Size: 841.6 KB (841642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b1efce7c1b75033060ddc06d651f1eed0c3b69c9a10650783d1338a8de16e7`  
		Last Modified: Sat, 24 Apr 2021 00:17:25 GMT  
		Size: 14.7 MB (14702594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2167b3eed350794a813a746a5221289779308d78aaa084b713ed9d9fe83250e`  
		Last Modified: Sat, 24 Apr 2021 00:17:22 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022f6080d75ae23a63af8b6f85496b1763e39be8adf414b532ba5c7c93d3ef5e`  
		Last Modified: Sat, 24 Apr 2021 00:17:22 GMT  
		Size: 5.5 KB (5462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eabad2f1e30aa275f7020a73e7de0e8a97a32bc118f054bf82728eb193e2afc9`  
		Last Modified: Wed, 28 Apr 2021 19:19:44 GMT  
		Size: 226.1 MB (226119504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b5cb82b4c59623b5f8c6e65ecdc7c2ab0f5e9fa8867dfdd8241053f70b5110`  
		Last Modified: Wed, 28 Apr 2021 19:19:13 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae774eb51589c862bac1fa1f0b62375be72035e4e4912c3c2277e44b297ab2e`  
		Last Modified: Wed, 28 Apr 2021 19:20:24 GMT  
		Size: 145.2 MB (145206604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo9-bionic`

```console
$ docker pull gazebo@sha256:7287a8929e72d0f10a52886c4434e25bd3ecf9d682622a6f9a20d8f64bc58e40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo9-bionic` - linux; amd64

```console
$ docker pull gazebo@sha256:70efc8f21b3df88198e62011f415d601386b34cc691c9646d00c1147e3dbead2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.6 MB (413575482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcad5fb2d713712ceb2fd8f96459bcd6db27beadc9bb686a2893a2efc2bfe9b8`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 23 Apr 2021 22:21:22 GMT
ADD file:d7fa3c26651f9204a5629287a1a9a6e7dc6a0bc6eb499e82c433c0c8f67ff46b in / 
# Fri, 23 Apr 2021 22:21:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:21:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 23 Apr 2021 22:21:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:21:25 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:54:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:54:22 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:54:23 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Fri, 23 Apr 2021 23:54:24 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Wed, 28 Apr 2021 19:13:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.17.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 28 Apr 2021 19:13:28 GMT
EXPOSE 11345
# Wed, 28 Apr 2021 19:13:29 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Wed, 28 Apr 2021 19:13:29 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Wed, 28 Apr 2021 19:13:29 GMT
CMD ["gzserver"]
# Wed, 28 Apr 2021 19:16:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo9-dev=9.17.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:01bf7da0a88c9e37ae418d17c0aeed0621524848d80ccb9e38c67e7ab8e11928`  
		Last Modified: Fri, 16 Apr 2021 15:20:23 GMT  
		Size: 26.7 MB (26697009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b4a5f15c7a0722b4f22e61b5387317eaf2602c27ffb2bceac9a25f19fbd156`  
		Last Modified: Fri, 23 Apr 2021 22:22:45 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ffbe87baa135002dddb7a7460082c5d6a352186e1be9464c5f31db81378824`  
		Last Modified: Fri, 23 Apr 2021 22:22:45 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cfad5d88235e65844b7c8944e2bd9a0cacde3a1ea196f87712547e7b0a19c3f`  
		Last Modified: Sat, 24 Apr 2021 00:17:26 GMT  
		Size: 841.6 KB (841642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b1efce7c1b75033060ddc06d651f1eed0c3b69c9a10650783d1338a8de16e7`  
		Last Modified: Sat, 24 Apr 2021 00:17:25 GMT  
		Size: 14.7 MB (14702594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2167b3eed350794a813a746a5221289779308d78aaa084b713ed9d9fe83250e`  
		Last Modified: Sat, 24 Apr 2021 00:17:22 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022f6080d75ae23a63af8b6f85496b1763e39be8adf414b532ba5c7c93d3ef5e`  
		Last Modified: Sat, 24 Apr 2021 00:17:22 GMT  
		Size: 5.5 KB (5462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eabad2f1e30aa275f7020a73e7de0e8a97a32bc118f054bf82728eb193e2afc9`  
		Last Modified: Wed, 28 Apr 2021 19:19:44 GMT  
		Size: 226.1 MB (226119504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b5cb82b4c59623b5f8c6e65ecdc7c2ab0f5e9fa8867dfdd8241053f70b5110`  
		Last Modified: Wed, 28 Apr 2021 19:19:13 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae774eb51589c862bac1fa1f0b62375be72035e4e4912c3c2277e44b297ab2e`  
		Last Modified: Wed, 28 Apr 2021 19:20:24 GMT  
		Size: 145.2 MB (145206604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `gazebo:libgazebo9-xenial`

```console
$ docker pull gazebo@sha256:8f09987feef6612efd592ce83776c37f8c65ce0a488e20bf8662229cd7abe869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `gazebo:libgazebo9-xenial` - linux; amd64

```console
$ docker pull gazebo@sha256:4297f5cc5bdcc26c40fd1fbcbfe30c413f0221b543970b3b9e17b5b792755b1c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.4 MB (495434520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d1c3ed4c39ad91c3cb3d8aa7fce7e7a1ff597ddd4fd3945ffe7fb15eb82c9c`
-	Entrypoint: `["\/gzserver_entrypoint.sh"]`
-	Default Command: `["gzserver"]`

```dockerfile
# Fri, 23 Apr 2021 22:22:16 GMT
ADD file:34f9c325bb2e6ad9f9a062ce9a0237fab0c04aea83f31b8548ea0ae532255be0 in / 
# Fri, 23 Apr 2021 22:22:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 23 Apr 2021 22:22:18 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 22:22:19 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 23 Apr 2021 22:22:19 GMT
CMD ["/bin/bash"]
# Fri, 23 Apr 2021 23:48:31 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     lsb-release     && rm -rf /var/lib/apt/lists/*
# Fri, 23 Apr 2021 23:48:33 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys D2486D2DD83DB69272AFE98867170598AF249743
# Fri, 23 Apr 2021 23:48:34 GMT
RUN . /etc/os-release     && echo "deb http://packages.osrfoundation.org/gazebo/$ID-stable `lsb_release -sc` main" > /etc/apt/sources.list.d/gazebo-latest.list
# Wed, 28 Apr 2021 19:05:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     gazebo9=9.17.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 28 Apr 2021 19:05:33 GMT
EXPOSE 11345
# Wed, 28 Apr 2021 19:05:33 GMT
COPY file:b79966dec12c55a0a5c9e673326cc3faf9cbbeee0ea5f172e863df237eb8a601 in / 
# Wed, 28 Apr 2021 19:05:33 GMT
ENTRYPOINT ["/gzserver_entrypoint.sh"]
# Wed, 28 Apr 2021 19:05:34 GMT
CMD ["gzserver"]
# Wed, 28 Apr 2021 19:09:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     libgazebo9-dev=9.17.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:92473f7ef45574f608989888a6cfc8187d3a1425e3a63f974434acab03fed068`  
		Last Modified: Sat, 17 Apr 2021 15:20:07 GMT  
		Size: 46.3 MB (46254451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb52bde70123ac7f3a1b88fee95e74f4bdcdbd81917a91a35b56a52ec7671947`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64788f86be3fd71809b5de602deff9445f3de18d2f44a49d0a053dfc9a2008ae`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 527.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f6d5f2e001ababe3ddac4731d9c33121e1148ef32a87a83a5b470cb401abef`  
		Last Modified: Fri, 23 Apr 2021 22:24:04 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340f215ec5582c3709c8edd826b45865536aee4a0e309b5eaf54bbae4ec4bf2f`  
		Last Modified: Sat, 24 Apr 2021 00:15:49 GMT  
		Size: 16.3 MB (16279968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9887fad184bfee18f93dc0728afcc29ef5a9413cc8e7dd66e94fb7a803959a87`  
		Last Modified: Sat, 24 Apr 2021 00:15:45 GMT  
		Size: 14.8 KB (14759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaaacc64da264322798a93c66aec28cfa0fea4a1cb0cebe2694cd18209fe74a8`  
		Last Modified: Sat, 24 Apr 2021 00:15:45 GMT  
		Size: 5.6 KB (5551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5680ec8f99db4c4e5829e2d9d0fa07bbc48283956e97a4acf18748fcadb5903`  
		Last Modified: Wed, 28 Apr 2021 19:18:12 GMT  
		Size: 208.1 MB (208107667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc43beaaffbed249b82082f7a46abcf704a03fd57ec97d63722c0652a91f897`  
		Last Modified: Wed, 28 Apr 2021 19:17:45 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a3e00a1658db4a823a1f59a93f3ff677777d33e225d1505d0334cd3eb14753`  
		Last Modified: Wed, 28 Apr 2021 19:19:01 GMT  
		Size: 224.8 MB (224770390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:kinetic-ros-core-xenial`

```console
$ docker pull ros@sha256:43dcfc01f967f39f1b6a9f854de4c1d7d79f3b4769d1c4995a6abbf97ee061f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:kinetic-ros-core-xenial` - linux; amd64

```console
$ docker pull ros@sha256:c94deb20af73d58180dd7b703d15ef799dff449f39bcac46ab1853a572d919da
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.4 MB (238378573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59b0d7e4f907859feef6b924383080e43b294d56db7694ab3f5129b038d4255b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 25 Nov 2020 22:26:11 GMT
ADD file:8eef54430e581236e6d529a7d09df648f43c840e889d9ae132e5ed25d7bd2b88 in / 
# Wed, 25 Nov 2020 22:26:12 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 25 Nov 2020 22:26:13 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 22:26:14 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 25 Nov 2020 22:26:14 GMT
CMD ["/bin/bash"]
# Thu, 26 Nov 2020 01:42:00 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:42:01 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 26 Nov 2020 01:42:02 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 26 Nov 2020 01:42:02 GMT
ENV LANG=C.UTF-8
# Thu, 26 Nov 2020 01:42:02 GMT
ENV LC_ALL=C.UTF-8
# Thu, 26 Nov 2020 01:42:02 GMT
ENV ROS_DISTRO=kinetic
# Thu, 26 Nov 2020 01:43:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 26 Nov 2020 01:44:00 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 26 Nov 2020 01:44:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 26 Nov 2020 01:44:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:be8ec4e48d7f24a9a1c01063e5dfabb092c2c1ec73e125113848553c9b07eb8c`  
		Last Modified: Sat, 31 Oct 2020 14:20:23 GMT  
		Size: 45.8 MB (45838270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b8b485aff0509bb0fa67dff6a2aa82e9b7b17e5ef28c1673467ec83edb945d`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d887158cc58cbfc3d03cefd5c0b15175fae66ffbf6f28a56180c51cbb5062b8a`  
		Last Modified: Wed, 25 Nov 2020 22:27:14 GMT  
		Size: 533.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05895bb28c18264f614acd13e401b3c5594e12d9fe90d7e52929d3e810e11e97`  
		Last Modified: Wed, 25 Nov 2020 22:27:15 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94cf6b01927532a24fecba2e88d5aa3e553f087fcf3b5de780ace06aaeca5a1`  
		Last Modified: Thu, 26 Nov 2020 02:26:19 GMT  
		Size: 5.4 MB (5362832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d24686782e46b88375ad4ddd74396a1f29ccf5dd34d192a9724dcc476d4a77e3`  
		Last Modified: Thu, 26 Nov 2020 02:26:19 GMT  
		Size: 14.7 KB (14744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c37fb3954cf62deb7dd81f675735869a0bfb0b6f5821763a1591c9993e2f8a`  
		Last Modified: Thu, 26 Nov 2020 02:26:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6cd7524ada3336e2ca6610dead776b5982446e32d02bca2057be7a594c227b`  
		Last Modified: Thu, 26 Nov 2020 02:27:03 GMT  
		Size: 187.2 MB (187160759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79339e65150375f52bc82fc8585d2ff3cdad20ce09cf9a7b43fb374e1389a68`  
		Last Modified: Thu, 26 Nov 2020 02:26:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-ros-core-xenial` - linux; arm variant v7

```console
$ docker pull ros@sha256:953c366addc5e3183add3dedbc96b6079ea090f28674974a4bad305a1db22eb9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.7 MB (212657019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900e93078c3857b9b8afee0c573c27bae2f6ebc5488c24fd6e98590c354b3883`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:17:15 GMT
ADD file:c77c1a2ea3c8b1d59252626e6c8be57cca539dfce0a16a0ed2ff0311c0f5a265 in / 
# Thu, 21 Jan 2021 03:17:20 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:17:23 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:17:26 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:17:26 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 04:21:09 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:21:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 21 Jan 2021 04:21:14 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 21 Jan 2021 04:21:14 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 04:21:15 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Jan 2021 04:21:15 GMT
ENV ROS_DISTRO=kinetic
# Thu, 21 Jan 2021 04:23:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 04:24:02 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 21 Jan 2021 04:24:03 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Jan 2021 04:24:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2af2a813aac2db23328a29ab84155e95fbb6681e872751a4f11f688c005e84c5`  
		Last Modified: Mon, 18 Jan 2021 19:38:27 GMT  
		Size: 40.0 MB (39972659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:470ef2a276bd8b4a122330892d4a9b9383249f945d22fc34e7b2b0688fbf6af8`  
		Last Modified: Thu, 21 Jan 2021 03:19:28 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01c8ce931ce58b3726d3fa387bcf38f02ca4a4d9fa6db2a764bb8aae4f69079`  
		Last Modified: Thu, 21 Jan 2021 03:19:29 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9ba02aed017c06ce4541aa061d63a8068bd1651fc0f00b9c0995ec1b22bea3`  
		Last Modified: Thu, 21 Jan 2021 03:19:28 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453d6bcd4fcc109ea638feb11f4efb3cc42368c709239e97d0c80b058d7bac48`  
		Last Modified: Thu, 21 Jan 2021 05:08:43 GMT  
		Size: 4.6 MB (4615362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dada356e54fac0aeb0fc744ccbca68ed154ef97d589d1a9b2e810dab83264c6`  
		Last Modified: Thu, 21 Jan 2021 05:08:41 GMT  
		Size: 14.7 KB (14744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658b25c03a830017441e51bb0ee2af49968aa6de63b2d1c8dc15c295e3a71c60`  
		Last Modified: Thu, 21 Jan 2021 05:08:41 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dfd6725ae662c908d1df455362722a807ff5ce1dd3f66e0356c7fc3cba8f9a`  
		Last Modified: Thu, 21 Jan 2021 05:09:44 GMT  
		Size: 168.1 MB (168052304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffe4dcfe4ec1442358eef15e27bdb52616942a46251eeb5e16c05e6e01fc7abe`  
		Last Modified: Thu, 21 Jan 2021 05:08:41 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-ros-core-xenial` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:39186c19b9e2ccfa8e6ca3d0361898a5e4351b78a3ddd936885b020cbffb67cb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221744699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6fa6513cb709b0cb5cc095244c4a21bcb48b9816ce78f0ceece70e5c9e15f3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 21 Jan 2021 03:51:12 GMT
ADD file:e2f37be259f081b70bc884e3b7f652e5d9a0ad4ae443f2258b79a1b14377cc20 in / 
# Thu, 21 Jan 2021 03:51:17 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 21 Jan 2021 03:51:19 GMT
RUN rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 03:51:21 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 21 Jan 2021 03:51:22 GMT
CMD ["/bin/bash"]
# Thu, 21 Jan 2021 06:27:03 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 06:27:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 21 Jan 2021 06:27:09 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 21 Jan 2021 06:27:09 GMT
ENV LANG=C.UTF-8
# Thu, 21 Jan 2021 06:27:10 GMT
ENV LC_ALL=C.UTF-8
# Thu, 21 Jan 2021 06:27:11 GMT
ENV ROS_DISTRO=kinetic
# Thu, 21 Jan 2021 06:29:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 21 Jan 2021 06:29:20 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Thu, 21 Jan 2021 06:29:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 21 Jan 2021 06:29:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:79186a4c5361c6b018fe75c9bba66c9bf717db8d7d4a6ddb18fb86171f277b61`  
		Last Modified: Thu, 14 Jan 2021 16:25:21 GMT  
		Size: 40.9 MB (40885219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96f901e8ebcf64a42ec369549f6269ec96cd97b424389ca99a8ebb722c59c12`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36fd1545244608cb9ef92efa528b6e8c3229f1b01ca414ee8717219145cdff7d`  
		Last Modified: Thu, 21 Jan 2021 03:53:10 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d978c0f55122642ba1a22cc67abf7af2e898bfb42933b1879c2dd91fd987147d`  
		Last Modified: Thu, 21 Jan 2021 03:53:11 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0596a8732aadbc8704f74fca2d9a1a5a769d11c968c46103f313b03d4d5cd68`  
		Last Modified: Thu, 21 Jan 2021 07:22:49 GMT  
		Size: 4.8 MB (4820293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fbda91611b700613684e2b08b7cb4c1ce1b58c152f34838d51f2b320ceef983`  
		Last Modified: Thu, 21 Jan 2021 07:22:48 GMT  
		Size: 14.7 KB (14744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2b1318bd99b208ca1a2d36788e661df11ae80e5a774b26095bd70e517a8873`  
		Last Modified: Thu, 21 Jan 2021 07:22:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc8a247eee41c59c7799a7f9b83a86a04c4be4fb946d8b463b5f1f12b52b36fb`  
		Last Modified: Thu, 21 Jan 2021 07:23:36 GMT  
		Size: 176.0 MB (176022535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff9c81e12c5a66cd90daa8379fbca97b6a27b3005b29c5a698d1b6ef8ce185a`  
		Last Modified: Thu, 21 Jan 2021 07:22:48 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

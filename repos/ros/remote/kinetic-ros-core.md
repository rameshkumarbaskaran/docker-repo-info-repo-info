## `ros:kinetic-ros-core`

```console
$ docker pull ros@sha256:06bf105b8b2a425951ab39f8863510f2af32b10c60ecbc55075fecce8bef0c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:kinetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:b3881b49f5c0d3330d8afc9397d50deac4b907d66445e00a51416abbc4d9bd3f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.9 MB (236926546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d13ea23651b556ff2c026a856ab676fbca925e4d8144d2acea354b23ec2ece`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 Jul 2020 14:39:06 GMT
ADD file:513ae777bc4042f8446c0454f8cffc9a94f8429de963651d9a6dab95d4502007 in / 
# Fri, 24 Jul 2020 14:39:07 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 14:39:07 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 14:39:08 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 14:39:08 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 18:04:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 18:04:55 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 24 Jul 2020 18:04:56 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 24 Jul 2020 18:04:56 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jul 2020 18:04:56 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 Jul 2020 18:04:56 GMT
ENV ROS_DISTRO=kinetic
# Fri, 24 Jul 2020 18:06:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 18:06:57 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 24 Jul 2020 18:06:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 Jul 2020 18:06:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7b378fa0f9085667ced1c76c9919cde8663becf2218e8d20e2df8d0824311531`  
		Last Modified: Tue, 07 Jul 2020 13:19:56 GMT  
		Size: 44.4 MB (44401021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d77b1b29f2e9b6f141b9d8f74b601f40eb998544783f4a0a3cdc384873c1a4e`  
		Last Modified: Fri, 24 Jul 2020 14:39:50 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c793be88baee3f3204444e4d4e49c4e44c1709d40182c131cd5681c94e17227`  
		Last Modified: Fri, 24 Jul 2020 14:39:50 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc05c8a19c0cf83f2f44263c967c3fe81fffc4b41b592ad088fb1534c206e70`  
		Last Modified: Fri, 24 Jul 2020 14:39:49 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35d3e490359bfb27251001813204a784160c727634421f0c2e9dfa17b6fb0d8`  
		Last Modified: Fri, 24 Jul 2020 18:49:13 GMT  
		Size: 5.4 MB (5362308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b88a1122f09c1c0c1f8013020bb517e065fb454ee14c9198d0ebc81e8eb178`  
		Last Modified: Fri, 24 Jul 2020 18:49:12 GMT  
		Size: 14.7 KB (14742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56fd6ccab8aa88dd0da1a26c17d9d16c360babbbcf79c5053f83e8a9ede3c20`  
		Last Modified: Fri, 24 Jul 2020 18:49:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b3ea9059f6170d73a2f76687f4bc2cba92bf7a31a9c70945c59bce1ac727d6`  
		Last Modified: Fri, 24 Jul 2020 18:49:55 GMT  
		Size: 187.1 MB (187146511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f9ccf49031078286631b1c695648fbbd1128e27b5fad0b31e8b09163e130516`  
		Last Modified: Fri, 24 Jul 2020 18:49:12 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:9a38f4a4a8542b91a902a59784a275ac3c1d4b3f32587399951ae380b9a7b420
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.7 MB (211655165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9786706289028e1037ce76a0c58e836b50569c46678ef60f03bef7c1250fcbb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 Jul 2020 16:09:57 GMT
ADD file:c7836321aa9dc9832d8e14c042281f4a3525083619649e000d08159b6da79460 in / 
# Fri, 24 Jul 2020 16:10:21 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:11:04 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 16:11:42 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 16:11:59 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:25:23 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:25:30 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 24 Jul 2020 16:25:34 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 24 Jul 2020 16:25:44 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jul 2020 16:25:46 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 Jul 2020 16:25:51 GMT
ENV ROS_DISTRO=kinetic
# Fri, 24 Jul 2020 16:30:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:30:54 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 24 Jul 2020 16:30:55 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 Jul 2020 16:30:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:111f37a6818f459bbc8076c0f741a76111210d34c5738743f43dc1488cf91458`  
		Last Modified: Mon, 13 Jul 2020 15:55:00 GMT  
		Size: 39.0 MB (39022996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58fa2e8f0d9a725920aa624702144baeaae474875e43f4515d9e69c2bddec4bf`  
		Last Modified: Fri, 24 Jul 2020 16:20:13 GMT  
		Size: 510.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c110f6a5721b4e19fdabed9edeb5446f52132952947cd7b409ac4d4e50b7dc02`  
		Last Modified: Fri, 24 Jul 2020 16:20:13 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07bd4b31471725e34aa841d95fec2e7425ac418ee0a0f69b6d5ca73c6a17c9e`  
		Last Modified: Fri, 24 Jul 2020 16:20:13 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c8cb740b420db49d2b9df4cc36d3a7547d77acc2cbeacf15151cb9b940c125`  
		Last Modified: Fri, 24 Jul 2020 17:30:30 GMT  
		Size: 4.6 MB (4615060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a0003531b818fd1c35748797bb0869f814fc0b99b51c56daf1b18098d835ac`  
		Last Modified: Fri, 24 Jul 2020 17:30:28 GMT  
		Size: 14.7 KB (14743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ed872f7d0b6ec64dc1d274b933a10aa128065ea067bdd9c3103e948db94b6d`  
		Last Modified: Fri, 24 Jul 2020 17:30:28 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6db036ce8a45a21f6b3f6df19023dd48216e291a202f9073046646585139ebf`  
		Last Modified: Fri, 24 Jul 2020 17:31:58 GMT  
		Size: 168.0 MB (168000414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e3518cf7245e334ae0fbe802330fd68f7146b08830e2de8e2863667a77d8db`  
		Last Modified: Fri, 24 Jul 2020 17:30:28 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:49e75e63983f2000c326a2fd232503d21b617420db51e5643cab1ad83cbf4833
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220869699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a105d06660cd00920a5bdac53a5537a2a9a187d77241acbcae05c2be86a679`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 24 Jul 2020 16:25:59 GMT
ADD file:d816988decfebf469e2b28b4858ce7d4a991a101957a43051324255fbe64c86e in / 
# Fri, 24 Jul 2020 16:26:14 GMT
RUN rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:26:19 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 24 Jul 2020 16:26:24 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 24 Jul 2020 16:26:27 GMT
CMD ["/bin/bash"]
# Fri, 24 Jul 2020 16:31:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:31:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 24 Jul 2020 16:31:09 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 24 Jul 2020 16:31:10 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jul 2020 16:31:11 GMT
ENV LC_ALL=C.UTF-8
# Fri, 24 Jul 2020 16:31:12 GMT
ENV ROS_DISTRO=kinetic
# Fri, 24 Jul 2020 16:36:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-kinetic-ros-core=1.3.2-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 16:36:47 GMT
COPY file:cbbaa0f5d6a276512315f5b4d7347e94a120cefbda9058ebb0d678847ff4837f in / 
# Fri, 24 Jul 2020 16:36:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 Jul 2020 16:36:50 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f783735449ae0b09fb9e5ee128904f2f3131f6ba46fcf1350fb6a10f872866be`  
		Last Modified: Tue, 07 Jul 2020 00:25:09 GMT  
		Size: 40.1 MB (40050796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35a03aa6fbe0d9147b23501e6fa41d33cd4489470455008ddcbe201063d7b98`  
		Last Modified: Fri, 24 Jul 2020 16:27:47 GMT  
		Size: 468.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55e221892467d43fdd76b2b592c2fe46e1c69b08e0e9b94f2b383f38e681f65`  
		Last Modified: Fri, 24 Jul 2020 16:27:47 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a9069021914a77a3d51ffbff02ea5b8a200180601b2be52e9f98d31b6f1389`  
		Last Modified: Fri, 24 Jul 2020 16:27:47 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406ac69f173003c8bf0c008eaef291209c10ae7cd840633b6dfa0c3351a3c19a`  
		Last Modified: Fri, 24 Jul 2020 17:38:25 GMT  
		Size: 4.8 MB (4820044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9658dddd254b3a9732e5e0eff70e9f0c4ca573b2ffb9d7031fa9a89c1b99c518`  
		Last Modified: Fri, 24 Jul 2020 17:38:21 GMT  
		Size: 14.7 KB (14745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e008049660c6d8aae525a64b5fba4a4b918e212cc2548f8b1e35eb7a1cc35e41`  
		Last Modified: Fri, 24 Jul 2020 17:38:20 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b3f6f90a52db94535a8a10507e8b9981b17dddce080db1b8f558a66fdb497a`  
		Last Modified: Fri, 24 Jul 2020 17:40:19 GMT  
		Size: 176.0 MB (175982202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4782a0457e8a49bdd7b6d2f7935bf248fa8eb8dc68b418fdab6e7edccf157cb7`  
		Last Modified: Fri, 24 Jul 2020 17:38:20 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

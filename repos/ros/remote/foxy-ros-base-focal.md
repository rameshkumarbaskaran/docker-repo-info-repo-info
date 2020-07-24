## `ros:foxy-ros-base-focal`

```console
$ docker pull ros@sha256:3e00c9b04c281f18672712879dd506df0a25fa8a69dbe6eadc4e60ed143c40bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:82b59c32f2fa42ae9173823773c40740e7b0026eb403e1917322f3923d317b60
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231641319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3e03529c24d5b4317477bad8039e366f689da6e5487727ab876762c9241bed5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Jul 2020 21:56:28 GMT
ADD file:cf87af1f0e27aa6ffad26c57edca4ca55dc97861590a2d63475085a08d3b0063 in / 
# Mon, 06 Jul 2020 21:56:29 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 21:56:30 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 21:56:31 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 21:56:31 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 23:51:39 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:48:59 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:49:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jul 2020 01:08:51 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 07 Jul 2020 01:08:51 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jul 2020 01:08:51 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jul 2020 01:08:51 GMT
ENV ROS_DISTRO=foxy
# Fri, 24 Jul 2020 14:30:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 14:30:20 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Fri, 24 Jul 2020 14:30:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 24 Jul 2020 14:30:21 GMT
CMD ["bash"]
# Fri, 24 Jul 2020 14:31:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 24 Jul 2020 14:31:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 24 Jul 2020 14:31:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 24 Jul 2020 14:31:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:692c352adcf2821d6988021248da6b276cb738808f69dcc7bbb74a9c952146f7`  
		Last Modified: Fri, 03 Jul 2020 15:20:09 GMT  
		Size: 28.6 MB (28556756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97058a342707e39028c2597a4306fd3b1a2ebaf5423f8e514428c73fa508960c`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 32.3 KB (32327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2821b8e766f41f4f148dc2d378c41d60f3d2cbe6f03b2585dd5653c3873740ef`  
		Last Modified: Mon, 06 Jul 2020 21:57:27 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e643cc37772c094642f3168c56d1fcbcc9a07ecf72dbb5afdc35baf57e8bc29`  
		Last Modified: Mon, 06 Jul 2020 21:57:28 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbd34696aad22f9a861bdae9aed1bc14aed3426d245147e55a759747acc2357`  
		Last Modified: Tue, 07 Jul 2020 00:03:20 GMT  
		Size: 1.2 MB (1175806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8d44cae379b4797d812ed05b65c080aba6074d55e8d8b0b0c612b3923d9f5a`  
		Last Modified: Tue, 07 Jul 2020 01:21:06 GMT  
		Size: 5.5 MB (5549483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220c1b9e59cfca503e7910992752f72112d96b996c272d25c279bcbe31fb9210`  
		Last Modified: Tue, 07 Jul 2020 01:21:05 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b543ebbbdc63c94db2b759d1ed8cd54ae18f43a4819e01c5fadec51f9e2c393e`  
		Last Modified: Tue, 07 Jul 2020 01:27:20 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d003a0f5dc26d175f782264eaddf8fb8cf6e1e10a07307d6765b1582fa5e45c`  
		Last Modified: Fri, 24 Jul 2020 14:36:58 GMT  
		Size: 119.3 MB (119279442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c52b46d66f9aab35285d02768966d14241272f85bc61c30216a73f8afbd215`  
		Last Modified: Fri, 24 Jul 2020 14:36:24 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb70e9b07a847c28c519f5f1789a96f332c39d6f11053e7e34227073cff7d3f`  
		Last Modified: Fri, 24 Jul 2020 14:37:15 GMT  
		Size: 66.6 MB (66577782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f079a4538e2c3697923c719b286b1d1e24c5edbc88e40df11b2a5a11c31ac69`  
		Last Modified: Fri, 24 Jul 2020 14:37:02 GMT  
		Size: 187.5 KB (187547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a621d1e41de06dfd9d740b5d1c41df6db413a0fd7fcf0239ae614c3522cb4910`  
		Last Modified: Fri, 24 Jul 2020 14:37:02 GMT  
		Size: 2.0 KB (1997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f229b50eec377ce43e24d48a90ee34806029375e5ce3628c14f7ce6737b6c3d`  
		Last Modified: Fri, 24 Jul 2020 14:37:06 GMT  
		Size: 10.3 MB (10277327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3b0f8e682e0518a3b8f9f95bb0986e9bcdf2745e6a5170e4735063eb48403766
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207787058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d5a6d50324de0b3243a63f3206327a9cea5def4523191862d86dd43ef52beb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Jul 2020 22:05:29 GMT
ADD file:58177e63d6a7654c6ec25d5f171bfc6fe7070b9a42bc9753b2a0721c1e97ea98 in / 
# Mon, 06 Jul 2020 22:05:33 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Mon, 06 Jul 2020 22:05:35 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Mon, 06 Jul 2020 22:05:37 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Mon, 06 Jul 2020 22:05:37 GMT
CMD ["/bin/bash"]
# Mon, 06 Jul 2020 23:37:09 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 23:37:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Mon, 06 Jul 2020 23:37:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 07 Jul 2020 00:07:29 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 07 Jul 2020 00:07:30 GMT
ENV LANG=C.UTF-8
# Tue, 07 Jul 2020 00:07:31 GMT
ENV LC_ALL=C.UTF-8
# Tue, 07 Jul 2020 00:07:31 GMT
ENV ROS_DISTRO=foxy
# Tue, 07 Jul 2020 00:09:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.1-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:09:20 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Tue, 07 Jul 2020 00:09:21 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 07 Jul 2020 00:09:22 GMT
CMD ["bash"]
# Tue, 07 Jul 2020 00:10:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jul 2020 00:10:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 07 Jul 2020 00:10:28 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 07 Jul 2020 00:10:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.1-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f3801533dc70937af93edc176636ab9bdd9c13ffd6a577424da089f1a9b8835e`  
		Last Modified: Fri, 03 Jul 2020 08:25:21 GMT  
		Size: 27.2 MB (27159375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb81013b04c0969633d86eeb365874dc244f2b8685f64c968f6ef0ad5d673eff`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 32.4 KB (32350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f21a01347196e93b7698c17c93919e9116a779ce619428cfca2eb2051ad41c`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8e2b8980f01b2aa996f46fe4a36d64eb2c97ee3dfed66c3ebe5322155a0d91`  
		Last Modified: Mon, 06 Jul 2020 22:07:11 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1ab16d904a1fdd0d8d3bf4378ba8091441f6fa4efc5f1a4cbb96007992418a`  
		Last Modified: Tue, 07 Jul 2020 00:27:10 GMT  
		Size: 1.2 MB (1175980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4459a6ff20458c1e9ddb61cde61a0a3767b97c675670463e46b4942817e63283`  
		Last Modified: Tue, 07 Jul 2020 00:27:09 GMT  
		Size: 5.5 MB (5516710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1ce6ceb4dd155db7ff7ae84a01089eb66468a8907beeef35311a2dfecf5960`  
		Last Modified: Tue, 07 Jul 2020 00:27:08 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7e87ced0eb519f8277d457ddc46e036365a4fe5e6e4f631d81cc378955f631`  
		Last Modified: Tue, 07 Jul 2020 00:35:17 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4629a1c2e61428f122b390a0945bb55cff8a5b3cbb16e62a343897b01e87bd43`  
		Last Modified: Tue, 07 Jul 2020 00:35:49 GMT  
		Size: 103.5 MB (103488518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c3aadea147187dd3fa18bdb3b21f3bf3b163dcd331d2b54acf7a50ab6c3248`  
		Last Modified: Tue, 07 Jul 2020 00:35:17 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd1bb4742a50d4bddb3123ed522ab814296602042cf9e2724fe3983d86a9702`  
		Last Modified: Tue, 07 Jul 2020 00:36:12 GMT  
		Size: 60.9 MB (60928676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeccbb67bf1e97c6fc79f6a4acbfda1645bdd0534f20b247e34f323f5fabbbbd`  
		Last Modified: Tue, 07 Jul 2020 00:35:56 GMT  
		Size: 184.9 KB (184874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1f87c79ca6f5f66f7efda813ad34e4ad07fcc12d7d509cefe3fbac020fe05e6`  
		Last Modified: Tue, 07 Jul 2020 00:35:56 GMT  
		Size: 2.1 KB (2069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c7acfef4dc7d6a885dc15cc4de091d1613983d800f585491359c04c3c6ffb5`  
		Last Modified: Tue, 07 Jul 2020 00:36:00 GMT  
		Size: 9.3 MB (9295627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

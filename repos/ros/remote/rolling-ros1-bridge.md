## `ros:rolling-ros1-bridge`

```console
$ docker pull ros@sha256:9e2110b6e7d1e2d0c9857a25c5a039d1063908d7dc791007ff85999e6617a407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:c3a6d3fb7420e09ae43d7a5397575e73b46f3412934ff659b7ce6767e3b4b016
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.7 MB (333728355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9557995df1f0ff64217805675d17f89aa65b0d736455c5a80e8f81d519f6949f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Sep 2020 22:20:23 GMT
ADD file:1b4ec50586b9f0621095f51ee6baecc00a7f6d95b4a04e3bedc5393b28bc8a54 in / 
# Wed, 16 Sep 2020 22:20:24 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:20:24 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:20:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:20:25 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:37:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:34:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:34:53 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 17 Sep 2020 01:55:03 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 17 Sep 2020 01:55:03 GMT
ENV LANG=C.UTF-8
# Thu, 17 Sep 2020 01:55:03 GMT
ENV LC_ALL=C.UTF-8
# Thu, 17 Sep 2020 01:59:10 GMT
ENV ROS_DISTRO=rolling
# Thu, 17 Sep 2020 01:59:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.1-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:59:59 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 17 Sep 2020 01:59:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 17 Sep 2020 02:00:00 GMT
CMD ["bash"]
# Thu, 17 Sep 2020 02:00:24 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 02:00:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 17 Sep 2020 02:00:32 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 17 Sep 2020 02:00:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.1-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 02:00:46 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 17 Sep 2020 02:00:47 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 17 Sep 2020 02:00:47 GMT
ENV ROS1_DISTRO=noetic
# Thu, 17 Sep 2020 02:00:47 GMT
ENV ROS2_DISTRO=rolling
# Thu, 17 Sep 2020 02:01:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.8-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 02:01:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros1-bridge=0.9.2-2*     ros-rolling-demo-nodes-cpp=0.10.0-1*     ros-rolling-demo-nodes-py=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 02:01:36 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:e6ca3592b14484be6a9719617680e0c810e0107d89c437162c75d2401637c72c`  
		Last Modified: Wed, 16 Sep 2020 15:19:59 GMT  
		Size: 28.6 MB (28557166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534a5505201da9ddb334b5b2fcb3cec45fcafccd8e91b93ad4852e1a1bb318c1`  
		Last Modified: Wed, 16 Sep 2020 22:23:09 GMT  
		Size: 839.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990916bd23bbbf9c30d202dad557e813562d028f3076bf57904830c69d4cde83`  
		Last Modified: Wed, 16 Sep 2020 22:23:09 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd43f844b454143fefb276b0d47a08c31858e330ffeceef21130f4f907c2691e`  
		Last Modified: Thu, 17 Sep 2020 00:52:12 GMT  
		Size: 1.2 MB (1176444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25929632fd5b65202802f96157aaae95b55bcb587a77c708a4d63e5d2100db09`  
		Last Modified: Thu, 17 Sep 2020 02:08:15 GMT  
		Size: 5.5 MB (5547001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa5e6421658a99911cb295c7f31b4f12e6a3f61860c7814b87cddc1a985e215`  
		Last Modified: Thu, 17 Sep 2020 02:08:14 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b62c6d955edf0b3d12ec0e851b2c8e6901c44cc4798da5c77c35bef01209da`  
		Last Modified: Thu, 17 Sep 2020 02:14:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295deae1499b75745f88e8e8fe279724f5e40f6774db3c6bdea8010f9bd88743`  
		Last Modified: Thu, 17 Sep 2020 02:16:23 GMT  
		Size: 119.3 MB (119291847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72732fc2b062a35d766fe52f713a21ea53b4e805c8eabbb5e1d3e8deda04bdf`  
		Last Modified: Thu, 17 Sep 2020 02:15:50 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e22f799f4b3375517daed48011be12413233d9f09cc99a8369f847f3d7bc97`  
		Last Modified: Thu, 17 Sep 2020 02:16:40 GMT  
		Size: 66.6 MB (66580075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e9b1b30d496929de95e872f6d922b3cff405f677119d38fb2436fcc103ce01`  
		Last Modified: Thu, 17 Sep 2020 02:16:27 GMT  
		Size: 187.9 KB (187909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ac5c4bac57e4ea1bd6c9b63fe3f4a3690dca2d532594928867bf7bed26750c`  
		Last Modified: Thu, 17 Sep 2020 02:16:27 GMT  
		Size: 2.0 KB (1973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80dd9e91f2a2f65c1a9450590508516bbe098718b3908752cf323b466e7df19`  
		Last Modified: Thu, 17 Sep 2020 02:16:31 GMT  
		Size: 10.3 MB (10283012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4191a1e9018da7837c74557487b7fca328774b3be8b93630484a56a4cc66bae8`  
		Last Modified: Thu, 17 Sep 2020 02:16:46 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99acd1f9cdef2837bd65c9c492b9d9331c3a5a3e34bbc8199b03f883cb360fa3`  
		Last Modified: Thu, 17 Sep 2020 02:16:46 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea90d668d0dbefca0d4f6e72d4e6243e5c30eb1e1a4f7a390093992554e5083`  
		Last Modified: Thu, 17 Sep 2020 02:17:10 GMT  
		Size: 76.1 MB (76093059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae1bf2156b49b707240f5c360f88dc2513b1d075e64bdd239972069593abdf0`  
		Last Modified: Thu, 17 Sep 2020 02:16:53 GMT  
		Size: 26.0 MB (26006407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f384a8b0b46e2c602656d3fb925a922bf5938f58a3febce546a4692eac83c3`  
		Last Modified: Thu, 17 Sep 2020 02:16:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cc9ce50cf908018e6cc09247dd574b1671b4a8c70d9183f2bdc23c048b420f88
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (306952468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761397077332e7677859afdb06d3561b633e247e7133718db03c74e7942389ff`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 16 Sep 2020 23:16:56 GMT
ADD file:063d9d9577619d2eeb19bbc784fecf567039a314d8f741500841f6b4f3c847b3 in / 
# Wed, 16 Sep 2020 23:17:00 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 23:17:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 23:17:04 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 23:17:04 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 01:44:01 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:44:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 01:45:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 17 Sep 2020 02:13:08 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Thu, 17 Sep 2020 02:13:08 GMT
ENV LANG=C.UTF-8
# Thu, 17 Sep 2020 02:13:09 GMT
ENV LC_ALL=C.UTF-8
# Thu, 17 Sep 2020 02:18:34 GMT
ENV ROS_DISTRO=rolling
# Thu, 17 Sep 2020 02:20:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.9.1-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 02:20:24 GMT
COPY file:57f71198b74c2c1967889acdfddb85d428137580d18be4211971fc7381557b6c in / 
# Thu, 17 Sep 2020 02:20:25 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 17 Sep 2020 02:20:25 GMT
CMD ["bash"]
# Thu, 17 Sep 2020 02:21:16 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 02:21:26 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 17 Sep 2020 02:21:34 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Thu, 17 Sep 2020 02:22:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.9.1-2*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 02:22:28 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 17 Sep 2020 02:22:30 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 17 Sep 2020 02:22:34 GMT
ENV ROS1_DISTRO=noetic
# Thu, 17 Sep 2020 02:22:36 GMT
ENV ROS2_DISTRO=rolling
# Thu, 17 Sep 2020 02:23:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.8-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 02:24:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros1-bridge=0.9.2-2*     ros-rolling-demo-nodes-cpp=0.10.0-1*     ros-rolling-demo-nodes-py=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 02:24:32 GMT
COPY file:f2fca591c0e2a31379c7ea28a9948ef5ee9d4a95b4831016253c1ef1a4f39718 in / 
```

-	Layers:
	-	`sha256:33c9bf8777b52e6bc989f3a77a8a680861b9a7f7385e2d5ee02fdede89acf606`  
		Last Modified: Wed, 16 Sep 2020 08:25:33 GMT  
		Size: 27.2 MB (27158462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1900e162114f589f3e78ba5b26957f2b6ec38c8aaa6efdd8afbfaf5d9e8841`  
		Last Modified: Wed, 16 Sep 2020 23:18:40 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53c8a81c25472b52dd428e136c84a1f407ce933911cab5910676d1a7b7a4df3`  
		Last Modified: Wed, 16 Sep 2020 23:18:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:694ddde6856911f795c55f1e3e7d0658aa1d457594dbf63fd18f6cbc10fd0658`  
		Last Modified: Thu, 17 Sep 2020 02:36:11 GMT  
		Size: 1.2 MB (1177642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea3c413801c3e32051187650ead158523b1424776c96e4f3d3410b393309dc4`  
		Last Modified: Thu, 17 Sep 2020 02:36:03 GMT  
		Size: 5.5 MB (5513389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe76cc3db355f14c9557f875c35c68fbbd7d00a458bbc2ab91a3dd10ae61464b`  
		Last Modified: Thu, 17 Sep 2020 02:36:02 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd035db57351467e95400554c075d902030a7049744862ceb593f9fe9f3d4eed`  
		Last Modified: Thu, 17 Sep 2020 02:49:17 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12724d2403b69e3d36bf504e375b8f7b0a19f2bbb422b4389ea8830e77e06c8`  
		Last Modified: Thu, 17 Sep 2020 02:52:13 GMT  
		Size: 103.5 MB (103525814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49facaa47a0527243f7fa03d8f4423d867ab1e31fb283564d0862605a8131f04`  
		Last Modified: Thu, 17 Sep 2020 02:51:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174e1120b3c8f92589f69e18864846eae80e2c0e1f687e3aedb558b30bc4cb06`  
		Last Modified: Thu, 17 Sep 2020 02:52:43 GMT  
		Size: 60.9 MB (60936034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1717bbe64480e615f8400e5096cf92f2301be6889376b6c3c2d9c5faace0cb1`  
		Last Modified: Thu, 17 Sep 2020 02:52:23 GMT  
		Size: 188.0 KB (187961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246bbd677e626cdc02e76f99f3802463d0a6a8d1998ffc1f27c53544c8cf0e37`  
		Last Modified: Thu, 17 Sep 2020 02:52:22 GMT  
		Size: 2.0 KB (2046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c71727f7c7919ac4bdbc44d4df1bbebfe032559b701861342fea5e2aa9286e`  
		Last Modified: Thu, 17 Sep 2020 02:52:29 GMT  
		Size: 9.3 MB (9303912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee35bc521131507744c6803477f8b0fcf9223cbe8e90c9ef229a49f427ffe67d`  
		Last Modified: Thu, 17 Sep 2020 02:52:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdb680d29de92c253ec19c34caf35213c2fd38900f3f6eb002d6a522706832b`  
		Last Modified: Thu, 17 Sep 2020 02:52:53 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b13f5017f1c5d04cc0d25a2cee0a2bbebb7faea3c23e5d54f5e6586ebf64c78`  
		Last Modified: Thu, 17 Sep 2020 02:53:53 GMT  
		Size: 76.1 MB (76129086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dde7685fee0277cdc9fe354c9611781237ec2356c4faa7e224d32cf2f9b049a`  
		Last Modified: Thu, 17 Sep 2020 02:53:02 GMT  
		Size: 23.0 MB (23014619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238b2024da4b0ccd6539550aea1dfea0fc3f1f31787e9eab9e0fa0cf3b6c8575`  
		Last Modified: Thu, 17 Sep 2020 02:52:53 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

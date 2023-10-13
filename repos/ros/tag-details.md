<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ros`

-	[`ros:humble`](#roshumble)
-	[`ros:humble-perception`](#roshumble-perception)
-	[`ros:humble-perception-jammy`](#roshumble-perception-jammy)
-	[`ros:humble-ros-base`](#roshumble-ros-base)
-	[`ros:humble-ros-base-jammy`](#roshumble-ros-base-jammy)
-	[`ros:humble-ros-core`](#roshumble-ros-core)
-	[`ros:humble-ros-core-jammy`](#roshumble-ros-core-jammy)
-	[`ros:iron`](#rosiron)
-	[`ros:iron-perception`](#rosiron-perception)
-	[`ros:iron-perception-jammy`](#rosiron-perception-jammy)
-	[`ros:iron-ros-base`](#rosiron-ros-base)
-	[`ros:iron-ros-base-jammy`](#rosiron-ros-base-jammy)
-	[`ros:iron-ros-core`](#rosiron-ros-core)
-	[`ros:iron-ros-core-jammy`](#rosiron-ros-core-jammy)
-	[`ros:latest`](#roslatest)
-	[`ros:noetic`](#rosnoetic)
-	[`ros:noetic-perception`](#rosnoetic-perception)
-	[`ros:noetic-perception-focal`](#rosnoetic-perception-focal)
-	[`ros:noetic-robot`](#rosnoetic-robot)
-	[`ros:noetic-robot-focal`](#rosnoetic-robot-focal)
-	[`ros:noetic-ros-base`](#rosnoetic-ros-base)
-	[`ros:noetic-ros-base-focal`](#rosnoetic-ros-base-focal)
-	[`ros:noetic-ros-core`](#rosnoetic-ros-core)
-	[`ros:noetic-ros-core-focal`](#rosnoetic-ros-core-focal)
-	[`ros:rolling`](#rosrolling)
-	[`ros:rolling-perception`](#rosrolling-perception)
-	[`ros:rolling-perception-jammy`](#rosrolling-perception-jammy)
-	[`ros:rolling-ros-base`](#rosrolling-ros-base)
-	[`ros:rolling-ros-base-jammy`](#rosrolling-ros-base-jammy)
-	[`ros:rolling-ros-core`](#rosrolling-ros-core)
-	[`ros:rolling-ros-core-jammy`](#rosrolling-ros-core-jammy)

## `ros:humble`

```console
$ docker pull ros@sha256:3b96085953443c572f7c9e9fd8439e54a83f461ac68d27ec3dae83e827063fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:a9657e73a73dcb7f4bb9bd66e760c250201ff5be4e951b5f615d5fa8b176ebba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263454549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb143c7bfa18aa28b341e2067e86c63d8cbb24019f1ae72b23cf2a18cada317`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:09:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 03 Oct 2023 06:09:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV ROS_DISTRO=humble
# Tue, 03 Oct 2023 06:11:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:11:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 03 Oct 2023 06:11:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Oct 2023 06:11:49 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 06:12:55 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:13:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 03 Oct 2023 06:13:06 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 03 Oct 2023 06:14:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1370ba32049345dce3665687ae8209d03dc6e8d9d44e99e46c0ceb62f9f1f30d`  
		Last Modified: Tue, 03 Oct 2023 06:37:13 GMT  
		Size: 1.2 MB (1213056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c1e1f3dd2585388cc558f6237ee492769081f489b65cd386188d8efb6cdce6`  
		Last Modified: Tue, 03 Oct 2023 06:37:12 GMT  
		Size: 3.8 MB (3828981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198e4b86b803705bfcbea4adc86401d2d0cd4af88199c9e706cf0803b5be7842`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d310e00acb45665d82263e8800579055fb2ea11b71dd4926c8a7323855af7`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63af57a291ea0d8bef7998336bff74edc42cd8c81f6d753a2f5d4f2c809a2b1`  
		Last Modified: Tue, 03 Oct 2023 06:37:27 GMT  
		Size: 106.4 MB (106420533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e044e4a00a19b3e05de479e3a9337d89b05d2bb4bbb253140e06f1354096ac90`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c435980f0d57baf74d055c31cbe6f7c7e6cf2caa6f57ff81dc4e37bd122427fc`  
		Last Modified: Tue, 03 Oct 2023 06:37:48 GMT  
		Size: 98.1 MB (98133952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea32350106421e3ea17aa559eebc1e78a40d606c84104918810317208952319`  
		Last Modified: Tue, 03 Oct 2023 06:37:36 GMT  
		Size: 318.3 KB (318269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aeed20a10372b03facc5f0ed6f47eb4dfd48e64323af8a8b469941191530aef`  
		Last Modified: Tue, 03 Oct 2023 06:37:35 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57055b83861bdeb2d184d6a307e938f912b38d11743f7a00017a02ae8f08d42`  
		Last Modified: Tue, 03 Oct 2023 06:37:39 GMT  
		Size: 23.1 MB (23093974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6d1382ef38812fc2b77beb0e6265e927a1b68c2ab3e47469eb60c9783c9b91e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256085517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d59e3d4efad3c9ae8f9ba40a50e75f232a5ce6a332b493d0dcbddeedbbf537c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:37:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 13 Oct 2023 04:38:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:38:07 GMT
ENV ROS_DISTRO=humble
# Fri, 13 Oct 2023 04:39:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:39:35 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 13 Oct 2023 04:39:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:39:35 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 04:40:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:40:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 04:40:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 13 Oct 2023 04:41:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff18d61171fb1a17fb0edecb7a0600d4d0be1c103726f9d60cfb59071d3eccf9`  
		Last Modified: Fri, 13 Oct 2023 05:00:30 GMT  
		Size: 1.2 MB (1214464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa41e452048780b8d89bde1b448e5c130e073ab26d8a3c3e2ec3d4a4170f55f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 3.8 MB (3801906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c55f0e8967a89d129c1106434dacd41bd9239f7fe793b4dc37245f7a26762f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023f71811e459a590f4b10edecae765c4b654f7139277e4c704f11126c720c5f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c023537795c860c51cdc51a826448aa3f98423714b84b95dea685761f8e013d6`  
		Last Modified: Fri, 13 Oct 2023 05:00:48 GMT  
		Size: 104.2 MB (104151928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfda3e7987bf657d0a886fc085e34ebecaca449450d6b705392eb5c3170fe318`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0a489e10cbdefdd5f5cadbefeb08d5ebd7f0f8888a9aa8868bf249e7ba9498`  
		Last Modified: Fri, 13 Oct 2023 05:01:08 GMT  
		Size: 95.7 MB (95684475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ce9ac65ade437d7a093f3b80dcbc88126a337e45ce69f99234c87019c1bc35`  
		Last Modified: Fri, 13 Oct 2023 05:00:57 GMT  
		Size: 319.3 KB (319340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edfb5ed159e80825a9155603a7778bb0cd6f9f024fd0113561edcedd3909b8ed`  
		Last Modified: Fri, 13 Oct 2023 05:00:57 GMT  
		Size: 2.5 KB (2482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab14f4c10d226ff941d9d47bc4cef0f2f27c6612233a208ec6a18ac86a96daf`  
		Last Modified: Fri, 13 Oct 2023 05:01:01 GMT  
		Size: 22.5 MB (22516571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-perception`

```console
$ docker pull ros@sha256:5debc643ad71223e90640dcc3d43308af3ff0dacd04857ce31c110ef3aab24a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:9f9befd6e9a2a8f1149da2fbbd956bbe0b533a7208dec78a2b8de29d0e3fb700
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **953.6 MB (953632832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85973fd31d73585e9155017091d3f424e6c1984eabd06786b508b717ce87a3b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:09:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 03 Oct 2023 06:09:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV ROS_DISTRO=humble
# Tue, 03 Oct 2023 06:11:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:11:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 03 Oct 2023 06:11:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Oct 2023 06:11:49 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 06:12:55 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:13:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 03 Oct 2023 06:13:06 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 03 Oct 2023 06:14:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:28:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1370ba32049345dce3665687ae8209d03dc6e8d9d44e99e46c0ceb62f9f1f30d`  
		Last Modified: Tue, 03 Oct 2023 06:37:13 GMT  
		Size: 1.2 MB (1213056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c1e1f3dd2585388cc558f6237ee492769081f489b65cd386188d8efb6cdce6`  
		Last Modified: Tue, 03 Oct 2023 06:37:12 GMT  
		Size: 3.8 MB (3828981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198e4b86b803705bfcbea4adc86401d2d0cd4af88199c9e706cf0803b5be7842`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d310e00acb45665d82263e8800579055fb2ea11b71dd4926c8a7323855af7`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63af57a291ea0d8bef7998336bff74edc42cd8c81f6d753a2f5d4f2c809a2b1`  
		Last Modified: Tue, 03 Oct 2023 06:37:27 GMT  
		Size: 106.4 MB (106420533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e044e4a00a19b3e05de479e3a9337d89b05d2bb4bbb253140e06f1354096ac90`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c435980f0d57baf74d055c31cbe6f7c7e6cf2caa6f57ff81dc4e37bd122427fc`  
		Last Modified: Tue, 03 Oct 2023 06:37:48 GMT  
		Size: 98.1 MB (98133952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea32350106421e3ea17aa559eebc1e78a40d606c84104918810317208952319`  
		Last Modified: Tue, 03 Oct 2023 06:37:36 GMT  
		Size: 318.3 KB (318269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aeed20a10372b03facc5f0ed6f47eb4dfd48e64323af8a8b469941191530aef`  
		Last Modified: Tue, 03 Oct 2023 06:37:35 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57055b83861bdeb2d184d6a307e938f912b38d11743f7a00017a02ae8f08d42`  
		Last Modified: Tue, 03 Oct 2023 06:37:39 GMT  
		Size: 23.1 MB (23093974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd61337d9ebac30178159b987501f9338458478530a13c777b8d7969a738a2b`  
		Last Modified: Tue, 03 Oct 2023 06:39:30 GMT  
		Size: 690.2 MB (690178283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:75716a5acc09696b2d5f8ad6804782f5f6dfb2677f69b358cd0e91aa15d6e4cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.1 MB (914137086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c8f194e90b0756bf36dbf4619c86c30124506ffe90254c9b861055ce34b828`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:37:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 13 Oct 2023 04:38:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:38:07 GMT
ENV ROS_DISTRO=humble
# Fri, 13 Oct 2023 04:39:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:39:35 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 13 Oct 2023 04:39:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:39:35 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 04:40:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:40:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 04:40:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 13 Oct 2023 04:41:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:50:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff18d61171fb1a17fb0edecb7a0600d4d0be1c103726f9d60cfb59071d3eccf9`  
		Last Modified: Fri, 13 Oct 2023 05:00:30 GMT  
		Size: 1.2 MB (1214464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa41e452048780b8d89bde1b448e5c130e073ab26d8a3c3e2ec3d4a4170f55f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 3.8 MB (3801906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c55f0e8967a89d129c1106434dacd41bd9239f7fe793b4dc37245f7a26762f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023f71811e459a590f4b10edecae765c4b654f7139277e4c704f11126c720c5f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c023537795c860c51cdc51a826448aa3f98423714b84b95dea685761f8e013d6`  
		Last Modified: Fri, 13 Oct 2023 05:00:48 GMT  
		Size: 104.2 MB (104151928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfda3e7987bf657d0a886fc085e34ebecaca449450d6b705392eb5c3170fe318`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0a489e10cbdefdd5f5cadbefeb08d5ebd7f0f8888a9aa8868bf249e7ba9498`  
		Last Modified: Fri, 13 Oct 2023 05:01:08 GMT  
		Size: 95.7 MB (95684475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ce9ac65ade437d7a093f3b80dcbc88126a337e45ce69f99234c87019c1bc35`  
		Last Modified: Fri, 13 Oct 2023 05:00:57 GMT  
		Size: 319.3 KB (319340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edfb5ed159e80825a9155603a7778bb0cd6f9f024fd0113561edcedd3909b8ed`  
		Last Modified: Fri, 13 Oct 2023 05:00:57 GMT  
		Size: 2.5 KB (2482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab14f4c10d226ff941d9d47bc4cef0f2f27c6612233a208ec6a18ac86a96daf`  
		Last Modified: Fri, 13 Oct 2023 05:01:01 GMT  
		Size: 22.5 MB (22516571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7bc1ce33b1d69bab7e7619d5315fe767059a16a897d044c75626a48cd0c209`  
		Last Modified: Fri, 13 Oct 2023 05:02:46 GMT  
		Size: 658.1 MB (658051569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:5debc643ad71223e90640dcc3d43308af3ff0dacd04857ce31c110ef3aab24a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:9f9befd6e9a2a8f1149da2fbbd956bbe0b533a7208dec78a2b8de29d0e3fb700
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **953.6 MB (953632832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85973fd31d73585e9155017091d3f424e6c1984eabd06786b508b717ce87a3b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:09:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 03 Oct 2023 06:09:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV ROS_DISTRO=humble
# Tue, 03 Oct 2023 06:11:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:11:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 03 Oct 2023 06:11:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Oct 2023 06:11:49 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 06:12:55 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:13:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 03 Oct 2023 06:13:06 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 03 Oct 2023 06:14:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:28:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1370ba32049345dce3665687ae8209d03dc6e8d9d44e99e46c0ceb62f9f1f30d`  
		Last Modified: Tue, 03 Oct 2023 06:37:13 GMT  
		Size: 1.2 MB (1213056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c1e1f3dd2585388cc558f6237ee492769081f489b65cd386188d8efb6cdce6`  
		Last Modified: Tue, 03 Oct 2023 06:37:12 GMT  
		Size: 3.8 MB (3828981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198e4b86b803705bfcbea4adc86401d2d0cd4af88199c9e706cf0803b5be7842`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d310e00acb45665d82263e8800579055fb2ea11b71dd4926c8a7323855af7`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63af57a291ea0d8bef7998336bff74edc42cd8c81f6d753a2f5d4f2c809a2b1`  
		Last Modified: Tue, 03 Oct 2023 06:37:27 GMT  
		Size: 106.4 MB (106420533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e044e4a00a19b3e05de479e3a9337d89b05d2bb4bbb253140e06f1354096ac90`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c435980f0d57baf74d055c31cbe6f7c7e6cf2caa6f57ff81dc4e37bd122427fc`  
		Last Modified: Tue, 03 Oct 2023 06:37:48 GMT  
		Size: 98.1 MB (98133952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea32350106421e3ea17aa559eebc1e78a40d606c84104918810317208952319`  
		Last Modified: Tue, 03 Oct 2023 06:37:36 GMT  
		Size: 318.3 KB (318269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aeed20a10372b03facc5f0ed6f47eb4dfd48e64323af8a8b469941191530aef`  
		Last Modified: Tue, 03 Oct 2023 06:37:35 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57055b83861bdeb2d184d6a307e938f912b38d11743f7a00017a02ae8f08d42`  
		Last Modified: Tue, 03 Oct 2023 06:37:39 GMT  
		Size: 23.1 MB (23093974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acd61337d9ebac30178159b987501f9338458478530a13c777b8d7969a738a2b`  
		Last Modified: Tue, 03 Oct 2023 06:39:30 GMT  
		Size: 690.2 MB (690178283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:75716a5acc09696b2d5f8ad6804782f5f6dfb2677f69b358cd0e91aa15d6e4cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.1 MB (914137086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c8f194e90b0756bf36dbf4619c86c30124506ffe90254c9b861055ce34b828`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:37:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 13 Oct 2023 04:38:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:38:07 GMT
ENV ROS_DISTRO=humble
# Fri, 13 Oct 2023 04:39:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:39:35 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 13 Oct 2023 04:39:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:39:35 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 04:40:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:40:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 04:40:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 13 Oct 2023 04:41:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:50:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff18d61171fb1a17fb0edecb7a0600d4d0be1c103726f9d60cfb59071d3eccf9`  
		Last Modified: Fri, 13 Oct 2023 05:00:30 GMT  
		Size: 1.2 MB (1214464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa41e452048780b8d89bde1b448e5c130e073ab26d8a3c3e2ec3d4a4170f55f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 3.8 MB (3801906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c55f0e8967a89d129c1106434dacd41bd9239f7fe793b4dc37245f7a26762f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023f71811e459a590f4b10edecae765c4b654f7139277e4c704f11126c720c5f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c023537795c860c51cdc51a826448aa3f98423714b84b95dea685761f8e013d6`  
		Last Modified: Fri, 13 Oct 2023 05:00:48 GMT  
		Size: 104.2 MB (104151928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfda3e7987bf657d0a886fc085e34ebecaca449450d6b705392eb5c3170fe318`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0a489e10cbdefdd5f5cadbefeb08d5ebd7f0f8888a9aa8868bf249e7ba9498`  
		Last Modified: Fri, 13 Oct 2023 05:01:08 GMT  
		Size: 95.7 MB (95684475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ce9ac65ade437d7a093f3b80dcbc88126a337e45ce69f99234c87019c1bc35`  
		Last Modified: Fri, 13 Oct 2023 05:00:57 GMT  
		Size: 319.3 KB (319340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edfb5ed159e80825a9155603a7778bb0cd6f9f024fd0113561edcedd3909b8ed`  
		Last Modified: Fri, 13 Oct 2023 05:00:57 GMT  
		Size: 2.5 KB (2482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab14f4c10d226ff941d9d47bc4cef0f2f27c6612233a208ec6a18ac86a96daf`  
		Last Modified: Fri, 13 Oct 2023 05:01:01 GMT  
		Size: 22.5 MB (22516571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7bc1ce33b1d69bab7e7619d5315fe767059a16a897d044c75626a48cd0c209`  
		Last Modified: Fri, 13 Oct 2023 05:02:46 GMT  
		Size: 658.1 MB (658051569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:3b96085953443c572f7c9e9fd8439e54a83f461ac68d27ec3dae83e827063fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:a9657e73a73dcb7f4bb9bd66e760c250201ff5be4e951b5f615d5fa8b176ebba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263454549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb143c7bfa18aa28b341e2067e86c63d8cbb24019f1ae72b23cf2a18cada317`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:09:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 03 Oct 2023 06:09:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV ROS_DISTRO=humble
# Tue, 03 Oct 2023 06:11:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:11:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 03 Oct 2023 06:11:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Oct 2023 06:11:49 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 06:12:55 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:13:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 03 Oct 2023 06:13:06 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 03 Oct 2023 06:14:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1370ba32049345dce3665687ae8209d03dc6e8d9d44e99e46c0ceb62f9f1f30d`  
		Last Modified: Tue, 03 Oct 2023 06:37:13 GMT  
		Size: 1.2 MB (1213056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c1e1f3dd2585388cc558f6237ee492769081f489b65cd386188d8efb6cdce6`  
		Last Modified: Tue, 03 Oct 2023 06:37:12 GMT  
		Size: 3.8 MB (3828981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198e4b86b803705bfcbea4adc86401d2d0cd4af88199c9e706cf0803b5be7842`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d310e00acb45665d82263e8800579055fb2ea11b71dd4926c8a7323855af7`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63af57a291ea0d8bef7998336bff74edc42cd8c81f6d753a2f5d4f2c809a2b1`  
		Last Modified: Tue, 03 Oct 2023 06:37:27 GMT  
		Size: 106.4 MB (106420533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e044e4a00a19b3e05de479e3a9337d89b05d2bb4bbb253140e06f1354096ac90`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c435980f0d57baf74d055c31cbe6f7c7e6cf2caa6f57ff81dc4e37bd122427fc`  
		Last Modified: Tue, 03 Oct 2023 06:37:48 GMT  
		Size: 98.1 MB (98133952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea32350106421e3ea17aa559eebc1e78a40d606c84104918810317208952319`  
		Last Modified: Tue, 03 Oct 2023 06:37:36 GMT  
		Size: 318.3 KB (318269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aeed20a10372b03facc5f0ed6f47eb4dfd48e64323af8a8b469941191530aef`  
		Last Modified: Tue, 03 Oct 2023 06:37:35 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57055b83861bdeb2d184d6a307e938f912b38d11743f7a00017a02ae8f08d42`  
		Last Modified: Tue, 03 Oct 2023 06:37:39 GMT  
		Size: 23.1 MB (23093974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6d1382ef38812fc2b77beb0e6265e927a1b68c2ab3e47469eb60c9783c9b91e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256085517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d59e3d4efad3c9ae8f9ba40a50e75f232a5ce6a332b493d0dcbddeedbbf537c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:37:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 13 Oct 2023 04:38:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:38:07 GMT
ENV ROS_DISTRO=humble
# Fri, 13 Oct 2023 04:39:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:39:35 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 13 Oct 2023 04:39:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:39:35 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 04:40:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:40:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 04:40:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 13 Oct 2023 04:41:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff18d61171fb1a17fb0edecb7a0600d4d0be1c103726f9d60cfb59071d3eccf9`  
		Last Modified: Fri, 13 Oct 2023 05:00:30 GMT  
		Size: 1.2 MB (1214464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa41e452048780b8d89bde1b448e5c130e073ab26d8a3c3e2ec3d4a4170f55f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 3.8 MB (3801906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c55f0e8967a89d129c1106434dacd41bd9239f7fe793b4dc37245f7a26762f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023f71811e459a590f4b10edecae765c4b654f7139277e4c704f11126c720c5f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c023537795c860c51cdc51a826448aa3f98423714b84b95dea685761f8e013d6`  
		Last Modified: Fri, 13 Oct 2023 05:00:48 GMT  
		Size: 104.2 MB (104151928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfda3e7987bf657d0a886fc085e34ebecaca449450d6b705392eb5c3170fe318`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0a489e10cbdefdd5f5cadbefeb08d5ebd7f0f8888a9aa8868bf249e7ba9498`  
		Last Modified: Fri, 13 Oct 2023 05:01:08 GMT  
		Size: 95.7 MB (95684475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ce9ac65ade437d7a093f3b80dcbc88126a337e45ce69f99234c87019c1bc35`  
		Last Modified: Fri, 13 Oct 2023 05:00:57 GMT  
		Size: 319.3 KB (319340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edfb5ed159e80825a9155603a7778bb0cd6f9f024fd0113561edcedd3909b8ed`  
		Last Modified: Fri, 13 Oct 2023 05:00:57 GMT  
		Size: 2.5 KB (2482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab14f4c10d226ff941d9d47bc4cef0f2f27c6612233a208ec6a18ac86a96daf`  
		Last Modified: Fri, 13 Oct 2023 05:01:01 GMT  
		Size: 22.5 MB (22516571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:3b96085953443c572f7c9e9fd8439e54a83f461ac68d27ec3dae83e827063fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:a9657e73a73dcb7f4bb9bd66e760c250201ff5be4e951b5f615d5fa8b176ebba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263454549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb143c7bfa18aa28b341e2067e86c63d8cbb24019f1ae72b23cf2a18cada317`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:09:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 03 Oct 2023 06:09:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV ROS_DISTRO=humble
# Tue, 03 Oct 2023 06:11:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:11:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 03 Oct 2023 06:11:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Oct 2023 06:11:49 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 06:12:55 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:13:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 03 Oct 2023 06:13:06 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 03 Oct 2023 06:14:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1370ba32049345dce3665687ae8209d03dc6e8d9d44e99e46c0ceb62f9f1f30d`  
		Last Modified: Tue, 03 Oct 2023 06:37:13 GMT  
		Size: 1.2 MB (1213056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c1e1f3dd2585388cc558f6237ee492769081f489b65cd386188d8efb6cdce6`  
		Last Modified: Tue, 03 Oct 2023 06:37:12 GMT  
		Size: 3.8 MB (3828981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198e4b86b803705bfcbea4adc86401d2d0cd4af88199c9e706cf0803b5be7842`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d310e00acb45665d82263e8800579055fb2ea11b71dd4926c8a7323855af7`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63af57a291ea0d8bef7998336bff74edc42cd8c81f6d753a2f5d4f2c809a2b1`  
		Last Modified: Tue, 03 Oct 2023 06:37:27 GMT  
		Size: 106.4 MB (106420533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e044e4a00a19b3e05de479e3a9337d89b05d2bb4bbb253140e06f1354096ac90`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c435980f0d57baf74d055c31cbe6f7c7e6cf2caa6f57ff81dc4e37bd122427fc`  
		Last Modified: Tue, 03 Oct 2023 06:37:48 GMT  
		Size: 98.1 MB (98133952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea32350106421e3ea17aa559eebc1e78a40d606c84104918810317208952319`  
		Last Modified: Tue, 03 Oct 2023 06:37:36 GMT  
		Size: 318.3 KB (318269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aeed20a10372b03facc5f0ed6f47eb4dfd48e64323af8a8b469941191530aef`  
		Last Modified: Tue, 03 Oct 2023 06:37:35 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57055b83861bdeb2d184d6a307e938f912b38d11743f7a00017a02ae8f08d42`  
		Last Modified: Tue, 03 Oct 2023 06:37:39 GMT  
		Size: 23.1 MB (23093974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6d1382ef38812fc2b77beb0e6265e927a1b68c2ab3e47469eb60c9783c9b91e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256085517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d59e3d4efad3c9ae8f9ba40a50e75f232a5ce6a332b493d0dcbddeedbbf537c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:37:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 13 Oct 2023 04:38:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:38:07 GMT
ENV ROS_DISTRO=humble
# Fri, 13 Oct 2023 04:39:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:39:35 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 13 Oct 2023 04:39:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:39:35 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 04:40:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:40:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 04:40:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 13 Oct 2023 04:41:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff18d61171fb1a17fb0edecb7a0600d4d0be1c103726f9d60cfb59071d3eccf9`  
		Last Modified: Fri, 13 Oct 2023 05:00:30 GMT  
		Size: 1.2 MB (1214464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa41e452048780b8d89bde1b448e5c130e073ab26d8a3c3e2ec3d4a4170f55f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 3.8 MB (3801906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c55f0e8967a89d129c1106434dacd41bd9239f7fe793b4dc37245f7a26762f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023f71811e459a590f4b10edecae765c4b654f7139277e4c704f11126c720c5f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c023537795c860c51cdc51a826448aa3f98423714b84b95dea685761f8e013d6`  
		Last Modified: Fri, 13 Oct 2023 05:00:48 GMT  
		Size: 104.2 MB (104151928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfda3e7987bf657d0a886fc085e34ebecaca449450d6b705392eb5c3170fe318`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0a489e10cbdefdd5f5cadbefeb08d5ebd7f0f8888a9aa8868bf249e7ba9498`  
		Last Modified: Fri, 13 Oct 2023 05:01:08 GMT  
		Size: 95.7 MB (95684475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ce9ac65ade437d7a093f3b80dcbc88126a337e45ce69f99234c87019c1bc35`  
		Last Modified: Fri, 13 Oct 2023 05:00:57 GMT  
		Size: 319.3 KB (319340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edfb5ed159e80825a9155603a7778bb0cd6f9f024fd0113561edcedd3909b8ed`  
		Last Modified: Fri, 13 Oct 2023 05:00:57 GMT  
		Size: 2.5 KB (2482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab14f4c10d226ff941d9d47bc4cef0f2f27c6612233a208ec6a18ac86a96daf`  
		Last Modified: Fri, 13 Oct 2023 05:01:01 GMT  
		Size: 22.5 MB (22516571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:d3ffa0686d76a1846ecf4ed1ecaf3d5ec042cc22ca0a7d621489a02679f30592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:53c74e56feec06d6ce92013a2bba03f5adb30b8b378fa03300f7f3c61a3660b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141905855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e4795326da29494c410c38313f6db9ccb8342b7210bcfa8b2932e7c35246c0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:09:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 03 Oct 2023 06:09:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV ROS_DISTRO=humble
# Tue, 03 Oct 2023 06:11:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:11:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 03 Oct 2023 06:11:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Oct 2023 06:11:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1370ba32049345dce3665687ae8209d03dc6e8d9d44e99e46c0ceb62f9f1f30d`  
		Last Modified: Tue, 03 Oct 2023 06:37:13 GMT  
		Size: 1.2 MB (1213056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c1e1f3dd2585388cc558f6237ee492769081f489b65cd386188d8efb6cdce6`  
		Last Modified: Tue, 03 Oct 2023 06:37:12 GMT  
		Size: 3.8 MB (3828981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198e4b86b803705bfcbea4adc86401d2d0cd4af88199c9e706cf0803b5be7842`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d310e00acb45665d82263e8800579055fb2ea11b71dd4926c8a7323855af7`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63af57a291ea0d8bef7998336bff74edc42cd8c81f6d753a2f5d4f2c809a2b1`  
		Last Modified: Tue, 03 Oct 2023 06:37:27 GMT  
		Size: 106.4 MB (106420533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e044e4a00a19b3e05de479e3a9337d89b05d2bb4bbb253140e06f1354096ac90`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cbc7e852624d2c318fc4a363e4ea2a4f36d20ee00c54dd6728cbf70d6cf729ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137562649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a11217ed4a7b2efff89f4f5baaa1d07042502c240978402ce00e384881fcbdea`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:37:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 13 Oct 2023 04:38:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:38:07 GMT
ENV ROS_DISTRO=humble
# Fri, 13 Oct 2023 04:39:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:39:35 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 13 Oct 2023 04:39:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:39:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff18d61171fb1a17fb0edecb7a0600d4d0be1c103726f9d60cfb59071d3eccf9`  
		Last Modified: Fri, 13 Oct 2023 05:00:30 GMT  
		Size: 1.2 MB (1214464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa41e452048780b8d89bde1b448e5c130e073ab26d8a3c3e2ec3d4a4170f55f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 3.8 MB (3801906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c55f0e8967a89d129c1106434dacd41bd9239f7fe793b4dc37245f7a26762f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023f71811e459a590f4b10edecae765c4b654f7139277e4c704f11126c720c5f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c023537795c860c51cdc51a826448aa3f98423714b84b95dea685761f8e013d6`  
		Last Modified: Fri, 13 Oct 2023 05:00:48 GMT  
		Size: 104.2 MB (104151928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfda3e7987bf657d0a886fc085e34ebecaca449450d6b705392eb5c3170fe318`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:d3ffa0686d76a1846ecf4ed1ecaf3d5ec042cc22ca0a7d621489a02679f30592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:53c74e56feec06d6ce92013a2bba03f5adb30b8b378fa03300f7f3c61a3660b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141905855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e4795326da29494c410c38313f6db9ccb8342b7210bcfa8b2932e7c35246c0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:09:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 03 Oct 2023 06:09:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV ROS_DISTRO=humble
# Tue, 03 Oct 2023 06:11:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:11:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 03 Oct 2023 06:11:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Oct 2023 06:11:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1370ba32049345dce3665687ae8209d03dc6e8d9d44e99e46c0ceb62f9f1f30d`  
		Last Modified: Tue, 03 Oct 2023 06:37:13 GMT  
		Size: 1.2 MB (1213056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c1e1f3dd2585388cc558f6237ee492769081f489b65cd386188d8efb6cdce6`  
		Last Modified: Tue, 03 Oct 2023 06:37:12 GMT  
		Size: 3.8 MB (3828981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198e4b86b803705bfcbea4adc86401d2d0cd4af88199c9e706cf0803b5be7842`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d310e00acb45665d82263e8800579055fb2ea11b71dd4926c8a7323855af7`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63af57a291ea0d8bef7998336bff74edc42cd8c81f6d753a2f5d4f2c809a2b1`  
		Last Modified: Tue, 03 Oct 2023 06:37:27 GMT  
		Size: 106.4 MB (106420533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e044e4a00a19b3e05de479e3a9337d89b05d2bb4bbb253140e06f1354096ac90`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cbc7e852624d2c318fc4a363e4ea2a4f36d20ee00c54dd6728cbf70d6cf729ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137562649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a11217ed4a7b2efff89f4f5baaa1d07042502c240978402ce00e384881fcbdea`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:37:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 13 Oct 2023 04:38:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:38:07 GMT
ENV ROS_DISTRO=humble
# Fri, 13 Oct 2023 04:39:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:39:35 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 13 Oct 2023 04:39:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:39:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff18d61171fb1a17fb0edecb7a0600d4d0be1c103726f9d60cfb59071d3eccf9`  
		Last Modified: Fri, 13 Oct 2023 05:00:30 GMT  
		Size: 1.2 MB (1214464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa41e452048780b8d89bde1b448e5c130e073ab26d8a3c3e2ec3d4a4170f55f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 3.8 MB (3801906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c55f0e8967a89d129c1106434dacd41bd9239f7fe793b4dc37245f7a26762f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023f71811e459a590f4b10edecae765c4b654f7139277e4c704f11126c720c5f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c023537795c860c51cdc51a826448aa3f98423714b84b95dea685761f8e013d6`  
		Last Modified: Fri, 13 Oct 2023 05:00:48 GMT  
		Size: 104.2 MB (104151928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfda3e7987bf657d0a886fc085e34ebecaca449450d6b705392eb5c3170fe318`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron`

```console
$ docker pull ros@sha256:ca1916d2c292d2f57b40573bdb3c9937b8ceb3837f9b2b4d5faceb0e9fdd9b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron` - linux; amd64

```console
$ docker pull ros@sha256:61eb3c9f56d43eb810b2d192d604c692a9305f1f71ed56de06fa3fe1d4fbe142
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268906475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e095263ce4cd11daf04a3b7de88bd0d602d325c77a22fd9734ece4ce1e7892`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:09:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 03 Oct 2023 06:09:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Oct 2023 06:29:07 GMT
ENV ROS_DISTRO=iron
# Tue, 03 Oct 2023 06:30:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:30:15 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 03 Oct 2023 06:30:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Oct 2023 06:30:15 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 06:30:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:30:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 03 Oct 2023 06:30:56 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 03 Oct 2023 06:31:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1370ba32049345dce3665687ae8209d03dc6e8d9d44e99e46c0ceb62f9f1f30d`  
		Last Modified: Tue, 03 Oct 2023 06:37:13 GMT  
		Size: 1.2 MB (1213056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c1e1f3dd2585388cc558f6237ee492769081f489b65cd386188d8efb6cdce6`  
		Last Modified: Tue, 03 Oct 2023 06:37:12 GMT  
		Size: 3.8 MB (3828981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198e4b86b803705bfcbea4adc86401d2d0cd4af88199c9e706cf0803b5be7842`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d310e00acb45665d82263e8800579055fb2ea11b71dd4926c8a7323855af7`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23a4f8abcdb7d54b1be57c8c5a7b900175491bf0a6c728ec1ff988721eeb650`  
		Last Modified: Tue, 03 Oct 2023 06:39:58 GMT  
		Size: 124.2 MB (124214286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e5bde6e62e3000d8b94ad515014497a6fa4a570dad9498a8ae2f1237452198`  
		Last Modified: Tue, 03 Oct 2023 06:39:39 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e24fe421e5b439046c262749796b2f9d58ebc40de204cfadb5c956943845717`  
		Last Modified: Tue, 03 Oct 2023 06:40:19 GMT  
		Size: 85.2 MB (85169141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22179de2db23d58e3be85b024d47ba5a2380e9ee2d8da5dc834879354909c521`  
		Last Modified: Tue, 03 Oct 2023 06:40:09 GMT  
		Size: 304.7 KB (304715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74e90661265c45926e24a78f9376fa9773c906d6a6e0858990bab9abc0534c4`  
		Last Modified: Tue, 03 Oct 2023 06:40:08 GMT  
		Size: 2.5 KB (2480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6d02fed5e2a9b1964ba837a59e99999255fd8e141dc0a29a079ef8bef0201e`  
		Last Modified: Tue, 03 Oct 2023 06:40:14 GMT  
		Size: 23.7 MB (23730531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5a813a8e3985628fe6982d47598e20dc739668aa3dfc7ba751cf65b0a5de4fd4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261352622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63dbcd822b0ded6f61ded207258977796f50e596d7bcad3a7499a441251165a3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:37:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 13 Oct 2023 04:38:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:50:42 GMT
ENV ROS_DISTRO=iron
# Fri, 13 Oct 2023 04:51:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:51:31 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 13 Oct 2023 04:51:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:51:31 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 04:51:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:51:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 04:52:03 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 13 Oct 2023 04:52:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff18d61171fb1a17fb0edecb7a0600d4d0be1c103726f9d60cfb59071d3eccf9`  
		Last Modified: Fri, 13 Oct 2023 05:00:30 GMT  
		Size: 1.2 MB (1214464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa41e452048780b8d89bde1b448e5c130e073ab26d8a3c3e2ec3d4a4170f55f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 3.8 MB (3801906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c55f0e8967a89d129c1106434dacd41bd9239f7fe793b4dc37245f7a26762f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023f71811e459a590f4b10edecae765c4b654f7139277e4c704f11126c720c5f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe7e5397da56a4ded96341848bbe099efaf06181bb8a09f3720aeb98cd49c69`  
		Last Modified: Fri, 13 Oct 2023 05:03:18 GMT  
		Size: 121.7 MB (121671888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b628474c464bf47e0464b172ff209e5e12441f2570b8a83504c6ef68bc1f77`  
		Last Modified: Fri, 13 Oct 2023 05:02:55 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82511f0dabbf715d554877bab0fec36b1418a40aa932175ad0816f595105f435`  
		Last Modified: Fri, 13 Oct 2023 05:03:35 GMT  
		Size: 82.8 MB (82845322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a7517588a907a56e240f9131473fa8f9e8f3453f23e00a962242a46ea01bc9`  
		Last Modified: Fri, 13 Oct 2023 05:03:27 GMT  
		Size: 304.9 KB (304924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7110d57994728ed7d08117f21b0158ae78a4cb11c5efb4b68db0626e995e099`  
		Last Modified: Fri, 13 Oct 2023 05:03:27 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e9dc421947da7f84fb4df824e59128c51449f0220cbfa2ee41ee150798241d`  
		Last Modified: Fri, 13 Oct 2023 05:03:31 GMT  
		Size: 23.1 MB (23117319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-perception`

```console
$ docker pull ros@sha256:f7ebea3b5fedac76042d22fd01187fa52325aea7274c19191a0348c49b20ed19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-perception` - linux; amd64

```console
$ docker pull ros@sha256:17f5a767333182c62e6f28c297e9ee405b9942255c6d8c69b19b6b9e6e483f2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **959.8 MB (959785063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441c3e0644a795c2c0ed3ba2e4d2a8d6d211a85a0c61be4a3b8afb651491595c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:09:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 03 Oct 2023 06:09:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Oct 2023 06:29:07 GMT
ENV ROS_DISTRO=iron
# Tue, 03 Oct 2023 06:30:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:30:15 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 03 Oct 2023 06:30:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Oct 2023 06:30:15 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 06:30:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:30:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 03 Oct 2023 06:30:56 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 03 Oct 2023 06:31:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:32:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1370ba32049345dce3665687ae8209d03dc6e8d9d44e99e46c0ceb62f9f1f30d`  
		Last Modified: Tue, 03 Oct 2023 06:37:13 GMT  
		Size: 1.2 MB (1213056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c1e1f3dd2585388cc558f6237ee492769081f489b65cd386188d8efb6cdce6`  
		Last Modified: Tue, 03 Oct 2023 06:37:12 GMT  
		Size: 3.8 MB (3828981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198e4b86b803705bfcbea4adc86401d2d0cd4af88199c9e706cf0803b5be7842`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d310e00acb45665d82263e8800579055fb2ea11b71dd4926c8a7323855af7`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23a4f8abcdb7d54b1be57c8c5a7b900175491bf0a6c728ec1ff988721eeb650`  
		Last Modified: Tue, 03 Oct 2023 06:39:58 GMT  
		Size: 124.2 MB (124214286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e5bde6e62e3000d8b94ad515014497a6fa4a570dad9498a8ae2f1237452198`  
		Last Modified: Tue, 03 Oct 2023 06:39:39 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e24fe421e5b439046c262749796b2f9d58ebc40de204cfadb5c956943845717`  
		Last Modified: Tue, 03 Oct 2023 06:40:19 GMT  
		Size: 85.2 MB (85169141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22179de2db23d58e3be85b024d47ba5a2380e9ee2d8da5dc834879354909c521`  
		Last Modified: Tue, 03 Oct 2023 06:40:09 GMT  
		Size: 304.7 KB (304715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74e90661265c45926e24a78f9376fa9773c906d6a6e0858990bab9abc0534c4`  
		Last Modified: Tue, 03 Oct 2023 06:40:08 GMT  
		Size: 2.5 KB (2480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6d02fed5e2a9b1964ba837a59e99999255fd8e141dc0a29a079ef8bef0201e`  
		Last Modified: Tue, 03 Oct 2023 06:40:14 GMT  
		Size: 23.7 MB (23730531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d5b74305ac80126764d3e73b18f4217aab8897a19f93473082c60c22def31c`  
		Last Modified: Tue, 03 Oct 2023 06:42:01 GMT  
		Size: 690.9 MB (690878588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b834e3b6e098d103e392d8d18279ce16e41f80bd3d24fee8262623948cbd5ccc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.0 MB (920007927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca995c3df947fa505348a84f5e41a19b515da2924363f12278987903b8c5d4b9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:37:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 13 Oct 2023 04:38:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:50:42 GMT
ENV ROS_DISTRO=iron
# Fri, 13 Oct 2023 04:51:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:51:31 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 13 Oct 2023 04:51:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:51:31 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 04:51:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:51:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 04:52:03 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 13 Oct 2023 04:52:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:54:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff18d61171fb1a17fb0edecb7a0600d4d0be1c103726f9d60cfb59071d3eccf9`  
		Last Modified: Fri, 13 Oct 2023 05:00:30 GMT  
		Size: 1.2 MB (1214464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa41e452048780b8d89bde1b448e5c130e073ab26d8a3c3e2ec3d4a4170f55f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 3.8 MB (3801906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c55f0e8967a89d129c1106434dacd41bd9239f7fe793b4dc37245f7a26762f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023f71811e459a590f4b10edecae765c4b654f7139277e4c704f11126c720c5f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe7e5397da56a4ded96341848bbe099efaf06181bb8a09f3720aeb98cd49c69`  
		Last Modified: Fri, 13 Oct 2023 05:03:18 GMT  
		Size: 121.7 MB (121671888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b628474c464bf47e0464b172ff209e5e12441f2570b8a83504c6ef68bc1f77`  
		Last Modified: Fri, 13 Oct 2023 05:02:55 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82511f0dabbf715d554877bab0fec36b1418a40aa932175ad0816f595105f435`  
		Last Modified: Fri, 13 Oct 2023 05:03:35 GMT  
		Size: 82.8 MB (82845322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a7517588a907a56e240f9131473fa8f9e8f3453f23e00a962242a46ea01bc9`  
		Last Modified: Fri, 13 Oct 2023 05:03:27 GMT  
		Size: 304.9 KB (304924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7110d57994728ed7d08117f21b0158ae78a4cb11c5efb4b68db0626e995e099`  
		Last Modified: Fri, 13 Oct 2023 05:03:27 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e9dc421947da7f84fb4df824e59128c51449f0220cbfa2ee41ee150798241d`  
		Last Modified: Fri, 13 Oct 2023 05:03:31 GMT  
		Size: 23.1 MB (23117319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1faa38f97a7c630c926e01526405373d132b0e63c87daf4f874d27dea1eaa825`  
		Last Modified: Fri, 13 Oct 2023 05:05:11 GMT  
		Size: 658.7 MB (658655305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-perception-jammy`

```console
$ docker pull ros@sha256:f7ebea3b5fedac76042d22fd01187fa52325aea7274c19191a0348c49b20ed19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:17f5a767333182c62e6f28c297e9ee405b9942255c6d8c69b19b6b9e6e483f2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **959.8 MB (959785063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441c3e0644a795c2c0ed3ba2e4d2a8d6d211a85a0c61be4a3b8afb651491595c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:09:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 03 Oct 2023 06:09:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Oct 2023 06:29:07 GMT
ENV ROS_DISTRO=iron
# Tue, 03 Oct 2023 06:30:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:30:15 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 03 Oct 2023 06:30:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Oct 2023 06:30:15 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 06:30:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:30:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 03 Oct 2023 06:30:56 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 03 Oct 2023 06:31:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:32:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1370ba32049345dce3665687ae8209d03dc6e8d9d44e99e46c0ceb62f9f1f30d`  
		Last Modified: Tue, 03 Oct 2023 06:37:13 GMT  
		Size: 1.2 MB (1213056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c1e1f3dd2585388cc558f6237ee492769081f489b65cd386188d8efb6cdce6`  
		Last Modified: Tue, 03 Oct 2023 06:37:12 GMT  
		Size: 3.8 MB (3828981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198e4b86b803705bfcbea4adc86401d2d0cd4af88199c9e706cf0803b5be7842`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d310e00acb45665d82263e8800579055fb2ea11b71dd4926c8a7323855af7`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23a4f8abcdb7d54b1be57c8c5a7b900175491bf0a6c728ec1ff988721eeb650`  
		Last Modified: Tue, 03 Oct 2023 06:39:58 GMT  
		Size: 124.2 MB (124214286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e5bde6e62e3000d8b94ad515014497a6fa4a570dad9498a8ae2f1237452198`  
		Last Modified: Tue, 03 Oct 2023 06:39:39 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e24fe421e5b439046c262749796b2f9d58ebc40de204cfadb5c956943845717`  
		Last Modified: Tue, 03 Oct 2023 06:40:19 GMT  
		Size: 85.2 MB (85169141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22179de2db23d58e3be85b024d47ba5a2380e9ee2d8da5dc834879354909c521`  
		Last Modified: Tue, 03 Oct 2023 06:40:09 GMT  
		Size: 304.7 KB (304715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74e90661265c45926e24a78f9376fa9773c906d6a6e0858990bab9abc0534c4`  
		Last Modified: Tue, 03 Oct 2023 06:40:08 GMT  
		Size: 2.5 KB (2480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6d02fed5e2a9b1964ba837a59e99999255fd8e141dc0a29a079ef8bef0201e`  
		Last Modified: Tue, 03 Oct 2023 06:40:14 GMT  
		Size: 23.7 MB (23730531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d5b74305ac80126764d3e73b18f4217aab8897a19f93473082c60c22def31c`  
		Last Modified: Tue, 03 Oct 2023 06:42:01 GMT  
		Size: 690.9 MB (690878588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b834e3b6e098d103e392d8d18279ce16e41f80bd3d24fee8262623948cbd5ccc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.0 MB (920007927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca995c3df947fa505348a84f5e41a19b515da2924363f12278987903b8c5d4b9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:37:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 13 Oct 2023 04:38:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:50:42 GMT
ENV ROS_DISTRO=iron
# Fri, 13 Oct 2023 04:51:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:51:31 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 13 Oct 2023 04:51:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:51:31 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 04:51:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:51:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 04:52:03 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 13 Oct 2023 04:52:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:54:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-perception=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff18d61171fb1a17fb0edecb7a0600d4d0be1c103726f9d60cfb59071d3eccf9`  
		Last Modified: Fri, 13 Oct 2023 05:00:30 GMT  
		Size: 1.2 MB (1214464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa41e452048780b8d89bde1b448e5c130e073ab26d8a3c3e2ec3d4a4170f55f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 3.8 MB (3801906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c55f0e8967a89d129c1106434dacd41bd9239f7fe793b4dc37245f7a26762f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023f71811e459a590f4b10edecae765c4b654f7139277e4c704f11126c720c5f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe7e5397da56a4ded96341848bbe099efaf06181bb8a09f3720aeb98cd49c69`  
		Last Modified: Fri, 13 Oct 2023 05:03:18 GMT  
		Size: 121.7 MB (121671888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b628474c464bf47e0464b172ff209e5e12441f2570b8a83504c6ef68bc1f77`  
		Last Modified: Fri, 13 Oct 2023 05:02:55 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82511f0dabbf715d554877bab0fec36b1418a40aa932175ad0816f595105f435`  
		Last Modified: Fri, 13 Oct 2023 05:03:35 GMT  
		Size: 82.8 MB (82845322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a7517588a907a56e240f9131473fa8f9e8f3453f23e00a962242a46ea01bc9`  
		Last Modified: Fri, 13 Oct 2023 05:03:27 GMT  
		Size: 304.9 KB (304924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7110d57994728ed7d08117f21b0158ae78a4cb11c5efb4b68db0626e995e099`  
		Last Modified: Fri, 13 Oct 2023 05:03:27 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e9dc421947da7f84fb4df824e59128c51449f0220cbfa2ee41ee150798241d`  
		Last Modified: Fri, 13 Oct 2023 05:03:31 GMT  
		Size: 23.1 MB (23117319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1faa38f97a7c630c926e01526405373d132b0e63c87daf4f874d27dea1eaa825`  
		Last Modified: Fri, 13 Oct 2023 05:05:11 GMT  
		Size: 658.7 MB (658655305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-base`

```console
$ docker pull ros@sha256:ca1916d2c292d2f57b40573bdb3c9937b8ceb3837f9b2b4d5faceb0e9fdd9b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:61eb3c9f56d43eb810b2d192d604c692a9305f1f71ed56de06fa3fe1d4fbe142
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268906475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e095263ce4cd11daf04a3b7de88bd0d602d325c77a22fd9734ece4ce1e7892`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:09:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 03 Oct 2023 06:09:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Oct 2023 06:29:07 GMT
ENV ROS_DISTRO=iron
# Tue, 03 Oct 2023 06:30:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:30:15 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 03 Oct 2023 06:30:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Oct 2023 06:30:15 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 06:30:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:30:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 03 Oct 2023 06:30:56 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 03 Oct 2023 06:31:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1370ba32049345dce3665687ae8209d03dc6e8d9d44e99e46c0ceb62f9f1f30d`  
		Last Modified: Tue, 03 Oct 2023 06:37:13 GMT  
		Size: 1.2 MB (1213056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c1e1f3dd2585388cc558f6237ee492769081f489b65cd386188d8efb6cdce6`  
		Last Modified: Tue, 03 Oct 2023 06:37:12 GMT  
		Size: 3.8 MB (3828981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198e4b86b803705bfcbea4adc86401d2d0cd4af88199c9e706cf0803b5be7842`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d310e00acb45665d82263e8800579055fb2ea11b71dd4926c8a7323855af7`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23a4f8abcdb7d54b1be57c8c5a7b900175491bf0a6c728ec1ff988721eeb650`  
		Last Modified: Tue, 03 Oct 2023 06:39:58 GMT  
		Size: 124.2 MB (124214286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e5bde6e62e3000d8b94ad515014497a6fa4a570dad9498a8ae2f1237452198`  
		Last Modified: Tue, 03 Oct 2023 06:39:39 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e24fe421e5b439046c262749796b2f9d58ebc40de204cfadb5c956943845717`  
		Last Modified: Tue, 03 Oct 2023 06:40:19 GMT  
		Size: 85.2 MB (85169141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22179de2db23d58e3be85b024d47ba5a2380e9ee2d8da5dc834879354909c521`  
		Last Modified: Tue, 03 Oct 2023 06:40:09 GMT  
		Size: 304.7 KB (304715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74e90661265c45926e24a78f9376fa9773c906d6a6e0858990bab9abc0534c4`  
		Last Modified: Tue, 03 Oct 2023 06:40:08 GMT  
		Size: 2.5 KB (2480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6d02fed5e2a9b1964ba837a59e99999255fd8e141dc0a29a079ef8bef0201e`  
		Last Modified: Tue, 03 Oct 2023 06:40:14 GMT  
		Size: 23.7 MB (23730531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5a813a8e3985628fe6982d47598e20dc739668aa3dfc7ba751cf65b0a5de4fd4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261352622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63dbcd822b0ded6f61ded207258977796f50e596d7bcad3a7499a441251165a3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:37:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 13 Oct 2023 04:38:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:50:42 GMT
ENV ROS_DISTRO=iron
# Fri, 13 Oct 2023 04:51:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:51:31 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 13 Oct 2023 04:51:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:51:31 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 04:51:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:51:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 04:52:03 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 13 Oct 2023 04:52:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff18d61171fb1a17fb0edecb7a0600d4d0be1c103726f9d60cfb59071d3eccf9`  
		Last Modified: Fri, 13 Oct 2023 05:00:30 GMT  
		Size: 1.2 MB (1214464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa41e452048780b8d89bde1b448e5c130e073ab26d8a3c3e2ec3d4a4170f55f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 3.8 MB (3801906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c55f0e8967a89d129c1106434dacd41bd9239f7fe793b4dc37245f7a26762f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023f71811e459a590f4b10edecae765c4b654f7139277e4c704f11126c720c5f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe7e5397da56a4ded96341848bbe099efaf06181bb8a09f3720aeb98cd49c69`  
		Last Modified: Fri, 13 Oct 2023 05:03:18 GMT  
		Size: 121.7 MB (121671888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b628474c464bf47e0464b172ff209e5e12441f2570b8a83504c6ef68bc1f77`  
		Last Modified: Fri, 13 Oct 2023 05:02:55 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82511f0dabbf715d554877bab0fec36b1418a40aa932175ad0816f595105f435`  
		Last Modified: Fri, 13 Oct 2023 05:03:35 GMT  
		Size: 82.8 MB (82845322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a7517588a907a56e240f9131473fa8f9e8f3453f23e00a962242a46ea01bc9`  
		Last Modified: Fri, 13 Oct 2023 05:03:27 GMT  
		Size: 304.9 KB (304924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7110d57994728ed7d08117f21b0158ae78a4cb11c5efb4b68db0626e995e099`  
		Last Modified: Fri, 13 Oct 2023 05:03:27 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e9dc421947da7f84fb4df824e59128c51449f0220cbfa2ee41ee150798241d`  
		Last Modified: Fri, 13 Oct 2023 05:03:31 GMT  
		Size: 23.1 MB (23117319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-base-jammy`

```console
$ docker pull ros@sha256:ca1916d2c292d2f57b40573bdb3c9937b8ceb3837f9b2b4d5faceb0e9fdd9b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:61eb3c9f56d43eb810b2d192d604c692a9305f1f71ed56de06fa3fe1d4fbe142
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268906475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e095263ce4cd11daf04a3b7de88bd0d602d325c77a22fd9734ece4ce1e7892`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:09:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 03 Oct 2023 06:09:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Oct 2023 06:29:07 GMT
ENV ROS_DISTRO=iron
# Tue, 03 Oct 2023 06:30:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:30:15 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 03 Oct 2023 06:30:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Oct 2023 06:30:15 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 06:30:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:30:51 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 03 Oct 2023 06:30:56 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 03 Oct 2023 06:31:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1370ba32049345dce3665687ae8209d03dc6e8d9d44e99e46c0ceb62f9f1f30d`  
		Last Modified: Tue, 03 Oct 2023 06:37:13 GMT  
		Size: 1.2 MB (1213056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c1e1f3dd2585388cc558f6237ee492769081f489b65cd386188d8efb6cdce6`  
		Last Modified: Tue, 03 Oct 2023 06:37:12 GMT  
		Size: 3.8 MB (3828981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198e4b86b803705bfcbea4adc86401d2d0cd4af88199c9e706cf0803b5be7842`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d310e00acb45665d82263e8800579055fb2ea11b71dd4926c8a7323855af7`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23a4f8abcdb7d54b1be57c8c5a7b900175491bf0a6c728ec1ff988721eeb650`  
		Last Modified: Tue, 03 Oct 2023 06:39:58 GMT  
		Size: 124.2 MB (124214286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e5bde6e62e3000d8b94ad515014497a6fa4a570dad9498a8ae2f1237452198`  
		Last Modified: Tue, 03 Oct 2023 06:39:39 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e24fe421e5b439046c262749796b2f9d58ebc40de204cfadb5c956943845717`  
		Last Modified: Tue, 03 Oct 2023 06:40:19 GMT  
		Size: 85.2 MB (85169141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22179de2db23d58e3be85b024d47ba5a2380e9ee2d8da5dc834879354909c521`  
		Last Modified: Tue, 03 Oct 2023 06:40:09 GMT  
		Size: 304.7 KB (304715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74e90661265c45926e24a78f9376fa9773c906d6a6e0858990bab9abc0534c4`  
		Last Modified: Tue, 03 Oct 2023 06:40:08 GMT  
		Size: 2.5 KB (2480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6d02fed5e2a9b1964ba837a59e99999255fd8e141dc0a29a079ef8bef0201e`  
		Last Modified: Tue, 03 Oct 2023 06:40:14 GMT  
		Size: 23.7 MB (23730531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:5a813a8e3985628fe6982d47598e20dc739668aa3dfc7ba751cf65b0a5de4fd4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261352622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63dbcd822b0ded6f61ded207258977796f50e596d7bcad3a7499a441251165a3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:37:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 13 Oct 2023 04:38:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:50:42 GMT
ENV ROS_DISTRO=iron
# Fri, 13 Oct 2023 04:51:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:51:31 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 13 Oct 2023 04:51:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:51:31 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 04:51:53 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:51:57 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 04:52:03 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 13 Oct 2023 04:52:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-base=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff18d61171fb1a17fb0edecb7a0600d4d0be1c103726f9d60cfb59071d3eccf9`  
		Last Modified: Fri, 13 Oct 2023 05:00:30 GMT  
		Size: 1.2 MB (1214464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa41e452048780b8d89bde1b448e5c130e073ab26d8a3c3e2ec3d4a4170f55f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 3.8 MB (3801906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c55f0e8967a89d129c1106434dacd41bd9239f7fe793b4dc37245f7a26762f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023f71811e459a590f4b10edecae765c4b654f7139277e4c704f11126c720c5f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe7e5397da56a4ded96341848bbe099efaf06181bb8a09f3720aeb98cd49c69`  
		Last Modified: Fri, 13 Oct 2023 05:03:18 GMT  
		Size: 121.7 MB (121671888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b628474c464bf47e0464b172ff209e5e12441f2570b8a83504c6ef68bc1f77`  
		Last Modified: Fri, 13 Oct 2023 05:02:55 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82511f0dabbf715d554877bab0fec36b1418a40aa932175ad0816f595105f435`  
		Last Modified: Fri, 13 Oct 2023 05:03:35 GMT  
		Size: 82.8 MB (82845322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a7517588a907a56e240f9131473fa8f9e8f3453f23e00a962242a46ea01bc9`  
		Last Modified: Fri, 13 Oct 2023 05:03:27 GMT  
		Size: 304.9 KB (304924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7110d57994728ed7d08117f21b0158ae78a4cb11c5efb4b68db0626e995e099`  
		Last Modified: Fri, 13 Oct 2023 05:03:27 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e9dc421947da7f84fb4df824e59128c51449f0220cbfa2ee41ee150798241d`  
		Last Modified: Fri, 13 Oct 2023 05:03:31 GMT  
		Size: 23.1 MB (23117319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-core`

```console
$ docker pull ros@sha256:f3b8f436a0b3920a8f4407de50d03e879ae339b754f5ce1fc163901dfd4b4f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:fa53ad1e0c2f588cc6ef6b8bd0e3b78aca7e679c97d8e039831d6541693de72f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159699608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732ff69c7dea2ab74e36b248324ad3a5cb16f2c03b734884956e77919995c864`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:09:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 03 Oct 2023 06:09:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Oct 2023 06:29:07 GMT
ENV ROS_DISTRO=iron
# Tue, 03 Oct 2023 06:30:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:30:15 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 03 Oct 2023 06:30:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Oct 2023 06:30:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1370ba32049345dce3665687ae8209d03dc6e8d9d44e99e46c0ceb62f9f1f30d`  
		Last Modified: Tue, 03 Oct 2023 06:37:13 GMT  
		Size: 1.2 MB (1213056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c1e1f3dd2585388cc558f6237ee492769081f489b65cd386188d8efb6cdce6`  
		Last Modified: Tue, 03 Oct 2023 06:37:12 GMT  
		Size: 3.8 MB (3828981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198e4b86b803705bfcbea4adc86401d2d0cd4af88199c9e706cf0803b5be7842`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d310e00acb45665d82263e8800579055fb2ea11b71dd4926c8a7323855af7`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23a4f8abcdb7d54b1be57c8c5a7b900175491bf0a6c728ec1ff988721eeb650`  
		Last Modified: Tue, 03 Oct 2023 06:39:58 GMT  
		Size: 124.2 MB (124214286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e5bde6e62e3000d8b94ad515014497a6fa4a570dad9498a8ae2f1237452198`  
		Last Modified: Tue, 03 Oct 2023 06:39:39 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:72406c75aa72fcd711246fadac052734753c30ab3db640abb407750c7b47badd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155082610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a5671b7e0a5cc99900a4ea2b6df0647e7d42ce296c78b39fa226eb6e74d073`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:37:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 13 Oct 2023 04:38:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:50:42 GMT
ENV ROS_DISTRO=iron
# Fri, 13 Oct 2023 04:51:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:51:31 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 13 Oct 2023 04:51:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:51:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff18d61171fb1a17fb0edecb7a0600d4d0be1c103726f9d60cfb59071d3eccf9`  
		Last Modified: Fri, 13 Oct 2023 05:00:30 GMT  
		Size: 1.2 MB (1214464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa41e452048780b8d89bde1b448e5c130e073ab26d8a3c3e2ec3d4a4170f55f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 3.8 MB (3801906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c55f0e8967a89d129c1106434dacd41bd9239f7fe793b4dc37245f7a26762f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023f71811e459a590f4b10edecae765c4b654f7139277e4c704f11126c720c5f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe7e5397da56a4ded96341848bbe099efaf06181bb8a09f3720aeb98cd49c69`  
		Last Modified: Fri, 13 Oct 2023 05:03:18 GMT  
		Size: 121.7 MB (121671888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b628474c464bf47e0464b172ff209e5e12441f2570b8a83504c6ef68bc1f77`  
		Last Modified: Fri, 13 Oct 2023 05:02:55 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:iron-ros-core-jammy`

```console
$ docker pull ros@sha256:f3b8f436a0b3920a8f4407de50d03e879ae339b754f5ce1fc163901dfd4b4f3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:iron-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:fa53ad1e0c2f588cc6ef6b8bd0e3b78aca7e679c97d8e039831d6541693de72f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159699608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732ff69c7dea2ab74e36b248324ad3a5cb16f2c03b734884956e77919995c864`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:09:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 03 Oct 2023 06:09:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Oct 2023 06:29:07 GMT
ENV ROS_DISTRO=iron
# Tue, 03 Oct 2023 06:30:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:30:15 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 03 Oct 2023 06:30:15 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Oct 2023 06:30:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1370ba32049345dce3665687ae8209d03dc6e8d9d44e99e46c0ceb62f9f1f30d`  
		Last Modified: Tue, 03 Oct 2023 06:37:13 GMT  
		Size: 1.2 MB (1213056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c1e1f3dd2585388cc558f6237ee492769081f489b65cd386188d8efb6cdce6`  
		Last Modified: Tue, 03 Oct 2023 06:37:12 GMT  
		Size: 3.8 MB (3828981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198e4b86b803705bfcbea4adc86401d2d0cd4af88199c9e706cf0803b5be7842`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d310e00acb45665d82263e8800579055fb2ea11b71dd4926c8a7323855af7`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23a4f8abcdb7d54b1be57c8c5a7b900175491bf0a6c728ec1ff988721eeb650`  
		Last Modified: Tue, 03 Oct 2023 06:39:58 GMT  
		Size: 124.2 MB (124214286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e5bde6e62e3000d8b94ad515014497a6fa4a570dad9498a8ae2f1237452198`  
		Last Modified: Tue, 03 Oct 2023 06:39:39 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:iron-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:72406c75aa72fcd711246fadac052734753c30ab3db640abb407750c7b47badd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155082610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a5671b7e0a5cc99900a4ea2b6df0647e7d42ce296c78b39fa226eb6e74d073`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:37:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 13 Oct 2023 04:38:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:50:42 GMT
ENV ROS_DISTRO=iron
# Fri, 13 Oct 2023 04:51:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-iron-ros-core=0.10.0-3*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:51:31 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 13 Oct 2023 04:51:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:51:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff18d61171fb1a17fb0edecb7a0600d4d0be1c103726f9d60cfb59071d3eccf9`  
		Last Modified: Fri, 13 Oct 2023 05:00:30 GMT  
		Size: 1.2 MB (1214464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa41e452048780b8d89bde1b448e5c130e073ab26d8a3c3e2ec3d4a4170f55f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 3.8 MB (3801906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c55f0e8967a89d129c1106434dacd41bd9239f7fe793b4dc37245f7a26762f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023f71811e459a590f4b10edecae765c4b654f7139277e4c704f11126c720c5f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe7e5397da56a4ded96341848bbe099efaf06181bb8a09f3720aeb98cd49c69`  
		Last Modified: Fri, 13 Oct 2023 05:03:18 GMT  
		Size: 121.7 MB (121671888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b628474c464bf47e0464b172ff209e5e12441f2570b8a83504c6ef68bc1f77`  
		Last Modified: Fri, 13 Oct 2023 05:02:55 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:latest`

```console
$ docker pull ros@sha256:3b96085953443c572f7c9e9fd8439e54a83f461ac68d27ec3dae83e827063fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:a9657e73a73dcb7f4bb9bd66e760c250201ff5be4e951b5f615d5fa8b176ebba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263454549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb143c7bfa18aa28b341e2067e86c63d8cbb24019f1ae72b23cf2a18cada317`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:09:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 03 Oct 2023 06:09:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV ROS_DISTRO=humble
# Tue, 03 Oct 2023 06:11:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:11:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 03 Oct 2023 06:11:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Oct 2023 06:11:49 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 06:12:55 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:13:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 03 Oct 2023 06:13:06 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 03 Oct 2023 06:14:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1370ba32049345dce3665687ae8209d03dc6e8d9d44e99e46c0ceb62f9f1f30d`  
		Last Modified: Tue, 03 Oct 2023 06:37:13 GMT  
		Size: 1.2 MB (1213056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c1e1f3dd2585388cc558f6237ee492769081f489b65cd386188d8efb6cdce6`  
		Last Modified: Tue, 03 Oct 2023 06:37:12 GMT  
		Size: 3.8 MB (3828981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198e4b86b803705bfcbea4adc86401d2d0cd4af88199c9e706cf0803b5be7842`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d310e00acb45665d82263e8800579055fb2ea11b71dd4926c8a7323855af7`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63af57a291ea0d8bef7998336bff74edc42cd8c81f6d753a2f5d4f2c809a2b1`  
		Last Modified: Tue, 03 Oct 2023 06:37:27 GMT  
		Size: 106.4 MB (106420533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e044e4a00a19b3e05de479e3a9337d89b05d2bb4bbb253140e06f1354096ac90`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c435980f0d57baf74d055c31cbe6f7c7e6cf2caa6f57ff81dc4e37bd122427fc`  
		Last Modified: Tue, 03 Oct 2023 06:37:48 GMT  
		Size: 98.1 MB (98133952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cea32350106421e3ea17aa559eebc1e78a40d606c84104918810317208952319`  
		Last Modified: Tue, 03 Oct 2023 06:37:36 GMT  
		Size: 318.3 KB (318269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aeed20a10372b03facc5f0ed6f47eb4dfd48e64323af8a8b469941191530aef`  
		Last Modified: Tue, 03 Oct 2023 06:37:35 GMT  
		Size: 2.5 KB (2499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57055b83861bdeb2d184d6a307e938f912b38d11743f7a00017a02ae8f08d42`  
		Last Modified: Tue, 03 Oct 2023 06:37:39 GMT  
		Size: 23.1 MB (23093974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6d1382ef38812fc2b77beb0e6265e927a1b68c2ab3e47469eb60c9783c9b91e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256085517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d59e3d4efad3c9ae8f9ba40a50e75f232a5ce6a332b493d0dcbddeedbbf537c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:37:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 13 Oct 2023 04:38:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:38:07 GMT
ENV ROS_DISTRO=humble
# Fri, 13 Oct 2023 04:39:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:39:35 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 13 Oct 2023 04:39:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:39:35 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 04:40:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:40:19 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 04:40:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 13 Oct 2023 04:41:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff18d61171fb1a17fb0edecb7a0600d4d0be1c103726f9d60cfb59071d3eccf9`  
		Last Modified: Fri, 13 Oct 2023 05:00:30 GMT  
		Size: 1.2 MB (1214464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa41e452048780b8d89bde1b448e5c130e073ab26d8a3c3e2ec3d4a4170f55f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 3.8 MB (3801906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c55f0e8967a89d129c1106434dacd41bd9239f7fe793b4dc37245f7a26762f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023f71811e459a590f4b10edecae765c4b654f7139277e4c704f11126c720c5f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c023537795c860c51cdc51a826448aa3f98423714b84b95dea685761f8e013d6`  
		Last Modified: Fri, 13 Oct 2023 05:00:48 GMT  
		Size: 104.2 MB (104151928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfda3e7987bf657d0a886fc085e34ebecaca449450d6b705392eb5c3170fe318`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0a489e10cbdefdd5f5cadbefeb08d5ebd7f0f8888a9aa8868bf249e7ba9498`  
		Last Modified: Fri, 13 Oct 2023 05:01:08 GMT  
		Size: 95.7 MB (95684475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ce9ac65ade437d7a093f3b80dcbc88126a337e45ce69f99234c87019c1bc35`  
		Last Modified: Fri, 13 Oct 2023 05:00:57 GMT  
		Size: 319.3 KB (319340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edfb5ed159e80825a9155603a7778bb0cd6f9f024fd0113561edcedd3909b8ed`  
		Last Modified: Fri, 13 Oct 2023 05:00:57 GMT  
		Size: 2.5 KB (2482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab14f4c10d226ff941d9d47bc4cef0f2f27c6612233a208ec6a18ac86a96daf`  
		Last Modified: Fri, 13 Oct 2023 05:01:01 GMT  
		Size: 22.5 MB (22516571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic`

```console
$ docker pull ros@sha256:3ff6eb8c100ec747c1cafeb9fa426360f6b6f96d4808d04bda9dc748cac2769d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic` - linux; amd64

```console
$ docker pull ros@sha256:650483554542d585af1f7c6fd09a4fb64d1492243f19010662e5434e1489a9d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343156918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2661096a96da02ad942658f95aacd228d2d94aaa5334a9cc005367b9b88752`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 02:44:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:21:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:21:50 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 17 Aug 2023 07:21:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 17 Aug 2023 07:21:51 GMT
ENV LANG=C.UTF-8
# Thu, 17 Aug 2023 07:21:52 GMT
ENV LC_ALL=C.UTF-8
# Thu, 17 Aug 2023 07:21:52 GMT
ENV ROS_DISTRO=noetic
# Thu, 17 Aug 2023 07:23:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:23:53 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 17 Aug 2023 07:23:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 17 Aug 2023 07:23:54 GMT
CMD ["bash"]
# Thu, 17 Aug 2023 07:24:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:24:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 17 Aug 2023 07:25:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aab22f0326d7d89686f4eebe2ba52f86ca4e83a4c69d66dfe4f2b1494eae439`  
		Last Modified: Thu, 03 Aug 2023 02:53:09 GMT  
		Size: 1.2 MB (1198625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b915067b2cb577e1158572cfb9bb4edba91b52a0f5821152a8a4e2518dd702c`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 5.6 MB (5553744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87dd0b38cb0829def318257a357f2d9773c0c0f443432fe0ab8f0e28f8454a13`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b104afafaf102a6ecd5bc760e922c728c4ab27320895943844d8f53c908a025`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f437788a75a65f6ba1decf914b73eaf4b4712c46e542abaf9d51e92f1e6c32`  
		Last Modified: Thu, 17 Aug 2023 07:49:46 GMT  
		Size: 177.0 MB (176961988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a8de474ce644ddf64e37acf737479db384d569592e927234ba9775cbf3c044`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71044449a9df53317087cbf1480ae89d0864ed6c767b63f246f2a112cb697023`  
		Last Modified: Thu, 17 Aug 2023 07:50:07 GMT  
		Size: 50.9 MB (50940393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee57c22656c0736ccbe5b757eeada9768c4061541ea8fced3debcc9d8e5186c3`  
		Last Modified: Thu, 17 Aug 2023 07:49:59 GMT  
		Size: 305.0 KB (305044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01916643bc85febc6c44576e168005fd7892f275d1a187528964c1a062bb36a`  
		Last Modified: Thu, 17 Aug 2023 07:50:10 GMT  
		Size: 79.6 MB (79614040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm variant v7

```console
$ docker pull ros@sha256:17c021f745282198d89551e984956f5d32bf3b296d79d27c72eb5129feecba56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289222658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b381b176ed648076efff35763069250dfe58cad8d71f4ac9f298cae85523902`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Oct 2023 10:47:59 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:47:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:48:06 GMT
ADD file:8dffbfada6e0bebb2858525182aef87ac2cbd88c624f32696ec2cb947e71a4f3 in / 
# Tue, 03 Oct 2023 10:48:07 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 01:25:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:25:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:25:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 13 Oct 2023 01:25:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 01:25:43 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 01:25:44 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 01:25:44 GMT
ENV ROS_DISTRO=noetic
# Fri, 13 Oct 2023 01:28:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:28:12 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 13 Oct 2023 01:28:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 01:28:13 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:28:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:28:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 01:30:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b5f1ba1b648ae0824ed6a95ab17335537f8e689df99917fd374af5dd34078eb`  
		Last Modified: Fri, 13 Oct 2023 01:11:42 GMT  
		Size: 24.6 MB (24592174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a3643fb9ea7b4891593c2a71e53f70146f828b8896758ecc6804e843b3eb9d`  
		Last Modified: Fri, 13 Oct 2023 01:38:43 GMT  
		Size: 1.2 MB (1200040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d390fd421e090bebfad483fae5954c8ce4b3d98d6f7964b7d2af20febd3a8dd`  
		Last Modified: Fri, 13 Oct 2023 01:38:41 GMT  
		Size: 4.7 MB (4680598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f635e6735a4e72b10c5401661b398132793e75102ebdae3c1a4bb09369a9277b`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc440f8be875763f266a01bddecd7e5256b0f7024383d18f3ac27b3eefca620c`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8576e38b77aab0fa900f38b3857ac3f1f5f2f357b049bb4765eead409392f8ab`  
		Last Modified: Fri, 13 Oct 2023 01:39:16 GMT  
		Size: 157.4 MB (157433981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9929dceae2a7ac00be4bdeef95d2220d21923972182d5a0805ae6a130e9a5c`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbc9c70d09913eddb72c3c4f69d3eacc75f42772407b3a7f1b83b8ab76e8609`  
		Last Modified: Fri, 13 Oct 2023 01:39:37 GMT  
		Size: 40.5 MB (40504496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4c4f8456ac317553d22cb6aeb19337c7ba56c832bd9ce3050a5666e4e67276`  
		Last Modified: Fri, 13 Oct 2023 01:39:26 GMT  
		Size: 308.4 KB (308391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f11110f8ff52141ed436fcf91a65720ab159af26f35baf35ebec69235529767`  
		Last Modified: Fri, 13 Oct 2023 01:39:41 GMT  
		Size: 60.5 MB (60500564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e56292f13e93a79eaebd54ca1fc7cbce221cb489870c645c52c21a60984ae07c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.8 MB (322833438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ef0ff8399f8b8ffa366228b6c3a797d77f86744a8732f35f0389fdac3e32e0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:24:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:24:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:24:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 13 Oct 2023 04:24:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:24:38 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:24:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:24:38 GMT
ENV ROS_DISTRO=noetic
# Fri, 13 Oct 2023 04:27:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:27:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 13 Oct 2023 04:27:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:27:42 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 04:28:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:28:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 04:29:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6cba4020c0a193cd551ed8edf368670967e3546345b52c4ec66cb0931436e9b9`  
		Last Modified: Thu, 05 Oct 2023 12:12:17 GMT  
		Size: 27.2 MB (27199503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87696a1bdfb2280c9c8f032b8dad476643e285ea6a4daaaaf8dea807599345f3`  
		Last Modified: Fri, 13 Oct 2023 04:58:00 GMT  
		Size: 1.2 MB (1199301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c122b6409bbe49fd6863f4fe1b6c386aa8c0839b4d569cc6a7c864c54e4ebc`  
		Last Modified: Fri, 13 Oct 2023 04:57:58 GMT  
		Size: 5.5 MB (5532659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a917760d45f055be63dd5265386c3e099071676cbade870f5fad9204d410ad08`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f178865c356dfadb4351dd90e17e88bc0c96c7a5b00c3fa27f7a7a50854a6`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70efcc630f7ac8f41932a95504f9faf4f5d3a98261ec78847c0b7895c7e38c55`  
		Last Modified: Fri, 13 Oct 2023 04:58:33 GMT  
		Size: 171.4 MB (171412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7380be57882dd81c0bc849142d511e957f6f209e899d784c2169dd1268af381`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03ae63d5fe1e840f0cc374100c4a33137e2c3862f567675d2a4f2a632ca68fd`  
		Last Modified: Fri, 13 Oct 2023 04:58:54 GMT  
		Size: 45.2 MB (45206478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78bb804d06a6c2affa7a4df0cb90051039812dd200a146925a447da4c03248f`  
		Last Modified: Fri, 13 Oct 2023 04:58:44 GMT  
		Size: 308.4 KB (308395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee77018c303d0f8b15482607876c85bd6f9bd91d7320f861f1146fc7f1e5f98`  
		Last Modified: Fri, 13 Oct 2023 04:58:52 GMT  
		Size: 72.0 MB (71972672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception`

```console
$ docker pull ros@sha256:1276d1a1078d0e20b54e2d8d671ea08c51c6aa35ac849a1819cdd754c202ae29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception` - linux; amd64

```console
$ docker pull ros@sha256:ae2d31efb881f34de3d03d52d5addf87ee8125d1f886bf15babb5a1282242e1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.2 MB (835209394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23606c67a6f8bb711cbadbca4920eae8cfa1f0820596be362c1728e5f1f4ab40`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 02:44:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:21:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:21:50 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 17 Aug 2023 07:21:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 17 Aug 2023 07:21:51 GMT
ENV LANG=C.UTF-8
# Thu, 17 Aug 2023 07:21:52 GMT
ENV LC_ALL=C.UTF-8
# Thu, 17 Aug 2023 07:21:52 GMT
ENV ROS_DISTRO=noetic
# Thu, 17 Aug 2023 07:23:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:23:53 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 17 Aug 2023 07:23:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 17 Aug 2023 07:23:54 GMT
CMD ["bash"]
# Thu, 17 Aug 2023 07:24:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:24:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 17 Aug 2023 07:25:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:30:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aab22f0326d7d89686f4eebe2ba52f86ca4e83a4c69d66dfe4f2b1494eae439`  
		Last Modified: Thu, 03 Aug 2023 02:53:09 GMT  
		Size: 1.2 MB (1198625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b915067b2cb577e1158572cfb9bb4edba91b52a0f5821152a8a4e2518dd702c`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 5.6 MB (5553744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87dd0b38cb0829def318257a357f2d9773c0c0f443432fe0ab8f0e28f8454a13`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b104afafaf102a6ecd5bc760e922c728c4ab27320895943844d8f53c908a025`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f437788a75a65f6ba1decf914b73eaf4b4712c46e542abaf9d51e92f1e6c32`  
		Last Modified: Thu, 17 Aug 2023 07:49:46 GMT  
		Size: 177.0 MB (176961988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a8de474ce644ddf64e37acf737479db384d569592e927234ba9775cbf3c044`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71044449a9df53317087cbf1480ae89d0864ed6c767b63f246f2a112cb697023`  
		Last Modified: Thu, 17 Aug 2023 07:50:07 GMT  
		Size: 50.9 MB (50940393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee57c22656c0736ccbe5b757eeada9768c4061541ea8fced3debcc9d8e5186c3`  
		Last Modified: Thu, 17 Aug 2023 07:49:59 GMT  
		Size: 305.0 KB (305044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01916643bc85febc6c44576e168005fd7892f275d1a187528964c1a062bb36a`  
		Last Modified: Thu, 17 Aug 2023 07:50:10 GMT  
		Size: 79.6 MB (79614040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072cf6370b84c85da7ec392f4f550ee0e9e157b32afafab89c2d75a944cc33dd`  
		Last Modified: Thu, 17 Aug 2023 07:51:42 GMT  
		Size: 492.1 MB (492052476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:64cdf5a015a56c8c50a25ce8a7762e980b9d062bf078b4124fbe7b20c7de755d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.2 MB (726231284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9d973ac3b4f33261ee405c4a25103b08d20c97acf62ed9bffe2778bb245bb3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Oct 2023 10:47:59 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:47:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:48:06 GMT
ADD file:8dffbfada6e0bebb2858525182aef87ac2cbd88c624f32696ec2cb947e71a4f3 in / 
# Tue, 03 Oct 2023 10:48:07 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 01:25:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:25:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:25:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 13 Oct 2023 01:25:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 01:25:43 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 01:25:44 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 01:25:44 GMT
ENV ROS_DISTRO=noetic
# Fri, 13 Oct 2023 01:28:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:28:12 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 13 Oct 2023 01:28:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 01:28:13 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:28:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:28:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 01:30:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:38:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b5f1ba1b648ae0824ed6a95ab17335537f8e689df99917fd374af5dd34078eb`  
		Last Modified: Fri, 13 Oct 2023 01:11:42 GMT  
		Size: 24.6 MB (24592174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a3643fb9ea7b4891593c2a71e53f70146f828b8896758ecc6804e843b3eb9d`  
		Last Modified: Fri, 13 Oct 2023 01:38:43 GMT  
		Size: 1.2 MB (1200040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d390fd421e090bebfad483fae5954c8ce4b3d98d6f7964b7d2af20febd3a8dd`  
		Last Modified: Fri, 13 Oct 2023 01:38:41 GMT  
		Size: 4.7 MB (4680598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f635e6735a4e72b10c5401661b398132793e75102ebdae3c1a4bb09369a9277b`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc440f8be875763f266a01bddecd7e5256b0f7024383d18f3ac27b3eefca620c`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8576e38b77aab0fa900f38b3857ac3f1f5f2f357b049bb4765eead409392f8ab`  
		Last Modified: Fri, 13 Oct 2023 01:39:16 GMT  
		Size: 157.4 MB (157433981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9929dceae2a7ac00be4bdeef95d2220d21923972182d5a0805ae6a130e9a5c`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbc9c70d09913eddb72c3c4f69d3eacc75f42772407b3a7f1b83b8ab76e8609`  
		Last Modified: Fri, 13 Oct 2023 01:39:37 GMT  
		Size: 40.5 MB (40504496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4c4f8456ac317553d22cb6aeb19337c7ba56c832bd9ce3050a5666e4e67276`  
		Last Modified: Fri, 13 Oct 2023 01:39:26 GMT  
		Size: 308.4 KB (308391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f11110f8ff52141ed436fcf91a65720ab159af26f35baf35ebec69235529767`  
		Last Modified: Fri, 13 Oct 2023 01:39:41 GMT  
		Size: 60.5 MB (60500564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b602498648539ea59715c26650599737ca33cc85e4114378b54496cbaa937de`  
		Last Modified: Fri, 13 Oct 2023 01:41:18 GMT  
		Size: 437.0 MB (437008626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4662f58ca7042d7bea3716864a803504cab9706ccefce621c2626d9d773c0a84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.5 MB (785516714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1deb7cbbb0bc73df0b0089181bfbc29f478fe11ddd2d986d61db1a8eca0f37`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:24:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:24:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:24:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 13 Oct 2023 04:24:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:24:38 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:24:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:24:38 GMT
ENV ROS_DISTRO=noetic
# Fri, 13 Oct 2023 04:27:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:27:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 13 Oct 2023 04:27:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:27:42 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 04:28:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:28:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 04:29:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:37:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6cba4020c0a193cd551ed8edf368670967e3546345b52c4ec66cb0931436e9b9`  
		Last Modified: Thu, 05 Oct 2023 12:12:17 GMT  
		Size: 27.2 MB (27199503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87696a1bdfb2280c9c8f032b8dad476643e285ea6a4daaaaf8dea807599345f3`  
		Last Modified: Fri, 13 Oct 2023 04:58:00 GMT  
		Size: 1.2 MB (1199301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c122b6409bbe49fd6863f4fe1b6c386aa8c0839b4d569cc6a7c864c54e4ebc`  
		Last Modified: Fri, 13 Oct 2023 04:57:58 GMT  
		Size: 5.5 MB (5532659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a917760d45f055be63dd5265386c3e099071676cbade870f5fad9204d410ad08`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f178865c356dfadb4351dd90e17e88bc0c96c7a5b00c3fa27f7a7a50854a6`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70efcc630f7ac8f41932a95504f9faf4f5d3a98261ec78847c0b7895c7e38c55`  
		Last Modified: Fri, 13 Oct 2023 04:58:33 GMT  
		Size: 171.4 MB (171412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7380be57882dd81c0bc849142d511e957f6f209e899d784c2169dd1268af381`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03ae63d5fe1e840f0cc374100c4a33137e2c3862f567675d2a4f2a632ca68fd`  
		Last Modified: Fri, 13 Oct 2023 04:58:54 GMT  
		Size: 45.2 MB (45206478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78bb804d06a6c2affa7a4df0cb90051039812dd200a146925a447da4c03248f`  
		Last Modified: Fri, 13 Oct 2023 04:58:44 GMT  
		Size: 308.4 KB (308395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee77018c303d0f8b15482607876c85bd6f9bd91d7320f861f1146fc7f1e5f98`  
		Last Modified: Fri, 13 Oct 2023 04:58:52 GMT  
		Size: 72.0 MB (71972672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e2b31a08f80995828ceab4e41ee7b3b297824452520bcc426931dcb6ed0708`  
		Last Modified: Fri, 13 Oct 2023 05:00:17 GMT  
		Size: 462.7 MB (462683276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:1276d1a1078d0e20b54e2d8d671ea08c51c6aa35ac849a1819cdd754c202ae29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:ae2d31efb881f34de3d03d52d5addf87ee8125d1f886bf15babb5a1282242e1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.2 MB (835209394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23606c67a6f8bb711cbadbca4920eae8cfa1f0820596be362c1728e5f1f4ab40`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 02:44:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:21:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:21:50 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 17 Aug 2023 07:21:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 17 Aug 2023 07:21:51 GMT
ENV LANG=C.UTF-8
# Thu, 17 Aug 2023 07:21:52 GMT
ENV LC_ALL=C.UTF-8
# Thu, 17 Aug 2023 07:21:52 GMT
ENV ROS_DISTRO=noetic
# Thu, 17 Aug 2023 07:23:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:23:53 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 17 Aug 2023 07:23:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 17 Aug 2023 07:23:54 GMT
CMD ["bash"]
# Thu, 17 Aug 2023 07:24:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:24:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 17 Aug 2023 07:25:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:30:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aab22f0326d7d89686f4eebe2ba52f86ca4e83a4c69d66dfe4f2b1494eae439`  
		Last Modified: Thu, 03 Aug 2023 02:53:09 GMT  
		Size: 1.2 MB (1198625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b915067b2cb577e1158572cfb9bb4edba91b52a0f5821152a8a4e2518dd702c`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 5.6 MB (5553744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87dd0b38cb0829def318257a357f2d9773c0c0f443432fe0ab8f0e28f8454a13`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b104afafaf102a6ecd5bc760e922c728c4ab27320895943844d8f53c908a025`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f437788a75a65f6ba1decf914b73eaf4b4712c46e542abaf9d51e92f1e6c32`  
		Last Modified: Thu, 17 Aug 2023 07:49:46 GMT  
		Size: 177.0 MB (176961988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a8de474ce644ddf64e37acf737479db384d569592e927234ba9775cbf3c044`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71044449a9df53317087cbf1480ae89d0864ed6c767b63f246f2a112cb697023`  
		Last Modified: Thu, 17 Aug 2023 07:50:07 GMT  
		Size: 50.9 MB (50940393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee57c22656c0736ccbe5b757eeada9768c4061541ea8fced3debcc9d8e5186c3`  
		Last Modified: Thu, 17 Aug 2023 07:49:59 GMT  
		Size: 305.0 KB (305044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01916643bc85febc6c44576e168005fd7892f275d1a187528964c1a062bb36a`  
		Last Modified: Thu, 17 Aug 2023 07:50:10 GMT  
		Size: 79.6 MB (79614040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072cf6370b84c85da7ec392f4f550ee0e9e157b32afafab89c2d75a944cc33dd`  
		Last Modified: Thu, 17 Aug 2023 07:51:42 GMT  
		Size: 492.1 MB (492052476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:64cdf5a015a56c8c50a25ce8a7762e980b9d062bf078b4124fbe7b20c7de755d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.2 MB (726231284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9d973ac3b4f33261ee405c4a25103b08d20c97acf62ed9bffe2778bb245bb3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Oct 2023 10:47:59 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:47:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:48:06 GMT
ADD file:8dffbfada6e0bebb2858525182aef87ac2cbd88c624f32696ec2cb947e71a4f3 in / 
# Tue, 03 Oct 2023 10:48:07 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 01:25:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:25:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:25:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 13 Oct 2023 01:25:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 01:25:43 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 01:25:44 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 01:25:44 GMT
ENV ROS_DISTRO=noetic
# Fri, 13 Oct 2023 01:28:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:28:12 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 13 Oct 2023 01:28:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 01:28:13 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:28:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:28:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 01:30:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:38:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b5f1ba1b648ae0824ed6a95ab17335537f8e689df99917fd374af5dd34078eb`  
		Last Modified: Fri, 13 Oct 2023 01:11:42 GMT  
		Size: 24.6 MB (24592174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a3643fb9ea7b4891593c2a71e53f70146f828b8896758ecc6804e843b3eb9d`  
		Last Modified: Fri, 13 Oct 2023 01:38:43 GMT  
		Size: 1.2 MB (1200040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d390fd421e090bebfad483fae5954c8ce4b3d98d6f7964b7d2af20febd3a8dd`  
		Last Modified: Fri, 13 Oct 2023 01:38:41 GMT  
		Size: 4.7 MB (4680598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f635e6735a4e72b10c5401661b398132793e75102ebdae3c1a4bb09369a9277b`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc440f8be875763f266a01bddecd7e5256b0f7024383d18f3ac27b3eefca620c`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8576e38b77aab0fa900f38b3857ac3f1f5f2f357b049bb4765eead409392f8ab`  
		Last Modified: Fri, 13 Oct 2023 01:39:16 GMT  
		Size: 157.4 MB (157433981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9929dceae2a7ac00be4bdeef95d2220d21923972182d5a0805ae6a130e9a5c`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbc9c70d09913eddb72c3c4f69d3eacc75f42772407b3a7f1b83b8ab76e8609`  
		Last Modified: Fri, 13 Oct 2023 01:39:37 GMT  
		Size: 40.5 MB (40504496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4c4f8456ac317553d22cb6aeb19337c7ba56c832bd9ce3050a5666e4e67276`  
		Last Modified: Fri, 13 Oct 2023 01:39:26 GMT  
		Size: 308.4 KB (308391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f11110f8ff52141ed436fcf91a65720ab159af26f35baf35ebec69235529767`  
		Last Modified: Fri, 13 Oct 2023 01:39:41 GMT  
		Size: 60.5 MB (60500564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b602498648539ea59715c26650599737ca33cc85e4114378b54496cbaa937de`  
		Last Modified: Fri, 13 Oct 2023 01:41:18 GMT  
		Size: 437.0 MB (437008626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4662f58ca7042d7bea3716864a803504cab9706ccefce621c2626d9d773c0a84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.5 MB (785516714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1deb7cbbb0bc73df0b0089181bfbc29f478fe11ddd2d986d61db1a8eca0f37`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:24:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:24:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:24:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 13 Oct 2023 04:24:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:24:38 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:24:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:24:38 GMT
ENV ROS_DISTRO=noetic
# Fri, 13 Oct 2023 04:27:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:27:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 13 Oct 2023 04:27:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:27:42 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 04:28:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:28:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 04:29:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:37:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6cba4020c0a193cd551ed8edf368670967e3546345b52c4ec66cb0931436e9b9`  
		Last Modified: Thu, 05 Oct 2023 12:12:17 GMT  
		Size: 27.2 MB (27199503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87696a1bdfb2280c9c8f032b8dad476643e285ea6a4daaaaf8dea807599345f3`  
		Last Modified: Fri, 13 Oct 2023 04:58:00 GMT  
		Size: 1.2 MB (1199301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c122b6409bbe49fd6863f4fe1b6c386aa8c0839b4d569cc6a7c864c54e4ebc`  
		Last Modified: Fri, 13 Oct 2023 04:57:58 GMT  
		Size: 5.5 MB (5532659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a917760d45f055be63dd5265386c3e099071676cbade870f5fad9204d410ad08`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f178865c356dfadb4351dd90e17e88bc0c96c7a5b00c3fa27f7a7a50854a6`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70efcc630f7ac8f41932a95504f9faf4f5d3a98261ec78847c0b7895c7e38c55`  
		Last Modified: Fri, 13 Oct 2023 04:58:33 GMT  
		Size: 171.4 MB (171412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7380be57882dd81c0bc849142d511e957f6f209e899d784c2169dd1268af381`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03ae63d5fe1e840f0cc374100c4a33137e2c3862f567675d2a4f2a632ca68fd`  
		Last Modified: Fri, 13 Oct 2023 04:58:54 GMT  
		Size: 45.2 MB (45206478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78bb804d06a6c2affa7a4df0cb90051039812dd200a146925a447da4c03248f`  
		Last Modified: Fri, 13 Oct 2023 04:58:44 GMT  
		Size: 308.4 KB (308395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee77018c303d0f8b15482607876c85bd6f9bd91d7320f861f1146fc7f1e5f98`  
		Last Modified: Fri, 13 Oct 2023 04:58:52 GMT  
		Size: 72.0 MB (71972672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e2b31a08f80995828ceab4e41ee7b3b297824452520bcc426931dcb6ed0708`  
		Last Modified: Fri, 13 Oct 2023 05:00:17 GMT  
		Size: 462.7 MB (462683276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot`

```console
$ docker pull ros@sha256:a2ead4032040a7d6afa48a83f2342bfb13cb1f3bfeed36fd4940f860c7e672ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:26171861e9728cd5afc87ff920583f1da58207535c4fabbab64bcb1914d761d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (359019674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27dc1d4306276c53aaf0e61662f2418be18eabe34ff5b4173a789eb77f9d05d2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 02:44:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:21:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:21:50 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 17 Aug 2023 07:21:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 17 Aug 2023 07:21:51 GMT
ENV LANG=C.UTF-8
# Thu, 17 Aug 2023 07:21:52 GMT
ENV LC_ALL=C.UTF-8
# Thu, 17 Aug 2023 07:21:52 GMT
ENV ROS_DISTRO=noetic
# Thu, 17 Aug 2023 07:23:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:23:53 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 17 Aug 2023 07:23:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 17 Aug 2023 07:23:54 GMT
CMD ["bash"]
# Thu, 17 Aug 2023 07:24:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:24:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 17 Aug 2023 07:25:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:26:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aab22f0326d7d89686f4eebe2ba52f86ca4e83a4c69d66dfe4f2b1494eae439`  
		Last Modified: Thu, 03 Aug 2023 02:53:09 GMT  
		Size: 1.2 MB (1198625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b915067b2cb577e1158572cfb9bb4edba91b52a0f5821152a8a4e2518dd702c`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 5.6 MB (5553744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87dd0b38cb0829def318257a357f2d9773c0c0f443432fe0ab8f0e28f8454a13`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b104afafaf102a6ecd5bc760e922c728c4ab27320895943844d8f53c908a025`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f437788a75a65f6ba1decf914b73eaf4b4712c46e542abaf9d51e92f1e6c32`  
		Last Modified: Thu, 17 Aug 2023 07:49:46 GMT  
		Size: 177.0 MB (176961988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a8de474ce644ddf64e37acf737479db384d569592e927234ba9775cbf3c044`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71044449a9df53317087cbf1480ae89d0864ed6c767b63f246f2a112cb697023`  
		Last Modified: Thu, 17 Aug 2023 07:50:07 GMT  
		Size: 50.9 MB (50940393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee57c22656c0736ccbe5b757eeada9768c4061541ea8fced3debcc9d8e5186c3`  
		Last Modified: Thu, 17 Aug 2023 07:49:59 GMT  
		Size: 305.0 KB (305044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01916643bc85febc6c44576e168005fd7892f275d1a187528964c1a062bb36a`  
		Last Modified: Thu, 17 Aug 2023 07:50:10 GMT  
		Size: 79.6 MB (79614040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f781912f3aa6add79d8d355f91f4f813ea41cb3588b44b0946845b83c495dc3`  
		Last Modified: Thu, 17 Aug 2023 07:50:27 GMT  
		Size: 15.9 MB (15862756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:c41539a5a68e47e13122787650225bc42370886628f92db240c164f64f00fc4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303292113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9832067cc8944698d44d3ee6bc021869db790caf4c7eacc6d6f9dafc84f5060d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Oct 2023 10:47:59 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:47:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:48:06 GMT
ADD file:8dffbfada6e0bebb2858525182aef87ac2cbd88c624f32696ec2cb947e71a4f3 in / 
# Tue, 03 Oct 2023 10:48:07 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 01:25:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:25:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:25:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 13 Oct 2023 01:25:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 01:25:43 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 01:25:44 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 01:25:44 GMT
ENV ROS_DISTRO=noetic
# Fri, 13 Oct 2023 01:28:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:28:12 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 13 Oct 2023 01:28:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 01:28:13 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:28:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:28:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 01:30:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:30:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b5f1ba1b648ae0824ed6a95ab17335537f8e689df99917fd374af5dd34078eb`  
		Last Modified: Fri, 13 Oct 2023 01:11:42 GMT  
		Size: 24.6 MB (24592174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a3643fb9ea7b4891593c2a71e53f70146f828b8896758ecc6804e843b3eb9d`  
		Last Modified: Fri, 13 Oct 2023 01:38:43 GMT  
		Size: 1.2 MB (1200040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d390fd421e090bebfad483fae5954c8ce4b3d98d6f7964b7d2af20febd3a8dd`  
		Last Modified: Fri, 13 Oct 2023 01:38:41 GMT  
		Size: 4.7 MB (4680598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f635e6735a4e72b10c5401661b398132793e75102ebdae3c1a4bb09369a9277b`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc440f8be875763f266a01bddecd7e5256b0f7024383d18f3ac27b3eefca620c`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8576e38b77aab0fa900f38b3857ac3f1f5f2f357b049bb4765eead409392f8ab`  
		Last Modified: Fri, 13 Oct 2023 01:39:16 GMT  
		Size: 157.4 MB (157433981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9929dceae2a7ac00be4bdeef95d2220d21923972182d5a0805ae6a130e9a5c`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbc9c70d09913eddb72c3c4f69d3eacc75f42772407b3a7f1b83b8ab76e8609`  
		Last Modified: Fri, 13 Oct 2023 01:39:37 GMT  
		Size: 40.5 MB (40504496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4c4f8456ac317553d22cb6aeb19337c7ba56c832bd9ce3050a5666e4e67276`  
		Last Modified: Fri, 13 Oct 2023 01:39:26 GMT  
		Size: 308.4 KB (308391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f11110f8ff52141ed436fcf91a65720ab159af26f35baf35ebec69235529767`  
		Last Modified: Fri, 13 Oct 2023 01:39:41 GMT  
		Size: 60.5 MB (60500564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29cd9542cbabe9c5ca1a0dde9973ca6791e1de1468c878a7b6b95d90f1095178`  
		Last Modified: Fri, 13 Oct 2023 01:39:56 GMT  
		Size: 14.1 MB (14069455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e953d7f922e3e94877ce9936dbd76a64eea936fdaf7d24c5691c4661bc65450b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338292245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7334d608f23ea631771a9eead91ab532d13139c7ddb063074bdc1b74018eee86`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:24:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:24:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:24:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 13 Oct 2023 04:24:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:24:38 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:24:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:24:38 GMT
ENV ROS_DISTRO=noetic
# Fri, 13 Oct 2023 04:27:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:27:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 13 Oct 2023 04:27:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:27:42 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 04:28:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:28:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 04:29:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:30:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6cba4020c0a193cd551ed8edf368670967e3546345b52c4ec66cb0931436e9b9`  
		Last Modified: Thu, 05 Oct 2023 12:12:17 GMT  
		Size: 27.2 MB (27199503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87696a1bdfb2280c9c8f032b8dad476643e285ea6a4daaaaf8dea807599345f3`  
		Last Modified: Fri, 13 Oct 2023 04:58:00 GMT  
		Size: 1.2 MB (1199301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c122b6409bbe49fd6863f4fe1b6c386aa8c0839b4d569cc6a7c864c54e4ebc`  
		Last Modified: Fri, 13 Oct 2023 04:57:58 GMT  
		Size: 5.5 MB (5532659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a917760d45f055be63dd5265386c3e099071676cbade870f5fad9204d410ad08`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f178865c356dfadb4351dd90e17e88bc0c96c7a5b00c3fa27f7a7a50854a6`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70efcc630f7ac8f41932a95504f9faf4f5d3a98261ec78847c0b7895c7e38c55`  
		Last Modified: Fri, 13 Oct 2023 04:58:33 GMT  
		Size: 171.4 MB (171412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7380be57882dd81c0bc849142d511e957f6f209e899d784c2169dd1268af381`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03ae63d5fe1e840f0cc374100c4a33137e2c3862f567675d2a4f2a632ca68fd`  
		Last Modified: Fri, 13 Oct 2023 04:58:54 GMT  
		Size: 45.2 MB (45206478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78bb804d06a6c2affa7a4df0cb90051039812dd200a146925a447da4c03248f`  
		Last Modified: Fri, 13 Oct 2023 04:58:44 GMT  
		Size: 308.4 KB (308395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee77018c303d0f8b15482607876c85bd6f9bd91d7320f861f1146fc7f1e5f98`  
		Last Modified: Fri, 13 Oct 2023 04:58:52 GMT  
		Size: 72.0 MB (71972672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2096eb516266a125f99bb94d5b72cc5ffa2827b552aa2e1189a4fe247f072ee`  
		Last Modified: Fri, 13 Oct 2023 04:59:07 GMT  
		Size: 15.5 MB (15458807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot-focal`

```console
$ docker pull ros@sha256:a2ead4032040a7d6afa48a83f2342bfb13cb1f3bfeed36fd4940f860c7e672ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot-focal` - linux; amd64

```console
$ docker pull ros@sha256:26171861e9728cd5afc87ff920583f1da58207535c4fabbab64bcb1914d761d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (359019674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27dc1d4306276c53aaf0e61662f2418be18eabe34ff5b4173a789eb77f9d05d2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 02:44:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:21:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:21:50 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 17 Aug 2023 07:21:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 17 Aug 2023 07:21:51 GMT
ENV LANG=C.UTF-8
# Thu, 17 Aug 2023 07:21:52 GMT
ENV LC_ALL=C.UTF-8
# Thu, 17 Aug 2023 07:21:52 GMT
ENV ROS_DISTRO=noetic
# Thu, 17 Aug 2023 07:23:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:23:53 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 17 Aug 2023 07:23:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 17 Aug 2023 07:23:54 GMT
CMD ["bash"]
# Thu, 17 Aug 2023 07:24:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:24:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 17 Aug 2023 07:25:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:26:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aab22f0326d7d89686f4eebe2ba52f86ca4e83a4c69d66dfe4f2b1494eae439`  
		Last Modified: Thu, 03 Aug 2023 02:53:09 GMT  
		Size: 1.2 MB (1198625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b915067b2cb577e1158572cfb9bb4edba91b52a0f5821152a8a4e2518dd702c`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 5.6 MB (5553744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87dd0b38cb0829def318257a357f2d9773c0c0f443432fe0ab8f0e28f8454a13`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b104afafaf102a6ecd5bc760e922c728c4ab27320895943844d8f53c908a025`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f437788a75a65f6ba1decf914b73eaf4b4712c46e542abaf9d51e92f1e6c32`  
		Last Modified: Thu, 17 Aug 2023 07:49:46 GMT  
		Size: 177.0 MB (176961988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a8de474ce644ddf64e37acf737479db384d569592e927234ba9775cbf3c044`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71044449a9df53317087cbf1480ae89d0864ed6c767b63f246f2a112cb697023`  
		Last Modified: Thu, 17 Aug 2023 07:50:07 GMT  
		Size: 50.9 MB (50940393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee57c22656c0736ccbe5b757eeada9768c4061541ea8fced3debcc9d8e5186c3`  
		Last Modified: Thu, 17 Aug 2023 07:49:59 GMT  
		Size: 305.0 KB (305044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01916643bc85febc6c44576e168005fd7892f275d1a187528964c1a062bb36a`  
		Last Modified: Thu, 17 Aug 2023 07:50:10 GMT  
		Size: 79.6 MB (79614040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f781912f3aa6add79d8d355f91f4f813ea41cb3588b44b0946845b83c495dc3`  
		Last Modified: Thu, 17 Aug 2023 07:50:27 GMT  
		Size: 15.9 MB (15862756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:c41539a5a68e47e13122787650225bc42370886628f92db240c164f64f00fc4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303292113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9832067cc8944698d44d3ee6bc021869db790caf4c7eacc6d6f9dafc84f5060d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Oct 2023 10:47:59 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:47:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:48:06 GMT
ADD file:8dffbfada6e0bebb2858525182aef87ac2cbd88c624f32696ec2cb947e71a4f3 in / 
# Tue, 03 Oct 2023 10:48:07 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 01:25:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:25:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:25:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 13 Oct 2023 01:25:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 01:25:43 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 01:25:44 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 01:25:44 GMT
ENV ROS_DISTRO=noetic
# Fri, 13 Oct 2023 01:28:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:28:12 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 13 Oct 2023 01:28:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 01:28:13 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:28:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:28:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 01:30:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:30:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b5f1ba1b648ae0824ed6a95ab17335537f8e689df99917fd374af5dd34078eb`  
		Last Modified: Fri, 13 Oct 2023 01:11:42 GMT  
		Size: 24.6 MB (24592174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a3643fb9ea7b4891593c2a71e53f70146f828b8896758ecc6804e843b3eb9d`  
		Last Modified: Fri, 13 Oct 2023 01:38:43 GMT  
		Size: 1.2 MB (1200040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d390fd421e090bebfad483fae5954c8ce4b3d98d6f7964b7d2af20febd3a8dd`  
		Last Modified: Fri, 13 Oct 2023 01:38:41 GMT  
		Size: 4.7 MB (4680598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f635e6735a4e72b10c5401661b398132793e75102ebdae3c1a4bb09369a9277b`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc440f8be875763f266a01bddecd7e5256b0f7024383d18f3ac27b3eefca620c`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8576e38b77aab0fa900f38b3857ac3f1f5f2f357b049bb4765eead409392f8ab`  
		Last Modified: Fri, 13 Oct 2023 01:39:16 GMT  
		Size: 157.4 MB (157433981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9929dceae2a7ac00be4bdeef95d2220d21923972182d5a0805ae6a130e9a5c`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbc9c70d09913eddb72c3c4f69d3eacc75f42772407b3a7f1b83b8ab76e8609`  
		Last Modified: Fri, 13 Oct 2023 01:39:37 GMT  
		Size: 40.5 MB (40504496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4c4f8456ac317553d22cb6aeb19337c7ba56c832bd9ce3050a5666e4e67276`  
		Last Modified: Fri, 13 Oct 2023 01:39:26 GMT  
		Size: 308.4 KB (308391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f11110f8ff52141ed436fcf91a65720ab159af26f35baf35ebec69235529767`  
		Last Modified: Fri, 13 Oct 2023 01:39:41 GMT  
		Size: 60.5 MB (60500564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29cd9542cbabe9c5ca1a0dde9973ca6791e1de1468c878a7b6b95d90f1095178`  
		Last Modified: Fri, 13 Oct 2023 01:39:56 GMT  
		Size: 14.1 MB (14069455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e953d7f922e3e94877ce9936dbd76a64eea936fdaf7d24c5691c4661bc65450b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338292245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7334d608f23ea631771a9eead91ab532d13139c7ddb063074bdc1b74018eee86`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:24:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:24:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:24:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 13 Oct 2023 04:24:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:24:38 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:24:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:24:38 GMT
ENV ROS_DISTRO=noetic
# Fri, 13 Oct 2023 04:27:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:27:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 13 Oct 2023 04:27:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:27:42 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 04:28:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:28:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 04:29:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:30:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6cba4020c0a193cd551ed8edf368670967e3546345b52c4ec66cb0931436e9b9`  
		Last Modified: Thu, 05 Oct 2023 12:12:17 GMT  
		Size: 27.2 MB (27199503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87696a1bdfb2280c9c8f032b8dad476643e285ea6a4daaaaf8dea807599345f3`  
		Last Modified: Fri, 13 Oct 2023 04:58:00 GMT  
		Size: 1.2 MB (1199301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c122b6409bbe49fd6863f4fe1b6c386aa8c0839b4d569cc6a7c864c54e4ebc`  
		Last Modified: Fri, 13 Oct 2023 04:57:58 GMT  
		Size: 5.5 MB (5532659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a917760d45f055be63dd5265386c3e099071676cbade870f5fad9204d410ad08`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f178865c356dfadb4351dd90e17e88bc0c96c7a5b00c3fa27f7a7a50854a6`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70efcc630f7ac8f41932a95504f9faf4f5d3a98261ec78847c0b7895c7e38c55`  
		Last Modified: Fri, 13 Oct 2023 04:58:33 GMT  
		Size: 171.4 MB (171412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7380be57882dd81c0bc849142d511e957f6f209e899d784c2169dd1268af381`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03ae63d5fe1e840f0cc374100c4a33137e2c3862f567675d2a4f2a632ca68fd`  
		Last Modified: Fri, 13 Oct 2023 04:58:54 GMT  
		Size: 45.2 MB (45206478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78bb804d06a6c2affa7a4df0cb90051039812dd200a146925a447da4c03248f`  
		Last Modified: Fri, 13 Oct 2023 04:58:44 GMT  
		Size: 308.4 KB (308395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee77018c303d0f8b15482607876c85bd6f9bd91d7320f861f1146fc7f1e5f98`  
		Last Modified: Fri, 13 Oct 2023 04:58:52 GMT  
		Size: 72.0 MB (71972672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2096eb516266a125f99bb94d5b72cc5ffa2827b552aa2e1189a4fe247f072ee`  
		Last Modified: Fri, 13 Oct 2023 04:59:07 GMT  
		Size: 15.5 MB (15458807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:3ff6eb8c100ec747c1cafeb9fa426360f6b6f96d4808d04bda9dc748cac2769d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:650483554542d585af1f7c6fd09a4fb64d1492243f19010662e5434e1489a9d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343156918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2661096a96da02ad942658f95aacd228d2d94aaa5334a9cc005367b9b88752`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 02:44:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:21:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:21:50 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 17 Aug 2023 07:21:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 17 Aug 2023 07:21:51 GMT
ENV LANG=C.UTF-8
# Thu, 17 Aug 2023 07:21:52 GMT
ENV LC_ALL=C.UTF-8
# Thu, 17 Aug 2023 07:21:52 GMT
ENV ROS_DISTRO=noetic
# Thu, 17 Aug 2023 07:23:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:23:53 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 17 Aug 2023 07:23:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 17 Aug 2023 07:23:54 GMT
CMD ["bash"]
# Thu, 17 Aug 2023 07:24:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:24:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 17 Aug 2023 07:25:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aab22f0326d7d89686f4eebe2ba52f86ca4e83a4c69d66dfe4f2b1494eae439`  
		Last Modified: Thu, 03 Aug 2023 02:53:09 GMT  
		Size: 1.2 MB (1198625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b915067b2cb577e1158572cfb9bb4edba91b52a0f5821152a8a4e2518dd702c`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 5.6 MB (5553744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87dd0b38cb0829def318257a357f2d9773c0c0f443432fe0ab8f0e28f8454a13`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b104afafaf102a6ecd5bc760e922c728c4ab27320895943844d8f53c908a025`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f437788a75a65f6ba1decf914b73eaf4b4712c46e542abaf9d51e92f1e6c32`  
		Last Modified: Thu, 17 Aug 2023 07:49:46 GMT  
		Size: 177.0 MB (176961988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a8de474ce644ddf64e37acf737479db384d569592e927234ba9775cbf3c044`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71044449a9df53317087cbf1480ae89d0864ed6c767b63f246f2a112cb697023`  
		Last Modified: Thu, 17 Aug 2023 07:50:07 GMT  
		Size: 50.9 MB (50940393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee57c22656c0736ccbe5b757eeada9768c4061541ea8fced3debcc9d8e5186c3`  
		Last Modified: Thu, 17 Aug 2023 07:49:59 GMT  
		Size: 305.0 KB (305044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01916643bc85febc6c44576e168005fd7892f275d1a187528964c1a062bb36a`  
		Last Modified: Thu, 17 Aug 2023 07:50:10 GMT  
		Size: 79.6 MB (79614040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:17c021f745282198d89551e984956f5d32bf3b296d79d27c72eb5129feecba56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289222658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b381b176ed648076efff35763069250dfe58cad8d71f4ac9f298cae85523902`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Oct 2023 10:47:59 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:47:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:48:06 GMT
ADD file:8dffbfada6e0bebb2858525182aef87ac2cbd88c624f32696ec2cb947e71a4f3 in / 
# Tue, 03 Oct 2023 10:48:07 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 01:25:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:25:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:25:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 13 Oct 2023 01:25:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 01:25:43 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 01:25:44 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 01:25:44 GMT
ENV ROS_DISTRO=noetic
# Fri, 13 Oct 2023 01:28:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:28:12 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 13 Oct 2023 01:28:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 01:28:13 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:28:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:28:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 01:30:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b5f1ba1b648ae0824ed6a95ab17335537f8e689df99917fd374af5dd34078eb`  
		Last Modified: Fri, 13 Oct 2023 01:11:42 GMT  
		Size: 24.6 MB (24592174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a3643fb9ea7b4891593c2a71e53f70146f828b8896758ecc6804e843b3eb9d`  
		Last Modified: Fri, 13 Oct 2023 01:38:43 GMT  
		Size: 1.2 MB (1200040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d390fd421e090bebfad483fae5954c8ce4b3d98d6f7964b7d2af20febd3a8dd`  
		Last Modified: Fri, 13 Oct 2023 01:38:41 GMT  
		Size: 4.7 MB (4680598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f635e6735a4e72b10c5401661b398132793e75102ebdae3c1a4bb09369a9277b`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc440f8be875763f266a01bddecd7e5256b0f7024383d18f3ac27b3eefca620c`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8576e38b77aab0fa900f38b3857ac3f1f5f2f357b049bb4765eead409392f8ab`  
		Last Modified: Fri, 13 Oct 2023 01:39:16 GMT  
		Size: 157.4 MB (157433981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9929dceae2a7ac00be4bdeef95d2220d21923972182d5a0805ae6a130e9a5c`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbc9c70d09913eddb72c3c4f69d3eacc75f42772407b3a7f1b83b8ab76e8609`  
		Last Modified: Fri, 13 Oct 2023 01:39:37 GMT  
		Size: 40.5 MB (40504496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4c4f8456ac317553d22cb6aeb19337c7ba56c832bd9ce3050a5666e4e67276`  
		Last Modified: Fri, 13 Oct 2023 01:39:26 GMT  
		Size: 308.4 KB (308391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f11110f8ff52141ed436fcf91a65720ab159af26f35baf35ebec69235529767`  
		Last Modified: Fri, 13 Oct 2023 01:39:41 GMT  
		Size: 60.5 MB (60500564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e56292f13e93a79eaebd54ca1fc7cbce221cb489870c645c52c21a60984ae07c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.8 MB (322833438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ef0ff8399f8b8ffa366228b6c3a797d77f86744a8732f35f0389fdac3e32e0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:24:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:24:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:24:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 13 Oct 2023 04:24:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:24:38 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:24:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:24:38 GMT
ENV ROS_DISTRO=noetic
# Fri, 13 Oct 2023 04:27:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:27:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 13 Oct 2023 04:27:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:27:42 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 04:28:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:28:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 04:29:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6cba4020c0a193cd551ed8edf368670967e3546345b52c4ec66cb0931436e9b9`  
		Last Modified: Thu, 05 Oct 2023 12:12:17 GMT  
		Size: 27.2 MB (27199503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87696a1bdfb2280c9c8f032b8dad476643e285ea6a4daaaaf8dea807599345f3`  
		Last Modified: Fri, 13 Oct 2023 04:58:00 GMT  
		Size: 1.2 MB (1199301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c122b6409bbe49fd6863f4fe1b6c386aa8c0839b4d569cc6a7c864c54e4ebc`  
		Last Modified: Fri, 13 Oct 2023 04:57:58 GMT  
		Size: 5.5 MB (5532659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a917760d45f055be63dd5265386c3e099071676cbade870f5fad9204d410ad08`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f178865c356dfadb4351dd90e17e88bc0c96c7a5b00c3fa27f7a7a50854a6`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70efcc630f7ac8f41932a95504f9faf4f5d3a98261ec78847c0b7895c7e38c55`  
		Last Modified: Fri, 13 Oct 2023 04:58:33 GMT  
		Size: 171.4 MB (171412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7380be57882dd81c0bc849142d511e957f6f209e899d784c2169dd1268af381`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03ae63d5fe1e840f0cc374100c4a33137e2c3862f567675d2a4f2a632ca68fd`  
		Last Modified: Fri, 13 Oct 2023 04:58:54 GMT  
		Size: 45.2 MB (45206478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78bb804d06a6c2affa7a4df0cb90051039812dd200a146925a447da4c03248f`  
		Last Modified: Fri, 13 Oct 2023 04:58:44 GMT  
		Size: 308.4 KB (308395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee77018c303d0f8b15482607876c85bd6f9bd91d7320f861f1146fc7f1e5f98`  
		Last Modified: Fri, 13 Oct 2023 04:58:52 GMT  
		Size: 72.0 MB (71972672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base-focal`

```console
$ docker pull ros@sha256:3ff6eb8c100ec747c1cafeb9fa426360f6b6f96d4808d04bda9dc748cac2769d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:650483554542d585af1f7c6fd09a4fb64d1492243f19010662e5434e1489a9d6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343156918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2661096a96da02ad942658f95aacd228d2d94aaa5334a9cc005367b9b88752`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 02:44:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:21:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:21:50 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 17 Aug 2023 07:21:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 17 Aug 2023 07:21:51 GMT
ENV LANG=C.UTF-8
# Thu, 17 Aug 2023 07:21:52 GMT
ENV LC_ALL=C.UTF-8
# Thu, 17 Aug 2023 07:21:52 GMT
ENV ROS_DISTRO=noetic
# Thu, 17 Aug 2023 07:23:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:23:53 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 17 Aug 2023 07:23:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 17 Aug 2023 07:23:54 GMT
CMD ["bash"]
# Thu, 17 Aug 2023 07:24:29 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:24:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 17 Aug 2023 07:25:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aab22f0326d7d89686f4eebe2ba52f86ca4e83a4c69d66dfe4f2b1494eae439`  
		Last Modified: Thu, 03 Aug 2023 02:53:09 GMT  
		Size: 1.2 MB (1198625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b915067b2cb577e1158572cfb9bb4edba91b52a0f5821152a8a4e2518dd702c`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 5.6 MB (5553744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87dd0b38cb0829def318257a357f2d9773c0c0f443432fe0ab8f0e28f8454a13`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b104afafaf102a6ecd5bc760e922c728c4ab27320895943844d8f53c908a025`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f437788a75a65f6ba1decf914b73eaf4b4712c46e542abaf9d51e92f1e6c32`  
		Last Modified: Thu, 17 Aug 2023 07:49:46 GMT  
		Size: 177.0 MB (176961988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a8de474ce644ddf64e37acf737479db384d569592e927234ba9775cbf3c044`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71044449a9df53317087cbf1480ae89d0864ed6c767b63f246f2a112cb697023`  
		Last Modified: Thu, 17 Aug 2023 07:50:07 GMT  
		Size: 50.9 MB (50940393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee57c22656c0736ccbe5b757eeada9768c4061541ea8fced3debcc9d8e5186c3`  
		Last Modified: Thu, 17 Aug 2023 07:49:59 GMT  
		Size: 305.0 KB (305044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01916643bc85febc6c44576e168005fd7892f275d1a187528964c1a062bb36a`  
		Last Modified: Thu, 17 Aug 2023 07:50:10 GMT  
		Size: 79.6 MB (79614040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:17c021f745282198d89551e984956f5d32bf3b296d79d27c72eb5129feecba56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289222658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b381b176ed648076efff35763069250dfe58cad8d71f4ac9f298cae85523902`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Oct 2023 10:47:59 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:47:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:48:06 GMT
ADD file:8dffbfada6e0bebb2858525182aef87ac2cbd88c624f32696ec2cb947e71a4f3 in / 
# Tue, 03 Oct 2023 10:48:07 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 01:25:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:25:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:25:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 13 Oct 2023 01:25:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 01:25:43 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 01:25:44 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 01:25:44 GMT
ENV ROS_DISTRO=noetic
# Fri, 13 Oct 2023 01:28:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:28:12 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 13 Oct 2023 01:28:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 01:28:13 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:28:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:28:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 01:30:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3b5f1ba1b648ae0824ed6a95ab17335537f8e689df99917fd374af5dd34078eb`  
		Last Modified: Fri, 13 Oct 2023 01:11:42 GMT  
		Size: 24.6 MB (24592174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a3643fb9ea7b4891593c2a71e53f70146f828b8896758ecc6804e843b3eb9d`  
		Last Modified: Fri, 13 Oct 2023 01:38:43 GMT  
		Size: 1.2 MB (1200040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d390fd421e090bebfad483fae5954c8ce4b3d98d6f7964b7d2af20febd3a8dd`  
		Last Modified: Fri, 13 Oct 2023 01:38:41 GMT  
		Size: 4.7 MB (4680598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f635e6735a4e72b10c5401661b398132793e75102ebdae3c1a4bb09369a9277b`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc440f8be875763f266a01bddecd7e5256b0f7024383d18f3ac27b3eefca620c`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8576e38b77aab0fa900f38b3857ac3f1f5f2f357b049bb4765eead409392f8ab`  
		Last Modified: Fri, 13 Oct 2023 01:39:16 GMT  
		Size: 157.4 MB (157433981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9929dceae2a7ac00be4bdeef95d2220d21923972182d5a0805ae6a130e9a5c`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbc9c70d09913eddb72c3c4f69d3eacc75f42772407b3a7f1b83b8ab76e8609`  
		Last Modified: Fri, 13 Oct 2023 01:39:37 GMT  
		Size: 40.5 MB (40504496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4c4f8456ac317553d22cb6aeb19337c7ba56c832bd9ce3050a5666e4e67276`  
		Last Modified: Fri, 13 Oct 2023 01:39:26 GMT  
		Size: 308.4 KB (308391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f11110f8ff52141ed436fcf91a65720ab159af26f35baf35ebec69235529767`  
		Last Modified: Fri, 13 Oct 2023 01:39:41 GMT  
		Size: 60.5 MB (60500564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e56292f13e93a79eaebd54ca1fc7cbce221cb489870c645c52c21a60984ae07c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.8 MB (322833438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ef0ff8399f8b8ffa366228b6c3a797d77f86744a8732f35f0389fdac3e32e0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:24:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:24:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:24:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 13 Oct 2023 04:24:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:24:38 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:24:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:24:38 GMT
ENV ROS_DISTRO=noetic
# Fri, 13 Oct 2023 04:27:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:27:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 13 Oct 2023 04:27:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:27:42 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 04:28:09 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:28:13 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 04:29:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6cba4020c0a193cd551ed8edf368670967e3546345b52c4ec66cb0931436e9b9`  
		Last Modified: Thu, 05 Oct 2023 12:12:17 GMT  
		Size: 27.2 MB (27199503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87696a1bdfb2280c9c8f032b8dad476643e285ea6a4daaaaf8dea807599345f3`  
		Last Modified: Fri, 13 Oct 2023 04:58:00 GMT  
		Size: 1.2 MB (1199301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c122b6409bbe49fd6863f4fe1b6c386aa8c0839b4d569cc6a7c864c54e4ebc`  
		Last Modified: Fri, 13 Oct 2023 04:57:58 GMT  
		Size: 5.5 MB (5532659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a917760d45f055be63dd5265386c3e099071676cbade870f5fad9204d410ad08`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f178865c356dfadb4351dd90e17e88bc0c96c7a5b00c3fa27f7a7a50854a6`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70efcc630f7ac8f41932a95504f9faf4f5d3a98261ec78847c0b7895c7e38c55`  
		Last Modified: Fri, 13 Oct 2023 04:58:33 GMT  
		Size: 171.4 MB (171412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7380be57882dd81c0bc849142d511e957f6f209e899d784c2169dd1268af381`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03ae63d5fe1e840f0cc374100c4a33137e2c3862f567675d2a4f2a632ca68fd`  
		Last Modified: Fri, 13 Oct 2023 04:58:54 GMT  
		Size: 45.2 MB (45206478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78bb804d06a6c2affa7a4df0cb90051039812dd200a146925a447da4c03248f`  
		Last Modified: Fri, 13 Oct 2023 04:58:44 GMT  
		Size: 308.4 KB (308395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee77018c303d0f8b15482607876c85bd6f9bd91d7320f861f1146fc7f1e5f98`  
		Last Modified: Fri, 13 Oct 2023 04:58:52 GMT  
		Size: 72.0 MB (71972672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:8194f525d32a5e79fbd53fafd715831c142e9e886f0eb89085993a1ee5d75827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:4567c93b88b61349305b4d46a5ab1db18e13e687f8cf7c044516b0a1317d0b1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212297441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48feda2e6ad6031588e90d77629741370feaca36cd10958f6a8aefd3613c704f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 02:44:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:21:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:21:50 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 17 Aug 2023 07:21:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 17 Aug 2023 07:21:51 GMT
ENV LANG=C.UTF-8
# Thu, 17 Aug 2023 07:21:52 GMT
ENV LC_ALL=C.UTF-8
# Thu, 17 Aug 2023 07:21:52 GMT
ENV ROS_DISTRO=noetic
# Thu, 17 Aug 2023 07:23:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:23:53 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 17 Aug 2023 07:23:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 17 Aug 2023 07:23:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aab22f0326d7d89686f4eebe2ba52f86ca4e83a4c69d66dfe4f2b1494eae439`  
		Last Modified: Thu, 03 Aug 2023 02:53:09 GMT  
		Size: 1.2 MB (1198625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b915067b2cb577e1158572cfb9bb4edba91b52a0f5821152a8a4e2518dd702c`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 5.6 MB (5553744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87dd0b38cb0829def318257a357f2d9773c0c0f443432fe0ab8f0e28f8454a13`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b104afafaf102a6ecd5bc760e922c728c4ab27320895943844d8f53c908a025`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f437788a75a65f6ba1decf914b73eaf4b4712c46e542abaf9d51e92f1e6c32`  
		Last Modified: Thu, 17 Aug 2023 07:49:46 GMT  
		Size: 177.0 MB (176961988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a8de474ce644ddf64e37acf737479db384d569592e927234ba9775cbf3c044`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:52c14fc420e59c653e4bf30904f6ba6b7eae002c315f6c92d1fda70d4db59fed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187909207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33bb258e0838ea9918ba8dd90b76a6ffe1b5c82533481b3a8faa82e9ade5a9b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Oct 2023 10:47:59 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:47:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:48:06 GMT
ADD file:8dffbfada6e0bebb2858525182aef87ac2cbd88c624f32696ec2cb947e71a4f3 in / 
# Tue, 03 Oct 2023 10:48:07 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 01:25:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:25:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:25:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 13 Oct 2023 01:25:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 01:25:43 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 01:25:44 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 01:25:44 GMT
ENV ROS_DISTRO=noetic
# Fri, 13 Oct 2023 01:28:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:28:12 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 13 Oct 2023 01:28:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 01:28:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3b5f1ba1b648ae0824ed6a95ab17335537f8e689df99917fd374af5dd34078eb`  
		Last Modified: Fri, 13 Oct 2023 01:11:42 GMT  
		Size: 24.6 MB (24592174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a3643fb9ea7b4891593c2a71e53f70146f828b8896758ecc6804e843b3eb9d`  
		Last Modified: Fri, 13 Oct 2023 01:38:43 GMT  
		Size: 1.2 MB (1200040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d390fd421e090bebfad483fae5954c8ce4b3d98d6f7964b7d2af20febd3a8dd`  
		Last Modified: Fri, 13 Oct 2023 01:38:41 GMT  
		Size: 4.7 MB (4680598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f635e6735a4e72b10c5401661b398132793e75102ebdae3c1a4bb09369a9277b`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc440f8be875763f266a01bddecd7e5256b0f7024383d18f3ac27b3eefca620c`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8576e38b77aab0fa900f38b3857ac3f1f5f2f357b049bb4765eead409392f8ab`  
		Last Modified: Fri, 13 Oct 2023 01:39:16 GMT  
		Size: 157.4 MB (157433981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9929dceae2a7ac00be4bdeef95d2220d21923972182d5a0805ae6a130e9a5c`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d8975039cd04a15b6ce7eadaac78a500a8b3a0312d569aab2046d6d130261036
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205345893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca610446a7d617cb86f2b0d7814de4fa74de4b7d3e1f317815f3c534f19623b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:24:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:24:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:24:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 13 Oct 2023 04:24:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:24:38 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:24:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:24:38 GMT
ENV ROS_DISTRO=noetic
# Fri, 13 Oct 2023 04:27:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:27:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 13 Oct 2023 04:27:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:27:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6cba4020c0a193cd551ed8edf368670967e3546345b52c4ec66cb0931436e9b9`  
		Last Modified: Thu, 05 Oct 2023 12:12:17 GMT  
		Size: 27.2 MB (27199503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87696a1bdfb2280c9c8f032b8dad476643e285ea6a4daaaaf8dea807599345f3`  
		Last Modified: Fri, 13 Oct 2023 04:58:00 GMT  
		Size: 1.2 MB (1199301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c122b6409bbe49fd6863f4fe1b6c386aa8c0839b4d569cc6a7c864c54e4ebc`  
		Last Modified: Fri, 13 Oct 2023 04:57:58 GMT  
		Size: 5.5 MB (5532659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a917760d45f055be63dd5265386c3e099071676cbade870f5fad9204d410ad08`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f178865c356dfadb4351dd90e17e88bc0c96c7a5b00c3fa27f7a7a50854a6`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70efcc630f7ac8f41932a95504f9faf4f5d3a98261ec78847c0b7895c7e38c55`  
		Last Modified: Fri, 13 Oct 2023 04:58:33 GMT  
		Size: 171.4 MB (171412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7380be57882dd81c0bc849142d511e957f6f209e899d784c2169dd1268af381`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:8194f525d32a5e79fbd53fafd715831c142e9e886f0eb89085993a1ee5d75827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:4567c93b88b61349305b4d46a5ab1db18e13e687f8cf7c044516b0a1317d0b1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212297441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48feda2e6ad6031588e90d77629741370feaca36cd10958f6a8aefd3613c704f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Aug 2023 06:16:43 GMT
ARG RELEASE
# Tue, 01 Aug 2023 06:16:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Aug 2023 06:16:44 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Aug 2023 06:16:45 GMT
ADD file:233702cd816c07bc9fed02881b11fb3bdcaee41f3ce3ec1c9f0c4a060b155d5b in / 
# Tue, 01 Aug 2023 06:16:46 GMT
CMD ["/bin/bash"]
# Thu, 03 Aug 2023 02:44:48 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:21:50 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:21:50 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 17 Aug 2023 07:21:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 17 Aug 2023 07:21:51 GMT
ENV LANG=C.UTF-8
# Thu, 17 Aug 2023 07:21:52 GMT
ENV LC_ALL=C.UTF-8
# Thu, 17 Aug 2023 07:21:52 GMT
ENV ROS_DISTRO=noetic
# Thu, 17 Aug 2023 07:23:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 07:23:53 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 17 Aug 2023 07:23:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 17 Aug 2023 07:23:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7007490126efaae58924972668256aaeb4858e6c4537eb4257e1978719b958c7`  
		Last Modified: Tue, 01 Aug 2023 08:35:40 GMT  
		Size: 28.6 MB (28580671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aab22f0326d7d89686f4eebe2ba52f86ca4e83a4c69d66dfe4f2b1494eae439`  
		Last Modified: Thu, 03 Aug 2023 02:53:09 GMT  
		Size: 1.2 MB (1198625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b915067b2cb577e1158572cfb9bb4edba91b52a0f5821152a8a4e2518dd702c`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 5.6 MB (5553744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87dd0b38cb0829def318257a357f2d9773c0c0f443432fe0ab8f0e28f8454a13`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b104afafaf102a6ecd5bc760e922c728c4ab27320895943844d8f53c908a025`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9f437788a75a65f6ba1decf914b73eaf4b4712c46e542abaf9d51e92f1e6c32`  
		Last Modified: Thu, 17 Aug 2023 07:49:46 GMT  
		Size: 177.0 MB (176961988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a8de474ce644ddf64e37acf737479db384d569592e927234ba9775cbf3c044`  
		Last Modified: Thu, 17 Aug 2023 07:49:20 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:52c14fc420e59c653e4bf30904f6ba6b7eae002c315f6c92d1fda70d4db59fed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187909207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33bb258e0838ea9918ba8dd90b76a6ffe1b5c82533481b3a8faa82e9ade5a9b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Oct 2023 10:47:59 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:47:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:47:59 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:48:06 GMT
ADD file:8dffbfada6e0bebb2858525182aef87ac2cbd88c624f32696ec2cb947e71a4f3 in / 
# Tue, 03 Oct 2023 10:48:07 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 01:25:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:25:41 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:25:42 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 13 Oct 2023 01:25:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 01:25:43 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 01:25:44 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 01:25:44 GMT
ENV ROS_DISTRO=noetic
# Fri, 13 Oct 2023 01:28:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 01:28:12 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 13 Oct 2023 01:28:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 01:28:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3b5f1ba1b648ae0824ed6a95ab17335537f8e689df99917fd374af5dd34078eb`  
		Last Modified: Fri, 13 Oct 2023 01:11:42 GMT  
		Size: 24.6 MB (24592174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a3643fb9ea7b4891593c2a71e53f70146f828b8896758ecc6804e843b3eb9d`  
		Last Modified: Fri, 13 Oct 2023 01:38:43 GMT  
		Size: 1.2 MB (1200040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d390fd421e090bebfad483fae5954c8ce4b3d98d6f7964b7d2af20febd3a8dd`  
		Last Modified: Fri, 13 Oct 2023 01:38:41 GMT  
		Size: 4.7 MB (4680598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f635e6735a4e72b10c5401661b398132793e75102ebdae3c1a4bb09369a9277b`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc440f8be875763f266a01bddecd7e5256b0f7024383d18f3ac27b3eefca620c`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8576e38b77aab0fa900f38b3857ac3f1f5f2f357b049bb4765eead409392f8ab`  
		Last Modified: Fri, 13 Oct 2023 01:39:16 GMT  
		Size: 157.4 MB (157433981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9929dceae2a7ac00be4bdeef95d2220d21923972182d5a0805ae6a130e9a5c`  
		Last Modified: Fri, 13 Oct 2023 01:38:40 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d8975039cd04a15b6ce7eadaac78a500a8b3a0312d569aab2046d6d130261036
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205345893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca610446a7d617cb86f2b0d7814de4fa74de4b7d3e1f317815f3c534f19623b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:24:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:24:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:24:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 13 Oct 2023 04:24:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:24:38 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:24:38 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:24:38 GMT
ENV ROS_DISTRO=noetic
# Fri, 13 Oct 2023 04:27:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:27:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 13 Oct 2023 04:27:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:27:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6cba4020c0a193cd551ed8edf368670967e3546345b52c4ec66cb0931436e9b9`  
		Last Modified: Thu, 05 Oct 2023 12:12:17 GMT  
		Size: 27.2 MB (27199503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87696a1bdfb2280c9c8f032b8dad476643e285ea6a4daaaaf8dea807599345f3`  
		Last Modified: Fri, 13 Oct 2023 04:58:00 GMT  
		Size: 1.2 MB (1199301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c122b6409bbe49fd6863f4fe1b6c386aa8c0839b4d569cc6a7c864c54e4ebc`  
		Last Modified: Fri, 13 Oct 2023 04:57:58 GMT  
		Size: 5.5 MB (5532659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a917760d45f055be63dd5265386c3e099071676cbade870f5fad9204d410ad08`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f178865c356dfadb4351dd90e17e88bc0c96c7a5b00c3fa27f7a7a50854a6`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70efcc630f7ac8f41932a95504f9faf4f5d3a98261ec78847c0b7895c7e38c55`  
		Last Modified: Fri, 13 Oct 2023 04:58:33 GMT  
		Size: 171.4 MB (171412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7380be57882dd81c0bc849142d511e957f6f209e899d784c2169dd1268af381`  
		Last Modified: Fri, 13 Oct 2023 04:57:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling`

```console
$ docker pull ros@sha256:3675cabe283a5abad8d55c4a0c1fd128c7e21ba169431539c3186c0e7b2e71f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:79b213db34b99fb725c9a7b6572eaf29b8bcbb8e39a7e0f679a187d962d2a0d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268920835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6516d0ed0221d02f13adf0f0729e3a3a5c6f1e1092067cae33b36a99d3144b5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:09:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 03 Oct 2023 06:09:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Oct 2023 06:33:13 GMT
ENV ROS_DISTRO=rolling
# Tue, 03 Oct 2023 06:33:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:33:59 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 03 Oct 2023 06:34:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Oct 2023 06:34:00 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 06:34:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:34:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 03 Oct 2023 06:34:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 03 Oct 2023 06:34:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1370ba32049345dce3665687ae8209d03dc6e8d9d44e99e46c0ceb62f9f1f30d`  
		Last Modified: Tue, 03 Oct 2023 06:37:13 GMT  
		Size: 1.2 MB (1213056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c1e1f3dd2585388cc558f6237ee492769081f489b65cd386188d8efb6cdce6`  
		Last Modified: Tue, 03 Oct 2023 06:37:12 GMT  
		Size: 3.8 MB (3828981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198e4b86b803705bfcbea4adc86401d2d0cd4af88199c9e706cf0803b5be7842`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d310e00acb45665d82263e8800579055fb2ea11b71dd4926c8a7323855af7`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b293927275b81c0d4e6656435654ec293113bba612b31ca59e3aa388e1135f95`  
		Last Modified: Tue, 03 Oct 2023 06:42:33 GMT  
		Size: 124.2 MB (124189046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223180173aa5341b495187f6e300564465cda4640e1b148b6ca8ed0cc899c68e`  
		Last Modified: Tue, 03 Oct 2023 06:42:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e2773c9029123cdd8290196a82de02887242fa5c728c5b8886bfed45463802`  
		Last Modified: Tue, 03 Oct 2023 06:42:52 GMT  
		Size: 85.2 MB (85169808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9c1915ec06d4fd80a44fcb58109d86f37fdaf823c11cc8c005d7669904f4c5`  
		Last Modified: Tue, 03 Oct 2023 06:42:42 GMT  
		Size: 299.7 KB (299676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d355b33996f748fb2d58db4698a2e35d77ac2ba6aa76e1d0d1bcb825b13a82`  
		Last Modified: Tue, 03 Oct 2023 06:42:41 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca27a8f8b5f2ed75039543c7f20e06042a503755099656d45c94af78b093ebff`  
		Last Modified: Tue, 03 Oct 2023 06:42:45 GMT  
		Size: 23.8 MB (23774523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f8fdccf48e9b81b602a8445b5cef7a2e4034e978a22bf12852154e02ea5fa31f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261370321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ccba50e4a9274d03a4e53a87de3dec55751b85b08bccc5bc689652d8fca241`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:37:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 13 Oct 2023 04:38:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:54:13 GMT
ENV ROS_DISTRO=rolling
# Fri, 13 Oct 2023 04:54:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:54:53 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 13 Oct 2023 04:54:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:54:53 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 04:55:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:55:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 04:55:22 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 13 Oct 2023 04:55:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff18d61171fb1a17fb0edecb7a0600d4d0be1c103726f9d60cfb59071d3eccf9`  
		Last Modified: Fri, 13 Oct 2023 05:00:30 GMT  
		Size: 1.2 MB (1214464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa41e452048780b8d89bde1b448e5c130e073ab26d8a3c3e2ec3d4a4170f55f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 3.8 MB (3801906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c55f0e8967a89d129c1106434dacd41bd9239f7fe793b4dc37245f7a26762f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023f71811e459a590f4b10edecae765c4b654f7139277e4c704f11126c720c5f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76919e69d9bf2e3d2ca8ae0d65ff46ad78ea4ad6cb40564909d2ab3ca2cb1dd`  
		Last Modified: Fri, 13 Oct 2023 05:05:47 GMT  
		Size: 121.7 MB (121650914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78ad5922e8a4b2b9b64791f4eb98c6ce309e5d8ff2ff1a652ce79787364cf87`  
		Last Modified: Fri, 13 Oct 2023 05:05:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f0a588fd72820cb49eac55ed707a7428229cb4c8228701ebfcc96dcf24ca78`  
		Last Modified: Fri, 13 Oct 2023 05:06:06 GMT  
		Size: 82.8 MB (82845847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbb9063833248fce2192270990d5eeb31b7fb4a3c64df34c1c823789260081d`  
		Last Modified: Fri, 13 Oct 2023 05:05:57 GMT  
		Size: 299.7 KB (299701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9128e572254481ae3dc8f9100bc18797c961736b9dfa5e760792d29234e8c7`  
		Last Modified: Fri, 13 Oct 2023 05:05:57 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e186e48e905c962ffd30c9312077a518788ba2a26f2622cbeda0814718023cb`  
		Last Modified: Fri, 13 Oct 2023 05:06:01 GMT  
		Size: 23.2 MB (23160671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:8eae9dda4463f44fd695f643f7c7f156fd9fafddb56980af027c204792f92721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:86e7eaa92357b439a81e54d37947e17aff159dd5c5ba5b7b6abf930163c6859a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **959.8 MB (959784314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050325da5da6f6a75638ec1aa7f73994c8c4327f6915a22fce8c475e22ac384d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:09:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 03 Oct 2023 06:09:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Oct 2023 06:33:13 GMT
ENV ROS_DISTRO=rolling
# Tue, 03 Oct 2023 06:33:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:33:59 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 03 Oct 2023 06:34:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Oct 2023 06:34:00 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 06:34:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:34:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 03 Oct 2023 06:34:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 03 Oct 2023 06:34:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:36:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1370ba32049345dce3665687ae8209d03dc6e8d9d44e99e46c0ceb62f9f1f30d`  
		Last Modified: Tue, 03 Oct 2023 06:37:13 GMT  
		Size: 1.2 MB (1213056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c1e1f3dd2585388cc558f6237ee492769081f489b65cd386188d8efb6cdce6`  
		Last Modified: Tue, 03 Oct 2023 06:37:12 GMT  
		Size: 3.8 MB (3828981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198e4b86b803705bfcbea4adc86401d2d0cd4af88199c9e706cf0803b5be7842`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d310e00acb45665d82263e8800579055fb2ea11b71dd4926c8a7323855af7`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b293927275b81c0d4e6656435654ec293113bba612b31ca59e3aa388e1135f95`  
		Last Modified: Tue, 03 Oct 2023 06:42:33 GMT  
		Size: 124.2 MB (124189046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223180173aa5341b495187f6e300564465cda4640e1b148b6ca8ed0cc899c68e`  
		Last Modified: Tue, 03 Oct 2023 06:42:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e2773c9029123cdd8290196a82de02887242fa5c728c5b8886bfed45463802`  
		Last Modified: Tue, 03 Oct 2023 06:42:52 GMT  
		Size: 85.2 MB (85169808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9c1915ec06d4fd80a44fcb58109d86f37fdaf823c11cc8c005d7669904f4c5`  
		Last Modified: Tue, 03 Oct 2023 06:42:42 GMT  
		Size: 299.7 KB (299676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d355b33996f748fb2d58db4698a2e35d77ac2ba6aa76e1d0d1bcb825b13a82`  
		Last Modified: Tue, 03 Oct 2023 06:42:41 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca27a8f8b5f2ed75039543c7f20e06042a503755099656d45c94af78b093ebff`  
		Last Modified: Tue, 03 Oct 2023 06:42:45 GMT  
		Size: 23.8 MB (23774523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efed89e0cee4a08cae9cee68cdf8e1c8d2a8c575be665775686709f68f527cb9`  
		Last Modified: Tue, 03 Oct 2023 06:44:32 GMT  
		Size: 690.9 MB (690863479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:28bbaa7371b7bb8e0243b2a9111cb01b5e3313ec3de02c25d1ba4ed15412c518
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.1 MB (920055745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607cc914ad92d99cbd36b4b58aeabb941c6515e34f2c256327c175b2aae5a81a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:37:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 13 Oct 2023 04:38:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:54:13 GMT
ENV ROS_DISTRO=rolling
# Fri, 13 Oct 2023 04:54:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:54:53 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 13 Oct 2023 04:54:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:54:53 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 04:55:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:55:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 04:55:22 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 13 Oct 2023 04:55:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff18d61171fb1a17fb0edecb7a0600d4d0be1c103726f9d60cfb59071d3eccf9`  
		Last Modified: Fri, 13 Oct 2023 05:00:30 GMT  
		Size: 1.2 MB (1214464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa41e452048780b8d89bde1b448e5c130e073ab26d8a3c3e2ec3d4a4170f55f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 3.8 MB (3801906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c55f0e8967a89d129c1106434dacd41bd9239f7fe793b4dc37245f7a26762f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023f71811e459a590f4b10edecae765c4b654f7139277e4c704f11126c720c5f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76919e69d9bf2e3d2ca8ae0d65ff46ad78ea4ad6cb40564909d2ab3ca2cb1dd`  
		Last Modified: Fri, 13 Oct 2023 05:05:47 GMT  
		Size: 121.7 MB (121650914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78ad5922e8a4b2b9b64791f4eb98c6ce309e5d8ff2ff1a652ce79787364cf87`  
		Last Modified: Fri, 13 Oct 2023 05:05:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f0a588fd72820cb49eac55ed707a7428229cb4c8228701ebfcc96dcf24ca78`  
		Last Modified: Fri, 13 Oct 2023 05:06:06 GMT  
		Size: 82.8 MB (82845847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbb9063833248fce2192270990d5eeb31b7fb4a3c64df34c1c823789260081d`  
		Last Modified: Fri, 13 Oct 2023 05:05:57 GMT  
		Size: 299.7 KB (299701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9128e572254481ae3dc8f9100bc18797c961736b9dfa5e760792d29234e8c7`  
		Last Modified: Fri, 13 Oct 2023 05:05:57 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e186e48e905c962ffd30c9312077a518788ba2a26f2622cbeda0814718023cb`  
		Last Modified: Fri, 13 Oct 2023 05:06:01 GMT  
		Size: 23.2 MB (23160671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5bfa3cc1ec62d14cf59d104ba0db344c4e61d8eed20816c317ab5cfe17d554`  
		Last Modified: Fri, 13 Oct 2023 05:07:39 GMT  
		Size: 658.7 MB (658685424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-perception-jammy`

```console
$ docker pull ros@sha256:8eae9dda4463f44fd695f643f7c7f156fd9fafddb56980af027c204792f92721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:86e7eaa92357b439a81e54d37947e17aff159dd5c5ba5b7b6abf930163c6859a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **959.8 MB (959784314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:050325da5da6f6a75638ec1aa7f73994c8c4327f6915a22fce8c475e22ac384d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:09:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 03 Oct 2023 06:09:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Oct 2023 06:33:13 GMT
ENV ROS_DISTRO=rolling
# Tue, 03 Oct 2023 06:33:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:33:59 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 03 Oct 2023 06:34:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Oct 2023 06:34:00 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 06:34:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:34:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 03 Oct 2023 06:34:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 03 Oct 2023 06:34:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:36:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1370ba32049345dce3665687ae8209d03dc6e8d9d44e99e46c0ceb62f9f1f30d`  
		Last Modified: Tue, 03 Oct 2023 06:37:13 GMT  
		Size: 1.2 MB (1213056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c1e1f3dd2585388cc558f6237ee492769081f489b65cd386188d8efb6cdce6`  
		Last Modified: Tue, 03 Oct 2023 06:37:12 GMT  
		Size: 3.8 MB (3828981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198e4b86b803705bfcbea4adc86401d2d0cd4af88199c9e706cf0803b5be7842`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d310e00acb45665d82263e8800579055fb2ea11b71dd4926c8a7323855af7`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b293927275b81c0d4e6656435654ec293113bba612b31ca59e3aa388e1135f95`  
		Last Modified: Tue, 03 Oct 2023 06:42:33 GMT  
		Size: 124.2 MB (124189046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223180173aa5341b495187f6e300564465cda4640e1b148b6ca8ed0cc899c68e`  
		Last Modified: Tue, 03 Oct 2023 06:42:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e2773c9029123cdd8290196a82de02887242fa5c728c5b8886bfed45463802`  
		Last Modified: Tue, 03 Oct 2023 06:42:52 GMT  
		Size: 85.2 MB (85169808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9c1915ec06d4fd80a44fcb58109d86f37fdaf823c11cc8c005d7669904f4c5`  
		Last Modified: Tue, 03 Oct 2023 06:42:42 GMT  
		Size: 299.7 KB (299676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d355b33996f748fb2d58db4698a2e35d77ac2ba6aa76e1d0d1bcb825b13a82`  
		Last Modified: Tue, 03 Oct 2023 06:42:41 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca27a8f8b5f2ed75039543c7f20e06042a503755099656d45c94af78b093ebff`  
		Last Modified: Tue, 03 Oct 2023 06:42:45 GMT  
		Size: 23.8 MB (23774523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efed89e0cee4a08cae9cee68cdf8e1c8d2a8c575be665775686709f68f527cb9`  
		Last Modified: Tue, 03 Oct 2023 06:44:32 GMT  
		Size: 690.9 MB (690863479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:28bbaa7371b7bb8e0243b2a9111cb01b5e3313ec3de02c25d1ba4ed15412c518
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **920.1 MB (920055745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607cc914ad92d99cbd36b4b58aeabb941c6515e34f2c256327c175b2aae5a81a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:37:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 13 Oct 2023 04:38:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:54:13 GMT
ENV ROS_DISTRO=rolling
# Fri, 13 Oct 2023 04:54:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:54:53 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 13 Oct 2023 04:54:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:54:53 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 04:55:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:55:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 04:55:22 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 13 Oct 2023 04:55:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff18d61171fb1a17fb0edecb7a0600d4d0be1c103726f9d60cfb59071d3eccf9`  
		Last Modified: Fri, 13 Oct 2023 05:00:30 GMT  
		Size: 1.2 MB (1214464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa41e452048780b8d89bde1b448e5c130e073ab26d8a3c3e2ec3d4a4170f55f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 3.8 MB (3801906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c55f0e8967a89d129c1106434dacd41bd9239f7fe793b4dc37245f7a26762f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023f71811e459a590f4b10edecae765c4b654f7139277e4c704f11126c720c5f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76919e69d9bf2e3d2ca8ae0d65ff46ad78ea4ad6cb40564909d2ab3ca2cb1dd`  
		Last Modified: Fri, 13 Oct 2023 05:05:47 GMT  
		Size: 121.7 MB (121650914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78ad5922e8a4b2b9b64791f4eb98c6ce309e5d8ff2ff1a652ce79787364cf87`  
		Last Modified: Fri, 13 Oct 2023 05:05:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f0a588fd72820cb49eac55ed707a7428229cb4c8228701ebfcc96dcf24ca78`  
		Last Modified: Fri, 13 Oct 2023 05:06:06 GMT  
		Size: 82.8 MB (82845847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbb9063833248fce2192270990d5eeb31b7fb4a3c64df34c1c823789260081d`  
		Last Modified: Fri, 13 Oct 2023 05:05:57 GMT  
		Size: 299.7 KB (299701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9128e572254481ae3dc8f9100bc18797c961736b9dfa5e760792d29234e8c7`  
		Last Modified: Fri, 13 Oct 2023 05:05:57 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e186e48e905c962ffd30c9312077a518788ba2a26f2622cbeda0814718023cb`  
		Last Modified: Fri, 13 Oct 2023 05:06:01 GMT  
		Size: 23.2 MB (23160671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5bfa3cc1ec62d14cf59d104ba0db344c4e61d8eed20816c317ab5cfe17d554`  
		Last Modified: Fri, 13 Oct 2023 05:07:39 GMT  
		Size: 658.7 MB (658685424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:3675cabe283a5abad8d55c4a0c1fd128c7e21ba169431539c3186c0e7b2e71f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:79b213db34b99fb725c9a7b6572eaf29b8bcbb8e39a7e0f679a187d962d2a0d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268920835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6516d0ed0221d02f13adf0f0729e3a3a5c6f1e1092067cae33b36a99d3144b5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:09:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 03 Oct 2023 06:09:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Oct 2023 06:33:13 GMT
ENV ROS_DISTRO=rolling
# Tue, 03 Oct 2023 06:33:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:33:59 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 03 Oct 2023 06:34:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Oct 2023 06:34:00 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 06:34:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:34:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 03 Oct 2023 06:34:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 03 Oct 2023 06:34:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1370ba32049345dce3665687ae8209d03dc6e8d9d44e99e46c0ceb62f9f1f30d`  
		Last Modified: Tue, 03 Oct 2023 06:37:13 GMT  
		Size: 1.2 MB (1213056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c1e1f3dd2585388cc558f6237ee492769081f489b65cd386188d8efb6cdce6`  
		Last Modified: Tue, 03 Oct 2023 06:37:12 GMT  
		Size: 3.8 MB (3828981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198e4b86b803705bfcbea4adc86401d2d0cd4af88199c9e706cf0803b5be7842`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d310e00acb45665d82263e8800579055fb2ea11b71dd4926c8a7323855af7`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b293927275b81c0d4e6656435654ec293113bba612b31ca59e3aa388e1135f95`  
		Last Modified: Tue, 03 Oct 2023 06:42:33 GMT  
		Size: 124.2 MB (124189046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223180173aa5341b495187f6e300564465cda4640e1b148b6ca8ed0cc899c68e`  
		Last Modified: Tue, 03 Oct 2023 06:42:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e2773c9029123cdd8290196a82de02887242fa5c728c5b8886bfed45463802`  
		Last Modified: Tue, 03 Oct 2023 06:42:52 GMT  
		Size: 85.2 MB (85169808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9c1915ec06d4fd80a44fcb58109d86f37fdaf823c11cc8c005d7669904f4c5`  
		Last Modified: Tue, 03 Oct 2023 06:42:42 GMT  
		Size: 299.7 KB (299676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d355b33996f748fb2d58db4698a2e35d77ac2ba6aa76e1d0d1bcb825b13a82`  
		Last Modified: Tue, 03 Oct 2023 06:42:41 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca27a8f8b5f2ed75039543c7f20e06042a503755099656d45c94af78b093ebff`  
		Last Modified: Tue, 03 Oct 2023 06:42:45 GMT  
		Size: 23.8 MB (23774523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f8fdccf48e9b81b602a8445b5cef7a2e4034e978a22bf12852154e02ea5fa31f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261370321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ccba50e4a9274d03a4e53a87de3dec55751b85b08bccc5bc689652d8fca241`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:37:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 13 Oct 2023 04:38:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:54:13 GMT
ENV ROS_DISTRO=rolling
# Fri, 13 Oct 2023 04:54:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:54:53 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 13 Oct 2023 04:54:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:54:53 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 04:55:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:55:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 04:55:22 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 13 Oct 2023 04:55:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff18d61171fb1a17fb0edecb7a0600d4d0be1c103726f9d60cfb59071d3eccf9`  
		Last Modified: Fri, 13 Oct 2023 05:00:30 GMT  
		Size: 1.2 MB (1214464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa41e452048780b8d89bde1b448e5c130e073ab26d8a3c3e2ec3d4a4170f55f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 3.8 MB (3801906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c55f0e8967a89d129c1106434dacd41bd9239f7fe793b4dc37245f7a26762f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023f71811e459a590f4b10edecae765c4b654f7139277e4c704f11126c720c5f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76919e69d9bf2e3d2ca8ae0d65ff46ad78ea4ad6cb40564909d2ab3ca2cb1dd`  
		Last Modified: Fri, 13 Oct 2023 05:05:47 GMT  
		Size: 121.7 MB (121650914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78ad5922e8a4b2b9b64791f4eb98c6ce309e5d8ff2ff1a652ce79787364cf87`  
		Last Modified: Fri, 13 Oct 2023 05:05:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f0a588fd72820cb49eac55ed707a7428229cb4c8228701ebfcc96dcf24ca78`  
		Last Modified: Fri, 13 Oct 2023 05:06:06 GMT  
		Size: 82.8 MB (82845847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbb9063833248fce2192270990d5eeb31b7fb4a3c64df34c1c823789260081d`  
		Last Modified: Fri, 13 Oct 2023 05:05:57 GMT  
		Size: 299.7 KB (299701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9128e572254481ae3dc8f9100bc18797c961736b9dfa5e760792d29234e8c7`  
		Last Modified: Fri, 13 Oct 2023 05:05:57 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e186e48e905c962ffd30c9312077a518788ba2a26f2622cbeda0814718023cb`  
		Last Modified: Fri, 13 Oct 2023 05:06:01 GMT  
		Size: 23.2 MB (23160671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base-jammy`

```console
$ docker pull ros@sha256:3675cabe283a5abad8d55c4a0c1fd128c7e21ba169431539c3186c0e7b2e71f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:79b213db34b99fb725c9a7b6572eaf29b8bcbb8e39a7e0f679a187d962d2a0d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268920835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6516d0ed0221d02f13adf0f0729e3a3a5c6f1e1092067cae33b36a99d3144b5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:09:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 03 Oct 2023 06:09:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Oct 2023 06:33:13 GMT
ENV ROS_DISTRO=rolling
# Tue, 03 Oct 2023 06:33:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:33:59 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 03 Oct 2023 06:34:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Oct 2023 06:34:00 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 06:34:17 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:34:22 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 03 Oct 2023 06:34:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 03 Oct 2023 06:34:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1370ba32049345dce3665687ae8209d03dc6e8d9d44e99e46c0ceb62f9f1f30d`  
		Last Modified: Tue, 03 Oct 2023 06:37:13 GMT  
		Size: 1.2 MB (1213056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c1e1f3dd2585388cc558f6237ee492769081f489b65cd386188d8efb6cdce6`  
		Last Modified: Tue, 03 Oct 2023 06:37:12 GMT  
		Size: 3.8 MB (3828981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198e4b86b803705bfcbea4adc86401d2d0cd4af88199c9e706cf0803b5be7842`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d310e00acb45665d82263e8800579055fb2ea11b71dd4926c8a7323855af7`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b293927275b81c0d4e6656435654ec293113bba612b31ca59e3aa388e1135f95`  
		Last Modified: Tue, 03 Oct 2023 06:42:33 GMT  
		Size: 124.2 MB (124189046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223180173aa5341b495187f6e300564465cda4640e1b148b6ca8ed0cc899c68e`  
		Last Modified: Tue, 03 Oct 2023 06:42:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e2773c9029123cdd8290196a82de02887242fa5c728c5b8886bfed45463802`  
		Last Modified: Tue, 03 Oct 2023 06:42:52 GMT  
		Size: 85.2 MB (85169808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9c1915ec06d4fd80a44fcb58109d86f37fdaf823c11cc8c005d7669904f4c5`  
		Last Modified: Tue, 03 Oct 2023 06:42:42 GMT  
		Size: 299.7 KB (299676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d355b33996f748fb2d58db4698a2e35d77ac2ba6aa76e1d0d1bcb825b13a82`  
		Last Modified: Tue, 03 Oct 2023 06:42:41 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca27a8f8b5f2ed75039543c7f20e06042a503755099656d45c94af78b093ebff`  
		Last Modified: Tue, 03 Oct 2023 06:42:45 GMT  
		Size: 23.8 MB (23774523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f8fdccf48e9b81b602a8445b5cef7a2e4034e978a22bf12852154e02ea5fa31f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261370321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ccba50e4a9274d03a4e53a87de3dec55751b85b08bccc5bc689652d8fca241`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:37:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 13 Oct 2023 04:38:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:54:13 GMT
ENV ROS_DISTRO=rolling
# Fri, 13 Oct 2023 04:54:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:54:53 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 13 Oct 2023 04:54:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:54:53 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 04:55:14 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:55:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 13 Oct 2023 04:55:22 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 13 Oct 2023 04:55:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff18d61171fb1a17fb0edecb7a0600d4d0be1c103726f9d60cfb59071d3eccf9`  
		Last Modified: Fri, 13 Oct 2023 05:00:30 GMT  
		Size: 1.2 MB (1214464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa41e452048780b8d89bde1b448e5c130e073ab26d8a3c3e2ec3d4a4170f55f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 3.8 MB (3801906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c55f0e8967a89d129c1106434dacd41bd9239f7fe793b4dc37245f7a26762f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023f71811e459a590f4b10edecae765c4b654f7139277e4c704f11126c720c5f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76919e69d9bf2e3d2ca8ae0d65ff46ad78ea4ad6cb40564909d2ab3ca2cb1dd`  
		Last Modified: Fri, 13 Oct 2023 05:05:47 GMT  
		Size: 121.7 MB (121650914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78ad5922e8a4b2b9b64791f4eb98c6ce309e5d8ff2ff1a652ce79787364cf87`  
		Last Modified: Fri, 13 Oct 2023 05:05:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f0a588fd72820cb49eac55ed707a7428229cb4c8228701ebfcc96dcf24ca78`  
		Last Modified: Fri, 13 Oct 2023 05:06:06 GMT  
		Size: 82.8 MB (82845847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbb9063833248fce2192270990d5eeb31b7fb4a3c64df34c1c823789260081d`  
		Last Modified: Fri, 13 Oct 2023 05:05:57 GMT  
		Size: 299.7 KB (299701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9128e572254481ae3dc8f9100bc18797c961736b9dfa5e760792d29234e8c7`  
		Last Modified: Fri, 13 Oct 2023 05:05:57 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e186e48e905c962ffd30c9312077a518788ba2a26f2622cbeda0814718023cb`  
		Last Modified: Fri, 13 Oct 2023 05:06:01 GMT  
		Size: 23.2 MB (23160671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:1a1da3f393a7e216a6a27b701122d0fc81852467d9515f323077170000434a2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:82e943d3795de3208b880176e44ef3c1fe938e2a645cd4324cee9176e37a63ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159674366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1a375fa361d6d2dbb1b8150b27a0610a6a3683ebdc6d364167c63b1671cc34`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:09:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 03 Oct 2023 06:09:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Oct 2023 06:33:13 GMT
ENV ROS_DISTRO=rolling
# Tue, 03 Oct 2023 06:33:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:33:59 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 03 Oct 2023 06:34:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Oct 2023 06:34:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1370ba32049345dce3665687ae8209d03dc6e8d9d44e99e46c0ceb62f9f1f30d`  
		Last Modified: Tue, 03 Oct 2023 06:37:13 GMT  
		Size: 1.2 MB (1213056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c1e1f3dd2585388cc558f6237ee492769081f489b65cd386188d8efb6cdce6`  
		Last Modified: Tue, 03 Oct 2023 06:37:12 GMT  
		Size: 3.8 MB (3828981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198e4b86b803705bfcbea4adc86401d2d0cd4af88199c9e706cf0803b5be7842`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d310e00acb45665d82263e8800579055fb2ea11b71dd4926c8a7323855af7`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b293927275b81c0d4e6656435654ec293113bba612b31ca59e3aa388e1135f95`  
		Last Modified: Tue, 03 Oct 2023 06:42:33 GMT  
		Size: 124.2 MB (124189046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223180173aa5341b495187f6e300564465cda4640e1b148b6ca8ed0cc899c68e`  
		Last Modified: Tue, 03 Oct 2023 06:42:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ab2505deb5f42c48cb360b80157d2be11857c4382a68dd09bc6939e111899d76
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155061635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a97697aa23f24fc57efab234b9550dcd9ba538bf56ab64ed516f8575b6cec8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:37:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 13 Oct 2023 04:38:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:54:13 GMT
ENV ROS_DISTRO=rolling
# Fri, 13 Oct 2023 04:54:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:54:53 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 13 Oct 2023 04:54:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:54:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff18d61171fb1a17fb0edecb7a0600d4d0be1c103726f9d60cfb59071d3eccf9`  
		Last Modified: Fri, 13 Oct 2023 05:00:30 GMT  
		Size: 1.2 MB (1214464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa41e452048780b8d89bde1b448e5c130e073ab26d8a3c3e2ec3d4a4170f55f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 3.8 MB (3801906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c55f0e8967a89d129c1106434dacd41bd9239f7fe793b4dc37245f7a26762f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023f71811e459a590f4b10edecae765c4b654f7139277e4c704f11126c720c5f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76919e69d9bf2e3d2ca8ae0d65ff46ad78ea4ad6cb40564909d2ab3ca2cb1dd`  
		Last Modified: Fri, 13 Oct 2023 05:05:47 GMT  
		Size: 121.7 MB (121650914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78ad5922e8a4b2b9b64791f4eb98c6ce309e5d8ff2ff1a652ce79787364cf87`  
		Last Modified: Fri, 13 Oct 2023 05:05:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core-jammy`

```console
$ docker pull ros@sha256:1a1da3f393a7e216a6a27b701122d0fc81852467d9515f323077170000434a2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:82e943d3795de3208b880176e44ef3c1fe938e2a645cd4324cee9176e37a63ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159674366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1a375fa361d6d2dbb1b8150b27a0610a6a3683ebdc6d364167c63b1671cc34`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:09:00 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:06 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:09:07 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 03 Oct 2023 06:09:08 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 06:09:08 GMT
ENV LC_ALL=C.UTF-8
# Tue, 03 Oct 2023 06:33:13 GMT
ENV ROS_DISTRO=rolling
# Tue, 03 Oct 2023 06:33:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:33:59 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 03 Oct 2023 06:34:00 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 03 Oct 2023 06:34:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1370ba32049345dce3665687ae8209d03dc6e8d9d44e99e46c0ceb62f9f1f30d`  
		Last Modified: Tue, 03 Oct 2023 06:37:13 GMT  
		Size: 1.2 MB (1213056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c1e1f3dd2585388cc558f6237ee492769081f489b65cd386188d8efb6cdce6`  
		Last Modified: Tue, 03 Oct 2023 06:37:12 GMT  
		Size: 3.8 MB (3828981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198e4b86b803705bfcbea4adc86401d2d0cd4af88199c9e706cf0803b5be7842`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa2d310e00acb45665d82263e8800579055fb2ea11b71dd4926c8a7323855af7`  
		Last Modified: Tue, 03 Oct 2023 06:37:11 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b293927275b81c0d4e6656435654ec293113bba612b31ca59e3aa388e1135f95`  
		Last Modified: Tue, 03 Oct 2023 06:42:33 GMT  
		Size: 124.2 MB (124189046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223180173aa5341b495187f6e300564465cda4640e1b148b6ca8ed0cc899c68e`  
		Last Modified: Tue, 03 Oct 2023 06:42:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:ab2505deb5f42c48cb360b80157d2be11857c4382a68dd09bc6939e111899d76
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155061635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a97697aa23f24fc57efab234b9550dcd9ba538bf56ab64ed516f8575b6cec8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 04:37:54 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:38:05 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 13 Oct 2023 04:38:06 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LANG=C.UTF-8
# Fri, 13 Oct 2023 04:38:06 GMT
ENV LC_ALL=C.UTF-8
# Fri, 13 Oct 2023 04:54:13 GMT
ENV ROS_DISTRO=rolling
# Fri, 13 Oct 2023 04:54:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 13 Oct 2023 04:54:53 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 13 Oct 2023 04:54:53 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 13 Oct 2023 04:54:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff18d61171fb1a17fb0edecb7a0600d4d0be1c103726f9d60cfb59071d3eccf9`  
		Last Modified: Fri, 13 Oct 2023 05:00:30 GMT  
		Size: 1.2 MB (1214464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa41e452048780b8d89bde1b448e5c130e073ab26d8a3c3e2ec3d4a4170f55f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 3.8 MB (3801906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c55f0e8967a89d129c1106434dacd41bd9239f7fe793b4dc37245f7a26762f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023f71811e459a590f4b10edecae765c4b654f7139277e4c704f11126c720c5f`  
		Last Modified: Fri, 13 Oct 2023 05:00:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76919e69d9bf2e3d2ca8ae0d65ff46ad78ea4ad6cb40564909d2ab3ca2cb1dd`  
		Last Modified: Fri, 13 Oct 2023 05:05:47 GMT  
		Size: 121.7 MB (121650914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78ad5922e8a4b2b9b64791f4eb98c6ce309e5d8ff2ff1a652ce79787364cf87`  
		Last Modified: Fri, 13 Oct 2023 05:05:23 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

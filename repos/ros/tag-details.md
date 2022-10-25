<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `ros`

-	[`ros:foxy`](#rosfoxy)
-	[`ros:foxy-ros-base`](#rosfoxy-ros-base)
-	[`ros:foxy-ros-base-focal`](#rosfoxy-ros-base-focal)
-	[`ros:foxy-ros-core`](#rosfoxy-ros-core)
-	[`ros:foxy-ros-core-focal`](#rosfoxy-ros-core-focal)
-	[`ros:foxy-ros1-bridge`](#rosfoxy-ros1-bridge)
-	[`ros:foxy-ros1-bridge-focal`](#rosfoxy-ros1-bridge-focal)
-	[`ros:galactic`](#rosgalactic)
-	[`ros:galactic-ros-base`](#rosgalactic-ros-base)
-	[`ros:galactic-ros-base-focal`](#rosgalactic-ros-base-focal)
-	[`ros:galactic-ros-core`](#rosgalactic-ros-core)
-	[`ros:galactic-ros-core-focal`](#rosgalactic-ros-core-focal)
-	[`ros:galactic-ros1-bridge`](#rosgalactic-ros1-bridge)
-	[`ros:galactic-ros1-bridge-focal`](#rosgalactic-ros1-bridge-focal)
-	[`ros:humble`](#roshumble)
-	[`ros:humble-perception`](#roshumble-perception)
-	[`ros:humble-perception-jammy`](#roshumble-perception-jammy)
-	[`ros:humble-ros-base`](#roshumble-ros-base)
-	[`ros:humble-ros-base-jammy`](#roshumble-ros-base-jammy)
-	[`ros:humble-ros-core`](#roshumble-ros-core)
-	[`ros:humble-ros-core-jammy`](#roshumble-ros-core-jammy)
-	[`ros:latest`](#roslatest)
-	[`ros:melodic`](#rosmelodic)
-	[`ros:melodic-perception`](#rosmelodic-perception)
-	[`ros:melodic-perception-bionic`](#rosmelodic-perception-bionic)
-	[`ros:melodic-robot`](#rosmelodic-robot)
-	[`ros:melodic-robot-bionic`](#rosmelodic-robot-bionic)
-	[`ros:melodic-ros-base`](#rosmelodic-ros-base)
-	[`ros:melodic-ros-base-bionic`](#rosmelodic-ros-base-bionic)
-	[`ros:melodic-ros-core`](#rosmelodic-ros-core)
-	[`ros:melodic-ros-core-bionic`](#rosmelodic-ros-core-bionic)
-	[`ros:noetic`](#rosnoetic)
-	[`ros:noetic-perception`](#rosnoetic-perception)
-	[`ros:noetic-perception-buster`](#rosnoetic-perception-buster)
-	[`ros:noetic-perception-focal`](#rosnoetic-perception-focal)
-	[`ros:noetic-robot`](#rosnoetic-robot)
-	[`ros:noetic-robot-buster`](#rosnoetic-robot-buster)
-	[`ros:noetic-robot-focal`](#rosnoetic-robot-focal)
-	[`ros:noetic-ros-base`](#rosnoetic-ros-base)
-	[`ros:noetic-ros-base-buster`](#rosnoetic-ros-base-buster)
-	[`ros:noetic-ros-base-focal`](#rosnoetic-ros-base-focal)
-	[`ros:noetic-ros-core`](#rosnoetic-ros-core)
-	[`ros:noetic-ros-core-buster`](#rosnoetic-ros-core-buster)
-	[`ros:noetic-ros-core-focal`](#rosnoetic-ros-core-focal)
-	[`ros:rolling`](#rosrolling)
-	[`ros:rolling-perception`](#rosrolling-perception)
-	[`ros:rolling-perception-jammy`](#rosrolling-perception-jammy)
-	[`ros:rolling-ros-base`](#rosrolling-ros-base)
-	[`ros:rolling-ros-base-jammy`](#rosrolling-ros-base-jammy)
-	[`ros:rolling-ros-core`](#rosrolling-ros-core)
-	[`ros:rolling-ros-core-jammy`](#rosrolling-ros-core-jammy)

## `ros:foxy`

```console
$ docker pull ros@sha256:5693e05d0adddaa5ea05b76564cddf000acc88019778663695c5247e8ba694d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy` - linux; amd64

```console
$ docker pull ros@sha256:2a2cb6ec4fa94c8405549a3ba868f1be8e7cc9ba3530bf9909f1d7517fc33acd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 MB (250910730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79dc804c68414a56e2bc462fd1705c10a1815d04042c72e88ced0971e695f5b8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV ROS_DISTRO=foxy
# Tue, 25 Oct 2022 07:26:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:26:27 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:26:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:26:27 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:27:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:27:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:27:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:28:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122af75c69e965a1d4b50e964ea95ec60ddd9997347536d0e79ecf1dc96f8e4d`  
		Last Modified: Tue, 25 Oct 2022 07:59:22 GMT  
		Size: 120.4 MB (120353945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fb29cc59034ebd9df4a3ddc0a423888144631e3a1e4b4cffff2ce4396d52ed`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5fb36af82e519ef989f9d9107e767f04c18c153572130e0f6c3a343ebb0ce0`  
		Last Modified: Tue, 25 Oct 2022 07:59:43 GMT  
		Size: 73.3 MB (73325743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837655cef3c4cc06788fbad7c6df8a77081a39d3392b8bafed1ea74c35a302e3`  
		Last Modified: Tue, 25 Oct 2022 07:59:32 GMT  
		Size: 269.4 KB (269364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb41d05e0bd11afe16ecfcf7ef668e3908835201cc94fa813d0bf7783c3ba24f`  
		Last Modified: Tue, 25 Oct 2022 07:59:31 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0f073c138f041e9b85ff0ddae19609c388a359370280ec72e5d549f73206c8`  
		Last Modified: Tue, 25 Oct 2022 07:59:35 GMT  
		Size: 21.7 MB (21663794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:70f4a3bc45e257fba41f608f2f06358381f46476287c05ebd2acbc6a9e42d658
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226394124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cbcd1b77d057daa39433a40f5ee770ec42c38f88e2df4979685b4613fabcfc2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:48:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:48:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:48:53 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:48:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:48:55 GMT
ENV ROS_DISTRO=foxy
# Wed, 05 Oct 2022 13:49:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:49:45 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 13:49:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:49:46 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:50:13 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:50:18 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:50:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 13:50:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2066945f278504a3fbe15500f54112556cb9e9febb0b4d07edd644ecbae9209c`  
		Last Modified: Wed, 05 Oct 2022 14:09:02 GMT  
		Size: 1.2 MB (1164049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ca1624225b52b4e52d61f82b52ba0653fdefd1bcde8f1017fc0031f256a5d`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 5.3 MB (5322416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe2304592d4de6867917f39d4e63cc411cb662d76bc30f54ac6c390d02e993`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a824a2931c1c7d4e723b854a254a721dbaaa0d525baef8fc9bffdaa2beacd42`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761c65c3947a6f0c271454a1a4196e78bc089909ef0635e4fb722f0d26058386`  
		Last Modified: Wed, 05 Oct 2022 14:14:18 GMT  
		Size: 104.6 MB (104627758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63d57dc14ffab1724d55720e415410361be4700ed6ecc13df5afc8d58b22afd`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b933fcbe46312ae813f092369a156c253b1e52cb3a43298b9a4fdbee1eb6fa6b`  
		Last Modified: Wed, 05 Oct 2022 14:14:40 GMT  
		Size: 67.4 MB (67449275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d7c2e640d21fee0497f12b54a0f888d39799eb93389888e1da33e797737919`  
		Last Modified: Wed, 05 Oct 2022 14:14:30 GMT  
		Size: 267.3 KB (267323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e2d4224582edb4e076612a46599ad24ba3ccfc164b2d512b2006c21094a621`  
		Last Modified: Wed, 05 Oct 2022 14:14:30 GMT  
		Size: 2.4 KB (2400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81d9c31822b3bf7270af1ce9bc509a7516e60401dcfc80333756e3f62d45364`  
		Last Modified: Wed, 05 Oct 2022 14:14:33 GMT  
		Size: 20.4 MB (20366915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-base`

```console
$ docker pull ros@sha256:5693e05d0adddaa5ea05b76564cddf000acc88019778663695c5247e8ba694d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:2a2cb6ec4fa94c8405549a3ba868f1be8e7cc9ba3530bf9909f1d7517fc33acd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 MB (250910730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79dc804c68414a56e2bc462fd1705c10a1815d04042c72e88ced0971e695f5b8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV ROS_DISTRO=foxy
# Tue, 25 Oct 2022 07:26:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:26:27 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:26:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:26:27 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:27:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:27:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:27:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:28:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122af75c69e965a1d4b50e964ea95ec60ddd9997347536d0e79ecf1dc96f8e4d`  
		Last Modified: Tue, 25 Oct 2022 07:59:22 GMT  
		Size: 120.4 MB (120353945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fb29cc59034ebd9df4a3ddc0a423888144631e3a1e4b4cffff2ce4396d52ed`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5fb36af82e519ef989f9d9107e767f04c18c153572130e0f6c3a343ebb0ce0`  
		Last Modified: Tue, 25 Oct 2022 07:59:43 GMT  
		Size: 73.3 MB (73325743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837655cef3c4cc06788fbad7c6df8a77081a39d3392b8bafed1ea74c35a302e3`  
		Last Modified: Tue, 25 Oct 2022 07:59:32 GMT  
		Size: 269.4 KB (269364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb41d05e0bd11afe16ecfcf7ef668e3908835201cc94fa813d0bf7783c3ba24f`  
		Last Modified: Tue, 25 Oct 2022 07:59:31 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0f073c138f041e9b85ff0ddae19609c388a359370280ec72e5d549f73206c8`  
		Last Modified: Tue, 25 Oct 2022 07:59:35 GMT  
		Size: 21.7 MB (21663794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:70f4a3bc45e257fba41f608f2f06358381f46476287c05ebd2acbc6a9e42d658
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226394124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cbcd1b77d057daa39433a40f5ee770ec42c38f88e2df4979685b4613fabcfc2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:48:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:48:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:48:53 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:48:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:48:55 GMT
ENV ROS_DISTRO=foxy
# Wed, 05 Oct 2022 13:49:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:49:45 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 13:49:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:49:46 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:50:13 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:50:18 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:50:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 13:50:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2066945f278504a3fbe15500f54112556cb9e9febb0b4d07edd644ecbae9209c`  
		Last Modified: Wed, 05 Oct 2022 14:09:02 GMT  
		Size: 1.2 MB (1164049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ca1624225b52b4e52d61f82b52ba0653fdefd1bcde8f1017fc0031f256a5d`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 5.3 MB (5322416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe2304592d4de6867917f39d4e63cc411cb662d76bc30f54ac6c390d02e993`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a824a2931c1c7d4e723b854a254a721dbaaa0d525baef8fc9bffdaa2beacd42`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761c65c3947a6f0c271454a1a4196e78bc089909ef0635e4fb722f0d26058386`  
		Last Modified: Wed, 05 Oct 2022 14:14:18 GMT  
		Size: 104.6 MB (104627758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63d57dc14ffab1724d55720e415410361be4700ed6ecc13df5afc8d58b22afd`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b933fcbe46312ae813f092369a156c253b1e52cb3a43298b9a4fdbee1eb6fa6b`  
		Last Modified: Wed, 05 Oct 2022 14:14:40 GMT  
		Size: 67.4 MB (67449275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d7c2e640d21fee0497f12b54a0f888d39799eb93389888e1da33e797737919`  
		Last Modified: Wed, 05 Oct 2022 14:14:30 GMT  
		Size: 267.3 KB (267323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e2d4224582edb4e076612a46599ad24ba3ccfc164b2d512b2006c21094a621`  
		Last Modified: Wed, 05 Oct 2022 14:14:30 GMT  
		Size: 2.4 KB (2400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81d9c31822b3bf7270af1ce9bc509a7516e60401dcfc80333756e3f62d45364`  
		Last Modified: Wed, 05 Oct 2022 14:14:33 GMT  
		Size: 20.4 MB (20366915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-base-focal`

```console
$ docker pull ros@sha256:5693e05d0adddaa5ea05b76564cddf000acc88019778663695c5247e8ba694d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:2a2cb6ec4fa94c8405549a3ba868f1be8e7cc9ba3530bf9909f1d7517fc33acd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 MB (250910730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79dc804c68414a56e2bc462fd1705c10a1815d04042c72e88ced0971e695f5b8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV ROS_DISTRO=foxy
# Tue, 25 Oct 2022 07:26:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:26:27 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:26:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:26:27 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:27:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:27:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:27:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:28:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122af75c69e965a1d4b50e964ea95ec60ddd9997347536d0e79ecf1dc96f8e4d`  
		Last Modified: Tue, 25 Oct 2022 07:59:22 GMT  
		Size: 120.4 MB (120353945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fb29cc59034ebd9df4a3ddc0a423888144631e3a1e4b4cffff2ce4396d52ed`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5fb36af82e519ef989f9d9107e767f04c18c153572130e0f6c3a343ebb0ce0`  
		Last Modified: Tue, 25 Oct 2022 07:59:43 GMT  
		Size: 73.3 MB (73325743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837655cef3c4cc06788fbad7c6df8a77081a39d3392b8bafed1ea74c35a302e3`  
		Last Modified: Tue, 25 Oct 2022 07:59:32 GMT  
		Size: 269.4 KB (269364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb41d05e0bd11afe16ecfcf7ef668e3908835201cc94fa813d0bf7783c3ba24f`  
		Last Modified: Tue, 25 Oct 2022 07:59:31 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0f073c138f041e9b85ff0ddae19609c388a359370280ec72e5d549f73206c8`  
		Last Modified: Tue, 25 Oct 2022 07:59:35 GMT  
		Size: 21.7 MB (21663794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:70f4a3bc45e257fba41f608f2f06358381f46476287c05ebd2acbc6a9e42d658
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226394124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cbcd1b77d057daa39433a40f5ee770ec42c38f88e2df4979685b4613fabcfc2`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:48:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:48:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:48:53 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:48:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:48:55 GMT
ENV ROS_DISTRO=foxy
# Wed, 05 Oct 2022 13:49:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:49:45 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 13:49:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:49:46 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:50:13 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:50:18 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:50:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 13:50:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2066945f278504a3fbe15500f54112556cb9e9febb0b4d07edd644ecbae9209c`  
		Last Modified: Wed, 05 Oct 2022 14:09:02 GMT  
		Size: 1.2 MB (1164049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ca1624225b52b4e52d61f82b52ba0653fdefd1bcde8f1017fc0031f256a5d`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 5.3 MB (5322416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe2304592d4de6867917f39d4e63cc411cb662d76bc30f54ac6c390d02e993`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a824a2931c1c7d4e723b854a254a721dbaaa0d525baef8fc9bffdaa2beacd42`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761c65c3947a6f0c271454a1a4196e78bc089909ef0635e4fb722f0d26058386`  
		Last Modified: Wed, 05 Oct 2022 14:14:18 GMT  
		Size: 104.6 MB (104627758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63d57dc14ffab1724d55720e415410361be4700ed6ecc13df5afc8d58b22afd`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b933fcbe46312ae813f092369a156c253b1e52cb3a43298b9a4fdbee1eb6fa6b`  
		Last Modified: Wed, 05 Oct 2022 14:14:40 GMT  
		Size: 67.4 MB (67449275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d7c2e640d21fee0497f12b54a0f888d39799eb93389888e1da33e797737919`  
		Last Modified: Wed, 05 Oct 2022 14:14:30 GMT  
		Size: 267.3 KB (267323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e2d4224582edb4e076612a46599ad24ba3ccfc164b2d512b2006c21094a621`  
		Last Modified: Wed, 05 Oct 2022 14:14:30 GMT  
		Size: 2.4 KB (2400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81d9c31822b3bf7270af1ce9bc509a7516e60401dcfc80333756e3f62d45364`  
		Last Modified: Wed, 05 Oct 2022 14:14:33 GMT  
		Size: 20.4 MB (20366915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-core`

```console
$ docker pull ros@sha256:3076541907e3a68ab2df53ada23f2d3e415e285faa2cf9280e099c27ea6737a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:87d8f4e045ca908ea1e9fc36cd58992b068c2243cd417af51df28015cae361c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155649379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f133e19ba781eb57466f334011e632c7258cb020aa4bd3f02210dc2724fc2f68`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV ROS_DISTRO=foxy
# Tue, 25 Oct 2022 07:26:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:26:27 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:26:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:26:27 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122af75c69e965a1d4b50e964ea95ec60ddd9997347536d0e79ecf1dc96f8e4d`  
		Last Modified: Tue, 25 Oct 2022 07:59:22 GMT  
		Size: 120.4 MB (120353945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fb29cc59034ebd9df4a3ddc0a423888144631e3a1e4b4cffff2ce4396d52ed`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:52ee321733098fccaaf6a0618e45b7dc52f08ce058fb8349984592e05de6bf38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138308211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9bc639ef7ce7d698d0dce478a9a4828085c53c24246570ed03bd3b8871dc0b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:48:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:48:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:48:53 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:48:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:48:55 GMT
ENV ROS_DISTRO=foxy
# Wed, 05 Oct 2022 13:49:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:49:45 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 13:49:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:49:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2066945f278504a3fbe15500f54112556cb9e9febb0b4d07edd644ecbae9209c`  
		Last Modified: Wed, 05 Oct 2022 14:09:02 GMT  
		Size: 1.2 MB (1164049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ca1624225b52b4e52d61f82b52ba0653fdefd1bcde8f1017fc0031f256a5d`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 5.3 MB (5322416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe2304592d4de6867917f39d4e63cc411cb662d76bc30f54ac6c390d02e993`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a824a2931c1c7d4e723b854a254a721dbaaa0d525baef8fc9bffdaa2beacd42`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761c65c3947a6f0c271454a1a4196e78bc089909ef0635e4fb722f0d26058386`  
		Last Modified: Wed, 05 Oct 2022 14:14:18 GMT  
		Size: 104.6 MB (104627758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63d57dc14ffab1724d55720e415410361be4700ed6ecc13df5afc8d58b22afd`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-core-focal`

```console
$ docker pull ros@sha256:3076541907e3a68ab2df53ada23f2d3e415e285faa2cf9280e099c27ea6737a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:87d8f4e045ca908ea1e9fc36cd58992b068c2243cd417af51df28015cae361c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155649379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f133e19ba781eb57466f334011e632c7258cb020aa4bd3f02210dc2724fc2f68`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV ROS_DISTRO=foxy
# Tue, 25 Oct 2022 07:26:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:26:27 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:26:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:26:27 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122af75c69e965a1d4b50e964ea95ec60ddd9997347536d0e79ecf1dc96f8e4d`  
		Last Modified: Tue, 25 Oct 2022 07:59:22 GMT  
		Size: 120.4 MB (120353945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fb29cc59034ebd9df4a3ddc0a423888144631e3a1e4b4cffff2ce4396d52ed`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:52ee321733098fccaaf6a0618e45b7dc52f08ce058fb8349984592e05de6bf38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138308211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d9bc639ef7ce7d698d0dce478a9a4828085c53c24246570ed03bd3b8871dc0b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:48:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:48:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:48:53 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:48:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:48:55 GMT
ENV ROS_DISTRO=foxy
# Wed, 05 Oct 2022 13:49:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:49:45 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 13:49:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:49:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2066945f278504a3fbe15500f54112556cb9e9febb0b4d07edd644ecbae9209c`  
		Last Modified: Wed, 05 Oct 2022 14:09:02 GMT  
		Size: 1.2 MB (1164049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ca1624225b52b4e52d61f82b52ba0653fdefd1bcde8f1017fc0031f256a5d`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 5.3 MB (5322416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe2304592d4de6867917f39d4e63cc411cb662d76bc30f54ac6c390d02e993`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a824a2931c1c7d4e723b854a254a721dbaaa0d525baef8fc9bffdaa2beacd42`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761c65c3947a6f0c271454a1a4196e78bc089909ef0635e4fb722f0d26058386`  
		Last Modified: Wed, 05 Oct 2022 14:14:18 GMT  
		Size: 104.6 MB (104627758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63d57dc14ffab1724d55720e415410361be4700ed6ecc13df5afc8d58b22afd`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros1-bridge`

```console
$ docker pull ros@sha256:0a804acec405cff4ddedd05a389e499e59be0c7691f9125570006be134b1ba38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:a5a14cf96a615b81a6a77674968ec07922a7104e7df9f40fa9f9cc33a9e0a915
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (349017846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a30f6376fb966081fc8055995c025832ef196fa1baac2115c933459278beae`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV ROS_DISTRO=foxy
# Tue, 25 Oct 2022 07:26:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:26:27 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:26:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:26:27 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:27:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:27:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:27:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:28:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:28:11 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:28:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:28:12 GMT
ENV ROS1_DISTRO=noetic
# Tue, 25 Oct 2022 07:28:13 GMT
ENV ROS2_DISTRO=foxy
# Tue, 25 Oct 2022 07:29:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:29:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.4-1*     ros-foxy-demo-nodes-py=0.9.4-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:29:38 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122af75c69e965a1d4b50e964ea95ec60ddd9997347536d0e79ecf1dc96f8e4d`  
		Last Modified: Tue, 25 Oct 2022 07:59:22 GMT  
		Size: 120.4 MB (120353945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fb29cc59034ebd9df4a3ddc0a423888144631e3a1e4b4cffff2ce4396d52ed`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5fb36af82e519ef989f9d9107e767f04c18c153572130e0f6c3a343ebb0ce0`  
		Last Modified: Tue, 25 Oct 2022 07:59:43 GMT  
		Size: 73.3 MB (73325743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837655cef3c4cc06788fbad7c6df8a77081a39d3392b8bafed1ea74c35a302e3`  
		Last Modified: Tue, 25 Oct 2022 07:59:32 GMT  
		Size: 269.4 KB (269364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb41d05e0bd11afe16ecfcf7ef668e3908835201cc94fa813d0bf7783c3ba24f`  
		Last Modified: Tue, 25 Oct 2022 07:59:31 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0f073c138f041e9b85ff0ddae19609c388a359370280ec72e5d549f73206c8`  
		Last Modified: Tue, 25 Oct 2022 07:59:35 GMT  
		Size: 21.7 MB (21663794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b18f13baebbb1e3f7ffc35466142e70d5913b88c27a49f5e5dbb9eab829e68e`  
		Last Modified: Tue, 25 Oct 2022 07:59:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff282c273773346a09f274c19f2310cf509f62c59ff80bf3c1831cb16577d048`  
		Last Modified: Tue, 25 Oct 2022 07:59:55 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084feb2aa93fcf8c7e68b0013adaf1d13ea903cabbc95d109fdc87c981859bb3`  
		Last Modified: Tue, 25 Oct 2022 08:00:15 GMT  
		Size: 76.4 MB (76434548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cadfac8cbf4b04e9e6ae0d30ae6985b445e23b413674c326c68a9a8688d00ee`  
		Last Modified: Tue, 25 Oct 2022 08:00:02 GMT  
		Size: 21.7 MB (21671942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4d8f780e2f7a944a9cbf79dd4545e29a7068cc6da18d290768c7a2c7a5dc59`  
		Last Modified: Tue, 25 Oct 2022 07:59:55 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9ff7fc96b5af30a5599b70993ddb7041334f53323b4ca7640b57ff9e1e68c4a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.8 MB (316765174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbacdad4c164be3b4c8a143c155c989069e4828ffb5b6bde2b18b7349c7c079b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:48:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:48:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:48:53 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:48:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:48:55 GMT
ENV ROS_DISTRO=foxy
# Wed, 05 Oct 2022 13:49:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:49:45 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 13:49:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:49:46 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:50:13 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:50:18 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:50:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 13:50:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:50:54 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:50:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:50:57 GMT
ENV ROS1_DISTRO=noetic
# Wed, 05 Oct 2022 13:50:59 GMT
ENV ROS2_DISTRO=foxy
# Wed, 05 Oct 2022 13:51:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:51:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.4-1*     ros-foxy-demo-nodes-py=0.9.4-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:51:45 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2066945f278504a3fbe15500f54112556cb9e9febb0b4d07edd644ecbae9209c`  
		Last Modified: Wed, 05 Oct 2022 14:09:02 GMT  
		Size: 1.2 MB (1164049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ca1624225b52b4e52d61f82b52ba0653fdefd1bcde8f1017fc0031f256a5d`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 5.3 MB (5322416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe2304592d4de6867917f39d4e63cc411cb662d76bc30f54ac6c390d02e993`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a824a2931c1c7d4e723b854a254a721dbaaa0d525baef8fc9bffdaa2beacd42`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761c65c3947a6f0c271454a1a4196e78bc089909ef0635e4fb722f0d26058386`  
		Last Modified: Wed, 05 Oct 2022 14:14:18 GMT  
		Size: 104.6 MB (104627758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63d57dc14ffab1724d55720e415410361be4700ed6ecc13df5afc8d58b22afd`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b933fcbe46312ae813f092369a156c253b1e52cb3a43298b9a4fdbee1eb6fa6b`  
		Last Modified: Wed, 05 Oct 2022 14:14:40 GMT  
		Size: 67.4 MB (67449275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d7c2e640d21fee0497f12b54a0f888d39799eb93389888e1da33e797737919`  
		Last Modified: Wed, 05 Oct 2022 14:14:30 GMT  
		Size: 267.3 KB (267323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e2d4224582edb4e076612a46599ad24ba3ccfc164b2d512b2006c21094a621`  
		Last Modified: Wed, 05 Oct 2022 14:14:30 GMT  
		Size: 2.4 KB (2400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81d9c31822b3bf7270af1ce9bc509a7516e60401dcfc80333756e3f62d45364`  
		Last Modified: Wed, 05 Oct 2022 14:14:33 GMT  
		Size: 20.4 MB (20366915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2f2c8f261aabc480326a91bee38a862a180cfdd89bb015b9d655b99993403e`  
		Last Modified: Wed, 05 Oct 2022 14:14:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3614d3bded093673281f432c55f0f746dbe555a0849f2c657164b0dd0a2725`  
		Last Modified: Wed, 05 Oct 2022 14:15:10 GMT  
		Size: 76.3 MB (76271820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301707bbed02236a81c065964e76a9676c5058644e3974e8e8970beeb8e4d4f0`  
		Last Modified: Wed, 05 Oct 2022 14:14:58 GMT  
		Size: 14.1 MB (14098760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3769ba38f03d3d37fa954731a02f330fbfd4cf12cbd6179196026f9909fe85cc`  
		Last Modified: Wed, 05 Oct 2022 14:14:55 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros1-bridge-focal`

```console
$ docker pull ros@sha256:0a804acec405cff4ddedd05a389e499e59be0c7691f9125570006be134b1ba38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:a5a14cf96a615b81a6a77674968ec07922a7104e7df9f40fa9f9cc33a9e0a915
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (349017846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a30f6376fb966081fc8055995c025832ef196fa1baac2115c933459278beae`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV ROS_DISTRO=foxy
# Tue, 25 Oct 2022 07:26:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:26:27 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:26:27 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:26:27 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:27:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:27:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:27:25 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:28:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:28:11 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:28:12 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:28:12 GMT
ENV ROS1_DISTRO=noetic
# Tue, 25 Oct 2022 07:28:13 GMT
ENV ROS2_DISTRO=foxy
# Tue, 25 Oct 2022 07:29:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:29:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.4-1*     ros-foxy-demo-nodes-py=0.9.4-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:29:38 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122af75c69e965a1d4b50e964ea95ec60ddd9997347536d0e79ecf1dc96f8e4d`  
		Last Modified: Tue, 25 Oct 2022 07:59:22 GMT  
		Size: 120.4 MB (120353945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1fb29cc59034ebd9df4a3ddc0a423888144631e3a1e4b4cffff2ce4396d52ed`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5fb36af82e519ef989f9d9107e767f04c18c153572130e0f6c3a343ebb0ce0`  
		Last Modified: Tue, 25 Oct 2022 07:59:43 GMT  
		Size: 73.3 MB (73325743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:837655cef3c4cc06788fbad7c6df8a77081a39d3392b8bafed1ea74c35a302e3`  
		Last Modified: Tue, 25 Oct 2022 07:59:32 GMT  
		Size: 269.4 KB (269364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb41d05e0bd11afe16ecfcf7ef668e3908835201cc94fa813d0bf7783c3ba24f`  
		Last Modified: Tue, 25 Oct 2022 07:59:31 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0f073c138f041e9b85ff0ddae19609c388a359370280ec72e5d549f73206c8`  
		Last Modified: Tue, 25 Oct 2022 07:59:35 GMT  
		Size: 21.7 MB (21663794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b18f13baebbb1e3f7ffc35466142e70d5913b88c27a49f5e5dbb9eab829e68e`  
		Last Modified: Tue, 25 Oct 2022 07:59:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff282c273773346a09f274c19f2310cf509f62c59ff80bf3c1831cb16577d048`  
		Last Modified: Tue, 25 Oct 2022 07:59:55 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084feb2aa93fcf8c7e68b0013adaf1d13ea903cabbc95d109fdc87c981859bb3`  
		Last Modified: Tue, 25 Oct 2022 08:00:15 GMT  
		Size: 76.4 MB (76434548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cadfac8cbf4b04e9e6ae0d30ae6985b445e23b413674c326c68a9a8688d00ee`  
		Last Modified: Tue, 25 Oct 2022 08:00:02 GMT  
		Size: 21.7 MB (21671942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4d8f780e2f7a944a9cbf79dd4545e29a7068cc6da18d290768c7a2c7a5dc59`  
		Last Modified: Tue, 25 Oct 2022 07:59:55 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9ff7fc96b5af30a5599b70993ddb7041334f53323b4ca7640b57ff9e1e68c4a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.8 MB (316765174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbacdad4c164be3b4c8a143c155c989069e4828ffb5b6bde2b18b7349c7c079b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:48:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:48:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:48:53 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:48:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:48:55 GMT
ENV ROS_DISTRO=foxy
# Wed, 05 Oct 2022 13:49:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:49:45 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 13:49:45 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:49:46 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:50:13 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:50:18 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:50:24 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 13:50:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:50:54 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:50:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:50:57 GMT
ENV ROS1_DISTRO=noetic
# Wed, 05 Oct 2022 13:50:59 GMT
ENV ROS2_DISTRO=foxy
# Wed, 05 Oct 2022 13:51:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:51:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.4-1*     ros-foxy-demo-nodes-py=0.9.4-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:51:45 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2066945f278504a3fbe15500f54112556cb9e9febb0b4d07edd644ecbae9209c`  
		Last Modified: Wed, 05 Oct 2022 14:09:02 GMT  
		Size: 1.2 MB (1164049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ca1624225b52b4e52d61f82b52ba0653fdefd1bcde8f1017fc0031f256a5d`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 5.3 MB (5322416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe2304592d4de6867917f39d4e63cc411cb662d76bc30f54ac6c390d02e993`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a824a2931c1c7d4e723b854a254a721dbaaa0d525baef8fc9bffdaa2beacd42`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761c65c3947a6f0c271454a1a4196e78bc089909ef0635e4fb722f0d26058386`  
		Last Modified: Wed, 05 Oct 2022 14:14:18 GMT  
		Size: 104.6 MB (104627758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63d57dc14ffab1724d55720e415410361be4700ed6ecc13df5afc8d58b22afd`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b933fcbe46312ae813f092369a156c253b1e52cb3a43298b9a4fdbee1eb6fa6b`  
		Last Modified: Wed, 05 Oct 2022 14:14:40 GMT  
		Size: 67.4 MB (67449275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d7c2e640d21fee0497f12b54a0f888d39799eb93389888e1da33e797737919`  
		Last Modified: Wed, 05 Oct 2022 14:14:30 GMT  
		Size: 267.3 KB (267323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e2d4224582edb4e076612a46599ad24ba3ccfc164b2d512b2006c21094a621`  
		Last Modified: Wed, 05 Oct 2022 14:14:30 GMT  
		Size: 2.4 KB (2400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81d9c31822b3bf7270af1ce9bc509a7516e60401dcfc80333756e3f62d45364`  
		Last Modified: Wed, 05 Oct 2022 14:14:33 GMT  
		Size: 20.4 MB (20366915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2f2c8f261aabc480326a91bee38a862a180cfdd89bb015b9d655b99993403e`  
		Last Modified: Wed, 05 Oct 2022 14:14:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3614d3bded093673281f432c55f0f746dbe555a0849f2c657164b0dd0a2725`  
		Last Modified: Wed, 05 Oct 2022 14:15:10 GMT  
		Size: 76.3 MB (76271820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301707bbed02236a81c065964e76a9676c5058644e3974e8e8970beeb8e4d4f0`  
		Last Modified: Wed, 05 Oct 2022 14:14:58 GMT  
		Size: 14.1 MB (14098760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3769ba38f03d3d37fa954731a02f330fbfd4cf12cbd6179196026f9909fe85cc`  
		Last Modified: Wed, 05 Oct 2022 14:14:55 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic`

```console
$ docker pull ros@sha256:06ecb5169858b8e1ee682d78ba772db6e76fa555105dc006de81e16c4d65fa51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic` - linux; amd64

```console
$ docker pull ros@sha256:569696e5621fad056b14672265a27fb12507999bba8a6d8dcf332d16e6a2dad1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234891739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da8c152231c267d0724f107b91d186a7da80f21ae25d40984d9b4ce79d3985f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:29:48 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 Oct 2022 07:30:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:30:35 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:30:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:30:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:31:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:31:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:31:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:31:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c34379670d69cf7211d3babcb41e5d7851c837e47be70bf7e93d4c243031e3`  
		Last Modified: Tue, 25 Oct 2022 08:00:51 GMT  
		Size: 103.9 MB (103894975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4200c5a3f7cd026b35c4c14ddd08ce81b9a8286688a9d195b89dd005dac72263`  
		Last Modified: Tue, 25 Oct 2022 08:00:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e7f5b5c701916838562eb61ea9d238d42ecdcf4603217d5f36de002d875373`  
		Last Modified: Tue, 25 Oct 2022 08:01:15 GMT  
		Size: 73.3 MB (73280543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066dfb5edf358837c3acdfe4765a62b10a0588d5ee88a202f18c6decb245a6c4`  
		Last Modified: Tue, 25 Oct 2022 08:01:01 GMT  
		Size: 279.6 KB (279618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81213e1334be0f25c6545b79677786f9e06c1aaea8a510b21195f4dc08b6ecac`  
		Last Modified: Tue, 25 Oct 2022 08:01:01 GMT  
		Size: 2.4 KB (2420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c4d1072c5bb0b70378dd5a649ff6468e2763e77a087f95fa4e934dfa18632e`  
		Last Modified: Tue, 25 Oct 2022 08:01:06 GMT  
		Size: 22.1 MB (22138749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9823d71d84a6facb9ad6ab94361c78eaafb082eedee10eb50d0fcf03e3196e40
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.2 MB (223197069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a96e112da177db105e7ab8a4629e2f05d7ebf4a0f23fba4094e15b8f76174cb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:48:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:48:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:48:53 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:48:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:51:53 GMT
ENV ROS_DISTRO=galactic
# Wed, 05 Oct 2022 13:52:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:52:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 13:52:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:52:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:53:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:53:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 13:53:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2066945f278504a3fbe15500f54112556cb9e9febb0b4d07edd644ecbae9209c`  
		Last Modified: Wed, 05 Oct 2022 14:09:02 GMT  
		Size: 1.2 MB (1164049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ca1624225b52b4e52d61f82b52ba0653fdefd1bcde8f1017fc0031f256a5d`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 5.3 MB (5322416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe2304592d4de6867917f39d4e63cc411cb662d76bc30f54ac6c390d02e993`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a824a2931c1c7d4e723b854a254a721dbaaa0d525baef8fc9bffdaa2beacd42`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8d16a1f7ff237a77f29323231038803c348a1a9f11afc6bb177737dfdcad1c`  
		Last Modified: Wed, 05 Oct 2022 14:15:38 GMT  
		Size: 100.4 MB (100375443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b03d420b9714c9f3dc15cd95ef79baf5b4457aa24c478be8fc2000236b33fc`  
		Last Modified: Wed, 05 Oct 2022 14:15:22 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a956f99c4721f7dc25bfe3b1c9c90ce2a2d8b0474b19e342030574fa077dbc98`  
		Last Modified: Wed, 05 Oct 2022 14:15:59 GMT  
		Size: 67.4 MB (67402819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1231122a3faa9e29e7dcfbc07429b9a375bde70cf77017ed38de61d4a42bb924`  
		Last Modified: Wed, 05 Oct 2022 14:15:50 GMT  
		Size: 277.8 KB (277756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5317376816f40e243dc89e1427d6106c53bd777b2ad592afdce65fa1301cdce8`  
		Last Modified: Wed, 05 Oct 2022 14:15:49 GMT  
		Size: 2.4 KB (2357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a90f00672da01678118f187b2830f6621555d9e05eddf1d8c10a2d25f967f2`  
		Last Modified: Wed, 05 Oct 2022 14:15:53 GMT  
		Size: 21.5 MB (21458239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-base`

```console
$ docker pull ros@sha256:06ecb5169858b8e1ee682d78ba772db6e76fa555105dc006de81e16c4d65fa51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:569696e5621fad056b14672265a27fb12507999bba8a6d8dcf332d16e6a2dad1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234891739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da8c152231c267d0724f107b91d186a7da80f21ae25d40984d9b4ce79d3985f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:29:48 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 Oct 2022 07:30:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:30:35 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:30:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:30:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:31:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:31:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:31:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:31:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c34379670d69cf7211d3babcb41e5d7851c837e47be70bf7e93d4c243031e3`  
		Last Modified: Tue, 25 Oct 2022 08:00:51 GMT  
		Size: 103.9 MB (103894975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4200c5a3f7cd026b35c4c14ddd08ce81b9a8286688a9d195b89dd005dac72263`  
		Last Modified: Tue, 25 Oct 2022 08:00:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e7f5b5c701916838562eb61ea9d238d42ecdcf4603217d5f36de002d875373`  
		Last Modified: Tue, 25 Oct 2022 08:01:15 GMT  
		Size: 73.3 MB (73280543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066dfb5edf358837c3acdfe4765a62b10a0588d5ee88a202f18c6decb245a6c4`  
		Last Modified: Tue, 25 Oct 2022 08:01:01 GMT  
		Size: 279.6 KB (279618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81213e1334be0f25c6545b79677786f9e06c1aaea8a510b21195f4dc08b6ecac`  
		Last Modified: Tue, 25 Oct 2022 08:01:01 GMT  
		Size: 2.4 KB (2420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c4d1072c5bb0b70378dd5a649ff6468e2763e77a087f95fa4e934dfa18632e`  
		Last Modified: Tue, 25 Oct 2022 08:01:06 GMT  
		Size: 22.1 MB (22138749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9823d71d84a6facb9ad6ab94361c78eaafb082eedee10eb50d0fcf03e3196e40
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.2 MB (223197069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a96e112da177db105e7ab8a4629e2f05d7ebf4a0f23fba4094e15b8f76174cb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:48:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:48:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:48:53 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:48:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:51:53 GMT
ENV ROS_DISTRO=galactic
# Wed, 05 Oct 2022 13:52:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:52:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 13:52:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:52:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:53:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:53:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 13:53:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2066945f278504a3fbe15500f54112556cb9e9febb0b4d07edd644ecbae9209c`  
		Last Modified: Wed, 05 Oct 2022 14:09:02 GMT  
		Size: 1.2 MB (1164049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ca1624225b52b4e52d61f82b52ba0653fdefd1bcde8f1017fc0031f256a5d`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 5.3 MB (5322416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe2304592d4de6867917f39d4e63cc411cb662d76bc30f54ac6c390d02e993`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a824a2931c1c7d4e723b854a254a721dbaaa0d525baef8fc9bffdaa2beacd42`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8d16a1f7ff237a77f29323231038803c348a1a9f11afc6bb177737dfdcad1c`  
		Last Modified: Wed, 05 Oct 2022 14:15:38 GMT  
		Size: 100.4 MB (100375443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b03d420b9714c9f3dc15cd95ef79baf5b4457aa24c478be8fc2000236b33fc`  
		Last Modified: Wed, 05 Oct 2022 14:15:22 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a956f99c4721f7dc25bfe3b1c9c90ce2a2d8b0474b19e342030574fa077dbc98`  
		Last Modified: Wed, 05 Oct 2022 14:15:59 GMT  
		Size: 67.4 MB (67402819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1231122a3faa9e29e7dcfbc07429b9a375bde70cf77017ed38de61d4a42bb924`  
		Last Modified: Wed, 05 Oct 2022 14:15:50 GMT  
		Size: 277.8 KB (277756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5317376816f40e243dc89e1427d6106c53bd777b2ad592afdce65fa1301cdce8`  
		Last Modified: Wed, 05 Oct 2022 14:15:49 GMT  
		Size: 2.4 KB (2357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a90f00672da01678118f187b2830f6621555d9e05eddf1d8c10a2d25f967f2`  
		Last Modified: Wed, 05 Oct 2022 14:15:53 GMT  
		Size: 21.5 MB (21458239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-base-focal`

```console
$ docker pull ros@sha256:06ecb5169858b8e1ee682d78ba772db6e76fa555105dc006de81e16c4d65fa51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:569696e5621fad056b14672265a27fb12507999bba8a6d8dcf332d16e6a2dad1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234891739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da8c152231c267d0724f107b91d186a7da80f21ae25d40984d9b4ce79d3985f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:29:48 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 Oct 2022 07:30:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:30:35 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:30:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:30:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:31:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:31:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:31:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:31:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c34379670d69cf7211d3babcb41e5d7851c837e47be70bf7e93d4c243031e3`  
		Last Modified: Tue, 25 Oct 2022 08:00:51 GMT  
		Size: 103.9 MB (103894975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4200c5a3f7cd026b35c4c14ddd08ce81b9a8286688a9d195b89dd005dac72263`  
		Last Modified: Tue, 25 Oct 2022 08:00:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e7f5b5c701916838562eb61ea9d238d42ecdcf4603217d5f36de002d875373`  
		Last Modified: Tue, 25 Oct 2022 08:01:15 GMT  
		Size: 73.3 MB (73280543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066dfb5edf358837c3acdfe4765a62b10a0588d5ee88a202f18c6decb245a6c4`  
		Last Modified: Tue, 25 Oct 2022 08:01:01 GMT  
		Size: 279.6 KB (279618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81213e1334be0f25c6545b79677786f9e06c1aaea8a510b21195f4dc08b6ecac`  
		Last Modified: Tue, 25 Oct 2022 08:01:01 GMT  
		Size: 2.4 KB (2420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c4d1072c5bb0b70378dd5a649ff6468e2763e77a087f95fa4e934dfa18632e`  
		Last Modified: Tue, 25 Oct 2022 08:01:06 GMT  
		Size: 22.1 MB (22138749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:9823d71d84a6facb9ad6ab94361c78eaafb082eedee10eb50d0fcf03e3196e40
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.2 MB (223197069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a96e112da177db105e7ab8a4629e2f05d7ebf4a0f23fba4094e15b8f76174cb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:48:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:48:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:48:53 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:48:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:51:53 GMT
ENV ROS_DISTRO=galactic
# Wed, 05 Oct 2022 13:52:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:52:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 13:52:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:52:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:53:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:53:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 13:53:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2066945f278504a3fbe15500f54112556cb9e9febb0b4d07edd644ecbae9209c`  
		Last Modified: Wed, 05 Oct 2022 14:09:02 GMT  
		Size: 1.2 MB (1164049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ca1624225b52b4e52d61f82b52ba0653fdefd1bcde8f1017fc0031f256a5d`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 5.3 MB (5322416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe2304592d4de6867917f39d4e63cc411cb662d76bc30f54ac6c390d02e993`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a824a2931c1c7d4e723b854a254a721dbaaa0d525baef8fc9bffdaa2beacd42`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8d16a1f7ff237a77f29323231038803c348a1a9f11afc6bb177737dfdcad1c`  
		Last Modified: Wed, 05 Oct 2022 14:15:38 GMT  
		Size: 100.4 MB (100375443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b03d420b9714c9f3dc15cd95ef79baf5b4457aa24c478be8fc2000236b33fc`  
		Last Modified: Wed, 05 Oct 2022 14:15:22 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a956f99c4721f7dc25bfe3b1c9c90ce2a2d8b0474b19e342030574fa077dbc98`  
		Last Modified: Wed, 05 Oct 2022 14:15:59 GMT  
		Size: 67.4 MB (67402819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1231122a3faa9e29e7dcfbc07429b9a375bde70cf77017ed38de61d4a42bb924`  
		Last Modified: Wed, 05 Oct 2022 14:15:50 GMT  
		Size: 277.8 KB (277756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5317376816f40e243dc89e1427d6106c53bd777b2ad592afdce65fa1301cdce8`  
		Last Modified: Wed, 05 Oct 2022 14:15:49 GMT  
		Size: 2.4 KB (2357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a90f00672da01678118f187b2830f6621555d9e05eddf1d8c10a2d25f967f2`  
		Last Modified: Wed, 05 Oct 2022 14:15:53 GMT  
		Size: 21.5 MB (21458239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-core`

```console
$ docker pull ros@sha256:adf888d097027232bb05a56027627a7f672bd311940adcddd9f287bc215ae83e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:92e1833b32530d7a5e8f72ebb1d0bffa7c492fc1d1ba6137b107f8df2c94f264
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.2 MB (139190409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9c7553e926bb17363c98f4a1766d20d7e6c10c4b439a1b3746eb1010493a86`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:29:48 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 Oct 2022 07:30:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:30:35 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:30:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:30:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c34379670d69cf7211d3babcb41e5d7851c837e47be70bf7e93d4c243031e3`  
		Last Modified: Tue, 25 Oct 2022 08:00:51 GMT  
		Size: 103.9 MB (103894975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4200c5a3f7cd026b35c4c14ddd08ce81b9a8286688a9d195b89dd005dac72263`  
		Last Modified: Tue, 25 Oct 2022 08:00:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c377541227217e0215aa8042eb861480f28bf127e4a1df6ac7e1bd1033ac4813
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134055898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f30bc0a078ad834182a2ab27c40a5ae2c4edeeb57645071c9b3163fcd3ffcad`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:48:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:48:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:48:53 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:48:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:51:53 GMT
ENV ROS_DISTRO=galactic
# Wed, 05 Oct 2022 13:52:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:52:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 13:52:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:52:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2066945f278504a3fbe15500f54112556cb9e9febb0b4d07edd644ecbae9209c`  
		Last Modified: Wed, 05 Oct 2022 14:09:02 GMT  
		Size: 1.2 MB (1164049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ca1624225b52b4e52d61f82b52ba0653fdefd1bcde8f1017fc0031f256a5d`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 5.3 MB (5322416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe2304592d4de6867917f39d4e63cc411cb662d76bc30f54ac6c390d02e993`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a824a2931c1c7d4e723b854a254a721dbaaa0d525baef8fc9bffdaa2beacd42`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8d16a1f7ff237a77f29323231038803c348a1a9f11afc6bb177737dfdcad1c`  
		Last Modified: Wed, 05 Oct 2022 14:15:38 GMT  
		Size: 100.4 MB (100375443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b03d420b9714c9f3dc15cd95ef79baf5b4457aa24c478be8fc2000236b33fc`  
		Last Modified: Wed, 05 Oct 2022 14:15:22 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-core-focal`

```console
$ docker pull ros@sha256:adf888d097027232bb05a56027627a7f672bd311940adcddd9f287bc215ae83e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:92e1833b32530d7a5e8f72ebb1d0bffa7c492fc1d1ba6137b107f8df2c94f264
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.2 MB (139190409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9c7553e926bb17363c98f4a1766d20d7e6c10c4b439a1b3746eb1010493a86`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:29:48 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 Oct 2022 07:30:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:30:35 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:30:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:30:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c34379670d69cf7211d3babcb41e5d7851c837e47be70bf7e93d4c243031e3`  
		Last Modified: Tue, 25 Oct 2022 08:00:51 GMT  
		Size: 103.9 MB (103894975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4200c5a3f7cd026b35c4c14ddd08ce81b9a8286688a9d195b89dd005dac72263`  
		Last Modified: Tue, 25 Oct 2022 08:00:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c377541227217e0215aa8042eb861480f28bf127e4a1df6ac7e1bd1033ac4813
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 MB (134055898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f30bc0a078ad834182a2ab27c40a5ae2c4edeeb57645071c9b3163fcd3ffcad`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:48:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:48:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:48:53 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:48:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:51:53 GMT
ENV ROS_DISTRO=galactic
# Wed, 05 Oct 2022 13:52:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:52:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 13:52:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:52:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2066945f278504a3fbe15500f54112556cb9e9febb0b4d07edd644ecbae9209c`  
		Last Modified: Wed, 05 Oct 2022 14:09:02 GMT  
		Size: 1.2 MB (1164049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ca1624225b52b4e52d61f82b52ba0653fdefd1bcde8f1017fc0031f256a5d`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 5.3 MB (5322416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe2304592d4de6867917f39d4e63cc411cb662d76bc30f54ac6c390d02e993`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a824a2931c1c7d4e723b854a254a721dbaaa0d525baef8fc9bffdaa2beacd42`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8d16a1f7ff237a77f29323231038803c348a1a9f11afc6bb177737dfdcad1c`  
		Last Modified: Wed, 05 Oct 2022 14:15:38 GMT  
		Size: 100.4 MB (100375443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b03d420b9714c9f3dc15cd95ef79baf5b4457aa24c478be8fc2000236b33fc`  
		Last Modified: Wed, 05 Oct 2022 14:15:22 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros1-bridge`

```console
$ docker pull ros@sha256:31631350cef1e44d927c63efb58eb407541ae1dadd9ae9ad3d92c4187dae9fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:fb1588e66a4a6f00f08cfc6630778c7832183cb9e9fd45b0acb7abe3a3f4bf34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.1 MB (330065345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1103face6f7a2af3d3e3c726f3bd94530f4969844ce30db1218e7c14fcfbbb9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:29:48 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 Oct 2022 07:30:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:30:35 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:30:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:30:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:31:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:31:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:31:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:31:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:31:35 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:31:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:31:37 GMT
ENV ROS1_DISTRO=noetic
# Tue, 25 Oct 2022 07:31:37 GMT
ENV ROS2_DISTRO=galactic
# Tue, 25 Oct 2022 07:32:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:16 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c34379670d69cf7211d3babcb41e5d7851c837e47be70bf7e93d4c243031e3`  
		Last Modified: Tue, 25 Oct 2022 08:00:51 GMT  
		Size: 103.9 MB (103894975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4200c5a3f7cd026b35c4c14ddd08ce81b9a8286688a9d195b89dd005dac72263`  
		Last Modified: Tue, 25 Oct 2022 08:00:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e7f5b5c701916838562eb61ea9d238d42ecdcf4603217d5f36de002d875373`  
		Last Modified: Tue, 25 Oct 2022 08:01:15 GMT  
		Size: 73.3 MB (73280543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066dfb5edf358837c3acdfe4765a62b10a0588d5ee88a202f18c6decb245a6c4`  
		Last Modified: Tue, 25 Oct 2022 08:01:01 GMT  
		Size: 279.6 KB (279618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81213e1334be0f25c6545b79677786f9e06c1aaea8a510b21195f4dc08b6ecac`  
		Last Modified: Tue, 25 Oct 2022 08:01:01 GMT  
		Size: 2.4 KB (2420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c4d1072c5bb0b70378dd5a649ff6468e2763e77a087f95fa4e934dfa18632e`  
		Last Modified: Tue, 25 Oct 2022 08:01:06 GMT  
		Size: 22.1 MB (22138749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f8c44f31c8de7186a01b87fd4516c3397f99b9cd341f36f8cd884940d852be`  
		Last Modified: Tue, 25 Oct 2022 08:01:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08eb43ea9a6ec61bf6c97f1d126b6a349c84449712c18182f9bc67d4229193fe`  
		Last Modified: Tue, 25 Oct 2022 08:01:28 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958d3e0b946c5d65a557f59ae5c08267cf58ab8bc2c3cd5532b048ae84be8c57`  
		Last Modified: Tue, 25 Oct 2022 08:01:52 GMT  
		Size: 78.7 MB (78708239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65688e59ce9e0915a5cf388ddd2bd68f8a2ff7aaddfa7a370e04170897984fb`  
		Last Modified: Tue, 25 Oct 2022 08:01:34 GMT  
		Size: 16.5 MB (16464739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86260963e5bdc8000fea22d746d7a7c68579e6bed5f3c76edb7a319a68e5aae`  
		Last Modified: Tue, 25 Oct 2022 08:01:28 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c910804e3fa1439223ed0c67c552d14e326bf7064a773000904f3d23937780f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.4 MB (317407737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9581a373856b8b4cefc18a6aec6600f5c8b14c2cd30fd17381407f2ca8abc33d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:48:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:48:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:48:53 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:48:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:51:53 GMT
ENV ROS_DISTRO=galactic
# Wed, 05 Oct 2022 13:52:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:52:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 13:52:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:52:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:53:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:53:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 13:53:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:53:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:53:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:54:00 GMT
ENV ROS1_DISTRO=noetic
# Wed, 05 Oct 2022 13:54:01 GMT
ENV ROS2_DISTRO=galactic
# Wed, 05 Oct 2022 13:54:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:54:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:54:51 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2066945f278504a3fbe15500f54112556cb9e9febb0b4d07edd644ecbae9209c`  
		Last Modified: Wed, 05 Oct 2022 14:09:02 GMT  
		Size: 1.2 MB (1164049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ca1624225b52b4e52d61f82b52ba0653fdefd1bcde8f1017fc0031f256a5d`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 5.3 MB (5322416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe2304592d4de6867917f39d4e63cc411cb662d76bc30f54ac6c390d02e993`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a824a2931c1c7d4e723b854a254a721dbaaa0d525baef8fc9bffdaa2beacd42`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8d16a1f7ff237a77f29323231038803c348a1a9f11afc6bb177737dfdcad1c`  
		Last Modified: Wed, 05 Oct 2022 14:15:38 GMT  
		Size: 100.4 MB (100375443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b03d420b9714c9f3dc15cd95ef79baf5b4457aa24c478be8fc2000236b33fc`  
		Last Modified: Wed, 05 Oct 2022 14:15:22 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a956f99c4721f7dc25bfe3b1c9c90ce2a2d8b0474b19e342030574fa077dbc98`  
		Last Modified: Wed, 05 Oct 2022 14:15:59 GMT  
		Size: 67.4 MB (67402819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1231122a3faa9e29e7dcfbc07429b9a375bde70cf77017ed38de61d4a42bb924`  
		Last Modified: Wed, 05 Oct 2022 14:15:50 GMT  
		Size: 277.8 KB (277756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5317376816f40e243dc89e1427d6106c53bd777b2ad592afdce65fa1301cdce8`  
		Last Modified: Wed, 05 Oct 2022 14:15:49 GMT  
		Size: 2.4 KB (2357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a90f00672da01678118f187b2830f6621555d9e05eddf1d8c10a2d25f967f2`  
		Last Modified: Wed, 05 Oct 2022 14:15:53 GMT  
		Size: 21.5 MB (21458239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05a5b57afce52501fd8743090826b3937ddca932b9a0b537f904c6a011e3551`  
		Last Modified: Wed, 05 Oct 2022 14:16:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54d7f1aa391ea856e1c1c056ed50ed4b9c2b2a888681732c8725415951e7e60`  
		Last Modified: Wed, 05 Oct 2022 14:16:31 GMT  
		Size: 78.4 MB (78448964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63592baf13af078baa1c931c7c508477a0dfd19142bbef22f18895c1ba8f3356`  
		Last Modified: Wed, 05 Oct 2022 14:16:19 GMT  
		Size: 15.8 MB (15761230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae922e3de5fb8dba104acafb21c858ab1e52a35c4ee38a588d60bcca69ee9b2`  
		Last Modified: Wed, 05 Oct 2022 14:16:16 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros1-bridge-focal`

```console
$ docker pull ros@sha256:31631350cef1e44d927c63efb58eb407541ae1dadd9ae9ad3d92c4187dae9fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:fb1588e66a4a6f00f08cfc6630778c7832183cb9e9fd45b0acb7abe3a3f4bf34
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.1 MB (330065345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1103face6f7a2af3d3e3c726f3bd94530f4969844ce30db1218e7c14fcfbbb9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:24 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:24:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:24:26 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:29:48 GMT
ENV ROS_DISTRO=galactic
# Tue, 25 Oct 2022 07:30:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:30:35 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:30:35 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:30:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:31:04 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:31:09 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:31:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:31:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:31:35 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:31:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:31:37 GMT
ENV ROS1_DISTRO=noetic
# Tue, 25 Oct 2022 07:31:37 GMT
ENV ROS2_DISTRO=galactic
# Tue, 25 Oct 2022 07:32:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:16 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0589eb768011f6ff991de1d9b06aa08cf9992361dcd95dcbbd19cab6f9367571`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6d7365895cad17027328617908a6ed236d9972fefa6c1bf5af11b3b35ecb35`  
		Last Modified: Tue, 25 Oct 2022 07:59:00 GMT  
		Size: 2.0 KB (1993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c34379670d69cf7211d3babcb41e5d7851c837e47be70bf7e93d4c243031e3`  
		Last Modified: Tue, 25 Oct 2022 08:00:51 GMT  
		Size: 103.9 MB (103894975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4200c5a3f7cd026b35c4c14ddd08ce81b9a8286688a9d195b89dd005dac72263`  
		Last Modified: Tue, 25 Oct 2022 08:00:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e7f5b5c701916838562eb61ea9d238d42ecdcf4603217d5f36de002d875373`  
		Last Modified: Tue, 25 Oct 2022 08:01:15 GMT  
		Size: 73.3 MB (73280543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066dfb5edf358837c3acdfe4765a62b10a0588d5ee88a202f18c6decb245a6c4`  
		Last Modified: Tue, 25 Oct 2022 08:01:01 GMT  
		Size: 279.6 KB (279618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81213e1334be0f25c6545b79677786f9e06c1aaea8a510b21195f4dc08b6ecac`  
		Last Modified: Tue, 25 Oct 2022 08:01:01 GMT  
		Size: 2.4 KB (2420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c4d1072c5bb0b70378dd5a649ff6468e2763e77a087f95fa4e934dfa18632e`  
		Last Modified: Tue, 25 Oct 2022 08:01:06 GMT  
		Size: 22.1 MB (22138749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f8c44f31c8de7186a01b87fd4516c3397f99b9cd341f36f8cd884940d852be`  
		Last Modified: Tue, 25 Oct 2022 08:01:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08eb43ea9a6ec61bf6c97f1d126b6a349c84449712c18182f9bc67d4229193fe`  
		Last Modified: Tue, 25 Oct 2022 08:01:28 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958d3e0b946c5d65a557f59ae5c08267cf58ab8bc2c3cd5532b048ae84be8c57`  
		Last Modified: Tue, 25 Oct 2022 08:01:52 GMT  
		Size: 78.7 MB (78708239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65688e59ce9e0915a5cf388ddd2bd68f8a2ff7aaddfa7a370e04170897984fb`  
		Last Modified: Tue, 25 Oct 2022 08:01:34 GMT  
		Size: 16.5 MB (16464739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86260963e5bdc8000fea22d746d7a7c68579e6bed5f3c76edb7a319a68e5aae`  
		Last Modified: Tue, 25 Oct 2022 08:01:28 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c910804e3fa1439223ed0c67c552d14e326bf7064a773000904f3d23937780f6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.4 MB (317407737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9581a373856b8b4cefc18a6aec6600f5c8b14c2cd30fd17381407f2ca8abc33d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:48:50 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:48:52 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:48:53 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:48:54 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:51:53 GMT
ENV ROS_DISTRO=galactic
# Wed, 05 Oct 2022 13:52:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:52:41 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 13:52:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:52:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:53:15 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:53:20 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:53:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 13:53:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:53:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:53:59 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:54:00 GMT
ENV ROS1_DISTRO=noetic
# Wed, 05 Oct 2022 13:54:01 GMT
ENV ROS2_DISTRO=galactic
# Wed, 05 Oct 2022 13:54:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:54:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:54:51 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2066945f278504a3fbe15500f54112556cb9e9febb0b4d07edd644ecbae9209c`  
		Last Modified: Wed, 05 Oct 2022 14:09:02 GMT  
		Size: 1.2 MB (1164049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ca1624225b52b4e52d61f82b52ba0653fdefd1bcde8f1017fc0031f256a5d`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 5.3 MB (5322416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe2304592d4de6867917f39d4e63cc411cb662d76bc30f54ac6c390d02e993`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a824a2931c1c7d4e723b854a254a721dbaaa0d525baef8fc9bffdaa2beacd42`  
		Last Modified: Wed, 05 Oct 2022 14:14:01 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e8d16a1f7ff237a77f29323231038803c348a1a9f11afc6bb177737dfdcad1c`  
		Last Modified: Wed, 05 Oct 2022 14:15:38 GMT  
		Size: 100.4 MB (100375443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b03d420b9714c9f3dc15cd95ef79baf5b4457aa24c478be8fc2000236b33fc`  
		Last Modified: Wed, 05 Oct 2022 14:15:22 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a956f99c4721f7dc25bfe3b1c9c90ce2a2d8b0474b19e342030574fa077dbc98`  
		Last Modified: Wed, 05 Oct 2022 14:15:59 GMT  
		Size: 67.4 MB (67402819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1231122a3faa9e29e7dcfbc07429b9a375bde70cf77017ed38de61d4a42bb924`  
		Last Modified: Wed, 05 Oct 2022 14:15:50 GMT  
		Size: 277.8 KB (277756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5317376816f40e243dc89e1427d6106c53bd777b2ad592afdce65fa1301cdce8`  
		Last Modified: Wed, 05 Oct 2022 14:15:49 GMT  
		Size: 2.4 KB (2357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2a90f00672da01678118f187b2830f6621555d9e05eddf1d8c10a2d25f967f2`  
		Last Modified: Wed, 05 Oct 2022 14:15:53 GMT  
		Size: 21.5 MB (21458239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05a5b57afce52501fd8743090826b3937ddca932b9a0b537f904c6a011e3551`  
		Last Modified: Wed, 05 Oct 2022 14:16:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54d7f1aa391ea856e1c1c056ed50ed4b9c2b2a888681732c8725415951e7e60`  
		Last Modified: Wed, 05 Oct 2022 14:16:31 GMT  
		Size: 78.4 MB (78448964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63592baf13af078baa1c931c7c508477a0dfd19142bbef22f18895c1ba8f3356`  
		Last Modified: Wed, 05 Oct 2022 14:16:19 GMT  
		Size: 15.8 MB (15761230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae922e3de5fb8dba104acafb21c858ab1e52a35c4ee38a588d60bcca69ee9b2`  
		Last Modified: Wed, 05 Oct 2022 14:16:16 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble`

```console
$ docker pull ros@sha256:08655071cb632ffc29160a7b953f05e14720f29bb08762190ecfea3edf125311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:0a802223f0f42ce6c021e103c88cebb39d34b33e6f27b6c5eeb664a4384581ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262845111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f340563a38bb44aee9bda8c1ce81c0eb80dde4b3d82200d63cafbf34e511942`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV ROS_DISTRO=humble
# Tue, 25 Oct 2022 07:34:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:34:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:34:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:34:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:35:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:35:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:35:47 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:36:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be1f7ccd647190e134f58b7bdaddc42b6477dff97e50567b748bc31b6303f00`  
		Last Modified: Tue, 25 Oct 2022 08:02:27 GMT  
		Size: 106.2 MB (106227052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd97e132a97f3e5517dacc0f9b6598427f1966b8505acab43d41575f53d2ee8`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd54d8e71568daecc9e521d17654239410a7a8d6895fb3167bb3e4b8735f5e5`  
		Last Modified: Tue, 25 Oct 2022 08:02:52 GMT  
		Size: 97.9 MB (97878471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d389ad8893cc3f537cfc3608c72ea4279d8ef1edc81ecdf82f4dbbdf4b8b604`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 295.6 KB (295633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d846403b95a3d13902aed833ac91f24ab2628f08871623f59fc2ef029c73ab2c`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710da595552b7d9324d2e432bcf0437dc8b7f054bf7ae402a6f33c2d5cbc281c`  
		Last Modified: Tue, 25 Oct 2022 08:02:42 GMT  
		Size: 23.0 MB (23008535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b52db8801d9e46e66e2f1b84031e242bd5f8c85d836c9ee80ae69bcb98b9e4a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255055044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97fa8fa54f8dd58526781db889c6bd8e5ee3e784971669964178b5512fcdb32`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:55:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:55:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:55:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:55:18 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:55:19 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Oct 2022 13:56:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:56:17 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 13:56:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:56:19 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:57:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:57:06 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:57:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 13:57:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a891d50162687d5b4db85383705535653c56066b48e0e3314badd3e76d2f8af`  
		Last Modified: Wed, 05 Oct 2022 14:16:45 GMT  
		Size: 1.2 MB (1178125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3fc4af9e9380eebc7d111e904fb1098bb4102f7271c19ade184c620ba4d5dc`  
		Last Modified: Wed, 05 Oct 2022 14:16:43 GMT  
		Size: 3.6 MB (3594928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc1176274b8951042f2b29277ebbcdc02bf43ea04b1e95a7e7f80c137ddb1d`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca88c2c17aef59df2c29525001e8bb7f45b3b5e37ef793847df2e89374421e`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c77135164a4ca214d5baefbf18732e85e199d498ecc59003672487d9c648b74`  
		Last Modified: Wed, 05 Oct 2022 14:16:58 GMT  
		Size: 104.0 MB (103957828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6965bb2d35a3d18ae4266c452f2a47be3cc9d2dba39a969448e52ad4b37a5b3`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce2c8431570b35ece0db3a51d240fe2781ad038af3c8da3b55b03b4fe8de8ac`  
		Last Modified: Wed, 05 Oct 2022 14:17:22 GMT  
		Size: 95.2 MB (95215132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f80f204207eef3b331605f2054caba003953f6e525e487fe268099461c7eef`  
		Last Modified: Wed, 05 Oct 2022 14:17:09 GMT  
		Size: 293.3 KB (293326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44490e7bf336a1cd0e4bbdfc0cb509173c0643c5572dea249d5900bd9121742a`  
		Last Modified: Wed, 05 Oct 2022 14:17:09 GMT  
		Size: 2.4 KB (2382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d44d5787adf5963e3ae22a342cafe9f33a160f2cc03b123c4d6996867e0535`  
		Last Modified: Wed, 05 Oct 2022 14:17:12 GMT  
		Size: 22.4 MB (22428695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-perception`

```console
$ docker pull ros@sha256:777725e051baea3119caa2479f38e77f904e54814fc2a463b4f76bdefdd00975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:76645b46dcf6ffbf3fdac6944597995377c4640b15b343bdb7f223d323b81e1f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1087032972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ae91661e2cf574b08b75a61ebef5b0786b5a33c59bdab811b81be7e84e98dd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV ROS_DISTRO=humble
# Tue, 25 Oct 2022 07:34:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:34:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:34:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:34:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:35:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:35:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:35:47 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:36:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:44:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be1f7ccd647190e134f58b7bdaddc42b6477dff97e50567b748bc31b6303f00`  
		Last Modified: Tue, 25 Oct 2022 08:02:27 GMT  
		Size: 106.2 MB (106227052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd97e132a97f3e5517dacc0f9b6598427f1966b8505acab43d41575f53d2ee8`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd54d8e71568daecc9e521d17654239410a7a8d6895fb3167bb3e4b8735f5e5`  
		Last Modified: Tue, 25 Oct 2022 08:02:52 GMT  
		Size: 97.9 MB (97878471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d389ad8893cc3f537cfc3608c72ea4279d8ef1edc81ecdf82f4dbbdf4b8b604`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 295.6 KB (295633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d846403b95a3d13902aed833ac91f24ab2628f08871623f59fc2ef029c73ab2c`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710da595552b7d9324d2e432bcf0437dc8b7f054bf7ae402a6f33c2d5cbc281c`  
		Last Modified: Tue, 25 Oct 2022 08:02:42 GMT  
		Size: 23.0 MB (23008535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811c764114f804d6bc0acc7e66e888ceacf4c5537574a5de8c4d40fb90c9999e`  
		Last Modified: Tue, 25 Oct 2022 08:05:05 GMT  
		Size: 824.2 MB (824187861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8d33b1eda15a566ef8d7f32e8d9def7e1da4c9bf71d80e0d9ce5495a9737f625
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1036772436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d72876cd51856f6c06f3479fae29de0e96685b3944854f72e4e39bc6c90566a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:55:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:55:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:55:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:55:18 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:55:19 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Oct 2022 13:56:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:56:17 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 13:56:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:56:19 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:57:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:57:06 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:57:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 13:57:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:00:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a891d50162687d5b4db85383705535653c56066b48e0e3314badd3e76d2f8af`  
		Last Modified: Wed, 05 Oct 2022 14:16:45 GMT  
		Size: 1.2 MB (1178125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3fc4af9e9380eebc7d111e904fb1098bb4102f7271c19ade184c620ba4d5dc`  
		Last Modified: Wed, 05 Oct 2022 14:16:43 GMT  
		Size: 3.6 MB (3594928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc1176274b8951042f2b29277ebbcdc02bf43ea04b1e95a7e7f80c137ddb1d`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca88c2c17aef59df2c29525001e8bb7f45b3b5e37ef793847df2e89374421e`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c77135164a4ca214d5baefbf18732e85e199d498ecc59003672487d9c648b74`  
		Last Modified: Wed, 05 Oct 2022 14:16:58 GMT  
		Size: 104.0 MB (103957828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6965bb2d35a3d18ae4266c452f2a47be3cc9d2dba39a969448e52ad4b37a5b3`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce2c8431570b35ece0db3a51d240fe2781ad038af3c8da3b55b03b4fe8de8ac`  
		Last Modified: Wed, 05 Oct 2022 14:17:22 GMT  
		Size: 95.2 MB (95215132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f80f204207eef3b331605f2054caba003953f6e525e487fe268099461c7eef`  
		Last Modified: Wed, 05 Oct 2022 14:17:09 GMT  
		Size: 293.3 KB (293326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44490e7bf336a1cd0e4bbdfc0cb509173c0643c5572dea249d5900bd9121742a`  
		Last Modified: Wed, 05 Oct 2022 14:17:09 GMT  
		Size: 2.4 KB (2382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d44d5787adf5963e3ae22a342cafe9f33a160f2cc03b123c4d6996867e0535`  
		Last Modified: Wed, 05 Oct 2022 14:17:12 GMT  
		Size: 22.4 MB (22428695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3bcbbe799e24821f61a98ab3360ded019455e6da2828098c9b7ed7d6f5a5d9`  
		Last Modified: Wed, 05 Oct 2022 14:19:54 GMT  
		Size: 781.7 MB (781717392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:777725e051baea3119caa2479f38e77f904e54814fc2a463b4f76bdefdd00975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:76645b46dcf6ffbf3fdac6944597995377c4640b15b343bdb7f223d323b81e1f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1087032972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ae91661e2cf574b08b75a61ebef5b0786b5a33c59bdab811b81be7e84e98dd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV ROS_DISTRO=humble
# Tue, 25 Oct 2022 07:34:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:34:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:34:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:34:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:35:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:35:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:35:47 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:36:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:44:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be1f7ccd647190e134f58b7bdaddc42b6477dff97e50567b748bc31b6303f00`  
		Last Modified: Tue, 25 Oct 2022 08:02:27 GMT  
		Size: 106.2 MB (106227052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd97e132a97f3e5517dacc0f9b6598427f1966b8505acab43d41575f53d2ee8`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd54d8e71568daecc9e521d17654239410a7a8d6895fb3167bb3e4b8735f5e5`  
		Last Modified: Tue, 25 Oct 2022 08:02:52 GMT  
		Size: 97.9 MB (97878471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d389ad8893cc3f537cfc3608c72ea4279d8ef1edc81ecdf82f4dbbdf4b8b604`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 295.6 KB (295633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d846403b95a3d13902aed833ac91f24ab2628f08871623f59fc2ef029c73ab2c`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710da595552b7d9324d2e432bcf0437dc8b7f054bf7ae402a6f33c2d5cbc281c`  
		Last Modified: Tue, 25 Oct 2022 08:02:42 GMT  
		Size: 23.0 MB (23008535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811c764114f804d6bc0acc7e66e888ceacf4c5537574a5de8c4d40fb90c9999e`  
		Last Modified: Tue, 25 Oct 2022 08:05:05 GMT  
		Size: 824.2 MB (824187861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8d33b1eda15a566ef8d7f32e8d9def7e1da4c9bf71d80e0d9ce5495a9737f625
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1036772436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d72876cd51856f6c06f3479fae29de0e96685b3944854f72e4e39bc6c90566a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:55:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:55:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:55:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:55:18 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:55:19 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Oct 2022 13:56:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:56:17 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 13:56:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:56:19 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:57:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:57:06 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:57:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 13:57:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:00:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a891d50162687d5b4db85383705535653c56066b48e0e3314badd3e76d2f8af`  
		Last Modified: Wed, 05 Oct 2022 14:16:45 GMT  
		Size: 1.2 MB (1178125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3fc4af9e9380eebc7d111e904fb1098bb4102f7271c19ade184c620ba4d5dc`  
		Last Modified: Wed, 05 Oct 2022 14:16:43 GMT  
		Size: 3.6 MB (3594928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc1176274b8951042f2b29277ebbcdc02bf43ea04b1e95a7e7f80c137ddb1d`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca88c2c17aef59df2c29525001e8bb7f45b3b5e37ef793847df2e89374421e`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c77135164a4ca214d5baefbf18732e85e199d498ecc59003672487d9c648b74`  
		Last Modified: Wed, 05 Oct 2022 14:16:58 GMT  
		Size: 104.0 MB (103957828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6965bb2d35a3d18ae4266c452f2a47be3cc9d2dba39a969448e52ad4b37a5b3`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce2c8431570b35ece0db3a51d240fe2781ad038af3c8da3b55b03b4fe8de8ac`  
		Last Modified: Wed, 05 Oct 2022 14:17:22 GMT  
		Size: 95.2 MB (95215132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f80f204207eef3b331605f2054caba003953f6e525e487fe268099461c7eef`  
		Last Modified: Wed, 05 Oct 2022 14:17:09 GMT  
		Size: 293.3 KB (293326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44490e7bf336a1cd0e4bbdfc0cb509173c0643c5572dea249d5900bd9121742a`  
		Last Modified: Wed, 05 Oct 2022 14:17:09 GMT  
		Size: 2.4 KB (2382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d44d5787adf5963e3ae22a342cafe9f33a160f2cc03b123c4d6996867e0535`  
		Last Modified: Wed, 05 Oct 2022 14:17:12 GMT  
		Size: 22.4 MB (22428695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3bcbbe799e24821f61a98ab3360ded019455e6da2828098c9b7ed7d6f5a5d9`  
		Last Modified: Wed, 05 Oct 2022 14:19:54 GMT  
		Size: 781.7 MB (781717392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:08655071cb632ffc29160a7b953f05e14720f29bb08762190ecfea3edf125311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:0a802223f0f42ce6c021e103c88cebb39d34b33e6f27b6c5eeb664a4384581ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262845111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f340563a38bb44aee9bda8c1ce81c0eb80dde4b3d82200d63cafbf34e511942`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV ROS_DISTRO=humble
# Tue, 25 Oct 2022 07:34:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:34:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:34:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:34:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:35:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:35:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:35:47 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:36:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be1f7ccd647190e134f58b7bdaddc42b6477dff97e50567b748bc31b6303f00`  
		Last Modified: Tue, 25 Oct 2022 08:02:27 GMT  
		Size: 106.2 MB (106227052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd97e132a97f3e5517dacc0f9b6598427f1966b8505acab43d41575f53d2ee8`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd54d8e71568daecc9e521d17654239410a7a8d6895fb3167bb3e4b8735f5e5`  
		Last Modified: Tue, 25 Oct 2022 08:02:52 GMT  
		Size: 97.9 MB (97878471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d389ad8893cc3f537cfc3608c72ea4279d8ef1edc81ecdf82f4dbbdf4b8b604`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 295.6 KB (295633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d846403b95a3d13902aed833ac91f24ab2628f08871623f59fc2ef029c73ab2c`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710da595552b7d9324d2e432bcf0437dc8b7f054bf7ae402a6f33c2d5cbc281c`  
		Last Modified: Tue, 25 Oct 2022 08:02:42 GMT  
		Size: 23.0 MB (23008535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b52db8801d9e46e66e2f1b84031e242bd5f8c85d836c9ee80ae69bcb98b9e4a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255055044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97fa8fa54f8dd58526781db889c6bd8e5ee3e784971669964178b5512fcdb32`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:55:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:55:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:55:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:55:18 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:55:19 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Oct 2022 13:56:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:56:17 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 13:56:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:56:19 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:57:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:57:06 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:57:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 13:57:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a891d50162687d5b4db85383705535653c56066b48e0e3314badd3e76d2f8af`  
		Last Modified: Wed, 05 Oct 2022 14:16:45 GMT  
		Size: 1.2 MB (1178125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3fc4af9e9380eebc7d111e904fb1098bb4102f7271c19ade184c620ba4d5dc`  
		Last Modified: Wed, 05 Oct 2022 14:16:43 GMT  
		Size: 3.6 MB (3594928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc1176274b8951042f2b29277ebbcdc02bf43ea04b1e95a7e7f80c137ddb1d`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca88c2c17aef59df2c29525001e8bb7f45b3b5e37ef793847df2e89374421e`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c77135164a4ca214d5baefbf18732e85e199d498ecc59003672487d9c648b74`  
		Last Modified: Wed, 05 Oct 2022 14:16:58 GMT  
		Size: 104.0 MB (103957828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6965bb2d35a3d18ae4266c452f2a47be3cc9d2dba39a969448e52ad4b37a5b3`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce2c8431570b35ece0db3a51d240fe2781ad038af3c8da3b55b03b4fe8de8ac`  
		Last Modified: Wed, 05 Oct 2022 14:17:22 GMT  
		Size: 95.2 MB (95215132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f80f204207eef3b331605f2054caba003953f6e525e487fe268099461c7eef`  
		Last Modified: Wed, 05 Oct 2022 14:17:09 GMT  
		Size: 293.3 KB (293326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44490e7bf336a1cd0e4bbdfc0cb509173c0643c5572dea249d5900bd9121742a`  
		Last Modified: Wed, 05 Oct 2022 14:17:09 GMT  
		Size: 2.4 KB (2382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d44d5787adf5963e3ae22a342cafe9f33a160f2cc03b123c4d6996867e0535`  
		Last Modified: Wed, 05 Oct 2022 14:17:12 GMT  
		Size: 22.4 MB (22428695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:08655071cb632ffc29160a7b953f05e14720f29bb08762190ecfea3edf125311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:0a802223f0f42ce6c021e103c88cebb39d34b33e6f27b6c5eeb664a4384581ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262845111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f340563a38bb44aee9bda8c1ce81c0eb80dde4b3d82200d63cafbf34e511942`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV ROS_DISTRO=humble
# Tue, 25 Oct 2022 07:34:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:34:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:34:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:34:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:35:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:35:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:35:47 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:36:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be1f7ccd647190e134f58b7bdaddc42b6477dff97e50567b748bc31b6303f00`  
		Last Modified: Tue, 25 Oct 2022 08:02:27 GMT  
		Size: 106.2 MB (106227052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd97e132a97f3e5517dacc0f9b6598427f1966b8505acab43d41575f53d2ee8`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd54d8e71568daecc9e521d17654239410a7a8d6895fb3167bb3e4b8735f5e5`  
		Last Modified: Tue, 25 Oct 2022 08:02:52 GMT  
		Size: 97.9 MB (97878471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d389ad8893cc3f537cfc3608c72ea4279d8ef1edc81ecdf82f4dbbdf4b8b604`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 295.6 KB (295633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d846403b95a3d13902aed833ac91f24ab2628f08871623f59fc2ef029c73ab2c`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710da595552b7d9324d2e432bcf0437dc8b7f054bf7ae402a6f33c2d5cbc281c`  
		Last Modified: Tue, 25 Oct 2022 08:02:42 GMT  
		Size: 23.0 MB (23008535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b52db8801d9e46e66e2f1b84031e242bd5f8c85d836c9ee80ae69bcb98b9e4a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255055044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97fa8fa54f8dd58526781db889c6bd8e5ee3e784971669964178b5512fcdb32`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:55:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:55:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:55:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:55:18 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:55:19 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Oct 2022 13:56:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:56:17 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 13:56:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:56:19 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:57:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:57:06 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:57:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 13:57:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a891d50162687d5b4db85383705535653c56066b48e0e3314badd3e76d2f8af`  
		Last Modified: Wed, 05 Oct 2022 14:16:45 GMT  
		Size: 1.2 MB (1178125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3fc4af9e9380eebc7d111e904fb1098bb4102f7271c19ade184c620ba4d5dc`  
		Last Modified: Wed, 05 Oct 2022 14:16:43 GMT  
		Size: 3.6 MB (3594928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc1176274b8951042f2b29277ebbcdc02bf43ea04b1e95a7e7f80c137ddb1d`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca88c2c17aef59df2c29525001e8bb7f45b3b5e37ef793847df2e89374421e`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c77135164a4ca214d5baefbf18732e85e199d498ecc59003672487d9c648b74`  
		Last Modified: Wed, 05 Oct 2022 14:16:58 GMT  
		Size: 104.0 MB (103957828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6965bb2d35a3d18ae4266c452f2a47be3cc9d2dba39a969448e52ad4b37a5b3`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce2c8431570b35ece0db3a51d240fe2781ad038af3c8da3b55b03b4fe8de8ac`  
		Last Modified: Wed, 05 Oct 2022 14:17:22 GMT  
		Size: 95.2 MB (95215132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f80f204207eef3b331605f2054caba003953f6e525e487fe268099461c7eef`  
		Last Modified: Wed, 05 Oct 2022 14:17:09 GMT  
		Size: 293.3 KB (293326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44490e7bf336a1cd0e4bbdfc0cb509173c0643c5572dea249d5900bd9121742a`  
		Last Modified: Wed, 05 Oct 2022 14:17:09 GMT  
		Size: 2.4 KB (2382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d44d5787adf5963e3ae22a342cafe9f33a160f2cc03b123c4d6996867e0535`  
		Last Modified: Wed, 05 Oct 2022 14:17:12 GMT  
		Size: 22.4 MB (22428695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:88fce7b9f81b177c3ba6347c1b023580ee171b03447a1ad3cbc69a039a02d935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:8bacb2ad63d34e815a7983fd8001a3f4183c28384feb5538e6dce2ec715eb7d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141660031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a32cd2767cb289a14d77fd1f6dd451fa60a7f107555bf2bc9a71dfe8dc5ac8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV ROS_DISTRO=humble
# Tue, 25 Oct 2022 07:34:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:34:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:34:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:34:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be1f7ccd647190e134f58b7bdaddc42b6477dff97e50567b748bc31b6303f00`  
		Last Modified: Tue, 25 Oct 2022 08:02:27 GMT  
		Size: 106.2 MB (106227052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd97e132a97f3e5517dacc0f9b6598427f1966b8505acab43d41575f53d2ee8`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dbcd22cabd0b7d5b685d0124b75499582924f3e619ecf3e12046df696d4b7040
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137115509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fff96ba234d061182e829199f8154b9ed0b8fb9a76718eed113695c1effb94`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:55:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:55:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:55:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:55:18 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:55:19 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Oct 2022 13:56:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:56:17 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 13:56:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:56:19 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a891d50162687d5b4db85383705535653c56066b48e0e3314badd3e76d2f8af`  
		Last Modified: Wed, 05 Oct 2022 14:16:45 GMT  
		Size: 1.2 MB (1178125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3fc4af9e9380eebc7d111e904fb1098bb4102f7271c19ade184c620ba4d5dc`  
		Last Modified: Wed, 05 Oct 2022 14:16:43 GMT  
		Size: 3.6 MB (3594928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc1176274b8951042f2b29277ebbcdc02bf43ea04b1e95a7e7f80c137ddb1d`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca88c2c17aef59df2c29525001e8bb7f45b3b5e37ef793847df2e89374421e`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c77135164a4ca214d5baefbf18732e85e199d498ecc59003672487d9c648b74`  
		Last Modified: Wed, 05 Oct 2022 14:16:58 GMT  
		Size: 104.0 MB (103957828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6965bb2d35a3d18ae4266c452f2a47be3cc9d2dba39a969448e52ad4b37a5b3`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:88fce7b9f81b177c3ba6347c1b023580ee171b03447a1ad3cbc69a039a02d935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:8bacb2ad63d34e815a7983fd8001a3f4183c28384feb5538e6dce2ec715eb7d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141660031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a32cd2767cb289a14d77fd1f6dd451fa60a7f107555bf2bc9a71dfe8dc5ac8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV ROS_DISTRO=humble
# Tue, 25 Oct 2022 07:34:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:34:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:34:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:34:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be1f7ccd647190e134f58b7bdaddc42b6477dff97e50567b748bc31b6303f00`  
		Last Modified: Tue, 25 Oct 2022 08:02:27 GMT  
		Size: 106.2 MB (106227052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd97e132a97f3e5517dacc0f9b6598427f1966b8505acab43d41575f53d2ee8`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:dbcd22cabd0b7d5b685d0124b75499582924f3e619ecf3e12046df696d4b7040
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137115509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fff96ba234d061182e829199f8154b9ed0b8fb9a76718eed113695c1effb94`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:55:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:55:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:55:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:55:18 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:55:19 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Oct 2022 13:56:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:56:17 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 13:56:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:56:19 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a891d50162687d5b4db85383705535653c56066b48e0e3314badd3e76d2f8af`  
		Last Modified: Wed, 05 Oct 2022 14:16:45 GMT  
		Size: 1.2 MB (1178125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3fc4af9e9380eebc7d111e904fb1098bb4102f7271c19ade184c620ba4d5dc`  
		Last Modified: Wed, 05 Oct 2022 14:16:43 GMT  
		Size: 3.6 MB (3594928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc1176274b8951042f2b29277ebbcdc02bf43ea04b1e95a7e7f80c137ddb1d`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca88c2c17aef59df2c29525001e8bb7f45b3b5e37ef793847df2e89374421e`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c77135164a4ca214d5baefbf18732e85e199d498ecc59003672487d9c648b74`  
		Last Modified: Wed, 05 Oct 2022 14:16:58 GMT  
		Size: 104.0 MB (103957828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6965bb2d35a3d18ae4266c452f2a47be3cc9d2dba39a969448e52ad4b37a5b3`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:latest`

```console
$ docker pull ros@sha256:08655071cb632ffc29160a7b953f05e14720f29bb08762190ecfea3edf125311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:0a802223f0f42ce6c021e103c88cebb39d34b33e6f27b6c5eeb664a4384581ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262845111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f340563a38bb44aee9bda8c1ce81c0eb80dde4b3d82200d63cafbf34e511942`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV ROS_DISTRO=humble
# Tue, 25 Oct 2022 07:34:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:34:42 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:34:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:34:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:35:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:35:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:35:47 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:36:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be1f7ccd647190e134f58b7bdaddc42b6477dff97e50567b748bc31b6303f00`  
		Last Modified: Tue, 25 Oct 2022 08:02:27 GMT  
		Size: 106.2 MB (106227052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd97e132a97f3e5517dacc0f9b6598427f1966b8505acab43d41575f53d2ee8`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd54d8e71568daecc9e521d17654239410a7a8d6895fb3167bb3e4b8735f5e5`  
		Last Modified: Tue, 25 Oct 2022 08:02:52 GMT  
		Size: 97.9 MB (97878471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d389ad8893cc3f537cfc3608c72ea4279d8ef1edc81ecdf82f4dbbdf4b8b604`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 295.6 KB (295633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d846403b95a3d13902aed833ac91f24ab2628f08871623f59fc2ef029c73ab2c`  
		Last Modified: Tue, 25 Oct 2022 08:02:37 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710da595552b7d9324d2e432bcf0437dc8b7f054bf7ae402a6f33c2d5cbc281c`  
		Last Modified: Tue, 25 Oct 2022 08:02:42 GMT  
		Size: 23.0 MB (23008535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b52db8801d9e46e66e2f1b84031e242bd5f8c85d836c9ee80ae69bcb98b9e4a5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255055044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97fa8fa54f8dd58526781db889c6bd8e5ee3e784971669964178b5512fcdb32`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:55:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:55:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:55:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:55:18 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:55:19 GMT
ENV ROS_DISTRO=humble
# Wed, 05 Oct 2022 13:56:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:56:17 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 13:56:18 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:56:19 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:57:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:57:06 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:57:13 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 13:57:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a891d50162687d5b4db85383705535653c56066b48e0e3314badd3e76d2f8af`  
		Last Modified: Wed, 05 Oct 2022 14:16:45 GMT  
		Size: 1.2 MB (1178125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3fc4af9e9380eebc7d111e904fb1098bb4102f7271c19ade184c620ba4d5dc`  
		Last Modified: Wed, 05 Oct 2022 14:16:43 GMT  
		Size: 3.6 MB (3594928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc1176274b8951042f2b29277ebbcdc02bf43ea04b1e95a7e7f80c137ddb1d`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca88c2c17aef59df2c29525001e8bb7f45b3b5e37ef793847df2e89374421e`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c77135164a4ca214d5baefbf18732e85e199d498ecc59003672487d9c648b74`  
		Last Modified: Wed, 05 Oct 2022 14:16:58 GMT  
		Size: 104.0 MB (103957828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6965bb2d35a3d18ae4266c452f2a47be3cc9d2dba39a969448e52ad4b37a5b3`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce2c8431570b35ece0db3a51d240fe2781ad038af3c8da3b55b03b4fe8de8ac`  
		Last Modified: Wed, 05 Oct 2022 14:17:22 GMT  
		Size: 95.2 MB (95215132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f80f204207eef3b331605f2054caba003953f6e525e487fe268099461c7eef`  
		Last Modified: Wed, 05 Oct 2022 14:17:09 GMT  
		Size: 293.3 KB (293326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44490e7bf336a1cd0e4bbdfc0cb509173c0643c5572dea249d5900bd9121742a`  
		Last Modified: Wed, 05 Oct 2022 14:17:09 GMT  
		Size: 2.4 KB (2382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d44d5787adf5963e3ae22a342cafe9f33a160f2cc03b123c4d6996867e0535`  
		Last Modified: Wed, 05 Oct 2022 14:17:12 GMT  
		Size: 22.4 MB (22428695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic`

```console
$ docker pull ros@sha256:ecf84b223a21ae4bc5dbeb24ff850fc8963031e00bd67121cdaf99b4f898c083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic` - linux; amd64

```console
$ docker pull ros@sha256:a7201ea28800aff6b84b5fc7ab4fd80b61bc58dc006b9c2cdca6ec7be32cf6ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.5 MB (437538991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898998df3ed57ef16b7e130a5148adf56b94754f794c70d6f6b5c670eb939dbf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:28 GMT
ADD file:fc5d658c47ede58827812b75a311353be776e41e2dd339b8906839527c9b5247 in / 
# Tue, 25 Oct 2022 01:53:28 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:51:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 06:51:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 06:55:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:55:51 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 06:55:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 06:55:51 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:56:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:56:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 06:58:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a404e54162968593b8d92b571f3cdd673e4c9eab5d9be28d7c494595c0aa6682`  
		Last Modified: Wed, 19 Oct 2022 22:03:02 GMT  
		Size: 26.7 MB (26712500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1955214fb5b152d9d9fa8ce9a39b19a4e6e8ea487bc617e76c0b7b33e1881bc`  
		Last Modified: Tue, 25 Oct 2022 07:50:06 GMT  
		Size: 831.1 KB (831118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b389880aa1534b94319b44ef0d7e8e52ae108ec326dc1efe1cf0e4e749a4190a`  
		Last Modified: Tue, 25 Oct 2022 07:50:04 GMT  
		Size: 4.9 MB (4877285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db68a36d4b9f8fa036da9f0c51e74b6d27dffd9d39317f42638ee84b29322668`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b325e4aad15f84b511f749de8e3b84dc88f98909bbfdd1961ac0e84f7d273f16`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ad76754b2b5a9699fc604ac8d1393dd3d6dfe21df82c8e930da67ffd6f6708`  
		Last Modified: Tue, 25 Oct 2022 07:50:52 GMT  
		Size: 259.6 MB (259567997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1318baf5e3f70ccdc707f97c58bf69e65917aadaa98ec26b67d1d2695572fa`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb834ce8392143178e871793c61a9bd2ac4e34031627b0f8d8453a1f1d836a1`  
		Last Modified: Tue, 25 Oct 2022 07:51:13 GMT  
		Size: 70.3 MB (70260436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874278d4c37ef6d13abdb486dd6dfd9900b104ad68492eb5ba5df13c5c947b37`  
		Last Modified: Tue, 25 Oct 2022 07:51:03 GMT  
		Size: 289.2 KB (289160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5236595b9f2b064d0593cf222d04423eaa11b12eaa5c8e78974d822f22c23287`  
		Last Modified: Tue, 25 Oct 2022 07:51:19 GMT  
		Size: 75.0 MB (74998649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic` - linux; arm variant v7

```console
$ docker pull ros@sha256:a45ac6c100b50466ddc1d7e743fa1245f7fd98846f6029690aea97d10f221e45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.0 MB (385994420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39885270420308b747b47cac016d290e8ce997f48e27902594c0fb48214d0fa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:31 GMT
ADD file:20e0d71059d38b1e18636b9db71f534d7297c3f571d73d45a75b4b8d3cac86c7 in / 
# Wed, 05 Oct 2022 00:13:32 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:46:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:46:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV ROS_DISTRO=melodic
# Thu, 06 Oct 2022 06:48:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:48:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:48:10 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:48:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:49:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:91bb9a9844d67fd31f07ebd74dc8a4f4f18e2f959d3aa2166aca86ae57f353c6`  
		Last Modified: Wed, 05 Oct 2022 00:15:26 GMT  
		Size: 22.3 MB (22305721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f25a09f0aff0cba5b24d07bd5b4c417734fbce77148b7b62042ac54dc95c068`  
		Last Modified: Thu, 06 Oct 2022 06:58:00 GMT  
		Size: 831.1 KB (831144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14397641aa51f3c3aa6ed2c352f3417b3bce0ebaca231e20759c931e3fe38560`  
		Last Modified: Thu, 06 Oct 2022 06:57:58 GMT  
		Size: 4.1 MB (4087217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a2d98c80683d1808b546f8ca1a247aecedcea1e9d2460d95343238dfabc896`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670273ddac9f5d6d6c7da9986d18661e88bbbc0126833dcd54f90992f9c9484d`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6664b634c5bf87720b15e47366d33bea9fefdd0032f110f86c336e5ae31a0e`  
		Last Modified: Thu, 06 Oct 2022 06:58:45 GMT  
		Size: 239.0 MB (239013225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074569eb7528b8c52dc9fd001aac258a83c59faaf1830e646c00899e79c3a889`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c925a21a964fb8486223de78f9a2d457f125c75f70114336548d871ef3aa6e97`  
		Last Modified: Thu, 06 Oct 2022 06:59:08 GMT  
		Size: 54.7 MB (54719854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176e6a18e2f88225c6c13f76a00ecd1530583b434fa9c482eee0a2179245adbd`  
		Last Modified: Thu, 06 Oct 2022 06:58:57 GMT  
		Size: 287.8 KB (287786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ace293972247ef40871f854b48d8ab1be13f2c1d04bc8c2d37a6be30a82a5e`  
		Last Modified: Thu, 06 Oct 2022 06:59:13 GMT  
		Size: 64.7 MB (64747626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4868ca46db01ab9b479444064b3f4b3919442f2de6fb4f78794359e36ffeb1a3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.7 MB (411711887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d006ec586d2e78a0b3c081f1811cfe9cf6ebc2d6e2cec7e0cbbec0e1012473a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:02 GMT
ADD file:4beae13e1fd7bb92776c08a5cd95feb81b8b3c80522ed8513f2441adfb1661ac in / 
# Wed, 05 Oct 2022 00:02:02 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:31:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:31:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:31:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:31:39 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:31:40 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:31:41 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:31:42 GMT
ENV ROS_DISTRO=melodic
# Wed, 05 Oct 2022 13:33:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:33:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 13:33:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:33:08 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:33:34 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:33:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:34:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0e9b69cf8198dafe5b7db1eee7b96b96238f8346ec641dd44f961f7996c2c152`  
		Last Modified: Wed, 05 Oct 2022 00:03:33 GMT  
		Size: 23.7 MB (23734594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe90d911d5615b705080d27fba0823b4f14f420d2d26ab56026456d57781d53`  
		Last Modified: Wed, 05 Oct 2022 14:06:42 GMT  
		Size: 831.4 KB (831396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31110fc43a4ce01227dd0a0453f904b221bd482dc4c0301b8ffa501b18ea30e`  
		Last Modified: Wed, 05 Oct 2022 14:06:40 GMT  
		Size: 4.3 MB (4265721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7365507dba87454ad0733144061a0542a771b554c28c0b8ebec0b48db8f8678c`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13820d6a8f15395e7f0229f1db78a33b5cab7627627dcf05a9f5aa25cc4c88a`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d3e83df9803da355f686ea14320ce21fd16f2d1d493aa0c23027119f31892e`  
		Last Modified: Wed, 05 Oct 2022 14:07:15 GMT  
		Size: 252.5 MB (252503449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13927152bbda1f9e5e4da3f8f076eeb25177cb22e6347a12dbb859a375a5dfaa`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb232301a9cb5bd90e93d2d742551234aab484877099d191004e68fd52c2939`  
		Last Modified: Wed, 05 Oct 2022 14:07:35 GMT  
		Size: 63.1 MB (63088887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e697dcc64c80657eb9b8cd7f3245242a6c1aa2c256512e00dc7a0b01c50e004`  
		Last Modified: Wed, 05 Oct 2022 14:07:26 GMT  
		Size: 287.6 KB (287598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0588145aba131c45bb37457b2bce2eb15ff97b20dc08c8706f0073a5940b0a37`  
		Last Modified: Wed, 05 Oct 2022 14:07:37 GMT  
		Size: 67.0 MB (66998442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-perception`

```console
$ docker pull ros@sha256:2d9a85cdacefd8d8ebbf360164061826e95fc3c15d91d4b1ea4ef2cbd62dfbff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-perception` - linux; amd64

```console
$ docker pull ros@sha256:760356bd129ecac893a2c56afe72c845c57258ec8d238e58be69eef50afcce0b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.9 MB (742894003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0abbf16914f8244ac1927554743a188b63ed7ab5c73d268af3cce4073bf7d27`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:28 GMT
ADD file:fc5d658c47ede58827812b75a311353be776e41e2dd339b8906839527c9b5247 in / 
# Tue, 25 Oct 2022 01:53:28 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:51:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 06:51:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 06:55:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:55:51 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 06:55:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 06:55:51 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:56:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:56:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 06:58:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a404e54162968593b8d92b571f3cdd673e4c9eab5d9be28d7c494595c0aa6682`  
		Last Modified: Wed, 19 Oct 2022 22:03:02 GMT  
		Size: 26.7 MB (26712500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1955214fb5b152d9d9fa8ce9a39b19a4e6e8ea487bc617e76c0b7b33e1881bc`  
		Last Modified: Tue, 25 Oct 2022 07:50:06 GMT  
		Size: 831.1 KB (831118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b389880aa1534b94319b44ef0d7e8e52ae108ec326dc1efe1cf0e4e749a4190a`  
		Last Modified: Tue, 25 Oct 2022 07:50:04 GMT  
		Size: 4.9 MB (4877285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db68a36d4b9f8fa036da9f0c51e74b6d27dffd9d39317f42638ee84b29322668`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b325e4aad15f84b511f749de8e3b84dc88f98909bbfdd1961ac0e84f7d273f16`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ad76754b2b5a9699fc604ac8d1393dd3d6dfe21df82c8e930da67ffd6f6708`  
		Last Modified: Tue, 25 Oct 2022 07:50:52 GMT  
		Size: 259.6 MB (259567997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1318baf5e3f70ccdc707f97c58bf69e65917aadaa98ec26b67d1d2695572fa`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb834ce8392143178e871793c61a9bd2ac4e34031627b0f8d8453a1f1d836a1`  
		Last Modified: Tue, 25 Oct 2022 07:51:13 GMT  
		Size: 70.3 MB (70260436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874278d4c37ef6d13abdb486dd6dfd9900b104ad68492eb5ba5df13c5c947b37`  
		Last Modified: Tue, 25 Oct 2022 07:51:03 GMT  
		Size: 289.2 KB (289160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5236595b9f2b064d0593cf222d04423eaa11b12eaa5c8e78974d822f22c23287`  
		Last Modified: Tue, 25 Oct 2022 07:51:19 GMT  
		Size: 75.0 MB (74998649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5938790ff52815fa00897b4584fc3cff933821fac6b497b443f30e51552f900e`  
		Last Modified: Tue, 25 Oct 2022 07:52:42 GMT  
		Size: 305.4 MB (305355012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:d4a2aed0652e148c3323aaf63d7bdbec3ab1a6cd6d46d0b5c259509134524bd3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **646.0 MB (646023839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cf1034097743a12d2ccc90d1828450af36facdf6c4a85c762d45f098854d328`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:31 GMT
ADD file:20e0d71059d38b1e18636b9db71f534d7297c3f571d73d45a75b4b8d3cac86c7 in / 
# Wed, 05 Oct 2022 00:13:32 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:46:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:46:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV ROS_DISTRO=melodic
# Thu, 06 Oct 2022 06:48:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:48:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:48:10 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:48:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:49:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:51:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:91bb9a9844d67fd31f07ebd74dc8a4f4f18e2f959d3aa2166aca86ae57f353c6`  
		Last Modified: Wed, 05 Oct 2022 00:15:26 GMT  
		Size: 22.3 MB (22305721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f25a09f0aff0cba5b24d07bd5b4c417734fbce77148b7b62042ac54dc95c068`  
		Last Modified: Thu, 06 Oct 2022 06:58:00 GMT  
		Size: 831.1 KB (831144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14397641aa51f3c3aa6ed2c352f3417b3bce0ebaca231e20759c931e3fe38560`  
		Last Modified: Thu, 06 Oct 2022 06:57:58 GMT  
		Size: 4.1 MB (4087217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a2d98c80683d1808b546f8ca1a247aecedcea1e9d2460d95343238dfabc896`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670273ddac9f5d6d6c7da9986d18661e88bbbc0126833dcd54f90992f9c9484d`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6664b634c5bf87720b15e47366d33bea9fefdd0032f110f86c336e5ae31a0e`  
		Last Modified: Thu, 06 Oct 2022 06:58:45 GMT  
		Size: 239.0 MB (239013225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074569eb7528b8c52dc9fd001aac258a83c59faaf1830e646c00899e79c3a889`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c925a21a964fb8486223de78f9a2d457f125c75f70114336548d871ef3aa6e97`  
		Last Modified: Thu, 06 Oct 2022 06:59:08 GMT  
		Size: 54.7 MB (54719854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176e6a18e2f88225c6c13f76a00ecd1530583b434fa9c482eee0a2179245adbd`  
		Last Modified: Thu, 06 Oct 2022 06:58:57 GMT  
		Size: 287.8 KB (287786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ace293972247ef40871f854b48d8ab1be13f2c1d04bc8c2d37a6be30a82a5e`  
		Last Modified: Thu, 06 Oct 2022 06:59:13 GMT  
		Size: 64.7 MB (64747626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b175cc34aa53aebf1e1d4adce550c8bce2cfb95ce33879a16e5f7646f701ba`  
		Last Modified: Thu, 06 Oct 2022 07:00:25 GMT  
		Size: 260.0 MB (260029419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:eaa3e6c56b18db14d30b5265127199964e86711e794ce6a97aff1f673eeecd80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.1 MB (703134850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16a4e6250b3ceb7ce4597efc02b57f3294d8c0f4a5fea3810b2703f925606b8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:02 GMT
ADD file:4beae13e1fd7bb92776c08a5cd95feb81b8b3c80522ed8513f2441adfb1661ac in / 
# Wed, 05 Oct 2022 00:02:02 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:31:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:31:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:31:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:31:39 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:31:40 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:31:41 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:31:42 GMT
ENV ROS_DISTRO=melodic
# Wed, 05 Oct 2022 13:33:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:33:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 13:33:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:33:08 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:33:34 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:33:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:34:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0e9b69cf8198dafe5b7db1eee7b96b96238f8346ec641dd44f961f7996c2c152`  
		Last Modified: Wed, 05 Oct 2022 00:03:33 GMT  
		Size: 23.7 MB (23734594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe90d911d5615b705080d27fba0823b4f14f420d2d26ab56026456d57781d53`  
		Last Modified: Wed, 05 Oct 2022 14:06:42 GMT  
		Size: 831.4 KB (831396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31110fc43a4ce01227dd0a0453f904b221bd482dc4c0301b8ffa501b18ea30e`  
		Last Modified: Wed, 05 Oct 2022 14:06:40 GMT  
		Size: 4.3 MB (4265721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7365507dba87454ad0733144061a0542a771b554c28c0b8ebec0b48db8f8678c`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13820d6a8f15395e7f0229f1db78a33b5cab7627627dcf05a9f5aa25cc4c88a`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d3e83df9803da355f686ea14320ce21fd16f2d1d493aa0c23027119f31892e`  
		Last Modified: Wed, 05 Oct 2022 14:07:15 GMT  
		Size: 252.5 MB (252503449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13927152bbda1f9e5e4da3f8f076eeb25177cb22e6347a12dbb859a375a5dfaa`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb232301a9cb5bd90e93d2d742551234aab484877099d191004e68fd52c2939`  
		Last Modified: Wed, 05 Oct 2022 14:07:35 GMT  
		Size: 63.1 MB (63088887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e697dcc64c80657eb9b8cd7f3245242a6c1aa2c256512e00dc7a0b01c50e004`  
		Last Modified: Wed, 05 Oct 2022 14:07:26 GMT  
		Size: 287.6 KB (287598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0588145aba131c45bb37457b2bce2eb15ff97b20dc08c8706f0073a5940b0a37`  
		Last Modified: Wed, 05 Oct 2022 14:07:37 GMT  
		Size: 67.0 MB (66998442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af2ce573d6bfab6526367347a90aac300a82c56c3b392c9271d4d28c9a4303c`  
		Last Modified: Wed, 05 Oct 2022 14:08:48 GMT  
		Size: 291.4 MB (291422963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-perception-bionic`

```console
$ docker pull ros@sha256:2d9a85cdacefd8d8ebbf360164061826e95fc3c15d91d4b1ea4ef2cbd62dfbff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-perception-bionic` - linux; amd64

```console
$ docker pull ros@sha256:760356bd129ecac893a2c56afe72c845c57258ec8d238e58be69eef50afcce0b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.9 MB (742894003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0abbf16914f8244ac1927554743a188b63ed7ab5c73d268af3cce4073bf7d27`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:28 GMT
ADD file:fc5d658c47ede58827812b75a311353be776e41e2dd339b8906839527c9b5247 in / 
# Tue, 25 Oct 2022 01:53:28 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:51:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 06:51:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 06:55:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:55:51 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 06:55:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 06:55:51 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:56:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:56:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 06:58:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a404e54162968593b8d92b571f3cdd673e4c9eab5d9be28d7c494595c0aa6682`  
		Last Modified: Wed, 19 Oct 2022 22:03:02 GMT  
		Size: 26.7 MB (26712500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1955214fb5b152d9d9fa8ce9a39b19a4e6e8ea487bc617e76c0b7b33e1881bc`  
		Last Modified: Tue, 25 Oct 2022 07:50:06 GMT  
		Size: 831.1 KB (831118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b389880aa1534b94319b44ef0d7e8e52ae108ec326dc1efe1cf0e4e749a4190a`  
		Last Modified: Tue, 25 Oct 2022 07:50:04 GMT  
		Size: 4.9 MB (4877285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db68a36d4b9f8fa036da9f0c51e74b6d27dffd9d39317f42638ee84b29322668`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b325e4aad15f84b511f749de8e3b84dc88f98909bbfdd1961ac0e84f7d273f16`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ad76754b2b5a9699fc604ac8d1393dd3d6dfe21df82c8e930da67ffd6f6708`  
		Last Modified: Tue, 25 Oct 2022 07:50:52 GMT  
		Size: 259.6 MB (259567997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1318baf5e3f70ccdc707f97c58bf69e65917aadaa98ec26b67d1d2695572fa`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb834ce8392143178e871793c61a9bd2ac4e34031627b0f8d8453a1f1d836a1`  
		Last Modified: Tue, 25 Oct 2022 07:51:13 GMT  
		Size: 70.3 MB (70260436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874278d4c37ef6d13abdb486dd6dfd9900b104ad68492eb5ba5df13c5c947b37`  
		Last Modified: Tue, 25 Oct 2022 07:51:03 GMT  
		Size: 289.2 KB (289160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5236595b9f2b064d0593cf222d04423eaa11b12eaa5c8e78974d822f22c23287`  
		Last Modified: Tue, 25 Oct 2022 07:51:19 GMT  
		Size: 75.0 MB (74998649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5938790ff52815fa00897b4584fc3cff933821fac6b497b443f30e51552f900e`  
		Last Modified: Tue, 25 Oct 2022 07:52:42 GMT  
		Size: 305.4 MB (305355012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:d4a2aed0652e148c3323aaf63d7bdbec3ab1a6cd6d46d0b5c259509134524bd3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **646.0 MB (646023839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cf1034097743a12d2ccc90d1828450af36facdf6c4a85c762d45f098854d328`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:31 GMT
ADD file:20e0d71059d38b1e18636b9db71f534d7297c3f571d73d45a75b4b8d3cac86c7 in / 
# Wed, 05 Oct 2022 00:13:32 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:46:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:46:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV ROS_DISTRO=melodic
# Thu, 06 Oct 2022 06:48:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:48:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:48:10 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:48:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:49:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:51:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:91bb9a9844d67fd31f07ebd74dc8a4f4f18e2f959d3aa2166aca86ae57f353c6`  
		Last Modified: Wed, 05 Oct 2022 00:15:26 GMT  
		Size: 22.3 MB (22305721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f25a09f0aff0cba5b24d07bd5b4c417734fbce77148b7b62042ac54dc95c068`  
		Last Modified: Thu, 06 Oct 2022 06:58:00 GMT  
		Size: 831.1 KB (831144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14397641aa51f3c3aa6ed2c352f3417b3bce0ebaca231e20759c931e3fe38560`  
		Last Modified: Thu, 06 Oct 2022 06:57:58 GMT  
		Size: 4.1 MB (4087217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a2d98c80683d1808b546f8ca1a247aecedcea1e9d2460d95343238dfabc896`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670273ddac9f5d6d6c7da9986d18661e88bbbc0126833dcd54f90992f9c9484d`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6664b634c5bf87720b15e47366d33bea9fefdd0032f110f86c336e5ae31a0e`  
		Last Modified: Thu, 06 Oct 2022 06:58:45 GMT  
		Size: 239.0 MB (239013225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074569eb7528b8c52dc9fd001aac258a83c59faaf1830e646c00899e79c3a889`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c925a21a964fb8486223de78f9a2d457f125c75f70114336548d871ef3aa6e97`  
		Last Modified: Thu, 06 Oct 2022 06:59:08 GMT  
		Size: 54.7 MB (54719854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176e6a18e2f88225c6c13f76a00ecd1530583b434fa9c482eee0a2179245adbd`  
		Last Modified: Thu, 06 Oct 2022 06:58:57 GMT  
		Size: 287.8 KB (287786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ace293972247ef40871f854b48d8ab1be13f2c1d04bc8c2d37a6be30a82a5e`  
		Last Modified: Thu, 06 Oct 2022 06:59:13 GMT  
		Size: 64.7 MB (64747626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b175cc34aa53aebf1e1d4adce550c8bce2cfb95ce33879a16e5f7646f701ba`  
		Last Modified: Thu, 06 Oct 2022 07:00:25 GMT  
		Size: 260.0 MB (260029419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:eaa3e6c56b18db14d30b5265127199964e86711e794ce6a97aff1f673eeecd80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.1 MB (703134850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16a4e6250b3ceb7ce4597efc02b57f3294d8c0f4a5fea3810b2703f925606b8`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:02 GMT
ADD file:4beae13e1fd7bb92776c08a5cd95feb81b8b3c80522ed8513f2441adfb1661ac in / 
# Wed, 05 Oct 2022 00:02:02 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:31:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:31:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:31:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:31:39 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:31:40 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:31:41 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:31:42 GMT
ENV ROS_DISTRO=melodic
# Wed, 05 Oct 2022 13:33:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:33:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 13:33:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:33:08 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:33:34 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:33:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:34:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0e9b69cf8198dafe5b7db1eee7b96b96238f8346ec641dd44f961f7996c2c152`  
		Last Modified: Wed, 05 Oct 2022 00:03:33 GMT  
		Size: 23.7 MB (23734594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe90d911d5615b705080d27fba0823b4f14f420d2d26ab56026456d57781d53`  
		Last Modified: Wed, 05 Oct 2022 14:06:42 GMT  
		Size: 831.4 KB (831396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31110fc43a4ce01227dd0a0453f904b221bd482dc4c0301b8ffa501b18ea30e`  
		Last Modified: Wed, 05 Oct 2022 14:06:40 GMT  
		Size: 4.3 MB (4265721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7365507dba87454ad0733144061a0542a771b554c28c0b8ebec0b48db8f8678c`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13820d6a8f15395e7f0229f1db78a33b5cab7627627dcf05a9f5aa25cc4c88a`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d3e83df9803da355f686ea14320ce21fd16f2d1d493aa0c23027119f31892e`  
		Last Modified: Wed, 05 Oct 2022 14:07:15 GMT  
		Size: 252.5 MB (252503449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13927152bbda1f9e5e4da3f8f076eeb25177cb22e6347a12dbb859a375a5dfaa`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb232301a9cb5bd90e93d2d742551234aab484877099d191004e68fd52c2939`  
		Last Modified: Wed, 05 Oct 2022 14:07:35 GMT  
		Size: 63.1 MB (63088887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e697dcc64c80657eb9b8cd7f3245242a6c1aa2c256512e00dc7a0b01c50e004`  
		Last Modified: Wed, 05 Oct 2022 14:07:26 GMT  
		Size: 287.6 KB (287598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0588145aba131c45bb37457b2bce2eb15ff97b20dc08c8706f0073a5940b0a37`  
		Last Modified: Wed, 05 Oct 2022 14:07:37 GMT  
		Size: 67.0 MB (66998442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6af2ce573d6bfab6526367347a90aac300a82c56c3b392c9271d4d28c9a4303c`  
		Last Modified: Wed, 05 Oct 2022 14:08:48 GMT  
		Size: 291.4 MB (291422963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-robot`

```console
$ docker pull ros@sha256:c422e48d7a2215440c557bd90b8b5b1e7d23894fbaa59c9aad0f6e119d67d779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-robot` - linux; amd64

```console
$ docker pull ros@sha256:7fb936bf3f4c1f768981550fbafaa6e7b7b43f00d4d95b05798c4f78962cb349
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.6 MB (448624983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56880250050883f30db34a14ba89363854f201ded84b8f75d95611f26b8a787`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:28 GMT
ADD file:fc5d658c47ede58827812b75a311353be776e41e2dd339b8906839527c9b5247 in / 
# Tue, 25 Oct 2022 01:53:28 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:51:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 06:51:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 06:55:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:55:51 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 06:55:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 06:55:51 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:56:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:56:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 06:58:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a404e54162968593b8d92b571f3cdd673e4c9eab5d9be28d7c494595c0aa6682`  
		Last Modified: Wed, 19 Oct 2022 22:03:02 GMT  
		Size: 26.7 MB (26712500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1955214fb5b152d9d9fa8ce9a39b19a4e6e8ea487bc617e76c0b7b33e1881bc`  
		Last Modified: Tue, 25 Oct 2022 07:50:06 GMT  
		Size: 831.1 KB (831118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b389880aa1534b94319b44ef0d7e8e52ae108ec326dc1efe1cf0e4e749a4190a`  
		Last Modified: Tue, 25 Oct 2022 07:50:04 GMT  
		Size: 4.9 MB (4877285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db68a36d4b9f8fa036da9f0c51e74b6d27dffd9d39317f42638ee84b29322668`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b325e4aad15f84b511f749de8e3b84dc88f98909bbfdd1961ac0e84f7d273f16`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ad76754b2b5a9699fc604ac8d1393dd3d6dfe21df82c8e930da67ffd6f6708`  
		Last Modified: Tue, 25 Oct 2022 07:50:52 GMT  
		Size: 259.6 MB (259567997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1318baf5e3f70ccdc707f97c58bf69e65917aadaa98ec26b67d1d2695572fa`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb834ce8392143178e871793c61a9bd2ac4e34031627b0f8d8453a1f1d836a1`  
		Last Modified: Tue, 25 Oct 2022 07:51:13 GMT  
		Size: 70.3 MB (70260436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874278d4c37ef6d13abdb486dd6dfd9900b104ad68492eb5ba5df13c5c947b37`  
		Last Modified: Tue, 25 Oct 2022 07:51:03 GMT  
		Size: 289.2 KB (289160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5236595b9f2b064d0593cf222d04423eaa11b12eaa5c8e78974d822f22c23287`  
		Last Modified: Tue, 25 Oct 2022 07:51:19 GMT  
		Size: 75.0 MB (74998649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04787df350a9858b29dcd5d866d17be1b134ac05697019c51a96201ec3a86463`  
		Last Modified: Tue, 25 Oct 2022 07:51:34 GMT  
		Size: 11.1 MB (11085992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:f41d68e783b7d250adc47fdf91c2d70b5bf9549309e96c6a3aeff32e79def5ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.1 MB (396117676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032becfc9cbe10179ba32714f7356484cde7fb78dd08f85f8380cc46ca85a675`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:31 GMT
ADD file:20e0d71059d38b1e18636b9db71f534d7297c3f571d73d45a75b4b8d3cac86c7 in / 
# Wed, 05 Oct 2022 00:13:32 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:46:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:46:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV ROS_DISTRO=melodic
# Thu, 06 Oct 2022 06:48:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:48:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:48:10 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:48:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:49:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:91bb9a9844d67fd31f07ebd74dc8a4f4f18e2f959d3aa2166aca86ae57f353c6`  
		Last Modified: Wed, 05 Oct 2022 00:15:26 GMT  
		Size: 22.3 MB (22305721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f25a09f0aff0cba5b24d07bd5b4c417734fbce77148b7b62042ac54dc95c068`  
		Last Modified: Thu, 06 Oct 2022 06:58:00 GMT  
		Size: 831.1 KB (831144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14397641aa51f3c3aa6ed2c352f3417b3bce0ebaca231e20759c931e3fe38560`  
		Last Modified: Thu, 06 Oct 2022 06:57:58 GMT  
		Size: 4.1 MB (4087217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a2d98c80683d1808b546f8ca1a247aecedcea1e9d2460d95343238dfabc896`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670273ddac9f5d6d6c7da9986d18661e88bbbc0126833dcd54f90992f9c9484d`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6664b634c5bf87720b15e47366d33bea9fefdd0032f110f86c336e5ae31a0e`  
		Last Modified: Thu, 06 Oct 2022 06:58:45 GMT  
		Size: 239.0 MB (239013225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074569eb7528b8c52dc9fd001aac258a83c59faaf1830e646c00899e79c3a889`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c925a21a964fb8486223de78f9a2d457f125c75f70114336548d871ef3aa6e97`  
		Last Modified: Thu, 06 Oct 2022 06:59:08 GMT  
		Size: 54.7 MB (54719854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176e6a18e2f88225c6c13f76a00ecd1530583b434fa9c482eee0a2179245adbd`  
		Last Modified: Thu, 06 Oct 2022 06:58:57 GMT  
		Size: 287.8 KB (287786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ace293972247ef40871f854b48d8ab1be13f2c1d04bc8c2d37a6be30a82a5e`  
		Last Modified: Thu, 06 Oct 2022 06:59:13 GMT  
		Size: 64.7 MB (64747626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335010a557901b56ebbeceac85af817dc563c72e83fe5f3c9d82d92e761187fe`  
		Last Modified: Thu, 06 Oct 2022 06:59:30 GMT  
		Size: 10.1 MB (10123256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6af49c17eb45365833a3015658f71db8cb1496edd7c4196ca5d44baf8cc6bae9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.4 MB (422447622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21b2b650b73f497fe2b2d6860d64416bf68f4185a20ce627275830641d309d5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:02 GMT
ADD file:4beae13e1fd7bb92776c08a5cd95feb81b8b3c80522ed8513f2441adfb1661ac in / 
# Wed, 05 Oct 2022 00:02:02 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:31:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:31:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:31:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:31:39 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:31:40 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:31:41 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:31:42 GMT
ENV ROS_DISTRO=melodic
# Wed, 05 Oct 2022 13:33:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:33:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 13:33:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:33:08 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:33:34 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:33:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:34:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:34:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0e9b69cf8198dafe5b7db1eee7b96b96238f8346ec641dd44f961f7996c2c152`  
		Last Modified: Wed, 05 Oct 2022 00:03:33 GMT  
		Size: 23.7 MB (23734594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe90d911d5615b705080d27fba0823b4f14f420d2d26ab56026456d57781d53`  
		Last Modified: Wed, 05 Oct 2022 14:06:42 GMT  
		Size: 831.4 KB (831396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31110fc43a4ce01227dd0a0453f904b221bd482dc4c0301b8ffa501b18ea30e`  
		Last Modified: Wed, 05 Oct 2022 14:06:40 GMT  
		Size: 4.3 MB (4265721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7365507dba87454ad0733144061a0542a771b554c28c0b8ebec0b48db8f8678c`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13820d6a8f15395e7f0229f1db78a33b5cab7627627dcf05a9f5aa25cc4c88a`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d3e83df9803da355f686ea14320ce21fd16f2d1d493aa0c23027119f31892e`  
		Last Modified: Wed, 05 Oct 2022 14:07:15 GMT  
		Size: 252.5 MB (252503449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13927152bbda1f9e5e4da3f8f076eeb25177cb22e6347a12dbb859a375a5dfaa`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb232301a9cb5bd90e93d2d742551234aab484877099d191004e68fd52c2939`  
		Last Modified: Wed, 05 Oct 2022 14:07:35 GMT  
		Size: 63.1 MB (63088887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e697dcc64c80657eb9b8cd7f3245242a6c1aa2c256512e00dc7a0b01c50e004`  
		Last Modified: Wed, 05 Oct 2022 14:07:26 GMT  
		Size: 287.6 KB (287598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0588145aba131c45bb37457b2bce2eb15ff97b20dc08c8706f0073a5940b0a37`  
		Last Modified: Wed, 05 Oct 2022 14:07:37 GMT  
		Size: 67.0 MB (66998442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b70eebce05e703acd0e9cd6a52e2061058ce5b16d05bde10bafa746e1109bd5`  
		Last Modified: Wed, 05 Oct 2022 14:07:54 GMT  
		Size: 10.7 MB (10735735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-robot-bionic`

```console
$ docker pull ros@sha256:c422e48d7a2215440c557bd90b8b5b1e7d23894fbaa59c9aad0f6e119d67d779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-robot-bionic` - linux; amd64

```console
$ docker pull ros@sha256:7fb936bf3f4c1f768981550fbafaa6e7b7b43f00d4d95b05798c4f78962cb349
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.6 MB (448624983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56880250050883f30db34a14ba89363854f201ded84b8f75d95611f26b8a787`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:28 GMT
ADD file:fc5d658c47ede58827812b75a311353be776e41e2dd339b8906839527c9b5247 in / 
# Tue, 25 Oct 2022 01:53:28 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:51:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 06:51:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 06:55:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:55:51 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 06:55:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 06:55:51 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:56:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:56:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 06:58:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a404e54162968593b8d92b571f3cdd673e4c9eab5d9be28d7c494595c0aa6682`  
		Last Modified: Wed, 19 Oct 2022 22:03:02 GMT  
		Size: 26.7 MB (26712500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1955214fb5b152d9d9fa8ce9a39b19a4e6e8ea487bc617e76c0b7b33e1881bc`  
		Last Modified: Tue, 25 Oct 2022 07:50:06 GMT  
		Size: 831.1 KB (831118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b389880aa1534b94319b44ef0d7e8e52ae108ec326dc1efe1cf0e4e749a4190a`  
		Last Modified: Tue, 25 Oct 2022 07:50:04 GMT  
		Size: 4.9 MB (4877285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db68a36d4b9f8fa036da9f0c51e74b6d27dffd9d39317f42638ee84b29322668`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b325e4aad15f84b511f749de8e3b84dc88f98909bbfdd1961ac0e84f7d273f16`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ad76754b2b5a9699fc604ac8d1393dd3d6dfe21df82c8e930da67ffd6f6708`  
		Last Modified: Tue, 25 Oct 2022 07:50:52 GMT  
		Size: 259.6 MB (259567997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1318baf5e3f70ccdc707f97c58bf69e65917aadaa98ec26b67d1d2695572fa`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb834ce8392143178e871793c61a9bd2ac4e34031627b0f8d8453a1f1d836a1`  
		Last Modified: Tue, 25 Oct 2022 07:51:13 GMT  
		Size: 70.3 MB (70260436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874278d4c37ef6d13abdb486dd6dfd9900b104ad68492eb5ba5df13c5c947b37`  
		Last Modified: Tue, 25 Oct 2022 07:51:03 GMT  
		Size: 289.2 KB (289160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5236595b9f2b064d0593cf222d04423eaa11b12eaa5c8e78974d822f22c23287`  
		Last Modified: Tue, 25 Oct 2022 07:51:19 GMT  
		Size: 75.0 MB (74998649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04787df350a9858b29dcd5d866d17be1b134ac05697019c51a96201ec3a86463`  
		Last Modified: Tue, 25 Oct 2022 07:51:34 GMT  
		Size: 11.1 MB (11085992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:f41d68e783b7d250adc47fdf91c2d70b5bf9549309e96c6a3aeff32e79def5ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.1 MB (396117676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032becfc9cbe10179ba32714f7356484cde7fb78dd08f85f8380cc46ca85a675`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:31 GMT
ADD file:20e0d71059d38b1e18636b9db71f534d7297c3f571d73d45a75b4b8d3cac86c7 in / 
# Wed, 05 Oct 2022 00:13:32 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:46:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:46:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV ROS_DISTRO=melodic
# Thu, 06 Oct 2022 06:48:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:48:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:48:10 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:48:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:49:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:49:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:91bb9a9844d67fd31f07ebd74dc8a4f4f18e2f959d3aa2166aca86ae57f353c6`  
		Last Modified: Wed, 05 Oct 2022 00:15:26 GMT  
		Size: 22.3 MB (22305721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f25a09f0aff0cba5b24d07bd5b4c417734fbce77148b7b62042ac54dc95c068`  
		Last Modified: Thu, 06 Oct 2022 06:58:00 GMT  
		Size: 831.1 KB (831144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14397641aa51f3c3aa6ed2c352f3417b3bce0ebaca231e20759c931e3fe38560`  
		Last Modified: Thu, 06 Oct 2022 06:57:58 GMT  
		Size: 4.1 MB (4087217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a2d98c80683d1808b546f8ca1a247aecedcea1e9d2460d95343238dfabc896`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670273ddac9f5d6d6c7da9986d18661e88bbbc0126833dcd54f90992f9c9484d`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6664b634c5bf87720b15e47366d33bea9fefdd0032f110f86c336e5ae31a0e`  
		Last Modified: Thu, 06 Oct 2022 06:58:45 GMT  
		Size: 239.0 MB (239013225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074569eb7528b8c52dc9fd001aac258a83c59faaf1830e646c00899e79c3a889`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c925a21a964fb8486223de78f9a2d457f125c75f70114336548d871ef3aa6e97`  
		Last Modified: Thu, 06 Oct 2022 06:59:08 GMT  
		Size: 54.7 MB (54719854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176e6a18e2f88225c6c13f76a00ecd1530583b434fa9c482eee0a2179245adbd`  
		Last Modified: Thu, 06 Oct 2022 06:58:57 GMT  
		Size: 287.8 KB (287786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ace293972247ef40871f854b48d8ab1be13f2c1d04bc8c2d37a6be30a82a5e`  
		Last Modified: Thu, 06 Oct 2022 06:59:13 GMT  
		Size: 64.7 MB (64747626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335010a557901b56ebbeceac85af817dc563c72e83fe5f3c9d82d92e761187fe`  
		Last Modified: Thu, 06 Oct 2022 06:59:30 GMT  
		Size: 10.1 MB (10123256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:6af49c17eb45365833a3015658f71db8cb1496edd7c4196ca5d44baf8cc6bae9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.4 MB (422447622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a21b2b650b73f497fe2b2d6860d64416bf68f4185a20ce627275830641d309d5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:02 GMT
ADD file:4beae13e1fd7bb92776c08a5cd95feb81b8b3c80522ed8513f2441adfb1661ac in / 
# Wed, 05 Oct 2022 00:02:02 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:31:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:31:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:31:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:31:39 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:31:40 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:31:41 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:31:42 GMT
ENV ROS_DISTRO=melodic
# Wed, 05 Oct 2022 13:33:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:33:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 13:33:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:33:08 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:33:34 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:33:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:34:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:34:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0e9b69cf8198dafe5b7db1eee7b96b96238f8346ec641dd44f961f7996c2c152`  
		Last Modified: Wed, 05 Oct 2022 00:03:33 GMT  
		Size: 23.7 MB (23734594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe90d911d5615b705080d27fba0823b4f14f420d2d26ab56026456d57781d53`  
		Last Modified: Wed, 05 Oct 2022 14:06:42 GMT  
		Size: 831.4 KB (831396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31110fc43a4ce01227dd0a0453f904b221bd482dc4c0301b8ffa501b18ea30e`  
		Last Modified: Wed, 05 Oct 2022 14:06:40 GMT  
		Size: 4.3 MB (4265721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7365507dba87454ad0733144061a0542a771b554c28c0b8ebec0b48db8f8678c`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13820d6a8f15395e7f0229f1db78a33b5cab7627627dcf05a9f5aa25cc4c88a`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d3e83df9803da355f686ea14320ce21fd16f2d1d493aa0c23027119f31892e`  
		Last Modified: Wed, 05 Oct 2022 14:07:15 GMT  
		Size: 252.5 MB (252503449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13927152bbda1f9e5e4da3f8f076eeb25177cb22e6347a12dbb859a375a5dfaa`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb232301a9cb5bd90e93d2d742551234aab484877099d191004e68fd52c2939`  
		Last Modified: Wed, 05 Oct 2022 14:07:35 GMT  
		Size: 63.1 MB (63088887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e697dcc64c80657eb9b8cd7f3245242a6c1aa2c256512e00dc7a0b01c50e004`  
		Last Modified: Wed, 05 Oct 2022 14:07:26 GMT  
		Size: 287.6 KB (287598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0588145aba131c45bb37457b2bce2eb15ff97b20dc08c8706f0073a5940b0a37`  
		Last Modified: Wed, 05 Oct 2022 14:07:37 GMT  
		Size: 67.0 MB (66998442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b70eebce05e703acd0e9cd6a52e2061058ce5b16d05bde10bafa746e1109bd5`  
		Last Modified: Wed, 05 Oct 2022 14:07:54 GMT  
		Size: 10.7 MB (10735735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-base`

```console
$ docker pull ros@sha256:ecf84b223a21ae4bc5dbeb24ff850fc8963031e00bd67121cdaf99b4f898c083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:a7201ea28800aff6b84b5fc7ab4fd80b61bc58dc006b9c2cdca6ec7be32cf6ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.5 MB (437538991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898998df3ed57ef16b7e130a5148adf56b94754f794c70d6f6b5c670eb939dbf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:28 GMT
ADD file:fc5d658c47ede58827812b75a311353be776e41e2dd339b8906839527c9b5247 in / 
# Tue, 25 Oct 2022 01:53:28 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:51:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 06:51:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 06:55:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:55:51 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 06:55:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 06:55:51 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:56:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:56:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 06:58:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a404e54162968593b8d92b571f3cdd673e4c9eab5d9be28d7c494595c0aa6682`  
		Last Modified: Wed, 19 Oct 2022 22:03:02 GMT  
		Size: 26.7 MB (26712500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1955214fb5b152d9d9fa8ce9a39b19a4e6e8ea487bc617e76c0b7b33e1881bc`  
		Last Modified: Tue, 25 Oct 2022 07:50:06 GMT  
		Size: 831.1 KB (831118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b389880aa1534b94319b44ef0d7e8e52ae108ec326dc1efe1cf0e4e749a4190a`  
		Last Modified: Tue, 25 Oct 2022 07:50:04 GMT  
		Size: 4.9 MB (4877285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db68a36d4b9f8fa036da9f0c51e74b6d27dffd9d39317f42638ee84b29322668`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b325e4aad15f84b511f749de8e3b84dc88f98909bbfdd1961ac0e84f7d273f16`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ad76754b2b5a9699fc604ac8d1393dd3d6dfe21df82c8e930da67ffd6f6708`  
		Last Modified: Tue, 25 Oct 2022 07:50:52 GMT  
		Size: 259.6 MB (259567997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1318baf5e3f70ccdc707f97c58bf69e65917aadaa98ec26b67d1d2695572fa`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb834ce8392143178e871793c61a9bd2ac4e34031627b0f8d8453a1f1d836a1`  
		Last Modified: Tue, 25 Oct 2022 07:51:13 GMT  
		Size: 70.3 MB (70260436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874278d4c37ef6d13abdb486dd6dfd9900b104ad68492eb5ba5df13c5c947b37`  
		Last Modified: Tue, 25 Oct 2022 07:51:03 GMT  
		Size: 289.2 KB (289160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5236595b9f2b064d0593cf222d04423eaa11b12eaa5c8e78974d822f22c23287`  
		Last Modified: Tue, 25 Oct 2022 07:51:19 GMT  
		Size: 75.0 MB (74998649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:a45ac6c100b50466ddc1d7e743fa1245f7fd98846f6029690aea97d10f221e45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.0 MB (385994420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39885270420308b747b47cac016d290e8ce997f48e27902594c0fb48214d0fa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:31 GMT
ADD file:20e0d71059d38b1e18636b9db71f534d7297c3f571d73d45a75b4b8d3cac86c7 in / 
# Wed, 05 Oct 2022 00:13:32 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:46:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:46:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV ROS_DISTRO=melodic
# Thu, 06 Oct 2022 06:48:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:48:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:48:10 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:48:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:49:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:91bb9a9844d67fd31f07ebd74dc8a4f4f18e2f959d3aa2166aca86ae57f353c6`  
		Last Modified: Wed, 05 Oct 2022 00:15:26 GMT  
		Size: 22.3 MB (22305721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f25a09f0aff0cba5b24d07bd5b4c417734fbce77148b7b62042ac54dc95c068`  
		Last Modified: Thu, 06 Oct 2022 06:58:00 GMT  
		Size: 831.1 KB (831144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14397641aa51f3c3aa6ed2c352f3417b3bce0ebaca231e20759c931e3fe38560`  
		Last Modified: Thu, 06 Oct 2022 06:57:58 GMT  
		Size: 4.1 MB (4087217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a2d98c80683d1808b546f8ca1a247aecedcea1e9d2460d95343238dfabc896`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670273ddac9f5d6d6c7da9986d18661e88bbbc0126833dcd54f90992f9c9484d`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6664b634c5bf87720b15e47366d33bea9fefdd0032f110f86c336e5ae31a0e`  
		Last Modified: Thu, 06 Oct 2022 06:58:45 GMT  
		Size: 239.0 MB (239013225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074569eb7528b8c52dc9fd001aac258a83c59faaf1830e646c00899e79c3a889`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c925a21a964fb8486223de78f9a2d457f125c75f70114336548d871ef3aa6e97`  
		Last Modified: Thu, 06 Oct 2022 06:59:08 GMT  
		Size: 54.7 MB (54719854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176e6a18e2f88225c6c13f76a00ecd1530583b434fa9c482eee0a2179245adbd`  
		Last Modified: Thu, 06 Oct 2022 06:58:57 GMT  
		Size: 287.8 KB (287786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ace293972247ef40871f854b48d8ab1be13f2c1d04bc8c2d37a6be30a82a5e`  
		Last Modified: Thu, 06 Oct 2022 06:59:13 GMT  
		Size: 64.7 MB (64747626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4868ca46db01ab9b479444064b3f4b3919442f2de6fb4f78794359e36ffeb1a3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.7 MB (411711887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d006ec586d2e78a0b3c081f1811cfe9cf6ebc2d6e2cec7e0cbbec0e1012473a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:02 GMT
ADD file:4beae13e1fd7bb92776c08a5cd95feb81b8b3c80522ed8513f2441adfb1661ac in / 
# Wed, 05 Oct 2022 00:02:02 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:31:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:31:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:31:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:31:39 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:31:40 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:31:41 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:31:42 GMT
ENV ROS_DISTRO=melodic
# Wed, 05 Oct 2022 13:33:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:33:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 13:33:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:33:08 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:33:34 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:33:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:34:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0e9b69cf8198dafe5b7db1eee7b96b96238f8346ec641dd44f961f7996c2c152`  
		Last Modified: Wed, 05 Oct 2022 00:03:33 GMT  
		Size: 23.7 MB (23734594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe90d911d5615b705080d27fba0823b4f14f420d2d26ab56026456d57781d53`  
		Last Modified: Wed, 05 Oct 2022 14:06:42 GMT  
		Size: 831.4 KB (831396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31110fc43a4ce01227dd0a0453f904b221bd482dc4c0301b8ffa501b18ea30e`  
		Last Modified: Wed, 05 Oct 2022 14:06:40 GMT  
		Size: 4.3 MB (4265721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7365507dba87454ad0733144061a0542a771b554c28c0b8ebec0b48db8f8678c`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13820d6a8f15395e7f0229f1db78a33b5cab7627627dcf05a9f5aa25cc4c88a`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d3e83df9803da355f686ea14320ce21fd16f2d1d493aa0c23027119f31892e`  
		Last Modified: Wed, 05 Oct 2022 14:07:15 GMT  
		Size: 252.5 MB (252503449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13927152bbda1f9e5e4da3f8f076eeb25177cb22e6347a12dbb859a375a5dfaa`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb232301a9cb5bd90e93d2d742551234aab484877099d191004e68fd52c2939`  
		Last Modified: Wed, 05 Oct 2022 14:07:35 GMT  
		Size: 63.1 MB (63088887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e697dcc64c80657eb9b8cd7f3245242a6c1aa2c256512e00dc7a0b01c50e004`  
		Last Modified: Wed, 05 Oct 2022 14:07:26 GMT  
		Size: 287.6 KB (287598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0588145aba131c45bb37457b2bce2eb15ff97b20dc08c8706f0073a5940b0a37`  
		Last Modified: Wed, 05 Oct 2022 14:07:37 GMT  
		Size: 67.0 MB (66998442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-base-bionic`

```console
$ docker pull ros@sha256:ecf84b223a21ae4bc5dbeb24ff850fc8963031e00bd67121cdaf99b4f898c083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-base-bionic` - linux; amd64

```console
$ docker pull ros@sha256:a7201ea28800aff6b84b5fc7ab4fd80b61bc58dc006b9c2cdca6ec7be32cf6ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.5 MB (437538991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898998df3ed57ef16b7e130a5148adf56b94754f794c70d6f6b5c670eb939dbf`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:28 GMT
ADD file:fc5d658c47ede58827812b75a311353be776e41e2dd339b8906839527c9b5247 in / 
# Tue, 25 Oct 2022 01:53:28 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:51:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 06:51:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 06:55:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:55:51 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 06:55:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 06:55:51 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:56:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:56:43 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 06:58:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a404e54162968593b8d92b571f3cdd673e4c9eab5d9be28d7c494595c0aa6682`  
		Last Modified: Wed, 19 Oct 2022 22:03:02 GMT  
		Size: 26.7 MB (26712500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1955214fb5b152d9d9fa8ce9a39b19a4e6e8ea487bc617e76c0b7b33e1881bc`  
		Last Modified: Tue, 25 Oct 2022 07:50:06 GMT  
		Size: 831.1 KB (831118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b389880aa1534b94319b44ef0d7e8e52ae108ec326dc1efe1cf0e4e749a4190a`  
		Last Modified: Tue, 25 Oct 2022 07:50:04 GMT  
		Size: 4.9 MB (4877285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db68a36d4b9f8fa036da9f0c51e74b6d27dffd9d39317f42638ee84b29322668`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b325e4aad15f84b511f749de8e3b84dc88f98909bbfdd1961ac0e84f7d273f16`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ad76754b2b5a9699fc604ac8d1393dd3d6dfe21df82c8e930da67ffd6f6708`  
		Last Modified: Tue, 25 Oct 2022 07:50:52 GMT  
		Size: 259.6 MB (259567997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1318baf5e3f70ccdc707f97c58bf69e65917aadaa98ec26b67d1d2695572fa`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb834ce8392143178e871793c61a9bd2ac4e34031627b0f8d8453a1f1d836a1`  
		Last Modified: Tue, 25 Oct 2022 07:51:13 GMT  
		Size: 70.3 MB (70260436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874278d4c37ef6d13abdb486dd6dfd9900b104ad68492eb5ba5df13c5c947b37`  
		Last Modified: Tue, 25 Oct 2022 07:51:03 GMT  
		Size: 289.2 KB (289160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5236595b9f2b064d0593cf222d04423eaa11b12eaa5c8e78974d822f22c23287`  
		Last Modified: Tue, 25 Oct 2022 07:51:19 GMT  
		Size: 75.0 MB (74998649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:a45ac6c100b50466ddc1d7e743fa1245f7fd98846f6029690aea97d10f221e45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.0 MB (385994420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b39885270420308b747b47cac016d290e8ce997f48e27902594c0fb48214d0fa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:31 GMT
ADD file:20e0d71059d38b1e18636b9db71f534d7297c3f571d73d45a75b4b8d3cac86c7 in / 
# Wed, 05 Oct 2022 00:13:32 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:46:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:46:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV ROS_DISTRO=melodic
# Thu, 06 Oct 2022 06:48:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:48:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:48:10 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:48:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:49:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:91bb9a9844d67fd31f07ebd74dc8a4f4f18e2f959d3aa2166aca86ae57f353c6`  
		Last Modified: Wed, 05 Oct 2022 00:15:26 GMT  
		Size: 22.3 MB (22305721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f25a09f0aff0cba5b24d07bd5b4c417734fbce77148b7b62042ac54dc95c068`  
		Last Modified: Thu, 06 Oct 2022 06:58:00 GMT  
		Size: 831.1 KB (831144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14397641aa51f3c3aa6ed2c352f3417b3bce0ebaca231e20759c931e3fe38560`  
		Last Modified: Thu, 06 Oct 2022 06:57:58 GMT  
		Size: 4.1 MB (4087217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a2d98c80683d1808b546f8ca1a247aecedcea1e9d2460d95343238dfabc896`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670273ddac9f5d6d6c7da9986d18661e88bbbc0126833dcd54f90992f9c9484d`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6664b634c5bf87720b15e47366d33bea9fefdd0032f110f86c336e5ae31a0e`  
		Last Modified: Thu, 06 Oct 2022 06:58:45 GMT  
		Size: 239.0 MB (239013225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074569eb7528b8c52dc9fd001aac258a83c59faaf1830e646c00899e79c3a889`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c925a21a964fb8486223de78f9a2d457f125c75f70114336548d871ef3aa6e97`  
		Last Modified: Thu, 06 Oct 2022 06:59:08 GMT  
		Size: 54.7 MB (54719854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176e6a18e2f88225c6c13f76a00ecd1530583b434fa9c482eee0a2179245adbd`  
		Last Modified: Thu, 06 Oct 2022 06:58:57 GMT  
		Size: 287.8 KB (287786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ace293972247ef40871f854b48d8ab1be13f2c1d04bc8c2d37a6be30a82a5e`  
		Last Modified: Thu, 06 Oct 2022 06:59:13 GMT  
		Size: 64.7 MB (64747626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4868ca46db01ab9b479444064b3f4b3919442f2de6fb4f78794359e36ffeb1a3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.7 MB (411711887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d006ec586d2e78a0b3c081f1811cfe9cf6ebc2d6e2cec7e0cbbec0e1012473a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:02 GMT
ADD file:4beae13e1fd7bb92776c08a5cd95feb81b8b3c80522ed8513f2441adfb1661ac in / 
# Wed, 05 Oct 2022 00:02:02 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:31:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:31:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:31:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:31:39 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:31:40 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:31:41 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:31:42 GMT
ENV ROS_DISTRO=melodic
# Wed, 05 Oct 2022 13:33:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:33:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 13:33:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:33:08 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:33:34 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:33:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:34:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0e9b69cf8198dafe5b7db1eee7b96b96238f8346ec641dd44f961f7996c2c152`  
		Last Modified: Wed, 05 Oct 2022 00:03:33 GMT  
		Size: 23.7 MB (23734594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe90d911d5615b705080d27fba0823b4f14f420d2d26ab56026456d57781d53`  
		Last Modified: Wed, 05 Oct 2022 14:06:42 GMT  
		Size: 831.4 KB (831396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31110fc43a4ce01227dd0a0453f904b221bd482dc4c0301b8ffa501b18ea30e`  
		Last Modified: Wed, 05 Oct 2022 14:06:40 GMT  
		Size: 4.3 MB (4265721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7365507dba87454ad0733144061a0542a771b554c28c0b8ebec0b48db8f8678c`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13820d6a8f15395e7f0229f1db78a33b5cab7627627dcf05a9f5aa25cc4c88a`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d3e83df9803da355f686ea14320ce21fd16f2d1d493aa0c23027119f31892e`  
		Last Modified: Wed, 05 Oct 2022 14:07:15 GMT  
		Size: 252.5 MB (252503449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13927152bbda1f9e5e4da3f8f076eeb25177cb22e6347a12dbb859a375a5dfaa`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb232301a9cb5bd90e93d2d742551234aab484877099d191004e68fd52c2939`  
		Last Modified: Wed, 05 Oct 2022 14:07:35 GMT  
		Size: 63.1 MB (63088887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e697dcc64c80657eb9b8cd7f3245242a6c1aa2c256512e00dc7a0b01c50e004`  
		Last Modified: Wed, 05 Oct 2022 14:07:26 GMT  
		Size: 287.6 KB (287598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0588145aba131c45bb37457b2bce2eb15ff97b20dc08c8706f0073a5940b0a37`  
		Last Modified: Wed, 05 Oct 2022 14:07:37 GMT  
		Size: 67.0 MB (66998442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-core`

```console
$ docker pull ros@sha256:ff83de7776e1d39ad2bd7c38aee5eebcd2f1ad6645da78e208a1816ac89faf7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:4823a905ffe0b3e7d527d857d533d78fc707ace416fed369a38da35f98b535bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (291990746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b750019b37ee79ded291459fd57709578c21c1a3c552e25109bf1f41e0d8dd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:28 GMT
ADD file:fc5d658c47ede58827812b75a311353be776e41e2dd339b8906839527c9b5247 in / 
# Tue, 25 Oct 2022 01:53:28 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:51:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 06:51:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 06:55:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:55:51 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 06:55:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 06:55:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a404e54162968593b8d92b571f3cdd673e4c9eab5d9be28d7c494595c0aa6682`  
		Last Modified: Wed, 19 Oct 2022 22:03:02 GMT  
		Size: 26.7 MB (26712500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1955214fb5b152d9d9fa8ce9a39b19a4e6e8ea487bc617e76c0b7b33e1881bc`  
		Last Modified: Tue, 25 Oct 2022 07:50:06 GMT  
		Size: 831.1 KB (831118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b389880aa1534b94319b44ef0d7e8e52ae108ec326dc1efe1cf0e4e749a4190a`  
		Last Modified: Tue, 25 Oct 2022 07:50:04 GMT  
		Size: 4.9 MB (4877285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db68a36d4b9f8fa036da9f0c51e74b6d27dffd9d39317f42638ee84b29322668`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b325e4aad15f84b511f749de8e3b84dc88f98909bbfdd1961ac0e84f7d273f16`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ad76754b2b5a9699fc604ac8d1393dd3d6dfe21df82c8e930da67ffd6f6708`  
		Last Modified: Tue, 25 Oct 2022 07:50:52 GMT  
		Size: 259.6 MB (259567997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1318baf5e3f70ccdc707f97c58bf69e65917aadaa98ec26b67d1d2695572fa`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:11cbb2f864a289726b9510d1a9b4e6e7414dfacb9a9d782b9d1e4754293f2056
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266239154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d83c28f326a67014793ddf881b3e99269c547c3a86ced293cec9f9fca7d46c0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:31 GMT
ADD file:20e0d71059d38b1e18636b9db71f534d7297c3f571d73d45a75b4b8d3cac86c7 in / 
# Wed, 05 Oct 2022 00:13:32 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:46:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:46:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV ROS_DISTRO=melodic
# Thu, 06 Oct 2022 06:48:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:48:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:48:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:91bb9a9844d67fd31f07ebd74dc8a4f4f18e2f959d3aa2166aca86ae57f353c6`  
		Last Modified: Wed, 05 Oct 2022 00:15:26 GMT  
		Size: 22.3 MB (22305721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f25a09f0aff0cba5b24d07bd5b4c417734fbce77148b7b62042ac54dc95c068`  
		Last Modified: Thu, 06 Oct 2022 06:58:00 GMT  
		Size: 831.1 KB (831144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14397641aa51f3c3aa6ed2c352f3417b3bce0ebaca231e20759c931e3fe38560`  
		Last Modified: Thu, 06 Oct 2022 06:57:58 GMT  
		Size: 4.1 MB (4087217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a2d98c80683d1808b546f8ca1a247aecedcea1e9d2460d95343238dfabc896`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670273ddac9f5d6d6c7da9986d18661e88bbbc0126833dcd54f90992f9c9484d`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6664b634c5bf87720b15e47366d33bea9fefdd0032f110f86c336e5ae31a0e`  
		Last Modified: Thu, 06 Oct 2022 06:58:45 GMT  
		Size: 239.0 MB (239013225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074569eb7528b8c52dc9fd001aac258a83c59faaf1830e646c00899e79c3a889`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1f76867405b52c64167fb70e1f09efb2123122401686455531be3b1a7ac3221e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281336960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b4b42a718b3881e44324b053aea4b4105bf5b40004428e1ca8c85a6a6ec75e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:02 GMT
ADD file:4beae13e1fd7bb92776c08a5cd95feb81b8b3c80522ed8513f2441adfb1661ac in / 
# Wed, 05 Oct 2022 00:02:02 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:31:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:31:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:31:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:31:39 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:31:40 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:31:41 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:31:42 GMT
ENV ROS_DISTRO=melodic
# Wed, 05 Oct 2022 13:33:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:33:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 13:33:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:33:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0e9b69cf8198dafe5b7db1eee7b96b96238f8346ec641dd44f961f7996c2c152`  
		Last Modified: Wed, 05 Oct 2022 00:03:33 GMT  
		Size: 23.7 MB (23734594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe90d911d5615b705080d27fba0823b4f14f420d2d26ab56026456d57781d53`  
		Last Modified: Wed, 05 Oct 2022 14:06:42 GMT  
		Size: 831.4 KB (831396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31110fc43a4ce01227dd0a0453f904b221bd482dc4c0301b8ffa501b18ea30e`  
		Last Modified: Wed, 05 Oct 2022 14:06:40 GMT  
		Size: 4.3 MB (4265721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7365507dba87454ad0733144061a0542a771b554c28c0b8ebec0b48db8f8678c`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13820d6a8f15395e7f0229f1db78a33b5cab7627627dcf05a9f5aa25cc4c88a`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d3e83df9803da355f686ea14320ce21fd16f2d1d493aa0c23027119f31892e`  
		Last Modified: Wed, 05 Oct 2022 14:07:15 GMT  
		Size: 252.5 MB (252503449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13927152bbda1f9e5e4da3f8f076eeb25177cb22e6347a12dbb859a375a5dfaa`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-core-bionic`

```console
$ docker pull ros@sha256:ff83de7776e1d39ad2bd7c38aee5eebcd2f1ad6645da78e208a1816ac89faf7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-core-bionic` - linux; amd64

```console
$ docker pull ros@sha256:4823a905ffe0b3e7d527d857d533d78fc707ace416fed369a38da35f98b535bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (291990746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b750019b37ee79ded291459fd57709578c21c1a3c552e25109bf1f41e0d8dd`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:28 GMT
ADD file:fc5d658c47ede58827812b75a311353be776e41e2dd339b8906839527c9b5247 in / 
# Tue, 25 Oct 2022 01:53:28 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:51:42 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:56 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:51:57 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 06:51:58 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 06:51:58 GMT
ENV ROS_DISTRO=melodic
# Tue, 25 Oct 2022 06:55:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:55:51 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 06:55:51 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 06:55:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a404e54162968593b8d92b571f3cdd673e4c9eab5d9be28d7c494595c0aa6682`  
		Last Modified: Wed, 19 Oct 2022 22:03:02 GMT  
		Size: 26.7 MB (26712500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1955214fb5b152d9d9fa8ce9a39b19a4e6e8ea487bc617e76c0b7b33e1881bc`  
		Last Modified: Tue, 25 Oct 2022 07:50:06 GMT  
		Size: 831.1 KB (831118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b389880aa1534b94319b44ef0d7e8e52ae108ec326dc1efe1cf0e4e749a4190a`  
		Last Modified: Tue, 25 Oct 2022 07:50:04 GMT  
		Size: 4.9 MB (4877285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db68a36d4b9f8fa036da9f0c51e74b6d27dffd9d39317f42638ee84b29322668`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b325e4aad15f84b511f749de8e3b84dc88f98909bbfdd1961ac0e84f7d273f16`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ad76754b2b5a9699fc604ac8d1393dd3d6dfe21df82c8e930da67ffd6f6708`  
		Last Modified: Tue, 25 Oct 2022 07:50:52 GMT  
		Size: 259.6 MB (259567997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1318baf5e3f70ccdc707f97c58bf69e65917aadaa98ec26b67d1d2695572fa`  
		Last Modified: Tue, 25 Oct 2022 07:50:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:11cbb2f864a289726b9510d1a9b4e6e7414dfacb9a9d782b9d1e4754293f2056
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266239154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d83c28f326a67014793ddf881b3e99269c547c3a86ced293cec9f9fca7d46c0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:31 GMT
ADD file:20e0d71059d38b1e18636b9db71f534d7297c3f571d73d45a75b4b8d3cac86c7 in / 
# Wed, 05 Oct 2022 00:13:32 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:46:30 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:40 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:46:41 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:46:42 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:46:42 GMT
ENV ROS_DISTRO=melodic
# Thu, 06 Oct 2022 06:48:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:48:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:48:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:48:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:91bb9a9844d67fd31f07ebd74dc8a4f4f18e2f959d3aa2166aca86ae57f353c6`  
		Last Modified: Wed, 05 Oct 2022 00:15:26 GMT  
		Size: 22.3 MB (22305721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f25a09f0aff0cba5b24d07bd5b4c417734fbce77148b7b62042ac54dc95c068`  
		Last Modified: Thu, 06 Oct 2022 06:58:00 GMT  
		Size: 831.1 KB (831144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14397641aa51f3c3aa6ed2c352f3417b3bce0ebaca231e20759c931e3fe38560`  
		Last Modified: Thu, 06 Oct 2022 06:57:58 GMT  
		Size: 4.1 MB (4087217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a2d98c80683d1808b546f8ca1a247aecedcea1e9d2460d95343238dfabc896`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670273ddac9f5d6d6c7da9986d18661e88bbbc0126833dcd54f90992f9c9484d`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6664b634c5bf87720b15e47366d33bea9fefdd0032f110f86c336e5ae31a0e`  
		Last Modified: Thu, 06 Oct 2022 06:58:45 GMT  
		Size: 239.0 MB (239013225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074569eb7528b8c52dc9fd001aac258a83c59faaf1830e646c00899e79c3a889`  
		Last Modified: Thu, 06 Oct 2022 06:57:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:1f76867405b52c64167fb70e1f09efb2123122401686455531be3b1a7ac3221e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281336960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b4b42a718b3881e44324b053aea4b4105bf5b40004428e1ca8c85a6a6ec75e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:02 GMT
ADD file:4beae13e1fd7bb92776c08a5cd95feb81b8b3c80522ed8513f2441adfb1661ac in / 
# Wed, 05 Oct 2022 00:02:02 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:31:26 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:31:36 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:31:37 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:31:39 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:31:40 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:31:41 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:31:42 GMT
ENV ROS_DISTRO=melodic
# Wed, 05 Oct 2022 13:33:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:33:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 13:33:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:33:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0e9b69cf8198dafe5b7db1eee7b96b96238f8346ec641dd44f961f7996c2c152`  
		Last Modified: Wed, 05 Oct 2022 00:03:33 GMT  
		Size: 23.7 MB (23734594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fe90d911d5615b705080d27fba0823b4f14f420d2d26ab56026456d57781d53`  
		Last Modified: Wed, 05 Oct 2022 14:06:42 GMT  
		Size: 831.4 KB (831396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31110fc43a4ce01227dd0a0453f904b221bd482dc4c0301b8ffa501b18ea30e`  
		Last Modified: Wed, 05 Oct 2022 14:06:40 GMT  
		Size: 4.3 MB (4265721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7365507dba87454ad0733144061a0542a771b554c28c0b8ebec0b48db8f8678c`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13820d6a8f15395e7f0229f1db78a33b5cab7627627dcf05a9f5aa25cc4c88a`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d3e83df9803da355f686ea14320ce21fd16f2d1d493aa0c23027119f31892e`  
		Last Modified: Wed, 05 Oct 2022 14:07:15 GMT  
		Size: 252.5 MB (252503449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13927152bbda1f9e5e4da3f8f076eeb25177cb22e6347a12dbb859a375a5dfaa`  
		Last Modified: Wed, 05 Oct 2022 14:06:39 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic`

```console
$ docker pull ros@sha256:740d7d54d8957dc99302fbfc01c591f6ced4750cb3d79dd5419fdd2f73ea45ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic` - linux; amd64

```console
$ docker pull ros@sha256:34cbfe55d811fe7c57add8b3d6f01ba9c209258ef1b4029cec5118dcd21e358f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343179990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6d7ab7e066ec3cc62a3c2bfe041ba6a0a444f0b66da68886d72c1906c5004a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:53 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:04:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:07:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:07:31 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:07:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:07:31 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:08:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:08:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:09:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcba2703cc13554dd6ac252966be0f9f0a9d6e79ee879b5e0289457bc632f55`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617320b8300618f53ec135b976c7f3a733354c5ef799b7c969108d82a8509f8`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f065fe084d225480619420eb81fce25e1ea4e12e4f4b95002773742fc0e01d67`  
		Last Modified: Tue, 25 Oct 2022 07:53:37 GMT  
		Size: 177.0 MB (177008909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f66f6a9e5d5690a6fcd01f03ca5ef0146410fa911f6fccb17d73db1bbec814`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcd60406762b57a7de1c5c937562c8a145da66c5f0d5716f70f5c5ae115ab71`  
		Last Modified: Tue, 25 Oct 2022 07:53:56 GMT  
		Size: 50.9 MB (50940379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb29d90361859f6ac155a32b08124b4fecb3b64649f15b68b7d6b59f22d70d4`  
		Last Modified: Tue, 25 Oct 2022 07:53:47 GMT  
		Size: 332.1 KB (332101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055f4ec67f38d1b1c161894d68208d46a4d5822664774d4554aaf150f243341c`  
		Last Modified: Tue, 25 Oct 2022 07:54:01 GMT  
		Size: 79.6 MB (79603171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm variant v7

```console
$ docker pull ros@sha256:282eece3c6e182e825057bcb769c29ec38c0a3e9b2c9cb0b913ede9dec5a8ccd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289297974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727b6d344ef45add4b6b86083e60223e9bb9840f5052ac125292637db637ef91`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:44 GMT
ADD file:75870468a948359044fa3df6c07c80badfea3dcde4823d41a19285436c40cf76 in / 
# Wed, 05 Oct 2022 00:13:44 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:52:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:52:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 06 Oct 2022 06:53:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:16 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:53:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:53:16 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:53:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e679d63f382033c15f8f921851bd71fb8a85a432c0a7a612bbef16e989075145`  
		Last Modified: Wed, 05 Oct 2022 00:15:44 GMT  
		Size: 24.6 MB (24590092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ab6ac546133bf21e51dc29641d455c42144b184821f494258ff1ec514556c`  
		Last Modified: Thu, 06 Oct 2022 07:00:40 GMT  
		Size: 1.2 MB (1163905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4706759f53c150848596edb49143a211c7e072793acea609cc8e9c0f267c4e3e`  
		Last Modified: Thu, 06 Oct 2022 07:00:38 GMT  
		Size: 4.7 MB (4675577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b0360f8c716b3c493ff9708abd3c165f9de06193430830ea64d829b1a6ac2`  
		Last Modified: Thu, 06 Oct 2022 07:00:37 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd789251f14b7842f745c35075b3e7f88a5aa3fb3b005a3bd0fde7d8f285d7f`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24248fc7fc767d03259bb795d6c177495b4f61cdb1ddcc6a6bb9bb7dcd5958db`  
		Last Modified: Thu, 06 Oct 2022 07:01:15 GMT  
		Size: 157.6 MB (157550749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1b296e1c261f003a529641cc88d1393116b3a0b1f7853da9463a2e9c16df7c`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1461e09b998de0d3b7ae285e2a3bb8bcb1b889f8a12f832e208d7ec8d3bfe847`  
		Last Modified: Thu, 06 Oct 2022 07:01:36 GMT  
		Size: 40.5 MB (40505592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e355cb57c65a1dc870c88f7e383d6a76770d5f6563b605a9a96dc5ceb24b3a`  
		Last Modified: Thu, 06 Oct 2022 07:01:28 GMT  
		Size: 329.9 KB (329943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b0b621043424762e62d798dd71533b7835ccd3741e94dcdc7fbbdd3ca4f723`  
		Last Modified: Thu, 06 Oct 2022 07:01:40 GMT  
		Size: 60.5 MB (60479707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:76fd0c9142e5ac05def8adba27f5ae4d8887f4d16e7997c9811a9b93691cadd3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322256415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5417df554ee3ec7fde99d2d44aa591593c7532653b7f97faafd2c5d48ec2baf4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:36:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:36:52 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:36:53 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:36:54 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Oct 2022 13:37:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:37:54 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 13:37:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:37:57 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:38:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:38:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:38:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2066945f278504a3fbe15500f54112556cb9e9febb0b4d07edd644ecbae9209c`  
		Last Modified: Wed, 05 Oct 2022 14:09:02 GMT  
		Size: 1.2 MB (1164049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ca1624225b52b4e52d61f82b52ba0653fdefd1bcde8f1017fc0031f256a5d`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 5.3 MB (5322416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f0727eb08e94e95fafae4d8d0079ee1413dc8ff544022ff06d844f4a53bf3c`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf931507240c54649243355c092bd81e83eae6916ab26a7620f410132c2d47c`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991837517e4c0d5001d2caa2a90cf5e70018524cf2ad724b9cf736dc76eb1d05`  
		Last Modified: Wed, 05 Oct 2022 14:09:29 GMT  
		Size: 171.5 MB (171504736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d4fe51a6dd429e99d46144fc5ddd118e6c466b37ffb21e3942c6fb1bcb67ac`  
		Last Modified: Wed, 05 Oct 2022 14:08:59 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a814635c2ec9fc6aa1c79542be862549465c5ec04cef8ec399952b79e14fe736`  
		Last Modified: Wed, 05 Oct 2022 14:09:46 GMT  
		Size: 45.0 MB (44987961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f762c4f58b5522b0b2e4a82a4b02573353cdb815242b32b47ea696270c4f74f0`  
		Last Modified: Wed, 05 Oct 2022 14:09:40 GMT  
		Size: 329.8 KB (329844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7389f48d507d2a20ca2a184d421e98d9717ff8bd42ce2a9e76b6b153dfc2ee27`  
		Last Modified: Wed, 05 Oct 2022 14:09:50 GMT  
		Size: 71.8 MB (71753417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception`

```console
$ docker pull ros@sha256:c53667dc915e56abe3ef22f5db7b5adfaf30e3cc966bbeb1713cb54457a3e771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception` - linux; amd64

```console
$ docker pull ros@sha256:cbbb6aa7e54b07b867ea1c6fefab9c1bd83f795f6e3a30a499c0a1f595db15c4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.1 MB (835147503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d806f6ce0fd63436af5228a1d9a4209bb5f7f8de53205864e5319df8784e227`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:53 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:04:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:07:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:07:31 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:07:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:07:31 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:08:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:08:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:09:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:16:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcba2703cc13554dd6ac252966be0f9f0a9d6e79ee879b5e0289457bc632f55`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617320b8300618f53ec135b976c7f3a733354c5ef799b7c969108d82a8509f8`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f065fe084d225480619420eb81fce25e1ea4e12e4f4b95002773742fc0e01d67`  
		Last Modified: Tue, 25 Oct 2022 07:53:37 GMT  
		Size: 177.0 MB (177008909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f66f6a9e5d5690a6fcd01f03ca5ef0146410fa911f6fccb17d73db1bbec814`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcd60406762b57a7de1c5c937562c8a145da66c5f0d5716f70f5c5ae115ab71`  
		Last Modified: Tue, 25 Oct 2022 07:53:56 GMT  
		Size: 50.9 MB (50940379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb29d90361859f6ac155a32b08124b4fecb3b64649f15b68b7d6b59f22d70d4`  
		Last Modified: Tue, 25 Oct 2022 07:53:47 GMT  
		Size: 332.1 KB (332101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055f4ec67f38d1b1c161894d68208d46a4d5822664774d4554aaf150f243341c`  
		Last Modified: Tue, 25 Oct 2022 07:54:01 GMT  
		Size: 79.6 MB (79603171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96304f40d98ec3ee8f481818e18af495a0d8da05d780423f6da8294be3c5fcc1`  
		Last Modified: Tue, 25 Oct 2022 07:55:56 GMT  
		Size: 492.0 MB (491967513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:d3a05ef88d081e15785fcfe16ff2c65f1202d8e5ec15369b110b406ff066c6bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.2 MB (726177866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2302d2ee97aca1cc80e68f815cc9e06f1b146c7567089608a5feb883d948ea4a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:44 GMT
ADD file:75870468a948359044fa3df6c07c80badfea3dcde4823d41a19285436c40cf76 in / 
# Wed, 05 Oct 2022 00:13:44 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:52:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:52:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 06 Oct 2022 06:53:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:16 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:53:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:53:16 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:53:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:57:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e679d63f382033c15f8f921851bd71fb8a85a432c0a7a612bbef16e989075145`  
		Last Modified: Wed, 05 Oct 2022 00:15:44 GMT  
		Size: 24.6 MB (24590092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ab6ac546133bf21e51dc29641d455c42144b184821f494258ff1ec514556c`  
		Last Modified: Thu, 06 Oct 2022 07:00:40 GMT  
		Size: 1.2 MB (1163905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4706759f53c150848596edb49143a211c7e072793acea609cc8e9c0f267c4e3e`  
		Last Modified: Thu, 06 Oct 2022 07:00:38 GMT  
		Size: 4.7 MB (4675577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b0360f8c716b3c493ff9708abd3c165f9de06193430830ea64d829b1a6ac2`  
		Last Modified: Thu, 06 Oct 2022 07:00:37 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd789251f14b7842f745c35075b3e7f88a5aa3fb3b005a3bd0fde7d8f285d7f`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24248fc7fc767d03259bb795d6c177495b4f61cdb1ddcc6a6bb9bb7dcd5958db`  
		Last Modified: Thu, 06 Oct 2022 07:01:15 GMT  
		Size: 157.6 MB (157550749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1b296e1c261f003a529641cc88d1393116b3a0b1f7853da9463a2e9c16df7c`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1461e09b998de0d3b7ae285e2a3bb8bcb1b889f8a12f832e208d7ec8d3bfe847`  
		Last Modified: Thu, 06 Oct 2022 07:01:36 GMT  
		Size: 40.5 MB (40505592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e355cb57c65a1dc870c88f7e383d6a76770d5f6563b605a9a96dc5ceb24b3a`  
		Last Modified: Thu, 06 Oct 2022 07:01:28 GMT  
		Size: 329.9 KB (329943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b0b621043424762e62d798dd71533b7835ccd3741e94dcdc7fbbdd3ca4f723`  
		Last Modified: Thu, 06 Oct 2022 07:01:40 GMT  
		Size: 60.5 MB (60479707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed30924832b5259516fe54fa5708a8ae36898b16de1c94f0898baa3d5d3b84a`  
		Last Modified: Thu, 06 Oct 2022 07:03:20 GMT  
		Size: 436.9 MB (436879892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c9ad66b6b36c2b6ca4ecc31c4f8f1f19bccceb47cf271dd5441c9dbac84ee8ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **784.8 MB (784795707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d38a613da5f472621d5e0844eafee839f3f0dd60170e73750a822cba8e910cc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:36:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:36:52 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:36:53 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:36:54 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Oct 2022 13:37:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:37:54 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 13:37:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:37:57 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:38:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:38:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:38:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:42:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2066945f278504a3fbe15500f54112556cb9e9febb0b4d07edd644ecbae9209c`  
		Last Modified: Wed, 05 Oct 2022 14:09:02 GMT  
		Size: 1.2 MB (1164049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ca1624225b52b4e52d61f82b52ba0653fdefd1bcde8f1017fc0031f256a5d`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 5.3 MB (5322416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f0727eb08e94e95fafae4d8d0079ee1413dc8ff544022ff06d844f4a53bf3c`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf931507240c54649243355c092bd81e83eae6916ab26a7620f410132c2d47c`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991837517e4c0d5001d2caa2a90cf5e70018524cf2ad724b9cf736dc76eb1d05`  
		Last Modified: Wed, 05 Oct 2022 14:09:29 GMT  
		Size: 171.5 MB (171504736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d4fe51a6dd429e99d46144fc5ddd118e6c466b37ffb21e3942c6fb1bcb67ac`  
		Last Modified: Wed, 05 Oct 2022 14:08:59 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a814635c2ec9fc6aa1c79542be862549465c5ec04cef8ec399952b79e14fe736`  
		Last Modified: Wed, 05 Oct 2022 14:09:46 GMT  
		Size: 45.0 MB (44987961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f762c4f58b5522b0b2e4a82a4b02573353cdb815242b32b47ea696270c4f74f0`  
		Last Modified: Wed, 05 Oct 2022 14:09:40 GMT  
		Size: 329.8 KB (329844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7389f48d507d2a20ca2a184d421e98d9717ff8bd42ce2a9e76b6b153dfc2ee27`  
		Last Modified: Wed, 05 Oct 2022 14:09:50 GMT  
		Size: 71.8 MB (71753417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74469c08d264edcc5ee135c5451f9ae9f9636a408d721ae64bb3afcbf69ee13b`  
		Last Modified: Wed, 05 Oct 2022 14:11:25 GMT  
		Size: 462.5 MB (462539292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception-buster`

```console
$ docker pull ros@sha256:ca28b2db18d47a83c100a8a9da8e109c4108509b79ba834c7cc9ec2ad22319b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-perception-buster` - linux; amd64

```console
$ docker pull ros@sha256:c958d3e0d30b8a78337d7ca918ba7121ae3773ff0a059854735268ec24a7123d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **951.4 MB (951441437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9db43d92b60e5b392a3e50febed01db2bf45270fe34bc49262c432ebef789b3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:02 GMT
ADD file:259be79d94a2549a667ad08a093fe18f15a6c93d66a0723292f49294e31fc7a1 in / 
# Tue, 25 Oct 2022 01:44:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:17:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:17:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:17:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:17:27 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:17:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:17:27 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:18:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:18:59 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:18:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:18:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:19:32 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:19:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:20:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:24:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fd31ec14dccdcda8f2472547f1a94ef0a23b8dabb764cd7b1d48aeee0afea7c8`  
		Last Modified: Tue, 25 Oct 2022 01:48:15 GMT  
		Size: 50.4 MB (50447742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7bb5a8d4409ae76ed240704c8628d248a907ec454b12a0f653fa5180822f32`  
		Last Modified: Tue, 25 Oct 2022 07:56:14 GMT  
		Size: 10.9 MB (10896941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9831692d445c53ad6706089a3b147d293d3267dd486b27109a911c9da182ed31`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2beecf1c3569265300a22936ddda05e835f0c83b2193ea68b4d60f2882113cd`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834cb0e33271e58107ddec676304ba095210344f2ee4310bb860d12b941b510c`  
		Last Modified: Tue, 25 Oct 2022 07:56:46 GMT  
		Size: 239.2 MB (239209563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdd4ac8f13eeeb7f19f875b6a9191a3aedf9fd8006aae02db37664d36f51883`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f066880bf184688bbe3b3bce165ab3ad72850aae130b41b408020b47003491`  
		Last Modified: Tue, 25 Oct 2022 07:57:07 GMT  
		Size: 86.6 MB (86586144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5c12225f8506452bbdfb135687a0e9642f4fd2bec37dacde2ff8e68f0031c8`  
		Last Modified: Tue, 25 Oct 2022 07:56:53 GMT  
		Size: 326.7 KB (326687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cb66701beaeeb105d227e3c100dab245e25d8e913dcb72fb68145181a9140f`  
		Last Modified: Tue, 25 Oct 2022 07:57:05 GMT  
		Size: 76.0 MB (75978159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f63a0255662de5afdca2ec51999af441f9c0591a5fcd779d7dd8fb7d38c5790`  
		Last Modified: Tue, 25 Oct 2022 07:58:52 GMT  
		Size: 488.0 MB (487993789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0be734205fcd3bb5d8d7b494b2480ee3c501e8e7bc80a22086c5fae168d0ff18
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 MB (867691466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0407a6c31b234440c08346172e561c78fdef9da60394cfc61d02ee81616aff43`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:54 GMT
ADD file:ef2ee78fb3eda698ebec33ff4b6dea672e03908b0f8630a28acb33ec9a7c3e13 in / 
# Tue, 04 Oct 2022 23:44:55 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:42:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:42:19 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:42:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:42:22 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:42:23 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:42:24 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Oct 2022 13:43:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:43:35 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 13:43:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:43:38 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:44:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:44:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:45:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:48:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:504dcdd9b4a0035dba7a55a5312cf594c3d22fb99b7bf676d397c464db919009`  
		Last Modified: Tue, 04 Oct 2022 23:50:47 GMT  
		Size: 49.2 MB (49228885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c286841822dd708cc8ec03c64947552384e955fad5e3df9a73a5acab4aaaed`  
		Last Modified: Wed, 05 Oct 2022 14:11:38 GMT  
		Size: 10.7 MB (10689488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b51b46470fae12ab22dbf0e0f68d92e335b5d2aec01faf4694f688dcff7ed7e`  
		Last Modified: Wed, 05 Oct 2022 14:11:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01f93551ac4426be901cafe628cfa60e541d98154404fcba3cb02cde1d85358`  
		Last Modified: Wed, 05 Oct 2022 14:11:37 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a850fdf218d14508c13532bd2745504750003968ec91b47bbc2a16d38af0791f`  
		Last Modified: Wed, 05 Oct 2022 14:12:09 GMT  
		Size: 184.4 MB (184402359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46befb9f0b1823e66932ff7e6bd3b3f7ef17e0115617e47457b2e68aa6db3103`  
		Last Modified: Wed, 05 Oct 2022 14:11:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70142cef45c79ed6c16def65c939723b912688d777616cd8f0394a0a9bed62b`  
		Last Modified: Wed, 05 Oct 2022 14:12:28 GMT  
		Size: 84.4 MB (84371054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec293e0c6336ccbd0d0986af98ef8fd2f6e8caebfc5454d01a8d50bf39f3310`  
		Last Modified: Wed, 05 Oct 2022 14:12:17 GMT  
		Size: 324.6 KB (324579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fdd5b15718815c6b2b180f7ba28bb586c4071861d49a281db790d1263561842`  
		Last Modified: Wed, 05 Oct 2022 14:12:26 GMT  
		Size: 73.9 MB (73865277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce03a7da0d66f047902e88c4c2a4af4a8a6d8ab4e8e457debc9fbdebb20bfc3e`  
		Last Modified: Wed, 05 Oct 2022 14:13:53 GMT  
		Size: 464.8 MB (464807456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:c53667dc915e56abe3ef22f5db7b5adfaf30e3cc966bbeb1713cb54457a3e771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:cbbb6aa7e54b07b867ea1c6fefab9c1bd83f795f6e3a30a499c0a1f595db15c4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.1 MB (835147503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d806f6ce0fd63436af5228a1d9a4209bb5f7f8de53205864e5319df8784e227`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:53 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:04:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:07:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:07:31 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:07:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:07:31 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:08:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:08:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:09:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:16:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcba2703cc13554dd6ac252966be0f9f0a9d6e79ee879b5e0289457bc632f55`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617320b8300618f53ec135b976c7f3a733354c5ef799b7c969108d82a8509f8`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f065fe084d225480619420eb81fce25e1ea4e12e4f4b95002773742fc0e01d67`  
		Last Modified: Tue, 25 Oct 2022 07:53:37 GMT  
		Size: 177.0 MB (177008909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f66f6a9e5d5690a6fcd01f03ca5ef0146410fa911f6fccb17d73db1bbec814`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcd60406762b57a7de1c5c937562c8a145da66c5f0d5716f70f5c5ae115ab71`  
		Last Modified: Tue, 25 Oct 2022 07:53:56 GMT  
		Size: 50.9 MB (50940379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb29d90361859f6ac155a32b08124b4fecb3b64649f15b68b7d6b59f22d70d4`  
		Last Modified: Tue, 25 Oct 2022 07:53:47 GMT  
		Size: 332.1 KB (332101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055f4ec67f38d1b1c161894d68208d46a4d5822664774d4554aaf150f243341c`  
		Last Modified: Tue, 25 Oct 2022 07:54:01 GMT  
		Size: 79.6 MB (79603171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96304f40d98ec3ee8f481818e18af495a0d8da05d780423f6da8294be3c5fcc1`  
		Last Modified: Tue, 25 Oct 2022 07:55:56 GMT  
		Size: 492.0 MB (491967513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:d3a05ef88d081e15785fcfe16ff2c65f1202d8e5ec15369b110b406ff066c6bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.2 MB (726177866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2302d2ee97aca1cc80e68f815cc9e06f1b146c7567089608a5feb883d948ea4a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:44 GMT
ADD file:75870468a948359044fa3df6c07c80badfea3dcde4823d41a19285436c40cf76 in / 
# Wed, 05 Oct 2022 00:13:44 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:52:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:52:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 06 Oct 2022 06:53:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:16 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:53:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:53:16 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:53:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:57:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e679d63f382033c15f8f921851bd71fb8a85a432c0a7a612bbef16e989075145`  
		Last Modified: Wed, 05 Oct 2022 00:15:44 GMT  
		Size: 24.6 MB (24590092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ab6ac546133bf21e51dc29641d455c42144b184821f494258ff1ec514556c`  
		Last Modified: Thu, 06 Oct 2022 07:00:40 GMT  
		Size: 1.2 MB (1163905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4706759f53c150848596edb49143a211c7e072793acea609cc8e9c0f267c4e3e`  
		Last Modified: Thu, 06 Oct 2022 07:00:38 GMT  
		Size: 4.7 MB (4675577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b0360f8c716b3c493ff9708abd3c165f9de06193430830ea64d829b1a6ac2`  
		Last Modified: Thu, 06 Oct 2022 07:00:37 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd789251f14b7842f745c35075b3e7f88a5aa3fb3b005a3bd0fde7d8f285d7f`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24248fc7fc767d03259bb795d6c177495b4f61cdb1ddcc6a6bb9bb7dcd5958db`  
		Last Modified: Thu, 06 Oct 2022 07:01:15 GMT  
		Size: 157.6 MB (157550749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1b296e1c261f003a529641cc88d1393116b3a0b1f7853da9463a2e9c16df7c`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1461e09b998de0d3b7ae285e2a3bb8bcb1b889f8a12f832e208d7ec8d3bfe847`  
		Last Modified: Thu, 06 Oct 2022 07:01:36 GMT  
		Size: 40.5 MB (40505592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e355cb57c65a1dc870c88f7e383d6a76770d5f6563b605a9a96dc5ceb24b3a`  
		Last Modified: Thu, 06 Oct 2022 07:01:28 GMT  
		Size: 329.9 KB (329943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b0b621043424762e62d798dd71533b7835ccd3741e94dcdc7fbbdd3ca4f723`  
		Last Modified: Thu, 06 Oct 2022 07:01:40 GMT  
		Size: 60.5 MB (60479707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed30924832b5259516fe54fa5708a8ae36898b16de1c94f0898baa3d5d3b84a`  
		Last Modified: Thu, 06 Oct 2022 07:03:20 GMT  
		Size: 436.9 MB (436879892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c9ad66b6b36c2b6ca4ecc31c4f8f1f19bccceb47cf271dd5441c9dbac84ee8ac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **784.8 MB (784795707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d38a613da5f472621d5e0844eafee839f3f0dd60170e73750a822cba8e910cc`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:36:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:36:52 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:36:53 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:36:54 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Oct 2022 13:37:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:37:54 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 13:37:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:37:57 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:38:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:38:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:38:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:42:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2066945f278504a3fbe15500f54112556cb9e9febb0b4d07edd644ecbae9209c`  
		Last Modified: Wed, 05 Oct 2022 14:09:02 GMT  
		Size: 1.2 MB (1164049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ca1624225b52b4e52d61f82b52ba0653fdefd1bcde8f1017fc0031f256a5d`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 5.3 MB (5322416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f0727eb08e94e95fafae4d8d0079ee1413dc8ff544022ff06d844f4a53bf3c`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf931507240c54649243355c092bd81e83eae6916ab26a7620f410132c2d47c`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991837517e4c0d5001d2caa2a90cf5e70018524cf2ad724b9cf736dc76eb1d05`  
		Last Modified: Wed, 05 Oct 2022 14:09:29 GMT  
		Size: 171.5 MB (171504736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d4fe51a6dd429e99d46144fc5ddd118e6c466b37ffb21e3942c6fb1bcb67ac`  
		Last Modified: Wed, 05 Oct 2022 14:08:59 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a814635c2ec9fc6aa1c79542be862549465c5ec04cef8ec399952b79e14fe736`  
		Last Modified: Wed, 05 Oct 2022 14:09:46 GMT  
		Size: 45.0 MB (44987961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f762c4f58b5522b0b2e4a82a4b02573353cdb815242b32b47ea696270c4f74f0`  
		Last Modified: Wed, 05 Oct 2022 14:09:40 GMT  
		Size: 329.8 KB (329844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7389f48d507d2a20ca2a184d421e98d9717ff8bd42ce2a9e76b6b153dfc2ee27`  
		Last Modified: Wed, 05 Oct 2022 14:09:50 GMT  
		Size: 71.8 MB (71753417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74469c08d264edcc5ee135c5451f9ae9f9636a408d721ae64bb3afcbf69ee13b`  
		Last Modified: Wed, 05 Oct 2022 14:11:25 GMT  
		Size: 462.5 MB (462539292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot`

```console
$ docker pull ros@sha256:3c77f1a57c579e87b1a568931fa306f67c17a5048f0cc29cb0b3ec39a2c26de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:f2cb64c09356a71a17270f40ae8e9d42d242509547d47b395d46e04fbfaa5c93
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (359041151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aae48c851939de656e19f202234d0491e2bf82aa82870ab8070c404b34a0bda`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:53 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:04:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:07:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:07:31 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:07:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:07:31 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:08:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:08:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:09:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:10:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcba2703cc13554dd6ac252966be0f9f0a9d6e79ee879b5e0289457bc632f55`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617320b8300618f53ec135b976c7f3a733354c5ef799b7c969108d82a8509f8`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f065fe084d225480619420eb81fce25e1ea4e12e4f4b95002773742fc0e01d67`  
		Last Modified: Tue, 25 Oct 2022 07:53:37 GMT  
		Size: 177.0 MB (177008909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f66f6a9e5d5690a6fcd01f03ca5ef0146410fa911f6fccb17d73db1bbec814`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcd60406762b57a7de1c5c937562c8a145da66c5f0d5716f70f5c5ae115ab71`  
		Last Modified: Tue, 25 Oct 2022 07:53:56 GMT  
		Size: 50.9 MB (50940379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb29d90361859f6ac155a32b08124b4fecb3b64649f15b68b7d6b59f22d70d4`  
		Last Modified: Tue, 25 Oct 2022 07:53:47 GMT  
		Size: 332.1 KB (332101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055f4ec67f38d1b1c161894d68208d46a4d5822664774d4554aaf150f243341c`  
		Last Modified: Tue, 25 Oct 2022 07:54:01 GMT  
		Size: 79.6 MB (79603171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a67e64bc6cfc11803ed4fdb948911a3d1d22b6f40e7ed61cd815d62c050a4fc`  
		Last Modified: Tue, 25 Oct 2022 07:54:17 GMT  
		Size: 15.9 MB (15861161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:931a8f67e0e7779bbadc154d28cb081ecc3163db2b77ac9539c413644b6ceff5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 MB (303363136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205efb50cd40a2dadaee4531776d2a257c8fce1a9728465df5468491f976aac3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:44 GMT
ADD file:75870468a948359044fa3df6c07c80badfea3dcde4823d41a19285436c40cf76 in / 
# Wed, 05 Oct 2022 00:13:44 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:52:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:52:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 06 Oct 2022 06:53:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:16 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:53:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:53:16 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:53:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:54:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e679d63f382033c15f8f921851bd71fb8a85a432c0a7a612bbef16e989075145`  
		Last Modified: Wed, 05 Oct 2022 00:15:44 GMT  
		Size: 24.6 MB (24590092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ab6ac546133bf21e51dc29641d455c42144b184821f494258ff1ec514556c`  
		Last Modified: Thu, 06 Oct 2022 07:00:40 GMT  
		Size: 1.2 MB (1163905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4706759f53c150848596edb49143a211c7e072793acea609cc8e9c0f267c4e3e`  
		Last Modified: Thu, 06 Oct 2022 07:00:38 GMT  
		Size: 4.7 MB (4675577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b0360f8c716b3c493ff9708abd3c165f9de06193430830ea64d829b1a6ac2`  
		Last Modified: Thu, 06 Oct 2022 07:00:37 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd789251f14b7842f745c35075b3e7f88a5aa3fb3b005a3bd0fde7d8f285d7f`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24248fc7fc767d03259bb795d6c177495b4f61cdb1ddcc6a6bb9bb7dcd5958db`  
		Last Modified: Thu, 06 Oct 2022 07:01:15 GMT  
		Size: 157.6 MB (157550749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1b296e1c261f003a529641cc88d1393116b3a0b1f7853da9463a2e9c16df7c`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1461e09b998de0d3b7ae285e2a3bb8bcb1b889f8a12f832e208d7ec8d3bfe847`  
		Last Modified: Thu, 06 Oct 2022 07:01:36 GMT  
		Size: 40.5 MB (40505592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e355cb57c65a1dc870c88f7e383d6a76770d5f6563b605a9a96dc5ceb24b3a`  
		Last Modified: Thu, 06 Oct 2022 07:01:28 GMT  
		Size: 329.9 KB (329943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b0b621043424762e62d798dd71533b7835ccd3741e94dcdc7fbbdd3ca4f723`  
		Last Modified: Thu, 06 Oct 2022 07:01:40 GMT  
		Size: 60.5 MB (60479707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4213011fc7a49cf580c896c00969f42891823b1dbe5356b6a627e03ac4bd6e13`  
		Last Modified: Thu, 06 Oct 2022 07:01:58 GMT  
		Size: 14.1 MB (14065162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cbf89f5bcbf5baf8a786e0945237b78bac1cc8cefb7ac4b9876ec84037d77ded
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.7 MB (337705362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da55244b8dc759186bfe3eb5d355819b03d26aa18833e3c469b3de63690a940e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:36:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:36:52 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:36:53 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:36:54 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Oct 2022 13:37:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:37:54 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 13:37:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:37:57 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:38:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:38:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:38:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:39:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2066945f278504a3fbe15500f54112556cb9e9febb0b4d07edd644ecbae9209c`  
		Last Modified: Wed, 05 Oct 2022 14:09:02 GMT  
		Size: 1.2 MB (1164049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ca1624225b52b4e52d61f82b52ba0653fdefd1bcde8f1017fc0031f256a5d`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 5.3 MB (5322416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f0727eb08e94e95fafae4d8d0079ee1413dc8ff544022ff06d844f4a53bf3c`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf931507240c54649243355c092bd81e83eae6916ab26a7620f410132c2d47c`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991837517e4c0d5001d2caa2a90cf5e70018524cf2ad724b9cf736dc76eb1d05`  
		Last Modified: Wed, 05 Oct 2022 14:09:29 GMT  
		Size: 171.5 MB (171504736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d4fe51a6dd429e99d46144fc5ddd118e6c466b37ffb21e3942c6fb1bcb67ac`  
		Last Modified: Wed, 05 Oct 2022 14:08:59 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a814635c2ec9fc6aa1c79542be862549465c5ec04cef8ec399952b79e14fe736`  
		Last Modified: Wed, 05 Oct 2022 14:09:46 GMT  
		Size: 45.0 MB (44987961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f762c4f58b5522b0b2e4a82a4b02573353cdb815242b32b47ea696270c4f74f0`  
		Last Modified: Wed, 05 Oct 2022 14:09:40 GMT  
		Size: 329.8 KB (329844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7389f48d507d2a20ca2a184d421e98d9717ff8bd42ce2a9e76b6b153dfc2ee27`  
		Last Modified: Wed, 05 Oct 2022 14:09:50 GMT  
		Size: 71.8 MB (71753417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635d5818920d712c2d0c966e72310e1423cd89ced677c40f6f31ddadb8bf6b8f`  
		Last Modified: Wed, 05 Oct 2022 14:10:07 GMT  
		Size: 15.4 MB (15448947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot-buster`

```console
$ docker pull ros@sha256:5c647a88e7c67804d7b3e57e1c557b771bd9a64fe57be52d361f2be5a9d21202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-robot-buster` - linux; amd64

```console
$ docker pull ros@sha256:1df3c892d86fd452b24e82eaee409fa376a344437411ebcc64174f683cc20db5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.9 MB (484899656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe1b1975f4b9abbde15c6fa7066017b6b11ed67f9bed0616d47b9d8eaa078533`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:02 GMT
ADD file:259be79d94a2549a667ad08a093fe18f15a6c93d66a0723292f49294e31fc7a1 in / 
# Tue, 25 Oct 2022 01:44:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:17:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:17:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:17:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:17:27 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:17:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:17:27 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:18:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:18:59 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:18:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:18:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:19:32 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:19:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:20:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:20:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fd31ec14dccdcda8f2472547f1a94ef0a23b8dabb764cd7b1d48aeee0afea7c8`  
		Last Modified: Tue, 25 Oct 2022 01:48:15 GMT  
		Size: 50.4 MB (50447742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7bb5a8d4409ae76ed240704c8628d248a907ec454b12a0f653fa5180822f32`  
		Last Modified: Tue, 25 Oct 2022 07:56:14 GMT  
		Size: 10.9 MB (10896941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9831692d445c53ad6706089a3b147d293d3267dd486b27109a911c9da182ed31`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2beecf1c3569265300a22936ddda05e835f0c83b2193ea68b4d60f2882113cd`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834cb0e33271e58107ddec676304ba095210344f2ee4310bb860d12b941b510c`  
		Last Modified: Tue, 25 Oct 2022 07:56:46 GMT  
		Size: 239.2 MB (239209563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdd4ac8f13eeeb7f19f875b6a9191a3aedf9fd8006aae02db37664d36f51883`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f066880bf184688bbe3b3bce165ab3ad72850aae130b41b408020b47003491`  
		Last Modified: Tue, 25 Oct 2022 07:57:07 GMT  
		Size: 86.6 MB (86586144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5c12225f8506452bbdfb135687a0e9642f4fd2bec37dacde2ff8e68f0031c8`  
		Last Modified: Tue, 25 Oct 2022 07:56:53 GMT  
		Size: 326.7 KB (326687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cb66701beaeeb105d227e3c100dab245e25d8e913dcb72fb68145181a9140f`  
		Last Modified: Tue, 25 Oct 2022 07:57:05 GMT  
		Size: 76.0 MB (75978159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e243b3e8516342ad34ac067531d9d7545ff8c35ac1742dfad88b051b3b043db`  
		Last Modified: Tue, 25 Oct 2022 07:57:18 GMT  
		Size: 21.5 MB (21452008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3b603a162a01cffc2f94f0638445bdb64192217fb369bb1d3cf5b3341a353b75
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.0 MB (423991607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c82425e01996b0f75a886f464dbcb66332c2a722fb5c343e861996462a994d70`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:54 GMT
ADD file:ef2ee78fb3eda698ebec33ff4b6dea672e03908b0f8630a28acb33ec9a7c3e13 in / 
# Tue, 04 Oct 2022 23:44:55 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:42:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:42:19 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:42:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:42:22 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:42:23 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:42:24 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Oct 2022 13:43:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:43:35 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 13:43:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:43:38 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:44:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:44:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:45:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:45:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:504dcdd9b4a0035dba7a55a5312cf594c3d22fb99b7bf676d397c464db919009`  
		Last Modified: Tue, 04 Oct 2022 23:50:47 GMT  
		Size: 49.2 MB (49228885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c286841822dd708cc8ec03c64947552384e955fad5e3df9a73a5acab4aaaed`  
		Last Modified: Wed, 05 Oct 2022 14:11:38 GMT  
		Size: 10.7 MB (10689488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b51b46470fae12ab22dbf0e0f68d92e335b5d2aec01faf4694f688dcff7ed7e`  
		Last Modified: Wed, 05 Oct 2022 14:11:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01f93551ac4426be901cafe628cfa60e541d98154404fcba3cb02cde1d85358`  
		Last Modified: Wed, 05 Oct 2022 14:11:37 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a850fdf218d14508c13532bd2745504750003968ec91b47bbc2a16d38af0791f`  
		Last Modified: Wed, 05 Oct 2022 14:12:09 GMT  
		Size: 184.4 MB (184402359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46befb9f0b1823e66932ff7e6bd3b3f7ef17e0115617e47457b2e68aa6db3103`  
		Last Modified: Wed, 05 Oct 2022 14:11:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70142cef45c79ed6c16def65c939723b912688d777616cd8f0394a0a9bed62b`  
		Last Modified: Wed, 05 Oct 2022 14:12:28 GMT  
		Size: 84.4 MB (84371054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec293e0c6336ccbd0d0986af98ef8fd2f6e8caebfc5454d01a8d50bf39f3310`  
		Last Modified: Wed, 05 Oct 2022 14:12:17 GMT  
		Size: 324.6 KB (324579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fdd5b15718815c6b2b180f7ba28bb586c4071861d49a281db790d1263561842`  
		Last Modified: Wed, 05 Oct 2022 14:12:26 GMT  
		Size: 73.9 MB (73865277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6113ec2fc7cc5403f1bec46f71179910d1b80ae4844ca9e0759bbaa64a354ea5`  
		Last Modified: Wed, 05 Oct 2022 14:12:38 GMT  
		Size: 21.1 MB (21107597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot-focal`

```console
$ docker pull ros@sha256:3c77f1a57c579e87b1a568931fa306f67c17a5048f0cc29cb0b3ec39a2c26de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot-focal` - linux; amd64

```console
$ docker pull ros@sha256:f2cb64c09356a71a17270f40ae8e9d42d242509547d47b395d46e04fbfaa5c93
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (359041151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aae48c851939de656e19f202234d0491e2bf82aa82870ab8070c404b34a0bda`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:53 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:04:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:07:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:07:31 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:07:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:07:31 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:08:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:08:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:09:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:10:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcba2703cc13554dd6ac252966be0f9f0a9d6e79ee879b5e0289457bc632f55`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617320b8300618f53ec135b976c7f3a733354c5ef799b7c969108d82a8509f8`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f065fe084d225480619420eb81fce25e1ea4e12e4f4b95002773742fc0e01d67`  
		Last Modified: Tue, 25 Oct 2022 07:53:37 GMT  
		Size: 177.0 MB (177008909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f66f6a9e5d5690a6fcd01f03ca5ef0146410fa911f6fccb17d73db1bbec814`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcd60406762b57a7de1c5c937562c8a145da66c5f0d5716f70f5c5ae115ab71`  
		Last Modified: Tue, 25 Oct 2022 07:53:56 GMT  
		Size: 50.9 MB (50940379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb29d90361859f6ac155a32b08124b4fecb3b64649f15b68b7d6b59f22d70d4`  
		Last Modified: Tue, 25 Oct 2022 07:53:47 GMT  
		Size: 332.1 KB (332101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055f4ec67f38d1b1c161894d68208d46a4d5822664774d4554aaf150f243341c`  
		Last Modified: Tue, 25 Oct 2022 07:54:01 GMT  
		Size: 79.6 MB (79603171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a67e64bc6cfc11803ed4fdb948911a3d1d22b6f40e7ed61cd815d62c050a4fc`  
		Last Modified: Tue, 25 Oct 2022 07:54:17 GMT  
		Size: 15.9 MB (15861161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:931a8f67e0e7779bbadc154d28cb081ecc3163db2b77ac9539c413644b6ceff5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 MB (303363136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205efb50cd40a2dadaee4531776d2a257c8fce1a9728465df5468491f976aac3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:44 GMT
ADD file:75870468a948359044fa3df6c07c80badfea3dcde4823d41a19285436c40cf76 in / 
# Wed, 05 Oct 2022 00:13:44 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:52:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:52:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 06 Oct 2022 06:53:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:16 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:53:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:53:16 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:53:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:54:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e679d63f382033c15f8f921851bd71fb8a85a432c0a7a612bbef16e989075145`  
		Last Modified: Wed, 05 Oct 2022 00:15:44 GMT  
		Size: 24.6 MB (24590092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ab6ac546133bf21e51dc29641d455c42144b184821f494258ff1ec514556c`  
		Last Modified: Thu, 06 Oct 2022 07:00:40 GMT  
		Size: 1.2 MB (1163905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4706759f53c150848596edb49143a211c7e072793acea609cc8e9c0f267c4e3e`  
		Last Modified: Thu, 06 Oct 2022 07:00:38 GMT  
		Size: 4.7 MB (4675577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b0360f8c716b3c493ff9708abd3c165f9de06193430830ea64d829b1a6ac2`  
		Last Modified: Thu, 06 Oct 2022 07:00:37 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd789251f14b7842f745c35075b3e7f88a5aa3fb3b005a3bd0fde7d8f285d7f`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24248fc7fc767d03259bb795d6c177495b4f61cdb1ddcc6a6bb9bb7dcd5958db`  
		Last Modified: Thu, 06 Oct 2022 07:01:15 GMT  
		Size: 157.6 MB (157550749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1b296e1c261f003a529641cc88d1393116b3a0b1f7853da9463a2e9c16df7c`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1461e09b998de0d3b7ae285e2a3bb8bcb1b889f8a12f832e208d7ec8d3bfe847`  
		Last Modified: Thu, 06 Oct 2022 07:01:36 GMT  
		Size: 40.5 MB (40505592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e355cb57c65a1dc870c88f7e383d6a76770d5f6563b605a9a96dc5ceb24b3a`  
		Last Modified: Thu, 06 Oct 2022 07:01:28 GMT  
		Size: 329.9 KB (329943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b0b621043424762e62d798dd71533b7835ccd3741e94dcdc7fbbdd3ca4f723`  
		Last Modified: Thu, 06 Oct 2022 07:01:40 GMT  
		Size: 60.5 MB (60479707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4213011fc7a49cf580c896c00969f42891823b1dbe5356b6a627e03ac4bd6e13`  
		Last Modified: Thu, 06 Oct 2022 07:01:58 GMT  
		Size: 14.1 MB (14065162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:cbf89f5bcbf5baf8a786e0945237b78bac1cc8cefb7ac4b9876ec84037d77ded
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.7 MB (337705362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da55244b8dc759186bfe3eb5d355819b03d26aa18833e3c469b3de63690a940e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:36:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:36:52 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:36:53 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:36:54 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Oct 2022 13:37:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:37:54 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 13:37:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:37:57 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:38:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:38:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:38:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:39:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2066945f278504a3fbe15500f54112556cb9e9febb0b4d07edd644ecbae9209c`  
		Last Modified: Wed, 05 Oct 2022 14:09:02 GMT  
		Size: 1.2 MB (1164049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ca1624225b52b4e52d61f82b52ba0653fdefd1bcde8f1017fc0031f256a5d`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 5.3 MB (5322416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f0727eb08e94e95fafae4d8d0079ee1413dc8ff544022ff06d844f4a53bf3c`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf931507240c54649243355c092bd81e83eae6916ab26a7620f410132c2d47c`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991837517e4c0d5001d2caa2a90cf5e70018524cf2ad724b9cf736dc76eb1d05`  
		Last Modified: Wed, 05 Oct 2022 14:09:29 GMT  
		Size: 171.5 MB (171504736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d4fe51a6dd429e99d46144fc5ddd118e6c466b37ffb21e3942c6fb1bcb67ac`  
		Last Modified: Wed, 05 Oct 2022 14:08:59 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a814635c2ec9fc6aa1c79542be862549465c5ec04cef8ec399952b79e14fe736`  
		Last Modified: Wed, 05 Oct 2022 14:09:46 GMT  
		Size: 45.0 MB (44987961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f762c4f58b5522b0b2e4a82a4b02573353cdb815242b32b47ea696270c4f74f0`  
		Last Modified: Wed, 05 Oct 2022 14:09:40 GMT  
		Size: 329.8 KB (329844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7389f48d507d2a20ca2a184d421e98d9717ff8bd42ce2a9e76b6b153dfc2ee27`  
		Last Modified: Wed, 05 Oct 2022 14:09:50 GMT  
		Size: 71.8 MB (71753417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635d5818920d712c2d0c966e72310e1423cd89ced677c40f6f31ddadb8bf6b8f`  
		Last Modified: Wed, 05 Oct 2022 14:10:07 GMT  
		Size: 15.4 MB (15448947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:740d7d54d8957dc99302fbfc01c591f6ced4750cb3d79dd5419fdd2f73ea45ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:34cbfe55d811fe7c57add8b3d6f01ba9c209258ef1b4029cec5118dcd21e358f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343179990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6d7ab7e066ec3cc62a3c2bfe041ba6a0a444f0b66da68886d72c1906c5004a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:53 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:04:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:07:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:07:31 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:07:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:07:31 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:08:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:08:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:09:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcba2703cc13554dd6ac252966be0f9f0a9d6e79ee879b5e0289457bc632f55`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617320b8300618f53ec135b976c7f3a733354c5ef799b7c969108d82a8509f8`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f065fe084d225480619420eb81fce25e1ea4e12e4f4b95002773742fc0e01d67`  
		Last Modified: Tue, 25 Oct 2022 07:53:37 GMT  
		Size: 177.0 MB (177008909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f66f6a9e5d5690a6fcd01f03ca5ef0146410fa911f6fccb17d73db1bbec814`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcd60406762b57a7de1c5c937562c8a145da66c5f0d5716f70f5c5ae115ab71`  
		Last Modified: Tue, 25 Oct 2022 07:53:56 GMT  
		Size: 50.9 MB (50940379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb29d90361859f6ac155a32b08124b4fecb3b64649f15b68b7d6b59f22d70d4`  
		Last Modified: Tue, 25 Oct 2022 07:53:47 GMT  
		Size: 332.1 KB (332101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055f4ec67f38d1b1c161894d68208d46a4d5822664774d4554aaf150f243341c`  
		Last Modified: Tue, 25 Oct 2022 07:54:01 GMT  
		Size: 79.6 MB (79603171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:282eece3c6e182e825057bcb769c29ec38c0a3e9b2c9cb0b913ede9dec5a8ccd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289297974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727b6d344ef45add4b6b86083e60223e9bb9840f5052ac125292637db637ef91`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:44 GMT
ADD file:75870468a948359044fa3df6c07c80badfea3dcde4823d41a19285436c40cf76 in / 
# Wed, 05 Oct 2022 00:13:44 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:52:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:52:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 06 Oct 2022 06:53:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:16 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:53:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:53:16 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:53:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e679d63f382033c15f8f921851bd71fb8a85a432c0a7a612bbef16e989075145`  
		Last Modified: Wed, 05 Oct 2022 00:15:44 GMT  
		Size: 24.6 MB (24590092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ab6ac546133bf21e51dc29641d455c42144b184821f494258ff1ec514556c`  
		Last Modified: Thu, 06 Oct 2022 07:00:40 GMT  
		Size: 1.2 MB (1163905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4706759f53c150848596edb49143a211c7e072793acea609cc8e9c0f267c4e3e`  
		Last Modified: Thu, 06 Oct 2022 07:00:38 GMT  
		Size: 4.7 MB (4675577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b0360f8c716b3c493ff9708abd3c165f9de06193430830ea64d829b1a6ac2`  
		Last Modified: Thu, 06 Oct 2022 07:00:37 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd789251f14b7842f745c35075b3e7f88a5aa3fb3b005a3bd0fde7d8f285d7f`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24248fc7fc767d03259bb795d6c177495b4f61cdb1ddcc6a6bb9bb7dcd5958db`  
		Last Modified: Thu, 06 Oct 2022 07:01:15 GMT  
		Size: 157.6 MB (157550749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1b296e1c261f003a529641cc88d1393116b3a0b1f7853da9463a2e9c16df7c`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1461e09b998de0d3b7ae285e2a3bb8bcb1b889f8a12f832e208d7ec8d3bfe847`  
		Last Modified: Thu, 06 Oct 2022 07:01:36 GMT  
		Size: 40.5 MB (40505592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e355cb57c65a1dc870c88f7e383d6a76770d5f6563b605a9a96dc5ceb24b3a`  
		Last Modified: Thu, 06 Oct 2022 07:01:28 GMT  
		Size: 329.9 KB (329943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b0b621043424762e62d798dd71533b7835ccd3741e94dcdc7fbbdd3ca4f723`  
		Last Modified: Thu, 06 Oct 2022 07:01:40 GMT  
		Size: 60.5 MB (60479707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:76fd0c9142e5ac05def8adba27f5ae4d8887f4d16e7997c9811a9b93691cadd3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322256415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5417df554ee3ec7fde99d2d44aa591593c7532653b7f97faafd2c5d48ec2baf4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:36:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:36:52 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:36:53 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:36:54 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Oct 2022 13:37:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:37:54 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 13:37:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:37:57 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:38:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:38:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:38:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2066945f278504a3fbe15500f54112556cb9e9febb0b4d07edd644ecbae9209c`  
		Last Modified: Wed, 05 Oct 2022 14:09:02 GMT  
		Size: 1.2 MB (1164049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ca1624225b52b4e52d61f82b52ba0653fdefd1bcde8f1017fc0031f256a5d`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 5.3 MB (5322416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f0727eb08e94e95fafae4d8d0079ee1413dc8ff544022ff06d844f4a53bf3c`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf931507240c54649243355c092bd81e83eae6916ab26a7620f410132c2d47c`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991837517e4c0d5001d2caa2a90cf5e70018524cf2ad724b9cf736dc76eb1d05`  
		Last Modified: Wed, 05 Oct 2022 14:09:29 GMT  
		Size: 171.5 MB (171504736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d4fe51a6dd429e99d46144fc5ddd118e6c466b37ffb21e3942c6fb1bcb67ac`  
		Last Modified: Wed, 05 Oct 2022 14:08:59 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a814635c2ec9fc6aa1c79542be862549465c5ec04cef8ec399952b79e14fe736`  
		Last Modified: Wed, 05 Oct 2022 14:09:46 GMT  
		Size: 45.0 MB (44987961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f762c4f58b5522b0b2e4a82a4b02573353cdb815242b32b47ea696270c4f74f0`  
		Last Modified: Wed, 05 Oct 2022 14:09:40 GMT  
		Size: 329.8 KB (329844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7389f48d507d2a20ca2a184d421e98d9717ff8bd42ce2a9e76b6b153dfc2ee27`  
		Last Modified: Wed, 05 Oct 2022 14:09:50 GMT  
		Size: 71.8 MB (71753417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base-buster`

```console
$ docker pull ros@sha256:646ce8f80f55948a7f089e3a7a5f00222c0cf3e82fea6c3a8ace1a51d15ea1ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-buster` - linux; amd64

```console
$ docker pull ros@sha256:953694421478b83fbba6976e01a5b90cad68357b90f6529b7d2ef1b3446a00c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.4 MB (463447648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761281453a86dd6f2a1f49082e6d95a477f3f57b89d6a5be4bfd28b811b19c6e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:02 GMT
ADD file:259be79d94a2549a667ad08a093fe18f15a6c93d66a0723292f49294e31fc7a1 in / 
# Tue, 25 Oct 2022 01:44:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:17:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:17:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:17:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:17:27 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:17:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:17:27 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:18:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:18:59 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:18:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:18:59 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:19:32 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:19:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:20:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fd31ec14dccdcda8f2472547f1a94ef0a23b8dabb764cd7b1d48aeee0afea7c8`  
		Last Modified: Tue, 25 Oct 2022 01:48:15 GMT  
		Size: 50.4 MB (50447742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7bb5a8d4409ae76ed240704c8628d248a907ec454b12a0f653fa5180822f32`  
		Last Modified: Tue, 25 Oct 2022 07:56:14 GMT  
		Size: 10.9 MB (10896941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9831692d445c53ad6706089a3b147d293d3267dd486b27109a911c9da182ed31`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2beecf1c3569265300a22936ddda05e835f0c83b2193ea68b4d60f2882113cd`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834cb0e33271e58107ddec676304ba095210344f2ee4310bb860d12b941b510c`  
		Last Modified: Tue, 25 Oct 2022 07:56:46 GMT  
		Size: 239.2 MB (239209563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdd4ac8f13eeeb7f19f875b6a9191a3aedf9fd8006aae02db37664d36f51883`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f066880bf184688bbe3b3bce165ab3ad72850aae130b41b408020b47003491`  
		Last Modified: Tue, 25 Oct 2022 07:57:07 GMT  
		Size: 86.6 MB (86586144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5c12225f8506452bbdfb135687a0e9642f4fd2bec37dacde2ff8e68f0031c8`  
		Last Modified: Tue, 25 Oct 2022 07:56:53 GMT  
		Size: 326.7 KB (326687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5cb66701beaeeb105d227e3c100dab245e25d8e913dcb72fb68145181a9140f`  
		Last Modified: Tue, 25 Oct 2022 07:57:05 GMT  
		Size: 76.0 MB (75978159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4e6ad0ca4781fdc64d09a1648afd8f8db480941c55c7584bb64df0449bfe27d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.9 MB (402884010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:943c47c820a9c53838514e9638c0e4218b301b3a485b2ded7c73b51629dc36e3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:54 GMT
ADD file:ef2ee78fb3eda698ebec33ff4b6dea672e03908b0f8630a28acb33ec9a7c3e13 in / 
# Tue, 04 Oct 2022 23:44:55 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:42:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:42:19 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:42:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:42:22 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:42:23 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:42:24 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Oct 2022 13:43:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:43:35 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 13:43:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:43:38 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:44:12 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:44:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:45:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:504dcdd9b4a0035dba7a55a5312cf594c3d22fb99b7bf676d397c464db919009`  
		Last Modified: Tue, 04 Oct 2022 23:50:47 GMT  
		Size: 49.2 MB (49228885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c286841822dd708cc8ec03c64947552384e955fad5e3df9a73a5acab4aaaed`  
		Last Modified: Wed, 05 Oct 2022 14:11:38 GMT  
		Size: 10.7 MB (10689488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b51b46470fae12ab22dbf0e0f68d92e335b5d2aec01faf4694f688dcff7ed7e`  
		Last Modified: Wed, 05 Oct 2022 14:11:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01f93551ac4426be901cafe628cfa60e541d98154404fcba3cb02cde1d85358`  
		Last Modified: Wed, 05 Oct 2022 14:11:37 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a850fdf218d14508c13532bd2745504750003968ec91b47bbc2a16d38af0791f`  
		Last Modified: Wed, 05 Oct 2022 14:12:09 GMT  
		Size: 184.4 MB (184402359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46befb9f0b1823e66932ff7e6bd3b3f7ef17e0115617e47457b2e68aa6db3103`  
		Last Modified: Wed, 05 Oct 2022 14:11:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70142cef45c79ed6c16def65c939723b912688d777616cd8f0394a0a9bed62b`  
		Last Modified: Wed, 05 Oct 2022 14:12:28 GMT  
		Size: 84.4 MB (84371054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec293e0c6336ccbd0d0986af98ef8fd2f6e8caebfc5454d01a8d50bf39f3310`  
		Last Modified: Wed, 05 Oct 2022 14:12:17 GMT  
		Size: 324.6 KB (324579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fdd5b15718815c6b2b180f7ba28bb586c4071861d49a281db790d1263561842`  
		Last Modified: Wed, 05 Oct 2022 14:12:26 GMT  
		Size: 73.9 MB (73865277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base-focal`

```console
$ docker pull ros@sha256:740d7d54d8957dc99302fbfc01c591f6ced4750cb3d79dd5419fdd2f73ea45ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:34cbfe55d811fe7c57add8b3d6f01ba9c209258ef1b4029cec5118dcd21e358f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343179990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6d7ab7e066ec3cc62a3c2bfe041ba6a0a444f0b66da68886d72c1906c5004a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:53 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:04:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:07:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:07:31 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:07:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:07:31 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:08:10 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:08:15 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:09:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcba2703cc13554dd6ac252966be0f9f0a9d6e79ee879b5e0289457bc632f55`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617320b8300618f53ec135b976c7f3a733354c5ef799b7c969108d82a8509f8`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f065fe084d225480619420eb81fce25e1ea4e12e4f4b95002773742fc0e01d67`  
		Last Modified: Tue, 25 Oct 2022 07:53:37 GMT  
		Size: 177.0 MB (177008909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f66f6a9e5d5690a6fcd01f03ca5ef0146410fa911f6fccb17d73db1bbec814`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fcd60406762b57a7de1c5c937562c8a145da66c5f0d5716f70f5c5ae115ab71`  
		Last Modified: Tue, 25 Oct 2022 07:53:56 GMT  
		Size: 50.9 MB (50940379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb29d90361859f6ac155a32b08124b4fecb3b64649f15b68b7d6b59f22d70d4`  
		Last Modified: Tue, 25 Oct 2022 07:53:47 GMT  
		Size: 332.1 KB (332101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:055f4ec67f38d1b1c161894d68208d46a4d5822664774d4554aaf150f243341c`  
		Last Modified: Tue, 25 Oct 2022 07:54:01 GMT  
		Size: 79.6 MB (79603171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:282eece3c6e182e825057bcb769c29ec38c0a3e9b2c9cb0b913ede9dec5a8ccd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289297974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727b6d344ef45add4b6b86083e60223e9bb9840f5052ac125292637db637ef91`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:44 GMT
ADD file:75870468a948359044fa3df6c07c80badfea3dcde4823d41a19285436c40cf76 in / 
# Wed, 05 Oct 2022 00:13:44 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:52:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:52:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 06 Oct 2022 06:53:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:16 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:53:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:53:16 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:53:37 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:42 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Thu, 06 Oct 2022 06:54:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e679d63f382033c15f8f921851bd71fb8a85a432c0a7a612bbef16e989075145`  
		Last Modified: Wed, 05 Oct 2022 00:15:44 GMT  
		Size: 24.6 MB (24590092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ab6ac546133bf21e51dc29641d455c42144b184821f494258ff1ec514556c`  
		Last Modified: Thu, 06 Oct 2022 07:00:40 GMT  
		Size: 1.2 MB (1163905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4706759f53c150848596edb49143a211c7e072793acea609cc8e9c0f267c4e3e`  
		Last Modified: Thu, 06 Oct 2022 07:00:38 GMT  
		Size: 4.7 MB (4675577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b0360f8c716b3c493ff9708abd3c165f9de06193430830ea64d829b1a6ac2`  
		Last Modified: Thu, 06 Oct 2022 07:00:37 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd789251f14b7842f745c35075b3e7f88a5aa3fb3b005a3bd0fde7d8f285d7f`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24248fc7fc767d03259bb795d6c177495b4f61cdb1ddcc6a6bb9bb7dcd5958db`  
		Last Modified: Thu, 06 Oct 2022 07:01:15 GMT  
		Size: 157.6 MB (157550749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1b296e1c261f003a529641cc88d1393116b3a0b1f7853da9463a2e9c16df7c`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1461e09b998de0d3b7ae285e2a3bb8bcb1b889f8a12f832e208d7ec8d3bfe847`  
		Last Modified: Thu, 06 Oct 2022 07:01:36 GMT  
		Size: 40.5 MB (40505592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e355cb57c65a1dc870c88f7e383d6a76770d5f6563b605a9a96dc5ceb24b3a`  
		Last Modified: Thu, 06 Oct 2022 07:01:28 GMT  
		Size: 329.9 KB (329943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b0b621043424762e62d798dd71533b7835ccd3741e94dcdc7fbbdd3ca4f723`  
		Last Modified: Thu, 06 Oct 2022 07:01:40 GMT  
		Size: 60.5 MB (60479707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:76fd0c9142e5ac05def8adba27f5ae4d8887f4d16e7997c9811a9b93691cadd3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322256415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5417df554ee3ec7fde99d2d44aa591593c7532653b7f97faafd2c5d48ec2baf4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:36:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:36:52 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:36:53 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:36:54 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Oct 2022 13:37:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:37:54 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 13:37:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:37:57 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:38:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:38:34 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 13:38:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2066945f278504a3fbe15500f54112556cb9e9febb0b4d07edd644ecbae9209c`  
		Last Modified: Wed, 05 Oct 2022 14:09:02 GMT  
		Size: 1.2 MB (1164049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ca1624225b52b4e52d61f82b52ba0653fdefd1bcde8f1017fc0031f256a5d`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 5.3 MB (5322416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f0727eb08e94e95fafae4d8d0079ee1413dc8ff544022ff06d844f4a53bf3c`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf931507240c54649243355c092bd81e83eae6916ab26a7620f410132c2d47c`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991837517e4c0d5001d2caa2a90cf5e70018524cf2ad724b9cf736dc76eb1d05`  
		Last Modified: Wed, 05 Oct 2022 14:09:29 GMT  
		Size: 171.5 MB (171504736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d4fe51a6dd429e99d46144fc5ddd118e6c466b37ffb21e3942c6fb1bcb67ac`  
		Last Modified: Wed, 05 Oct 2022 14:08:59 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a814635c2ec9fc6aa1c79542be862549465c5ec04cef8ec399952b79e14fe736`  
		Last Modified: Wed, 05 Oct 2022 14:09:46 GMT  
		Size: 45.0 MB (44987961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f762c4f58b5522b0b2e4a82a4b02573353cdb815242b32b47ea696270c4f74f0`  
		Last Modified: Wed, 05 Oct 2022 14:09:40 GMT  
		Size: 329.8 KB (329844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7389f48d507d2a20ca2a184d421e98d9717ff8bd42ce2a9e76b6b153dfc2ee27`  
		Last Modified: Wed, 05 Oct 2022 14:09:50 GMT  
		Size: 71.8 MB (71753417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:dcd32cd394a96ef4c078295a435f364ce065d1fbc95e87158eef5f576ec7d073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:846f250f6dd222e44ee17b7f871875e20abd569082de6299b1d3fb89b4a60ee9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212304339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c78d80b5cf8bf8109d294a84172eb5bc1f718d08607ed579e63932bac8cfa9d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:53 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:04:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:07:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:07:31 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:07:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:07:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcba2703cc13554dd6ac252966be0f9f0a9d6e79ee879b5e0289457bc632f55`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617320b8300618f53ec135b976c7f3a733354c5ef799b7c969108d82a8509f8`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f065fe084d225480619420eb81fce25e1ea4e12e4f4b95002773742fc0e01d67`  
		Last Modified: Tue, 25 Oct 2022 07:53:37 GMT  
		Size: 177.0 MB (177008909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f66f6a9e5d5690a6fcd01f03ca5ef0146410fa911f6fccb17d73db1bbec814`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:67ea8f522d8e90ade44c0d45a623b182c7dbb9f48f4b567f1079e6d3136ca48c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187982732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7c3f4179402fe66a367adbf02ca6941b11a372f4111ef176ab7c3c7de1f500`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:44 GMT
ADD file:75870468a948359044fa3df6c07c80badfea3dcde4823d41a19285436c40cf76 in / 
# Wed, 05 Oct 2022 00:13:44 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:52:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:52:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 06 Oct 2022 06:53:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:16 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:53:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:53:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e679d63f382033c15f8f921851bd71fb8a85a432c0a7a612bbef16e989075145`  
		Last Modified: Wed, 05 Oct 2022 00:15:44 GMT  
		Size: 24.6 MB (24590092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ab6ac546133bf21e51dc29641d455c42144b184821f494258ff1ec514556c`  
		Last Modified: Thu, 06 Oct 2022 07:00:40 GMT  
		Size: 1.2 MB (1163905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4706759f53c150848596edb49143a211c7e072793acea609cc8e9c0f267c4e3e`  
		Last Modified: Thu, 06 Oct 2022 07:00:38 GMT  
		Size: 4.7 MB (4675577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b0360f8c716b3c493ff9708abd3c165f9de06193430830ea64d829b1a6ac2`  
		Last Modified: Thu, 06 Oct 2022 07:00:37 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd789251f14b7842f745c35075b3e7f88a5aa3fb3b005a3bd0fde7d8f285d7f`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24248fc7fc767d03259bb795d6c177495b4f61cdb1ddcc6a6bb9bb7dcd5958db`  
		Last Modified: Thu, 06 Oct 2022 07:01:15 GMT  
		Size: 157.6 MB (157550749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1b296e1c261f003a529641cc88d1393116b3a0b1f7853da9463a2e9c16df7c`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f89895ef429256f804633dc9c6e2ab38c57680aa920bc071d8f71efbc5020e42
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.2 MB (205185193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9baaec59cb59cfd4a6e30cff261cc9b7590948f136dad75047c09c4eff7a60ec`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:36:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:36:52 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:36:53 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:36:54 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Oct 2022 13:37:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:37:54 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 13:37:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:37:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2066945f278504a3fbe15500f54112556cb9e9febb0b4d07edd644ecbae9209c`  
		Last Modified: Wed, 05 Oct 2022 14:09:02 GMT  
		Size: 1.2 MB (1164049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ca1624225b52b4e52d61f82b52ba0653fdefd1bcde8f1017fc0031f256a5d`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 5.3 MB (5322416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f0727eb08e94e95fafae4d8d0079ee1413dc8ff544022ff06d844f4a53bf3c`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf931507240c54649243355c092bd81e83eae6916ab26a7620f410132c2d47c`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991837517e4c0d5001d2caa2a90cf5e70018524cf2ad724b9cf736dc76eb1d05`  
		Last Modified: Wed, 05 Oct 2022 14:09:29 GMT  
		Size: 171.5 MB (171504736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d4fe51a6dd429e99d46144fc5ddd118e6c466b37ffb21e3942c6fb1bcb67ac`  
		Last Modified: Wed, 05 Oct 2022 14:08:59 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:f50f7d71b0234def8c92b7ae11474584f042f7673343bda8ef2053e0ef2590f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:53efc571f64b54efd30784d514c0fa3bd40c8d6b08ea7d4af6aa443dfc6685fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300556658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6517633704986256d83bc929f469d3f13adec737859a7b4c1e04b3251f94a064`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:02 GMT
ADD file:259be79d94a2549a667ad08a093fe18f15a6c93d66a0723292f49294e31fc7a1 in / 
# Tue, 25 Oct 2022 01:44:02 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:17:24 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:17:25 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:17:26 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:17:27 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:17:27 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:17:27 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:18:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:18:59 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:18:59 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:18:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fd31ec14dccdcda8f2472547f1a94ef0a23b8dabb764cd7b1d48aeee0afea7c8`  
		Last Modified: Tue, 25 Oct 2022 01:48:15 GMT  
		Size: 50.4 MB (50447742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b7bb5a8d4409ae76ed240704c8628d248a907ec454b12a0f653fa5180822f32`  
		Last Modified: Tue, 25 Oct 2022 07:56:14 GMT  
		Size: 10.9 MB (10896941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9831692d445c53ad6706089a3b147d293d3267dd486b27109a911c9da182ed31`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2beecf1c3569265300a22936ddda05e835f0c83b2193ea68b4d60f2882113cd`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834cb0e33271e58107ddec676304ba095210344f2ee4310bb860d12b941b510c`  
		Last Modified: Tue, 25 Oct 2022 07:56:46 GMT  
		Size: 239.2 MB (239209563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdd4ac8f13eeeb7f19f875b6a9191a3aedf9fd8006aae02db37664d36f51883`  
		Last Modified: Tue, 25 Oct 2022 07:56:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:afc032e9fa26896123d80250930a58078ebf41c1ff40beba11ea11c54d5a2193
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 MB (244323100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746f7bae696247627d344c0afb30c2178be92cef192a0b9831736fa090473713`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:54 GMT
ADD file:ef2ee78fb3eda698ebec33ff4b6dea672e03908b0f8630a28acb33ec9a7c3e13 in / 
# Tue, 04 Oct 2022 23:44:55 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:42:18 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:42:19 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:42:21 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:42:22 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:42:23 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:42:24 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Oct 2022 13:43:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:43:35 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 13:43:36 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:43:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:504dcdd9b4a0035dba7a55a5312cf594c3d22fb99b7bf676d397c464db919009`  
		Last Modified: Tue, 04 Oct 2022 23:50:47 GMT  
		Size: 49.2 MB (49228885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c286841822dd708cc8ec03c64947552384e955fad5e3df9a73a5acab4aaaed`  
		Last Modified: Wed, 05 Oct 2022 14:11:38 GMT  
		Size: 10.7 MB (10689488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b51b46470fae12ab22dbf0e0f68d92e335b5d2aec01faf4694f688dcff7ed7e`  
		Last Modified: Wed, 05 Oct 2022 14:11:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01f93551ac4426be901cafe628cfa60e541d98154404fcba3cb02cde1d85358`  
		Last Modified: Wed, 05 Oct 2022 14:11:37 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a850fdf218d14508c13532bd2745504750003968ec91b47bbc2a16d38af0791f`  
		Last Modified: Wed, 05 Oct 2022 14:12:09 GMT  
		Size: 184.4 MB (184402359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46befb9f0b1823e66932ff7e6bd3b3f7ef17e0115617e47457b2e68aa6db3103`  
		Last Modified: Wed, 05 Oct 2022 14:11:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:dcd32cd394a96ef4c078295a435f364ce065d1fbc95e87158eef5f576ec7d073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:846f250f6dd222e44ee17b7f871875e20abd569082de6299b1d3fb89b4a60ee9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212304339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c78d80b5cf8bf8109d294a84172eb5bc1f718d08607ed579e63932bac8cfa9d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:04:29 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:52 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:04:53 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 25 Oct 2022 07:04:54 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:04:54 GMT
ENV ROS_DISTRO=noetic
# Tue, 25 Oct 2022 07:07:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:07:31 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 25 Oct 2022 07:07:31 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:07:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff4b427f850657d03c70299694b020567ea6ea793e6e9113bc123ebe18aaf4`  
		Last Modified: Tue, 25 Oct 2022 07:52:57 GMT  
		Size: 1.2 MB (1163883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472155f6e6612bc976b4f23b2fbc13373ddcbbd7414f6b13ba9a6c11e853ec9b`  
		Last Modified: Tue, 25 Oct 2022 07:52:55 GMT  
		Size: 5.6 MB (5551301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcba2703cc13554dd6ac252966be0f9f0a9d6e79ee879b5e0289457bc632f55`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617320b8300618f53ec135b976c7f3a733354c5ef799b7c969108d82a8509f8`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f065fe084d225480619420eb81fce25e1ea4e12e4f4b95002773742fc0e01d67`  
		Last Modified: Tue, 25 Oct 2022 07:53:37 GMT  
		Size: 177.0 MB (177008909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f66f6a9e5d5690a6fcd01f03ca5ef0146410fa911f6fccb17d73db1bbec814`  
		Last Modified: Tue, 25 Oct 2022 07:52:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:67ea8f522d8e90ade44c0d45a623b182c7dbb9f48f4b567f1079e6d3136ca48c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187982732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7c3f4179402fe66a367adbf02ca6941b11a372f4111ef176ab7c3c7de1f500`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:13:44 GMT
ADD file:75870468a948359044fa3df6c07c80badfea3dcde4823d41a19285436c40cf76 in / 
# Wed, 05 Oct 2022 00:13:44 GMT
CMD ["bash"]
# Thu, 06 Oct 2022 06:52:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:52:15 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Thu, 06 Oct 2022 06:52:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LANG=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV LC_ALL=C.UTF-8
# Thu, 06 Oct 2022 06:52:16 GMT
ENV ROS_DISTRO=noetic
# Thu, 06 Oct 2022 06:53:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Thu, 06 Oct 2022 06:53:16 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Thu, 06 Oct 2022 06:53:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Thu, 06 Oct 2022 06:53:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e679d63f382033c15f8f921851bd71fb8a85a432c0a7a612bbef16e989075145`  
		Last Modified: Wed, 05 Oct 2022 00:15:44 GMT  
		Size: 24.6 MB (24590092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ab6ac546133bf21e51dc29641d455c42144b184821f494258ff1ec514556c`  
		Last Modified: Thu, 06 Oct 2022 07:00:40 GMT  
		Size: 1.2 MB (1163905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4706759f53c150848596edb49143a211c7e072793acea609cc8e9c0f267c4e3e`  
		Last Modified: Thu, 06 Oct 2022 07:00:38 GMT  
		Size: 4.7 MB (4675577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291b0360f8c716b3c493ff9708abd3c165f9de06193430830ea64d829b1a6ac2`  
		Last Modified: Thu, 06 Oct 2022 07:00:37 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd789251f14b7842f745c35075b3e7f88a5aa3fb3b005a3bd0fde7d8f285d7f`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 2.0 KB (1986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24248fc7fc767d03259bb795d6c177495b4f61cdb1ddcc6a6bb9bb7dcd5958db`  
		Last Modified: Thu, 06 Oct 2022 07:01:15 GMT  
		Size: 157.6 MB (157550749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1b296e1c261f003a529641cc88d1393116b3a0b1f7853da9463a2e9c16df7c`  
		Last Modified: Thu, 06 Oct 2022 07:00:36 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:f89895ef429256f804633dc9c6e2ab38c57680aa920bc071d8f71efbc5020e42
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.2 MB (205185193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9baaec59cb59cfd4a6e30cff261cc9b7590948f136dad75047c09c4eff7a60ec`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:10 GMT
ADD file:30b589901d2a6b82d0b7271487bdaf37514649a798cc13a17f74394321bdd051 in / 
# Wed, 05 Oct 2022 00:02:11 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:36:38 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:36:49 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 05 Oct 2022 13:36:51 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:36:52 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:36:53 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 13:36:54 GMT
ENV ROS_DISTRO=noetic
# Wed, 05 Oct 2022 13:37:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:37:54 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 05 Oct 2022 13:37:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 13:37:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:514fa78e57ce0d9437bc984cc36ab780c24b69da2b922bfff16737072e3e7de2`  
		Last Modified: Wed, 05 Oct 2022 00:03:51 GMT  
		Size: 27.2 MB (27191622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2066945f278504a3fbe15500f54112556cb9e9febb0b4d07edd644ecbae9209c`  
		Last Modified: Wed, 05 Oct 2022 14:09:02 GMT  
		Size: 1.2 MB (1164049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:234ca1624225b52b4e52d61f82b52ba0653fdefd1bcde8f1017fc0031f256a5d`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 5.3 MB (5322416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f0727eb08e94e95fafae4d8d0079ee1413dc8ff544022ff06d844f4a53bf3c`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf931507240c54649243355c092bd81e83eae6916ab26a7620f410132c2d47c`  
		Last Modified: Wed, 05 Oct 2022 14:09:00 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991837517e4c0d5001d2caa2a90cf5e70018524cf2ad724b9cf736dc76eb1d05`  
		Last Modified: Wed, 05 Oct 2022 14:09:29 GMT  
		Size: 171.5 MB (171504736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d4fe51a6dd429e99d46144fc5ddd118e6c466b37ffb21e3942c6fb1bcb67ac`  
		Last Modified: Wed, 05 Oct 2022 14:08:59 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling`

```console
$ docker pull ros@sha256:100afa8d605fdd232638c325f38ddb6d31c3ec2758e56f71b51192baf4b751f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:44bdbd819383462c025ea361c9c8427375ba5c38201356b93c5827ae7b1ebf8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263221662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd67ef1ef5ce96f4a5c4ee7e03559ae7c8da886e0ac2f52a705eb33428dce931`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:45:02 GMT
ENV ROS_DISTRO=rolling
# Tue, 25 Oct 2022 07:45:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:45:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:45:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:45:48 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:46:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:46:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:46:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:46:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7767abbf3782738860e3bb5ede4f627dba0211161ae5cfa4a72cf1dd43c58be4`  
		Last Modified: Tue, 25 Oct 2022 08:05:34 GMT  
		Size: 106.4 MB (106391215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8106ab6bf436bb06edcea0071debbc4b31d730b8cc8ca4d7fd6af8bd19ea702a`  
		Last Modified: Tue, 25 Oct 2022 08:05:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb38b610c9d923dbe6bbe532a0559a4064856d0105bf842e52ce1ad4ff11e8b`  
		Last Modified: Tue, 25 Oct 2022 08:05:58 GMT  
		Size: 97.9 MB (97879015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5faad8ca67596a7af7c25ade2313bccb1e13db2a2646e408a7171bdcce0e48b6`  
		Last Modified: Tue, 25 Oct 2022 08:05:44 GMT  
		Size: 289.2 KB (289222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e4659981956310c677c0249ba2e2eba19ae8b8670034f1b14176d899fde8b0`  
		Last Modified: Tue, 25 Oct 2022 08:05:44 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af086c324a03d7da5c2309c2b4691d12e9153d09eb5464a8a4442fa3a8c24ae`  
		Last Modified: Tue, 25 Oct 2022 08:05:49 GMT  
		Size: 23.2 MB (23226799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:33669f7bf08ec323d17bd2d63532f30fe9982bbb13f7cf849dd97b000c8a1827
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255407846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0b50bb3221f9dcf4ace9413a489fa328657908bfeada9464bac70440cca785`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:55:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:55:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:55:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:55:18 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 14:00:21 GMT
ENV ROS_DISTRO=rolling
# Wed, 05 Oct 2022 14:01:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:01:08 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 14:01:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 14:01:09 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 14:01:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:01:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 14:01:52 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 14:02:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a891d50162687d5b4db85383705535653c56066b48e0e3314badd3e76d2f8af`  
		Last Modified: Wed, 05 Oct 2022 14:16:45 GMT  
		Size: 1.2 MB (1178125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3fc4af9e9380eebc7d111e904fb1098bb4102f7271c19ade184c620ba4d5dc`  
		Last Modified: Wed, 05 Oct 2022 14:16:43 GMT  
		Size: 3.6 MB (3594928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc1176274b8951042f2b29277ebbcdc02bf43ea04b1e95a7e7f80c137ddb1d`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca88c2c17aef59df2c29525001e8bb7f45b3b5e37ef793847df2e89374421e`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3834504b668bb13d4fcded46b2444690bed0603eccbb71ffd03d0ab432593c8e`  
		Last Modified: Wed, 05 Oct 2022 14:20:23 GMT  
		Size: 104.1 MB (104103500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ce9b251482e03203dd3f2b75f07f06ff803e68b582e12a53ce6cc1028c9c58`  
		Last Modified: Wed, 05 Oct 2022 14:20:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2767f80cc9b7f92921da87e086a643d8d80b257ce273716d8795816f765216`  
		Last Modified: Wed, 05 Oct 2022 14:20:48 GMT  
		Size: 95.2 MB (95215484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1c34644006693e54ff50141efeaec2467a06586f1f28d4e4874485d96ad999`  
		Last Modified: Wed, 05 Oct 2022 14:20:35 GMT  
		Size: 287.8 KB (287799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9377d158c53ca57fb20de69f4e1e1f1bb1741c856365104a808553e58c611ecc`  
		Last Modified: Wed, 05 Oct 2022 14:20:35 GMT  
		Size: 2.4 KB (2353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f3f8b1a658efb974ec2a2c92261fc0ca9d5ad9d4eecf003b8752e7b82ab271`  
		Last Modified: Wed, 05 Oct 2022 14:20:38 GMT  
		Size: 22.6 MB (22641030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:447047b2f4f11416f680d9d04276e74d038fc664e85ecc429fe88e6892b7b74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:5b6c57eef6e1d7715608064ff21c0dda63c00346cf7aff24cb7d14e7cc1cfa5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1088048490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a22bed2655671151456cb87328451adae485aa8e08b1dbf61ce345483c70dce`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:45:02 GMT
ENV ROS_DISTRO=rolling
# Tue, 25 Oct 2022 07:45:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:45:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:45:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:45:48 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:46:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:46:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:46:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:46:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:48:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7767abbf3782738860e3bb5ede4f627dba0211161ae5cfa4a72cf1dd43c58be4`  
		Last Modified: Tue, 25 Oct 2022 08:05:34 GMT  
		Size: 106.4 MB (106391215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8106ab6bf436bb06edcea0071debbc4b31d730b8cc8ca4d7fd6af8bd19ea702a`  
		Last Modified: Tue, 25 Oct 2022 08:05:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb38b610c9d923dbe6bbe532a0559a4064856d0105bf842e52ce1ad4ff11e8b`  
		Last Modified: Tue, 25 Oct 2022 08:05:58 GMT  
		Size: 97.9 MB (97879015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5faad8ca67596a7af7c25ade2313bccb1e13db2a2646e408a7171bdcce0e48b6`  
		Last Modified: Tue, 25 Oct 2022 08:05:44 GMT  
		Size: 289.2 KB (289222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e4659981956310c677c0249ba2e2eba19ae8b8670034f1b14176d899fde8b0`  
		Last Modified: Tue, 25 Oct 2022 08:05:44 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af086c324a03d7da5c2309c2b4691d12e9153d09eb5464a8a4442fa3a8c24ae`  
		Last Modified: Tue, 25 Oct 2022 08:05:49 GMT  
		Size: 23.2 MB (23226799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57143ed7f731779085a0e57d22932271e243520fd47318ed7ccf08cd50211152`  
		Last Modified: Tue, 25 Oct 2022 08:07:51 GMT  
		Size: 824.8 MB (824826828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:78be1143dc94dd563150a00555027432042e7bf6add3629226596a7999011f96
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1037757233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9ba2abd3234b7b99a4632f3b505eb02d7129973d39e19be1d45f31ae01566e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:55:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:55:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:55:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:55:18 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 14:00:21 GMT
ENV ROS_DISTRO=rolling
# Wed, 05 Oct 2022 14:01:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:01:08 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 14:01:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 14:01:09 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 14:01:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:01:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 14:01:52 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 14:02:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:04:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a891d50162687d5b4db85383705535653c56066b48e0e3314badd3e76d2f8af`  
		Last Modified: Wed, 05 Oct 2022 14:16:45 GMT  
		Size: 1.2 MB (1178125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3fc4af9e9380eebc7d111e904fb1098bb4102f7271c19ade184c620ba4d5dc`  
		Last Modified: Wed, 05 Oct 2022 14:16:43 GMT  
		Size: 3.6 MB (3594928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc1176274b8951042f2b29277ebbcdc02bf43ea04b1e95a7e7f80c137ddb1d`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca88c2c17aef59df2c29525001e8bb7f45b3b5e37ef793847df2e89374421e`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3834504b668bb13d4fcded46b2444690bed0603eccbb71ffd03d0ab432593c8e`  
		Last Modified: Wed, 05 Oct 2022 14:20:23 GMT  
		Size: 104.1 MB (104103500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ce9b251482e03203dd3f2b75f07f06ff803e68b582e12a53ce6cc1028c9c58`  
		Last Modified: Wed, 05 Oct 2022 14:20:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2767f80cc9b7f92921da87e086a643d8d80b257ce273716d8795816f765216`  
		Last Modified: Wed, 05 Oct 2022 14:20:48 GMT  
		Size: 95.2 MB (95215484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1c34644006693e54ff50141efeaec2467a06586f1f28d4e4874485d96ad999`  
		Last Modified: Wed, 05 Oct 2022 14:20:35 GMT  
		Size: 287.8 KB (287799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9377d158c53ca57fb20de69f4e1e1f1bb1741c856365104a808553e58c611ecc`  
		Last Modified: Wed, 05 Oct 2022 14:20:35 GMT  
		Size: 2.4 KB (2353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f3f8b1a658efb974ec2a2c92261fc0ca9d5ad9d4eecf003b8752e7b82ab271`  
		Last Modified: Wed, 05 Oct 2022 14:20:38 GMT  
		Size: 22.6 MB (22641030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4de81c13532f2a3ae50f8a84d32f7fbe4788fc88103638857e208cc54f63ef1`  
		Last Modified: Wed, 05 Oct 2022 14:22:40 GMT  
		Size: 782.3 MB (782349387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-perception-jammy`

```console
$ docker pull ros@sha256:447047b2f4f11416f680d9d04276e74d038fc664e85ecc429fe88e6892b7b74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:5b6c57eef6e1d7715608064ff21c0dda63c00346cf7aff24cb7d14e7cc1cfa5b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1088048490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a22bed2655671151456cb87328451adae485aa8e08b1dbf61ce345483c70dce`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:45:02 GMT
ENV ROS_DISTRO=rolling
# Tue, 25 Oct 2022 07:45:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:45:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:45:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:45:48 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:46:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:46:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:46:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:46:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:48:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7767abbf3782738860e3bb5ede4f627dba0211161ae5cfa4a72cf1dd43c58be4`  
		Last Modified: Tue, 25 Oct 2022 08:05:34 GMT  
		Size: 106.4 MB (106391215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8106ab6bf436bb06edcea0071debbc4b31d730b8cc8ca4d7fd6af8bd19ea702a`  
		Last Modified: Tue, 25 Oct 2022 08:05:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb38b610c9d923dbe6bbe532a0559a4064856d0105bf842e52ce1ad4ff11e8b`  
		Last Modified: Tue, 25 Oct 2022 08:05:58 GMT  
		Size: 97.9 MB (97879015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5faad8ca67596a7af7c25ade2313bccb1e13db2a2646e408a7171bdcce0e48b6`  
		Last Modified: Tue, 25 Oct 2022 08:05:44 GMT  
		Size: 289.2 KB (289222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e4659981956310c677c0249ba2e2eba19ae8b8670034f1b14176d899fde8b0`  
		Last Modified: Tue, 25 Oct 2022 08:05:44 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af086c324a03d7da5c2309c2b4691d12e9153d09eb5464a8a4442fa3a8c24ae`  
		Last Modified: Tue, 25 Oct 2022 08:05:49 GMT  
		Size: 23.2 MB (23226799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57143ed7f731779085a0e57d22932271e243520fd47318ed7ccf08cd50211152`  
		Last Modified: Tue, 25 Oct 2022 08:07:51 GMT  
		Size: 824.8 MB (824826828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:78be1143dc94dd563150a00555027432042e7bf6add3629226596a7999011f96
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1037757233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9ba2abd3234b7b99a4632f3b505eb02d7129973d39e19be1d45f31ae01566e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:55:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:55:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:55:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:55:18 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 14:00:21 GMT
ENV ROS_DISTRO=rolling
# Wed, 05 Oct 2022 14:01:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:01:08 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 14:01:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 14:01:09 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 14:01:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:01:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 14:01:52 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 14:02:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:04:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a891d50162687d5b4db85383705535653c56066b48e0e3314badd3e76d2f8af`  
		Last Modified: Wed, 05 Oct 2022 14:16:45 GMT  
		Size: 1.2 MB (1178125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3fc4af9e9380eebc7d111e904fb1098bb4102f7271c19ade184c620ba4d5dc`  
		Last Modified: Wed, 05 Oct 2022 14:16:43 GMT  
		Size: 3.6 MB (3594928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc1176274b8951042f2b29277ebbcdc02bf43ea04b1e95a7e7f80c137ddb1d`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca88c2c17aef59df2c29525001e8bb7f45b3b5e37ef793847df2e89374421e`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3834504b668bb13d4fcded46b2444690bed0603eccbb71ffd03d0ab432593c8e`  
		Last Modified: Wed, 05 Oct 2022 14:20:23 GMT  
		Size: 104.1 MB (104103500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ce9b251482e03203dd3f2b75f07f06ff803e68b582e12a53ce6cc1028c9c58`  
		Last Modified: Wed, 05 Oct 2022 14:20:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2767f80cc9b7f92921da87e086a643d8d80b257ce273716d8795816f765216`  
		Last Modified: Wed, 05 Oct 2022 14:20:48 GMT  
		Size: 95.2 MB (95215484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1c34644006693e54ff50141efeaec2467a06586f1f28d4e4874485d96ad999`  
		Last Modified: Wed, 05 Oct 2022 14:20:35 GMT  
		Size: 287.8 KB (287799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9377d158c53ca57fb20de69f4e1e1f1bb1741c856365104a808553e58c611ecc`  
		Last Modified: Wed, 05 Oct 2022 14:20:35 GMT  
		Size: 2.4 KB (2353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f3f8b1a658efb974ec2a2c92261fc0ca9d5ad9d4eecf003b8752e7b82ab271`  
		Last Modified: Wed, 05 Oct 2022 14:20:38 GMT  
		Size: 22.6 MB (22641030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4de81c13532f2a3ae50f8a84d32f7fbe4788fc88103638857e208cc54f63ef1`  
		Last Modified: Wed, 05 Oct 2022 14:22:40 GMT  
		Size: 782.3 MB (782349387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:100afa8d605fdd232638c325f38ddb6d31c3ec2758e56f71b51192baf4b751f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:44bdbd819383462c025ea361c9c8427375ba5c38201356b93c5827ae7b1ebf8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263221662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd67ef1ef5ce96f4a5c4ee7e03559ae7c8da886e0ac2f52a705eb33428dce931`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:45:02 GMT
ENV ROS_DISTRO=rolling
# Tue, 25 Oct 2022 07:45:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:45:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:45:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:45:48 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:46:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:46:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:46:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:46:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7767abbf3782738860e3bb5ede4f627dba0211161ae5cfa4a72cf1dd43c58be4`  
		Last Modified: Tue, 25 Oct 2022 08:05:34 GMT  
		Size: 106.4 MB (106391215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8106ab6bf436bb06edcea0071debbc4b31d730b8cc8ca4d7fd6af8bd19ea702a`  
		Last Modified: Tue, 25 Oct 2022 08:05:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb38b610c9d923dbe6bbe532a0559a4064856d0105bf842e52ce1ad4ff11e8b`  
		Last Modified: Tue, 25 Oct 2022 08:05:58 GMT  
		Size: 97.9 MB (97879015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5faad8ca67596a7af7c25ade2313bccb1e13db2a2646e408a7171bdcce0e48b6`  
		Last Modified: Tue, 25 Oct 2022 08:05:44 GMT  
		Size: 289.2 KB (289222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e4659981956310c677c0249ba2e2eba19ae8b8670034f1b14176d899fde8b0`  
		Last Modified: Tue, 25 Oct 2022 08:05:44 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af086c324a03d7da5c2309c2b4691d12e9153d09eb5464a8a4442fa3a8c24ae`  
		Last Modified: Tue, 25 Oct 2022 08:05:49 GMT  
		Size: 23.2 MB (23226799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:33669f7bf08ec323d17bd2d63532f30fe9982bbb13f7cf849dd97b000c8a1827
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255407846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0b50bb3221f9dcf4ace9413a489fa328657908bfeada9464bac70440cca785`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:55:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:55:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:55:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:55:18 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 14:00:21 GMT
ENV ROS_DISTRO=rolling
# Wed, 05 Oct 2022 14:01:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:01:08 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 14:01:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 14:01:09 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 14:01:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:01:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 14:01:52 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 14:02:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a891d50162687d5b4db85383705535653c56066b48e0e3314badd3e76d2f8af`  
		Last Modified: Wed, 05 Oct 2022 14:16:45 GMT  
		Size: 1.2 MB (1178125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3fc4af9e9380eebc7d111e904fb1098bb4102f7271c19ade184c620ba4d5dc`  
		Last Modified: Wed, 05 Oct 2022 14:16:43 GMT  
		Size: 3.6 MB (3594928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc1176274b8951042f2b29277ebbcdc02bf43ea04b1e95a7e7f80c137ddb1d`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca88c2c17aef59df2c29525001e8bb7f45b3b5e37ef793847df2e89374421e`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3834504b668bb13d4fcded46b2444690bed0603eccbb71ffd03d0ab432593c8e`  
		Last Modified: Wed, 05 Oct 2022 14:20:23 GMT  
		Size: 104.1 MB (104103500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ce9b251482e03203dd3f2b75f07f06ff803e68b582e12a53ce6cc1028c9c58`  
		Last Modified: Wed, 05 Oct 2022 14:20:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2767f80cc9b7f92921da87e086a643d8d80b257ce273716d8795816f765216`  
		Last Modified: Wed, 05 Oct 2022 14:20:48 GMT  
		Size: 95.2 MB (95215484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1c34644006693e54ff50141efeaec2467a06586f1f28d4e4874485d96ad999`  
		Last Modified: Wed, 05 Oct 2022 14:20:35 GMT  
		Size: 287.8 KB (287799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9377d158c53ca57fb20de69f4e1e1f1bb1741c856365104a808553e58c611ecc`  
		Last Modified: Wed, 05 Oct 2022 14:20:35 GMT  
		Size: 2.4 KB (2353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f3f8b1a658efb974ec2a2c92261fc0ca9d5ad9d4eecf003b8752e7b82ab271`  
		Last Modified: Wed, 05 Oct 2022 14:20:38 GMT  
		Size: 22.6 MB (22641030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base-jammy`

```console
$ docker pull ros@sha256:100afa8d605fdd232638c325f38ddb6d31c3ec2758e56f71b51192baf4b751f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:44bdbd819383462c025ea361c9c8427375ba5c38201356b93c5827ae7b1ebf8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263221662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd67ef1ef5ce96f4a5c4ee7e03559ae7c8da886e0ac2f52a705eb33428dce931`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:45:02 GMT
ENV ROS_DISTRO=rolling
# Tue, 25 Oct 2022 07:45:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:45:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:45:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:45:48 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:46:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:46:16 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 25 Oct 2022 07:46:23 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 25 Oct 2022 07:46:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7767abbf3782738860e3bb5ede4f627dba0211161ae5cfa4a72cf1dd43c58be4`  
		Last Modified: Tue, 25 Oct 2022 08:05:34 GMT  
		Size: 106.4 MB (106391215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8106ab6bf436bb06edcea0071debbc4b31d730b8cc8ca4d7fd6af8bd19ea702a`  
		Last Modified: Tue, 25 Oct 2022 08:05:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beb38b610c9d923dbe6bbe532a0559a4064856d0105bf842e52ce1ad4ff11e8b`  
		Last Modified: Tue, 25 Oct 2022 08:05:58 GMT  
		Size: 97.9 MB (97879015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5faad8ca67596a7af7c25ade2313bccb1e13db2a2646e408a7171bdcce0e48b6`  
		Last Modified: Tue, 25 Oct 2022 08:05:44 GMT  
		Size: 289.2 KB (289222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e4659981956310c677c0249ba2e2eba19ae8b8670034f1b14176d899fde8b0`  
		Last Modified: Tue, 25 Oct 2022 08:05:44 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af086c324a03d7da5c2309c2b4691d12e9153d09eb5464a8a4442fa3a8c24ae`  
		Last Modified: Tue, 25 Oct 2022 08:05:49 GMT  
		Size: 23.2 MB (23226799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:33669f7bf08ec323d17bd2d63532f30fe9982bbb13f7cf849dd97b000c8a1827
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255407846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0b50bb3221f9dcf4ace9413a489fa328657908bfeada9464bac70440cca785`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:55:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:55:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:55:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:55:18 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 14:00:21 GMT
ENV ROS_DISTRO=rolling
# Wed, 05 Oct 2022 14:01:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:01:08 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 14:01:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 14:01:09 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 14:01:44 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:01:49 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 05 Oct 2022 14:01:52 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Wed, 05 Oct 2022 14:02:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a891d50162687d5b4db85383705535653c56066b48e0e3314badd3e76d2f8af`  
		Last Modified: Wed, 05 Oct 2022 14:16:45 GMT  
		Size: 1.2 MB (1178125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3fc4af9e9380eebc7d111e904fb1098bb4102f7271c19ade184c620ba4d5dc`  
		Last Modified: Wed, 05 Oct 2022 14:16:43 GMT  
		Size: 3.6 MB (3594928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc1176274b8951042f2b29277ebbcdc02bf43ea04b1e95a7e7f80c137ddb1d`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca88c2c17aef59df2c29525001e8bb7f45b3b5e37ef793847df2e89374421e`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3834504b668bb13d4fcded46b2444690bed0603eccbb71ffd03d0ab432593c8e`  
		Last Modified: Wed, 05 Oct 2022 14:20:23 GMT  
		Size: 104.1 MB (104103500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ce9b251482e03203dd3f2b75f07f06ff803e68b582e12a53ce6cc1028c9c58`  
		Last Modified: Wed, 05 Oct 2022 14:20:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f2767f80cc9b7f92921da87e086a643d8d80b257ce273716d8795816f765216`  
		Last Modified: Wed, 05 Oct 2022 14:20:48 GMT  
		Size: 95.2 MB (95215484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1c34644006693e54ff50141efeaec2467a06586f1f28d4e4874485d96ad999`  
		Last Modified: Wed, 05 Oct 2022 14:20:35 GMT  
		Size: 287.8 KB (287799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9377d158c53ca57fb20de69f4e1e1f1bb1741c856365104a808553e58c611ecc`  
		Last Modified: Wed, 05 Oct 2022 14:20:35 GMT  
		Size: 2.4 KB (2353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f3f8b1a658efb974ec2a2c92261fc0ca9d5ad9d4eecf003b8752e7b82ab271`  
		Last Modified: Wed, 05 Oct 2022 14:20:38 GMT  
		Size: 22.6 MB (22641030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:275ec7f48c48219a81fc8224dc3fea5445727eb9c749769442940686155c34d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:f4058c67b7489efe0031cbb8086a4f21cbb8ee27bf043cdcd9009a62c840324f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141824194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d20a7abc7499d2145cffd08fccb8263da40b4180e7b811d23faada47f7f2c2ab`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:45:02 GMT
ENV ROS_DISTRO=rolling
# Tue, 25 Oct 2022 07:45:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:45:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:45:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:45:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7767abbf3782738860e3bb5ede4f627dba0211161ae5cfa4a72cf1dd43c58be4`  
		Last Modified: Tue, 25 Oct 2022 08:05:34 GMT  
		Size: 106.4 MB (106391215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8106ab6bf436bb06edcea0071debbc4b31d730b8cc8ca4d7fd6af8bd19ea702a`  
		Last Modified: Tue, 25 Oct 2022 08:05:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:03416f64dcd141aa345f59cfd4dc2d15ac336756d80e80f0077506a039119f9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137261180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ad5a37135505c9a5387b812b23f105dbcd57cb12cf9a764166ed45c8594d86`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:55:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:55:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:55:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:55:18 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 14:00:21 GMT
ENV ROS_DISTRO=rolling
# Wed, 05 Oct 2022 14:01:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:01:08 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 14:01:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 14:01:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a891d50162687d5b4db85383705535653c56066b48e0e3314badd3e76d2f8af`  
		Last Modified: Wed, 05 Oct 2022 14:16:45 GMT  
		Size: 1.2 MB (1178125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3fc4af9e9380eebc7d111e904fb1098bb4102f7271c19ade184c620ba4d5dc`  
		Last Modified: Wed, 05 Oct 2022 14:16:43 GMT  
		Size: 3.6 MB (3594928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc1176274b8951042f2b29277ebbcdc02bf43ea04b1e95a7e7f80c137ddb1d`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca88c2c17aef59df2c29525001e8bb7f45b3b5e37ef793847df2e89374421e`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3834504b668bb13d4fcded46b2444690bed0603eccbb71ffd03d0ab432593c8e`  
		Last Modified: Wed, 05 Oct 2022 14:20:23 GMT  
		Size: 104.1 MB (104103500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ce9b251482e03203dd3f2b75f07f06ff803e68b582e12a53ce6cc1028c9c58`  
		Last Modified: Wed, 05 Oct 2022 14:20:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core-jammy`

```console
$ docker pull ros@sha256:275ec7f48c48219a81fc8224dc3fea5445727eb9c749769442940686155c34d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:f4058c67b7489efe0031cbb8086a4f21cbb8ee27bf043cdcd9009a62c840324f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141824194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d20a7abc7499d2145cffd08fccb8263da40b4180e7b811d23faada47f7f2c2ab`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:41 GMT
ADD file:ba96f963bbfd429a0839c40603fdd7829eaca58f20adfa0d15e6beae8244bc08 in / 
# Tue, 25 Oct 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:32:37 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:54 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:32:55 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 25 Oct 2022 07:32:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 25 Oct 2022 07:32:56 GMT
ENV LANG=C.UTF-8
# Tue, 25 Oct 2022 07:32:57 GMT
ENV LC_ALL=C.UTF-8
# Tue, 25 Oct 2022 07:45:02 GMT
ENV ROS_DISTRO=rolling
# Tue, 25 Oct 2022 07:45:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:45:48 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 25 Oct 2022 07:45:48 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 25 Oct 2022 07:45:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:301a8b74f71f85f3a31e9c7e7fedd5b001ead5bcf895bc2911c1d260e06bd987`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 30.4 MB (30426374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810da1dcda34dec7cc9bdad42bab8c8f38dedc6c6dc7513267571f3afa9ed8e1`  
		Last Modified: Tue, 25 Oct 2022 08:02:05 GMT  
		Size: 1.2 MB (1176179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97e36fbe1f9bef7faceabfeae190ada023e3587a740e9128ee2b6dd56567fb6`  
		Last Modified: Tue, 25 Oct 2022 08:02:03 GMT  
		Size: 3.8 MB (3828005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacbb17bd5fe6cb6960fa5525e41ffc12ed78be2d90a92e1d105cd5565365a1`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb08ac25022cf2256b5755d0425a8a1af2f96b8e0839eb598bf1d9b41b01adf`  
		Last Modified: Tue, 25 Oct 2022 08:02:02 GMT  
		Size: 2.0 KB (1991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7767abbf3782738860e3bb5ede4f627dba0211161ae5cfa4a72cf1dd43c58be4`  
		Last Modified: Tue, 25 Oct 2022 08:05:34 GMT  
		Size: 106.4 MB (106391215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8106ab6bf436bb06edcea0071debbc4b31d730b8cc8ca4d7fd6af8bd19ea702a`  
		Last Modified: Tue, 25 Oct 2022 08:05:17 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:03416f64dcd141aa345f59cfd4dc2d15ac336756d80e80f0077506a039119f9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137261180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ad5a37135505c9a5387b812b23f105dbcd57cb12cf9a764166ed45c8594d86`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:02:19 GMT
ADD file:fd8103ca1472a4f51eeff3e22fbd1dfd61a3d22c34f16a61ef1ba016352e3629 in / 
# Wed, 05 Oct 2022 00:02:20 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 13:55:04 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 13:55:14 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Wed, 05 Oct 2022 13:55:16 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 05 Oct 2022 13:55:17 GMT
ENV LANG=C.UTF-8
# Wed, 05 Oct 2022 13:55:18 GMT
ENV LC_ALL=C.UTF-8
# Wed, 05 Oct 2022 14:00:21 GMT
ENV ROS_DISTRO=rolling
# Wed, 05 Oct 2022 14:01:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:01:08 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Wed, 05 Oct 2022 14:01:09 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 05 Oct 2022 14:01:09 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d6cb415e2683249f7884ee5367306b023c72f907afeca2a30ca19c8de5f4f7d9`  
		Last Modified: Tue, 04 Oct 2022 15:08:22 GMT  
		Size: 28.4 MB (28382255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a891d50162687d5b4db85383705535653c56066b48e0e3314badd3e76d2f8af`  
		Last Modified: Wed, 05 Oct 2022 14:16:45 GMT  
		Size: 1.2 MB (1178125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3fc4af9e9380eebc7d111e904fb1098bb4102f7271c19ade184c620ba4d5dc`  
		Last Modified: Wed, 05 Oct 2022 14:16:43 GMT  
		Size: 3.6 MB (3594928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc1176274b8951042f2b29277ebbcdc02bf43ea04b1e95a7e7f80c137ddb1d`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ca88c2c17aef59df2c29525001e8bb7f45b3b5e37ef793847df2e89374421e`  
		Last Modified: Wed, 05 Oct 2022 14:16:42 GMT  
		Size: 1.9 KB (1947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3834504b668bb13d4fcded46b2444690bed0603eccbb71ffd03d0ab432593c8e`  
		Last Modified: Wed, 05 Oct 2022 14:20:23 GMT  
		Size: 104.1 MB (104103500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ce9b251482e03203dd3f2b75f07f06ff803e68b582e12a53ce6cc1028c9c58`  
		Last Modified: Wed, 05 Oct 2022 14:20:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

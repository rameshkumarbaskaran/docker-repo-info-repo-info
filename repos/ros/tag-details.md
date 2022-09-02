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
$ docker pull ros@sha256:60bcfcb8b92b1524ce1484c9969ff35efeb30fab6380ef3f8928b5420fedebd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy` - linux; amd64

```console
$ docker pull ros@sha256:add9970136f8920882152f611577326f7e23b0ef9a7069b8152de089ee9ac730
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250620496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2208eebb028dc4838ab0afc9b35e3de393855272172cdf1748b12e3c6704fe16`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:03:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:42:17 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:42:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:42:19 GMT
ENV ROS_DISTRO=foxy
# Fri, 02 Sep 2022 04:43:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:43:16 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 04:43:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:43:16 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:43:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:43:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:43:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 02 Sep 2022 04:44:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf19bc0e0d1d8bf1ec9b593eb3ddedecefdf4aff5f519ad585667a258956af1`  
		Last Modified: Fri, 02 Sep 2022 03:15:37 GMT  
		Size: 1.2 MB (1163757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff483ca449e233e69f18eb71e430f67ec1b4c8f5a965b4d7efc759a0ba2f18c4`  
		Last Modified: Fri, 02 Sep 2022 05:06:36 GMT  
		Size: 5.5 MB (5546993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077f60b8d79e0ce080c903c48fa8296ecb53f67cdcf73d748ec8b454d8d7ec96`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c152c32a5dfa1d8b81650a889c55e593122edd4a1b49983a5aae714fb567194c`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e812731a44ee6ed8eb6f479ee177db4e6f5dc9b8f586e3bec76b68bd87b057`  
		Last Modified: Fri, 02 Sep 2022 05:09:37 GMT  
		Size: 120.1 MB (120084257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430ce07703bc6ca66551202ce709d2db142f2284d1758e1ae63b0089816db684`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1890f880d76adc2a15589d899c1971bfe3b8c53a24b095b14ff503208a19d2fc`  
		Last Modified: Fri, 02 Sep 2022 05:09:58 GMT  
		Size: 73.3 MB (73321532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1250a9090832c70a8cbb5b16a1c4fb04bd15cb731dc383b88e5e8920a07637`  
		Last Modified: Fri, 02 Sep 2022 05:09:48 GMT  
		Size: 262.8 KB (262804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e10b955d6703772baf23131f34012e192b6651bae2f45d5ec1de94db2d65c9`  
		Last Modified: Fri, 02 Sep 2022 05:09:48 GMT  
		Size: 2.4 KB (2425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7586ba8a53515e3a1b9937feaad2e7fede1adbc084ac2d100da1e4a7babb88cf`  
		Last Modified: Fri, 02 Sep 2022 05:09:51 GMT  
		Size: 21.7 MB (21663632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:21ac406bc29b75b76613bfbeeaaf50ea812ecb0ae0747b0a4c017ae8b7d24594
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.0 MB (226048428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7c48b9d562076023020e2d5b4618b7394b41d20d86b7639ae4f5136c37e665`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:21:03 GMT
ENV ROS_DISTRO=foxy
# Tue, 02 Aug 2022 15:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:21:56 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:21:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:21:58 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:22:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:22:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:22:43 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:23:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c95a64572463fdd2d4da0ee7a97ef6c2697332b4ec60bd367e4cd19991e0e30`  
		Last Modified: Tue, 02 Aug 2022 15:46:46 GMT  
		Size: 104.3 MB (104269304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6081d9d7b2a4859859c99dbf1aad54f3b6ff971aab468768c5a4b82b1f9eb5f`  
		Last Modified: Tue, 02 Aug 2022 15:46:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384f02761631a00491d018951bf10473535158ed993973ee5a21534c0413691e`  
		Last Modified: Tue, 02 Aug 2022 15:47:08 GMT  
		Size: 67.4 MB (67448558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668918483f09cef23a428dc6fe3a5cbf56a08974b0c370421c3aaf02fbfdf045`  
		Last Modified: Tue, 02 Aug 2022 15:46:58 GMT  
		Size: 260.9 KB (260876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5bf6d2a082a0478f917366d67636027a403007d46b96d7f06a6b76eb4da6358`  
		Last Modified: Tue, 02 Aug 2022 15:46:58 GMT  
		Size: 2.2 KB (2248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b2892bdcdd7472d84ac2f6e5bdca785fda5551b8f2f9acb56309c2294fecef`  
		Last Modified: Tue, 02 Aug 2022 15:47:01 GMT  
		Size: 20.4 MB (20366890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-base`

```console
$ docker pull ros@sha256:60bcfcb8b92b1524ce1484c9969ff35efeb30fab6380ef3f8928b5420fedebd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:add9970136f8920882152f611577326f7e23b0ef9a7069b8152de089ee9ac730
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250620496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2208eebb028dc4838ab0afc9b35e3de393855272172cdf1748b12e3c6704fe16`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:03:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:42:17 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:42:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:42:19 GMT
ENV ROS_DISTRO=foxy
# Fri, 02 Sep 2022 04:43:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:43:16 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 04:43:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:43:16 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:43:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:43:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:43:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 02 Sep 2022 04:44:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf19bc0e0d1d8bf1ec9b593eb3ddedecefdf4aff5f519ad585667a258956af1`  
		Last Modified: Fri, 02 Sep 2022 03:15:37 GMT  
		Size: 1.2 MB (1163757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff483ca449e233e69f18eb71e430f67ec1b4c8f5a965b4d7efc759a0ba2f18c4`  
		Last Modified: Fri, 02 Sep 2022 05:06:36 GMT  
		Size: 5.5 MB (5546993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077f60b8d79e0ce080c903c48fa8296ecb53f67cdcf73d748ec8b454d8d7ec96`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c152c32a5dfa1d8b81650a889c55e593122edd4a1b49983a5aae714fb567194c`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e812731a44ee6ed8eb6f479ee177db4e6f5dc9b8f586e3bec76b68bd87b057`  
		Last Modified: Fri, 02 Sep 2022 05:09:37 GMT  
		Size: 120.1 MB (120084257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430ce07703bc6ca66551202ce709d2db142f2284d1758e1ae63b0089816db684`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1890f880d76adc2a15589d899c1971bfe3b8c53a24b095b14ff503208a19d2fc`  
		Last Modified: Fri, 02 Sep 2022 05:09:58 GMT  
		Size: 73.3 MB (73321532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1250a9090832c70a8cbb5b16a1c4fb04bd15cb731dc383b88e5e8920a07637`  
		Last Modified: Fri, 02 Sep 2022 05:09:48 GMT  
		Size: 262.8 KB (262804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e10b955d6703772baf23131f34012e192b6651bae2f45d5ec1de94db2d65c9`  
		Last Modified: Fri, 02 Sep 2022 05:09:48 GMT  
		Size: 2.4 KB (2425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7586ba8a53515e3a1b9937feaad2e7fede1adbc084ac2d100da1e4a7babb88cf`  
		Last Modified: Fri, 02 Sep 2022 05:09:51 GMT  
		Size: 21.7 MB (21663632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:21ac406bc29b75b76613bfbeeaaf50ea812ecb0ae0747b0a4c017ae8b7d24594
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.0 MB (226048428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7c48b9d562076023020e2d5b4618b7394b41d20d86b7639ae4f5136c37e665`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:21:03 GMT
ENV ROS_DISTRO=foxy
# Tue, 02 Aug 2022 15:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:21:56 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:21:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:21:58 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:22:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:22:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:22:43 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:23:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c95a64572463fdd2d4da0ee7a97ef6c2697332b4ec60bd367e4cd19991e0e30`  
		Last Modified: Tue, 02 Aug 2022 15:46:46 GMT  
		Size: 104.3 MB (104269304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6081d9d7b2a4859859c99dbf1aad54f3b6ff971aab468768c5a4b82b1f9eb5f`  
		Last Modified: Tue, 02 Aug 2022 15:46:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384f02761631a00491d018951bf10473535158ed993973ee5a21534c0413691e`  
		Last Modified: Tue, 02 Aug 2022 15:47:08 GMT  
		Size: 67.4 MB (67448558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668918483f09cef23a428dc6fe3a5cbf56a08974b0c370421c3aaf02fbfdf045`  
		Last Modified: Tue, 02 Aug 2022 15:46:58 GMT  
		Size: 260.9 KB (260876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5bf6d2a082a0478f917366d67636027a403007d46b96d7f06a6b76eb4da6358`  
		Last Modified: Tue, 02 Aug 2022 15:46:58 GMT  
		Size: 2.2 KB (2248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b2892bdcdd7472d84ac2f6e5bdca785fda5551b8f2f9acb56309c2294fecef`  
		Last Modified: Tue, 02 Aug 2022 15:47:01 GMT  
		Size: 20.4 MB (20366890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-base-focal`

```console
$ docker pull ros@sha256:60bcfcb8b92b1524ce1484c9969ff35efeb30fab6380ef3f8928b5420fedebd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:add9970136f8920882152f611577326f7e23b0ef9a7069b8152de089ee9ac730
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250620496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2208eebb028dc4838ab0afc9b35e3de393855272172cdf1748b12e3c6704fe16`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:03:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:42:17 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:42:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:42:19 GMT
ENV ROS_DISTRO=foxy
# Fri, 02 Sep 2022 04:43:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:43:16 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 04:43:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:43:16 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:43:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:43:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:43:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 02 Sep 2022 04:44:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf19bc0e0d1d8bf1ec9b593eb3ddedecefdf4aff5f519ad585667a258956af1`  
		Last Modified: Fri, 02 Sep 2022 03:15:37 GMT  
		Size: 1.2 MB (1163757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff483ca449e233e69f18eb71e430f67ec1b4c8f5a965b4d7efc759a0ba2f18c4`  
		Last Modified: Fri, 02 Sep 2022 05:06:36 GMT  
		Size: 5.5 MB (5546993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077f60b8d79e0ce080c903c48fa8296ecb53f67cdcf73d748ec8b454d8d7ec96`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c152c32a5dfa1d8b81650a889c55e593122edd4a1b49983a5aae714fb567194c`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e812731a44ee6ed8eb6f479ee177db4e6f5dc9b8f586e3bec76b68bd87b057`  
		Last Modified: Fri, 02 Sep 2022 05:09:37 GMT  
		Size: 120.1 MB (120084257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430ce07703bc6ca66551202ce709d2db142f2284d1758e1ae63b0089816db684`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1890f880d76adc2a15589d899c1971bfe3b8c53a24b095b14ff503208a19d2fc`  
		Last Modified: Fri, 02 Sep 2022 05:09:58 GMT  
		Size: 73.3 MB (73321532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1250a9090832c70a8cbb5b16a1c4fb04bd15cb731dc383b88e5e8920a07637`  
		Last Modified: Fri, 02 Sep 2022 05:09:48 GMT  
		Size: 262.8 KB (262804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e10b955d6703772baf23131f34012e192b6651bae2f45d5ec1de94db2d65c9`  
		Last Modified: Fri, 02 Sep 2022 05:09:48 GMT  
		Size: 2.4 KB (2425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7586ba8a53515e3a1b9937feaad2e7fede1adbc084ac2d100da1e4a7babb88cf`  
		Last Modified: Fri, 02 Sep 2022 05:09:51 GMT  
		Size: 21.7 MB (21663632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:21ac406bc29b75b76613bfbeeaaf50ea812ecb0ae0747b0a4c017ae8b7d24594
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.0 MB (226048428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7c48b9d562076023020e2d5b4618b7394b41d20d86b7639ae4f5136c37e665`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:21:03 GMT
ENV ROS_DISTRO=foxy
# Tue, 02 Aug 2022 15:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:21:56 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:21:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:21:58 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:22:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:22:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:22:43 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:23:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c95a64572463fdd2d4da0ee7a97ef6c2697332b4ec60bd367e4cd19991e0e30`  
		Last Modified: Tue, 02 Aug 2022 15:46:46 GMT  
		Size: 104.3 MB (104269304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6081d9d7b2a4859859c99dbf1aad54f3b6ff971aab468768c5a4b82b1f9eb5f`  
		Last Modified: Tue, 02 Aug 2022 15:46:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384f02761631a00491d018951bf10473535158ed993973ee5a21534c0413691e`  
		Last Modified: Tue, 02 Aug 2022 15:47:08 GMT  
		Size: 67.4 MB (67448558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668918483f09cef23a428dc6fe3a5cbf56a08974b0c370421c3aaf02fbfdf045`  
		Last Modified: Tue, 02 Aug 2022 15:46:58 GMT  
		Size: 260.9 KB (260876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5bf6d2a082a0478f917366d67636027a403007d46b96d7f06a6b76eb4da6358`  
		Last Modified: Tue, 02 Aug 2022 15:46:58 GMT  
		Size: 2.2 KB (2248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b2892bdcdd7472d84ac2f6e5bdca785fda5551b8f2f9acb56309c2294fecef`  
		Last Modified: Tue, 02 Aug 2022 15:47:01 GMT  
		Size: 20.4 MB (20366890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-core`

```console
$ docker pull ros@sha256:670c8fafdc70cfffbbaef29a9161ee9889b2d33fe42eba65cc2a7d264f6e590a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:68cb31a4783276ba8e372670025bc0bff8ef25aa6d267fd3f42f951bbb884a2d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155370103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986192fb90672dc6f66fd52c763b34d9a48034d6ba196e6b7405d9b9d693558f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:03:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:42:17 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:42:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:42:19 GMT
ENV ROS_DISTRO=foxy
# Fri, 02 Sep 2022 04:43:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:43:16 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 04:43:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:43:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf19bc0e0d1d8bf1ec9b593eb3ddedecefdf4aff5f519ad585667a258956af1`  
		Last Modified: Fri, 02 Sep 2022 03:15:37 GMT  
		Size: 1.2 MB (1163757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff483ca449e233e69f18eb71e430f67ec1b4c8f5a965b4d7efc759a0ba2f18c4`  
		Last Modified: Fri, 02 Sep 2022 05:06:36 GMT  
		Size: 5.5 MB (5546993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077f60b8d79e0ce080c903c48fa8296ecb53f67cdcf73d748ec8b454d8d7ec96`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c152c32a5dfa1d8b81650a889c55e593122edd4a1b49983a5aae714fb567194c`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e812731a44ee6ed8eb6f479ee177db4e6f5dc9b8f586e3bec76b68bd87b057`  
		Last Modified: Fri, 02 Sep 2022 05:09:37 GMT  
		Size: 120.1 MB (120084257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430ce07703bc6ca66551202ce709d2db142f2284d1758e1ae63b0089816db684`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4e3e2b4942f4ff2424e12fad581e08a73f65fd63a43ae6b30a25c31a1e57632a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (137969856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37682e32a97b7ad60c3f515317757740553ccb72e600e5e2b2e5e9a1316276a4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:21:03 GMT
ENV ROS_DISTRO=foxy
# Tue, 02 Aug 2022 15:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:21:56 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:21:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:21:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c95a64572463fdd2d4da0ee7a97ef6c2697332b4ec60bd367e4cd19991e0e30`  
		Last Modified: Tue, 02 Aug 2022 15:46:46 GMT  
		Size: 104.3 MB (104269304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6081d9d7b2a4859859c99dbf1aad54f3b6ff971aab468768c5a4b82b1f9eb5f`  
		Last Modified: Tue, 02 Aug 2022 15:46:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros-core-focal`

```console
$ docker pull ros@sha256:670c8fafdc70cfffbbaef29a9161ee9889b2d33fe42eba65cc2a7d264f6e590a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:68cb31a4783276ba8e372670025bc0bff8ef25aa6d267fd3f42f951bbb884a2d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155370103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986192fb90672dc6f66fd52c763b34d9a48034d6ba196e6b7405d9b9d693558f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:03:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:42:17 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:42:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:42:19 GMT
ENV ROS_DISTRO=foxy
# Fri, 02 Sep 2022 04:43:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:43:16 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 04:43:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:43:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf19bc0e0d1d8bf1ec9b593eb3ddedecefdf4aff5f519ad585667a258956af1`  
		Last Modified: Fri, 02 Sep 2022 03:15:37 GMT  
		Size: 1.2 MB (1163757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff483ca449e233e69f18eb71e430f67ec1b4c8f5a965b4d7efc759a0ba2f18c4`  
		Last Modified: Fri, 02 Sep 2022 05:06:36 GMT  
		Size: 5.5 MB (5546993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077f60b8d79e0ce080c903c48fa8296ecb53f67cdcf73d748ec8b454d8d7ec96`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c152c32a5dfa1d8b81650a889c55e593122edd4a1b49983a5aae714fb567194c`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e812731a44ee6ed8eb6f479ee177db4e6f5dc9b8f586e3bec76b68bd87b057`  
		Last Modified: Fri, 02 Sep 2022 05:09:37 GMT  
		Size: 120.1 MB (120084257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430ce07703bc6ca66551202ce709d2db142f2284d1758e1ae63b0089816db684`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:4e3e2b4942f4ff2424e12fad581e08a73f65fd63a43ae6b30a25c31a1e57632a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.0 MB (137969856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37682e32a97b7ad60c3f515317757740553ccb72e600e5e2b2e5e9a1316276a4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:21:03 GMT
ENV ROS_DISTRO=foxy
# Tue, 02 Aug 2022 15:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:21:56 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:21:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:21:58 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c95a64572463fdd2d4da0ee7a97ef6c2697332b4ec60bd367e4cd19991e0e30`  
		Last Modified: Tue, 02 Aug 2022 15:46:46 GMT  
		Size: 104.3 MB (104269304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6081d9d7b2a4859859c99dbf1aad54f3b6ff971aab468768c5a4b82b1f9eb5f`  
		Last Modified: Tue, 02 Aug 2022 15:46:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros1-bridge`

```console
$ docker pull ros@sha256:800edfa6a9eacce28718a0257eeff5f7caee53a3be443f90c49e031141516280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:3f78e8a90b6e387d4514aaae5162af4052a93d94d9c4239f3e53d3954232b05a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.6 MB (348586994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2511058a237dd47bcb3f87129403b6fda84704691af09610879963ae37bfb1de`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:03:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:42:17 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:42:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:42:19 GMT
ENV ROS_DISTRO=foxy
# Fri, 02 Sep 2022 04:43:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:43:16 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 04:43:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:43:16 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:43:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:43:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:43:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 02 Sep 2022 04:44:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:44:16 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Sep 2022 04:44:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:44:17 GMT
ENV ROS1_DISTRO=noetic
# Fri, 02 Sep 2022 04:44:17 GMT
ENV ROS2_DISTRO=foxy
# Fri, 02 Sep 2022 04:44:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:44:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:44:53 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf19bc0e0d1d8bf1ec9b593eb3ddedecefdf4aff5f519ad585667a258956af1`  
		Last Modified: Fri, 02 Sep 2022 03:15:37 GMT  
		Size: 1.2 MB (1163757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff483ca449e233e69f18eb71e430f67ec1b4c8f5a965b4d7efc759a0ba2f18c4`  
		Last Modified: Fri, 02 Sep 2022 05:06:36 GMT  
		Size: 5.5 MB (5546993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077f60b8d79e0ce080c903c48fa8296ecb53f67cdcf73d748ec8b454d8d7ec96`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c152c32a5dfa1d8b81650a889c55e593122edd4a1b49983a5aae714fb567194c`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e812731a44ee6ed8eb6f479ee177db4e6f5dc9b8f586e3bec76b68bd87b057`  
		Last Modified: Fri, 02 Sep 2022 05:09:37 GMT  
		Size: 120.1 MB (120084257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430ce07703bc6ca66551202ce709d2db142f2284d1758e1ae63b0089816db684`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1890f880d76adc2a15589d899c1971bfe3b8c53a24b095b14ff503208a19d2fc`  
		Last Modified: Fri, 02 Sep 2022 05:09:58 GMT  
		Size: 73.3 MB (73321532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1250a9090832c70a8cbb5b16a1c4fb04bd15cb731dc383b88e5e8920a07637`  
		Last Modified: Fri, 02 Sep 2022 05:09:48 GMT  
		Size: 262.8 KB (262804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e10b955d6703772baf23131f34012e192b6651bae2f45d5ec1de94db2d65c9`  
		Last Modified: Fri, 02 Sep 2022 05:09:48 GMT  
		Size: 2.4 KB (2425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7586ba8a53515e3a1b9937feaad2e7fede1adbc084ac2d100da1e4a7babb88cf`  
		Last Modified: Fri, 02 Sep 2022 05:09:51 GMT  
		Size: 21.7 MB (21663632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edcbcf9416ff36cdf21ebba78c090a721c2336ca975593da6eb8673fc001580`  
		Last Modified: Fri, 02 Sep 2022 05:10:15 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99f71dd80fe6b49b3017302c5cccc836ffd1c6cc3eb356f93e988cc3f179b42`  
		Last Modified: Fri, 02 Sep 2022 05:10:15 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6134584ea0d3a53090e953339399b9b3c8e07b079e17de3d728a076949e813`  
		Last Modified: Fri, 02 Sep 2022 05:10:29 GMT  
		Size: 76.4 MB (76429691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a059b78d35d8a1d65a5ccf510075adf5ea99daa2406f4d49535cefc53a951c2f`  
		Last Modified: Fri, 02 Sep 2022 05:10:19 GMT  
		Size: 21.5 MB (21536176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8666bcd29d3c8ee38ee47d39511a6abd61f7528a39d1298f59510fa77ece2ec6`  
		Last Modified: Fri, 02 Sep 2022 05:10:15 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e908c2d0016f5d0b80de3417ac4423550a10f52342b98bb9573ce1755a66d93e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.3 MB (316275648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07eb9def03493c71fa102c9e773ce7c768b6ce2584769d25759492121f77825e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:21:03 GMT
ENV ROS_DISTRO=foxy
# Tue, 02 Aug 2022 15:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:21:56 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:21:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:21:58 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:22:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:22:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:22:43 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:23:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:23:13 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:23:15 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:23:17 GMT
ENV ROS1_DISTRO=noetic
# Tue, 02 Aug 2022 15:23:18 GMT
ENV ROS2_DISTRO=foxy
# Tue, 02 Aug 2022 15:23:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:24:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:24:06 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c95a64572463fdd2d4da0ee7a97ef6c2697332b4ec60bd367e4cd19991e0e30`  
		Last Modified: Tue, 02 Aug 2022 15:46:46 GMT  
		Size: 104.3 MB (104269304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6081d9d7b2a4859859c99dbf1aad54f3b6ff971aab468768c5a4b82b1f9eb5f`  
		Last Modified: Tue, 02 Aug 2022 15:46:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384f02761631a00491d018951bf10473535158ed993973ee5a21534c0413691e`  
		Last Modified: Tue, 02 Aug 2022 15:47:08 GMT  
		Size: 67.4 MB (67448558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668918483f09cef23a428dc6fe3a5cbf56a08974b0c370421c3aaf02fbfdf045`  
		Last Modified: Tue, 02 Aug 2022 15:46:58 GMT  
		Size: 260.9 KB (260876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5bf6d2a082a0478f917366d67636027a403007d46b96d7f06a6b76eb4da6358`  
		Last Modified: Tue, 02 Aug 2022 15:46:58 GMT  
		Size: 2.2 KB (2248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b2892bdcdd7472d84ac2f6e5bdca785fda5551b8f2f9acb56309c2294fecef`  
		Last Modified: Tue, 02 Aug 2022 15:47:01 GMT  
		Size: 20.4 MB (20366890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbde1dfcc79d4a7217b8a62168774cb73c2d182e5e154b8bf035c2212d263fc`  
		Last Modified: Tue, 02 Aug 2022 15:47:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e84b0413c2629b20c17fe09106bfb54cbd61d076c1bfd09aba3cb192db7f7b6`  
		Last Modified: Tue, 02 Aug 2022 15:47:39 GMT  
		Size: 76.3 MB (76269498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e39c8f9bee1fefc9e6920baef31896530bf3cf37e7d7f1d16af3ace537f8a35`  
		Last Modified: Tue, 02 Aug 2022 15:47:27 GMT  
		Size: 14.0 MB (13957252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa581353eb222963439f599d8089571c19a9b3791d685d31ca76bababdbf27f`  
		Last Modified: Tue, 02 Aug 2022 15:47:25 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:foxy-ros1-bridge-focal`

```console
$ docker pull ros@sha256:800edfa6a9eacce28718a0257eeff5f7caee53a3be443f90c49e031141516280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:foxy-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:3f78e8a90b6e387d4514aaae5162af4052a93d94d9c4239f3e53d3954232b05a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.6 MB (348586994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2511058a237dd47bcb3f87129403b6fda84704691af09610879963ae37bfb1de`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:03:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:42:17 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:42:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:42:19 GMT
ENV ROS_DISTRO=foxy
# Fri, 02 Sep 2022 04:43:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:43:16 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 04:43:16 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:43:16 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:43:47 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:43:52 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:43:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 02 Sep 2022 04:44:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:44:16 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Sep 2022 04:44:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:44:17 GMT
ENV ROS1_DISTRO=noetic
# Fri, 02 Sep 2022 04:44:17 GMT
ENV ROS2_DISTRO=foxy
# Fri, 02 Sep 2022 04:44:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:44:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:44:53 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf19bc0e0d1d8bf1ec9b593eb3ddedecefdf4aff5f519ad585667a258956af1`  
		Last Modified: Fri, 02 Sep 2022 03:15:37 GMT  
		Size: 1.2 MB (1163757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff483ca449e233e69f18eb71e430f67ec1b4c8f5a965b4d7efc759a0ba2f18c4`  
		Last Modified: Fri, 02 Sep 2022 05:06:36 GMT  
		Size: 5.5 MB (5546993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077f60b8d79e0ce080c903c48fa8296ecb53f67cdcf73d748ec8b454d8d7ec96`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c152c32a5dfa1d8b81650a889c55e593122edd4a1b49983a5aae714fb567194c`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e812731a44ee6ed8eb6f479ee177db4e6f5dc9b8f586e3bec76b68bd87b057`  
		Last Modified: Fri, 02 Sep 2022 05:09:37 GMT  
		Size: 120.1 MB (120084257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430ce07703bc6ca66551202ce709d2db142f2284d1758e1ae63b0089816db684`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1890f880d76adc2a15589d899c1971bfe3b8c53a24b095b14ff503208a19d2fc`  
		Last Modified: Fri, 02 Sep 2022 05:09:58 GMT  
		Size: 73.3 MB (73321532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1250a9090832c70a8cbb5b16a1c4fb04bd15cb731dc383b88e5e8920a07637`  
		Last Modified: Fri, 02 Sep 2022 05:09:48 GMT  
		Size: 262.8 KB (262804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e10b955d6703772baf23131f34012e192b6651bae2f45d5ec1de94db2d65c9`  
		Last Modified: Fri, 02 Sep 2022 05:09:48 GMT  
		Size: 2.4 KB (2425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7586ba8a53515e3a1b9937feaad2e7fede1adbc084ac2d100da1e4a7babb88cf`  
		Last Modified: Fri, 02 Sep 2022 05:09:51 GMT  
		Size: 21.7 MB (21663632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edcbcf9416ff36cdf21ebba78c090a721c2336ca975593da6eb8673fc001580`  
		Last Modified: Fri, 02 Sep 2022 05:10:15 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99f71dd80fe6b49b3017302c5cccc836ffd1c6cc3eb356f93e988cc3f179b42`  
		Last Modified: Fri, 02 Sep 2022 05:10:15 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6134584ea0d3a53090e953339399b9b3c8e07b079e17de3d728a076949e813`  
		Last Modified: Fri, 02 Sep 2022 05:10:29 GMT  
		Size: 76.4 MB (76429691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a059b78d35d8a1d65a5ccf510075adf5ea99daa2406f4d49535cefc53a951c2f`  
		Last Modified: Fri, 02 Sep 2022 05:10:19 GMT  
		Size: 21.5 MB (21536176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8666bcd29d3c8ee38ee47d39511a6abd61f7528a39d1298f59510fa77ece2ec6`  
		Last Modified: Fri, 02 Sep 2022 05:10:15 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:foxy-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e908c2d0016f5d0b80de3417ac4423550a10f52342b98bb9573ce1755a66d93e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.3 MB (316275648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07eb9def03493c71fa102c9e773ce7c768b6ce2584769d25759492121f77825e`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:21:03 GMT
ENV ROS_DISTRO=foxy
# Tue, 02 Aug 2022 15:21:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-core=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:21:56 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:21:57 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:21:58 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:22:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:22:38 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:22:43 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:23:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros-base=0.9.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:23:13 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:23:15 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:23:17 GMT
ENV ROS1_DISTRO=noetic
# Tue, 02 Aug 2022 15:23:18 GMT
ENV ROS2_DISTRO=foxy
# Tue, 02 Aug 2022 15:23:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:24:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-foxy-ros1-bridge=0.9.6-1*     ros-foxy-demo-nodes-cpp=0.9.3-1*     ros-foxy-demo-nodes-py=0.9.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:24:06 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c95a64572463fdd2d4da0ee7a97ef6c2697332b4ec60bd367e4cd19991e0e30`  
		Last Modified: Tue, 02 Aug 2022 15:46:46 GMT  
		Size: 104.3 MB (104269304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6081d9d7b2a4859859c99dbf1aad54f3b6ff971aab468768c5a4b82b1f9eb5f`  
		Last Modified: Tue, 02 Aug 2022 15:46:28 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384f02761631a00491d018951bf10473535158ed993973ee5a21534c0413691e`  
		Last Modified: Tue, 02 Aug 2022 15:47:08 GMT  
		Size: 67.4 MB (67448558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668918483f09cef23a428dc6fe3a5cbf56a08974b0c370421c3aaf02fbfdf045`  
		Last Modified: Tue, 02 Aug 2022 15:46:58 GMT  
		Size: 260.9 KB (260876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5bf6d2a082a0478f917366d67636027a403007d46b96d7f06a6b76eb4da6358`  
		Last Modified: Tue, 02 Aug 2022 15:46:58 GMT  
		Size: 2.2 KB (2248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b2892bdcdd7472d84ac2f6e5bdca785fda5551b8f2f9acb56309c2294fecef`  
		Last Modified: Tue, 02 Aug 2022 15:47:01 GMT  
		Size: 20.4 MB (20366890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbde1dfcc79d4a7217b8a62168774cb73c2d182e5e154b8bf035c2212d263fc`  
		Last Modified: Tue, 02 Aug 2022 15:47:25 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e84b0413c2629b20c17fe09106bfb54cbd61d076c1bfd09aba3cb192db7f7b6`  
		Last Modified: Tue, 02 Aug 2022 15:47:39 GMT  
		Size: 76.3 MB (76269498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e39c8f9bee1fefc9e6920baef31896530bf3cf37e7d7f1d16af3ace537f8a35`  
		Last Modified: Tue, 02 Aug 2022 15:47:27 GMT  
		Size: 14.0 MB (13957252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa581353eb222963439f599d8089571c19a9b3791d685d31ca76bababdbf27f`  
		Last Modified: Tue, 02 Aug 2022 15:47:25 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic`

```console
$ docker pull ros@sha256:3d423f1a4b81f72c98a562852da5bdcce1e5f58ce031de0aa32c30d2ff01a2fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic` - linux; amd64

```console
$ docker pull ros@sha256:f672d5cb53360aa4035d84824f862a68a1345e40a5f81682914a6d5165402b30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234856213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2bcc3f4298470b8a7514532c09dddef7e113b1f5007d4031d4fcc9069cd754`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:03:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:42:17 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:42:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:44:56 GMT
ENV ROS_DISTRO=galactic
# Fri, 02 Sep 2022 04:45:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:45:40 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 04:45:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:45:40 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:46:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:46:06 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:46:09 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 02 Sep 2022 04:46:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf19bc0e0d1d8bf1ec9b593eb3ddedecefdf4aff5f519ad585667a258956af1`  
		Last Modified: Fri, 02 Sep 2022 03:15:37 GMT  
		Size: 1.2 MB (1163757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff483ca449e233e69f18eb71e430f67ec1b4c8f5a965b4d7efc759a0ba2f18c4`  
		Last Modified: Fri, 02 Sep 2022 05:06:36 GMT  
		Size: 5.5 MB (5546993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077f60b8d79e0ce080c903c48fa8296ecb53f67cdcf73d748ec8b454d8d7ec96`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c152c32a5dfa1d8b81650a889c55e593122edd4a1b49983a5aae714fb567194c`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4606a5228ccb52337657838c69716d528a1cd36a6adb320134ad9f72dac1b0`  
		Last Modified: Fri, 02 Sep 2022 05:10:57 GMT  
		Size: 103.9 MB (103882165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1077970b7ff447bda164171d709fbff427233431a1b4e67f2c042babb86581d`  
		Last Modified: Fri, 02 Sep 2022 05:10:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1623dc240f1486b24057900a44b1773cb529bb6eb79de2586e3d68e4612aca5d`  
		Last Modified: Fri, 02 Sep 2022 05:11:17 GMT  
		Size: 73.3 MB (73278501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c19349a79634056717413469829a12bf9869bc820130019d21c041134468f6a`  
		Last Modified: Fri, 02 Sep 2022 05:11:07 GMT  
		Size: 273.4 KB (273436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d38666d25b1c976245f649412489ae8d72bdaf049159320f9d06e29d9c12ab`  
		Last Modified: Fri, 02 Sep 2022 05:11:07 GMT  
		Size: 2.4 KB (2420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b5b062abae098c506dc5944c0c2dd15738658bdca2359cff971286f3a21ac3`  
		Last Modified: Fri, 02 Sep 2022 05:11:10 GMT  
		Size: 22.1 MB (22133844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d75f46e141a80f9b7cff2cf238925c2af89d02ac8adef6b989645cc01ce2eef2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.1 MB (223132370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ac4a489929fe9fffc868878c7d4ec54fa785d4d765c1994394c108c9ab7395`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:24:13 GMT
ENV ROS_DISTRO=galactic
# Tue, 02 Aug 2022 15:25:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:25:05 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:25:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:25:07 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:25:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:25:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:25:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:26:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec24629b846176e31ddaaf8b24b1ddfa5c013c36a5adc644cc1ea9cbfaf1f0d`  
		Last Modified: Tue, 02 Aug 2022 15:48:08 GMT  
		Size: 100.3 MB (100301595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb6c32d186e05482bc0d52ca6d3348f8f2135fe0ce5cb80694cbf0c402904ab`  
		Last Modified: Tue, 02 Aug 2022 15:47:51 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f1bc7aab31ae221d1d0a204692f57529cc52be37d783e9408e6091c9140e30`  
		Last Modified: Tue, 02 Aug 2022 15:48:30 GMT  
		Size: 67.4 MB (67403003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8728db5450b6ae980d219774ae0acd473093c7203a814add3754b37fa58d2f16`  
		Last Modified: Tue, 02 Aug 2022 15:48:20 GMT  
		Size: 271.8 KB (271758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b3c45ed46817bdd81a5f97bc0ac2f937e60aba727035f3fda0c52b1e8d3766`  
		Last Modified: Tue, 02 Aug 2022 15:48:20 GMT  
		Size: 2.2 KB (2208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb12350bd7ee355d38d341f83cd1fc612133c69ea151b66e1784eeb2e27e4a4`  
		Last Modified: Tue, 02 Aug 2022 15:48:23 GMT  
		Size: 21.5 MB (21453253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-base`

```console
$ docker pull ros@sha256:3d423f1a4b81f72c98a562852da5bdcce1e5f58ce031de0aa32c30d2ff01a2fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:f672d5cb53360aa4035d84824f862a68a1345e40a5f81682914a6d5165402b30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234856213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2bcc3f4298470b8a7514532c09dddef7e113b1f5007d4031d4fcc9069cd754`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:03:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:42:17 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:42:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:44:56 GMT
ENV ROS_DISTRO=galactic
# Fri, 02 Sep 2022 04:45:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:45:40 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 04:45:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:45:40 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:46:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:46:06 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:46:09 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 02 Sep 2022 04:46:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf19bc0e0d1d8bf1ec9b593eb3ddedecefdf4aff5f519ad585667a258956af1`  
		Last Modified: Fri, 02 Sep 2022 03:15:37 GMT  
		Size: 1.2 MB (1163757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff483ca449e233e69f18eb71e430f67ec1b4c8f5a965b4d7efc759a0ba2f18c4`  
		Last Modified: Fri, 02 Sep 2022 05:06:36 GMT  
		Size: 5.5 MB (5546993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077f60b8d79e0ce080c903c48fa8296ecb53f67cdcf73d748ec8b454d8d7ec96`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c152c32a5dfa1d8b81650a889c55e593122edd4a1b49983a5aae714fb567194c`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4606a5228ccb52337657838c69716d528a1cd36a6adb320134ad9f72dac1b0`  
		Last Modified: Fri, 02 Sep 2022 05:10:57 GMT  
		Size: 103.9 MB (103882165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1077970b7ff447bda164171d709fbff427233431a1b4e67f2c042babb86581d`  
		Last Modified: Fri, 02 Sep 2022 05:10:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1623dc240f1486b24057900a44b1773cb529bb6eb79de2586e3d68e4612aca5d`  
		Last Modified: Fri, 02 Sep 2022 05:11:17 GMT  
		Size: 73.3 MB (73278501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c19349a79634056717413469829a12bf9869bc820130019d21c041134468f6a`  
		Last Modified: Fri, 02 Sep 2022 05:11:07 GMT  
		Size: 273.4 KB (273436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d38666d25b1c976245f649412489ae8d72bdaf049159320f9d06e29d9c12ab`  
		Last Modified: Fri, 02 Sep 2022 05:11:07 GMT  
		Size: 2.4 KB (2420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b5b062abae098c506dc5944c0c2dd15738658bdca2359cff971286f3a21ac3`  
		Last Modified: Fri, 02 Sep 2022 05:11:10 GMT  
		Size: 22.1 MB (22133844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d75f46e141a80f9b7cff2cf238925c2af89d02ac8adef6b989645cc01ce2eef2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.1 MB (223132370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ac4a489929fe9fffc868878c7d4ec54fa785d4d765c1994394c108c9ab7395`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:24:13 GMT
ENV ROS_DISTRO=galactic
# Tue, 02 Aug 2022 15:25:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:25:05 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:25:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:25:07 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:25:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:25:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:25:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:26:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec24629b846176e31ddaaf8b24b1ddfa5c013c36a5adc644cc1ea9cbfaf1f0d`  
		Last Modified: Tue, 02 Aug 2022 15:48:08 GMT  
		Size: 100.3 MB (100301595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb6c32d186e05482bc0d52ca6d3348f8f2135fe0ce5cb80694cbf0c402904ab`  
		Last Modified: Tue, 02 Aug 2022 15:47:51 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f1bc7aab31ae221d1d0a204692f57529cc52be37d783e9408e6091c9140e30`  
		Last Modified: Tue, 02 Aug 2022 15:48:30 GMT  
		Size: 67.4 MB (67403003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8728db5450b6ae980d219774ae0acd473093c7203a814add3754b37fa58d2f16`  
		Last Modified: Tue, 02 Aug 2022 15:48:20 GMT  
		Size: 271.8 KB (271758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b3c45ed46817bdd81a5f97bc0ac2f937e60aba727035f3fda0c52b1e8d3766`  
		Last Modified: Tue, 02 Aug 2022 15:48:20 GMT  
		Size: 2.2 KB (2208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb12350bd7ee355d38d341f83cd1fc612133c69ea151b66e1784eeb2e27e4a4`  
		Last Modified: Tue, 02 Aug 2022 15:48:23 GMT  
		Size: 21.5 MB (21453253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-base-focal`

```console
$ docker pull ros@sha256:3d423f1a4b81f72c98a562852da5bdcce1e5f58ce031de0aa32c30d2ff01a2fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:f672d5cb53360aa4035d84824f862a68a1345e40a5f81682914a6d5165402b30
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234856213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2bcc3f4298470b8a7514532c09dddef7e113b1f5007d4031d4fcc9069cd754`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:03:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:42:17 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:42:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:44:56 GMT
ENV ROS_DISTRO=galactic
# Fri, 02 Sep 2022 04:45:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:45:40 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 04:45:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:45:40 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:46:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:46:06 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:46:09 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 02 Sep 2022 04:46:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf19bc0e0d1d8bf1ec9b593eb3ddedecefdf4aff5f519ad585667a258956af1`  
		Last Modified: Fri, 02 Sep 2022 03:15:37 GMT  
		Size: 1.2 MB (1163757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff483ca449e233e69f18eb71e430f67ec1b4c8f5a965b4d7efc759a0ba2f18c4`  
		Last Modified: Fri, 02 Sep 2022 05:06:36 GMT  
		Size: 5.5 MB (5546993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077f60b8d79e0ce080c903c48fa8296ecb53f67cdcf73d748ec8b454d8d7ec96`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c152c32a5dfa1d8b81650a889c55e593122edd4a1b49983a5aae714fb567194c`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4606a5228ccb52337657838c69716d528a1cd36a6adb320134ad9f72dac1b0`  
		Last Modified: Fri, 02 Sep 2022 05:10:57 GMT  
		Size: 103.9 MB (103882165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1077970b7ff447bda164171d709fbff427233431a1b4e67f2c042babb86581d`  
		Last Modified: Fri, 02 Sep 2022 05:10:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1623dc240f1486b24057900a44b1773cb529bb6eb79de2586e3d68e4612aca5d`  
		Last Modified: Fri, 02 Sep 2022 05:11:17 GMT  
		Size: 73.3 MB (73278501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c19349a79634056717413469829a12bf9869bc820130019d21c041134468f6a`  
		Last Modified: Fri, 02 Sep 2022 05:11:07 GMT  
		Size: 273.4 KB (273436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d38666d25b1c976245f649412489ae8d72bdaf049159320f9d06e29d9c12ab`  
		Last Modified: Fri, 02 Sep 2022 05:11:07 GMT  
		Size: 2.4 KB (2420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b5b062abae098c506dc5944c0c2dd15738658bdca2359cff971286f3a21ac3`  
		Last Modified: Fri, 02 Sep 2022 05:11:10 GMT  
		Size: 22.1 MB (22133844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d75f46e141a80f9b7cff2cf238925c2af89d02ac8adef6b989645cc01ce2eef2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.1 MB (223132370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ac4a489929fe9fffc868878c7d4ec54fa785d4d765c1994394c108c9ab7395`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:24:13 GMT
ENV ROS_DISTRO=galactic
# Tue, 02 Aug 2022 15:25:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:25:05 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:25:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:25:07 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:25:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:25:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:25:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:26:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec24629b846176e31ddaaf8b24b1ddfa5c013c36a5adc644cc1ea9cbfaf1f0d`  
		Last Modified: Tue, 02 Aug 2022 15:48:08 GMT  
		Size: 100.3 MB (100301595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb6c32d186e05482bc0d52ca6d3348f8f2135fe0ce5cb80694cbf0c402904ab`  
		Last Modified: Tue, 02 Aug 2022 15:47:51 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f1bc7aab31ae221d1d0a204692f57529cc52be37d783e9408e6091c9140e30`  
		Last Modified: Tue, 02 Aug 2022 15:48:30 GMT  
		Size: 67.4 MB (67403003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8728db5450b6ae980d219774ae0acd473093c7203a814add3754b37fa58d2f16`  
		Last Modified: Tue, 02 Aug 2022 15:48:20 GMT  
		Size: 271.8 KB (271758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b3c45ed46817bdd81a5f97bc0ac2f937e60aba727035f3fda0c52b1e8d3766`  
		Last Modified: Tue, 02 Aug 2022 15:48:20 GMT  
		Size: 2.2 KB (2208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb12350bd7ee355d38d341f83cd1fc612133c69ea151b66e1784eeb2e27e4a4`  
		Last Modified: Tue, 02 Aug 2022 15:48:23 GMT  
		Size: 21.5 MB (21453253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-core`

```console
$ docker pull ros@sha256:78e187b7198b30bf74a3763de70a1f6b9060d19129ffcf3dcaed0d85578fbb0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:103d58131043fe218f9fb1aeb8c1110d81005458d71000f117bb7219f62fad6d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.2 MB (139168012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91dbd16d87b5a79f30e898cd6e666e9491ca7ee7a46ac3a074a0f236c4b8c699`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:03:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:42:17 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:42:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:44:56 GMT
ENV ROS_DISTRO=galactic
# Fri, 02 Sep 2022 04:45:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:45:40 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 04:45:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:45:40 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf19bc0e0d1d8bf1ec9b593eb3ddedecefdf4aff5f519ad585667a258956af1`  
		Last Modified: Fri, 02 Sep 2022 03:15:37 GMT  
		Size: 1.2 MB (1163757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff483ca449e233e69f18eb71e430f67ec1b4c8f5a965b4d7efc759a0ba2f18c4`  
		Last Modified: Fri, 02 Sep 2022 05:06:36 GMT  
		Size: 5.5 MB (5546993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077f60b8d79e0ce080c903c48fa8296ecb53f67cdcf73d748ec8b454d8d7ec96`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c152c32a5dfa1d8b81650a889c55e593122edd4a1b49983a5aae714fb567194c`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4606a5228ccb52337657838c69716d528a1cd36a6adb320134ad9f72dac1b0`  
		Last Modified: Fri, 02 Sep 2022 05:10:57 GMT  
		Size: 103.9 MB (103882165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1077970b7ff447bda164171d709fbff427233431a1b4e67f2c042babb86581d`  
		Last Modified: Fri, 02 Sep 2022 05:10:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d188c2c8fa40b0a33ea208fdfa152bc426266ed2bb7206b4a1cdc951f93f4506
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134002148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e49fda94cfbb24093edc051b459c556171662bdd4b4a1a5157bc9ceb1dfba1f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:24:13 GMT
ENV ROS_DISTRO=galactic
# Tue, 02 Aug 2022 15:25:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:25:05 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:25:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:25:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec24629b846176e31ddaaf8b24b1ddfa5c013c36a5adc644cc1ea9cbfaf1f0d`  
		Last Modified: Tue, 02 Aug 2022 15:48:08 GMT  
		Size: 100.3 MB (100301595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb6c32d186e05482bc0d52ca6d3348f8f2135fe0ce5cb80694cbf0c402904ab`  
		Last Modified: Tue, 02 Aug 2022 15:47:51 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros-core-focal`

```console
$ docker pull ros@sha256:78e187b7198b30bf74a3763de70a1f6b9060d19129ffcf3dcaed0d85578fbb0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:103d58131043fe218f9fb1aeb8c1110d81005458d71000f117bb7219f62fad6d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.2 MB (139168012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91dbd16d87b5a79f30e898cd6e666e9491ca7ee7a46ac3a074a0f236c4b8c699`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:03:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:42:17 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:42:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:44:56 GMT
ENV ROS_DISTRO=galactic
# Fri, 02 Sep 2022 04:45:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:45:40 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 04:45:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:45:40 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf19bc0e0d1d8bf1ec9b593eb3ddedecefdf4aff5f519ad585667a258956af1`  
		Last Modified: Fri, 02 Sep 2022 03:15:37 GMT  
		Size: 1.2 MB (1163757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff483ca449e233e69f18eb71e430f67ec1b4c8f5a965b4d7efc759a0ba2f18c4`  
		Last Modified: Fri, 02 Sep 2022 05:06:36 GMT  
		Size: 5.5 MB (5546993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077f60b8d79e0ce080c903c48fa8296ecb53f67cdcf73d748ec8b454d8d7ec96`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c152c32a5dfa1d8b81650a889c55e593122edd4a1b49983a5aae714fb567194c`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4606a5228ccb52337657838c69716d528a1cd36a6adb320134ad9f72dac1b0`  
		Last Modified: Fri, 02 Sep 2022 05:10:57 GMT  
		Size: 103.9 MB (103882165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1077970b7ff447bda164171d709fbff427233431a1b4e67f2c042babb86581d`  
		Last Modified: Fri, 02 Sep 2022 05:10:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:d188c2c8fa40b0a33ea208fdfa152bc426266ed2bb7206b4a1cdc951f93f4506
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134002148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e49fda94cfbb24093edc051b459c556171662bdd4b4a1a5157bc9ceb1dfba1f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:24:13 GMT
ENV ROS_DISTRO=galactic
# Tue, 02 Aug 2022 15:25:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:25:05 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:25:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:25:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec24629b846176e31ddaaf8b24b1ddfa5c013c36a5adc644cc1ea9cbfaf1f0d`  
		Last Modified: Tue, 02 Aug 2022 15:48:08 GMT  
		Size: 100.3 MB (100301595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb6c32d186e05482bc0d52ca6d3348f8f2135fe0ce5cb80694cbf0c402904ab`  
		Last Modified: Tue, 02 Aug 2022 15:47:51 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros1-bridge`

```console
$ docker pull ros@sha256:f942c77db8321f0dcb471a6a2c39d0a091a63a3b8aa292a85aa961686b5603dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros1-bridge` - linux; amd64

```console
$ docker pull ros@sha256:6f868677049d21360ab3c77c7117cf3432bb0a45d625645fbbd4bad00010ddd9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.0 MB (330025494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a9b3283ccd5b50b76c43a25043d7b2fe3b0b97cad79b7e7a209c764f66f454`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:03:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:42:17 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:42:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:44:56 GMT
ENV ROS_DISTRO=galactic
# Fri, 02 Sep 2022 04:45:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:45:40 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 04:45:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:45:40 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:46:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:46:06 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:46:09 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 02 Sep 2022 04:46:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:46:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Sep 2022 04:46:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:46:34 GMT
ENV ROS1_DISTRO=noetic
# Fri, 02 Sep 2022 04:46:35 GMT
ENV ROS2_DISTRO=galactic
# Fri, 02 Sep 2022 04:47:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:11 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf19bc0e0d1d8bf1ec9b593eb3ddedecefdf4aff5f519ad585667a258956af1`  
		Last Modified: Fri, 02 Sep 2022 03:15:37 GMT  
		Size: 1.2 MB (1163757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff483ca449e233e69f18eb71e430f67ec1b4c8f5a965b4d7efc759a0ba2f18c4`  
		Last Modified: Fri, 02 Sep 2022 05:06:36 GMT  
		Size: 5.5 MB (5546993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077f60b8d79e0ce080c903c48fa8296ecb53f67cdcf73d748ec8b454d8d7ec96`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c152c32a5dfa1d8b81650a889c55e593122edd4a1b49983a5aae714fb567194c`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4606a5228ccb52337657838c69716d528a1cd36a6adb320134ad9f72dac1b0`  
		Last Modified: Fri, 02 Sep 2022 05:10:57 GMT  
		Size: 103.9 MB (103882165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1077970b7ff447bda164171d709fbff427233431a1b4e67f2c042babb86581d`  
		Last Modified: Fri, 02 Sep 2022 05:10:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1623dc240f1486b24057900a44b1773cb529bb6eb79de2586e3d68e4612aca5d`  
		Last Modified: Fri, 02 Sep 2022 05:11:17 GMT  
		Size: 73.3 MB (73278501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c19349a79634056717413469829a12bf9869bc820130019d21c041134468f6a`  
		Last Modified: Fri, 02 Sep 2022 05:11:07 GMT  
		Size: 273.4 KB (273436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d38666d25b1c976245f649412489ae8d72bdaf049159320f9d06e29d9c12ab`  
		Last Modified: Fri, 02 Sep 2022 05:11:07 GMT  
		Size: 2.4 KB (2420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b5b062abae098c506dc5944c0c2dd15738658bdca2359cff971286f3a21ac3`  
		Last Modified: Fri, 02 Sep 2022 05:11:10 GMT  
		Size: 22.1 MB (22133844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7042ec89f6d891cd95e94cd61209c7e05dec6bd0e5b8cea8f7de6e185eb2ba`  
		Last Modified: Fri, 02 Sep 2022 05:11:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59e95c9ba69710b05bbe0a10f7f318f27145d50937efd6e935208ddd6c651e0`  
		Last Modified: Fri, 02 Sep 2022 05:11:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91760914880a09803690d5d594d1b8e2bbe9dccf90c45668e5ce3e5519fe434c`  
		Last Modified: Fri, 02 Sep 2022 05:11:44 GMT  
		Size: 78.7 MB (78704188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c0409b4aafa794ecb20b46c1cd8f1de9548ba0dbbceb823a6c697f943457ea`  
		Last Modified: Fri, 02 Sep 2022 05:11:33 GMT  
		Size: 16.5 MB (16464464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ef861301145847f95ebf92976fe0df9dd8b6488b5c0d2ecd116013da505730`  
		Last Modified: Fri, 02 Sep 2022 05:11:30 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros1-bridge` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:703a9eac69888790c5e9f9b0ad8b2fe7c4212aefb8f87b468de8dfa49b46c55d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.3 MB (317344219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba234e3a95450c339cd2fb32a7fe82c0b586bcd441cb1568fb85614cea506395`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:24:13 GMT
ENV ROS_DISTRO=galactic
# Tue, 02 Aug 2022 15:25:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:25:05 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:25:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:25:07 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:25:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:25:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:25:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:26:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:26:16 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:26:18 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:26:20 GMT
ENV ROS1_DISTRO=noetic
# Tue, 02 Aug 2022 15:26:21 GMT
ENV ROS2_DISTRO=galactic
# Tue, 02 Aug 2022 15:26:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:07 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec24629b846176e31ddaaf8b24b1ddfa5c013c36a5adc644cc1ea9cbfaf1f0d`  
		Last Modified: Tue, 02 Aug 2022 15:48:08 GMT  
		Size: 100.3 MB (100301595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb6c32d186e05482bc0d52ca6d3348f8f2135fe0ce5cb80694cbf0c402904ab`  
		Last Modified: Tue, 02 Aug 2022 15:47:51 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f1bc7aab31ae221d1d0a204692f57529cc52be37d783e9408e6091c9140e30`  
		Last Modified: Tue, 02 Aug 2022 15:48:30 GMT  
		Size: 67.4 MB (67403003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8728db5450b6ae980d219774ae0acd473093c7203a814add3754b37fa58d2f16`  
		Last Modified: Tue, 02 Aug 2022 15:48:20 GMT  
		Size: 271.8 KB (271758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b3c45ed46817bdd81a5f97bc0ac2f937e60aba727035f3fda0c52b1e8d3766`  
		Last Modified: Tue, 02 Aug 2022 15:48:20 GMT  
		Size: 2.2 KB (2208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb12350bd7ee355d38d341f83cd1fc612133c69ea151b66e1784eeb2e27e4a4`  
		Last Modified: Tue, 02 Aug 2022 15:48:23 GMT  
		Size: 21.5 MB (21453253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88423f93f307272d4821bff3ed3a92da165133eeda2d669662750e2653e243c7`  
		Last Modified: Tue, 02 Aug 2022 15:48:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71bf2097533a80b1e6a12df87577fe260936fdbfc07806dee784658e7e11a32d`  
		Last Modified: Tue, 02 Aug 2022 15:49:01 GMT  
		Size: 78.4 MB (78449708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a9110e723a98854f8a59ac27a6fb2d57d6f09837880d7ed1362ac4b6c1329b`  
		Last Modified: Tue, 02 Aug 2022 15:48:49 GMT  
		Size: 15.8 MB (15761670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3349b8ec1b44856e85ff8fbf4aebd2b687e480b88d9b9b84574936a10cb12c03`  
		Last Modified: Tue, 02 Aug 2022 15:48:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:galactic-ros1-bridge-focal`

```console
$ docker pull ros@sha256:f942c77db8321f0dcb471a6a2c39d0a091a63a3b8aa292a85aa961686b5603dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:galactic-ros1-bridge-focal` - linux; amd64

```console
$ docker pull ros@sha256:6f868677049d21360ab3c77c7117cf3432bb0a45d625645fbbd4bad00010ddd9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.0 MB (330025494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a9b3283ccd5b50b76c43a25043d7b2fe3b0b97cad79b7e7a209c764f66f454`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:03:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:42:17 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:42:19 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:42:19 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:44:56 GMT
ENV ROS_DISTRO=galactic
# Fri, 02 Sep 2022 04:45:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:45:40 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 04:45:40 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:45:40 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:46:02 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:46:06 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:46:09 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 02 Sep 2022 04:46:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:46:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Sep 2022 04:46:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:46:34 GMT
ENV ROS1_DISTRO=noetic
# Fri, 02 Sep 2022 04:46:35 GMT
ENV ROS2_DISTRO=galactic
# Fri, 02 Sep 2022 04:47:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:11 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf19bc0e0d1d8bf1ec9b593eb3ddedecefdf4aff5f519ad585667a258956af1`  
		Last Modified: Fri, 02 Sep 2022 03:15:37 GMT  
		Size: 1.2 MB (1163757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff483ca449e233e69f18eb71e430f67ec1b4c8f5a965b4d7efc759a0ba2f18c4`  
		Last Modified: Fri, 02 Sep 2022 05:06:36 GMT  
		Size: 5.5 MB (5546993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077f60b8d79e0ce080c903c48fa8296ecb53f67cdcf73d748ec8b454d8d7ec96`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c152c32a5dfa1d8b81650a889c55e593122edd4a1b49983a5aae714fb567194c`  
		Last Modified: Fri, 02 Sep 2022 05:09:16 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4606a5228ccb52337657838c69716d528a1cd36a6adb320134ad9f72dac1b0`  
		Last Modified: Fri, 02 Sep 2022 05:10:57 GMT  
		Size: 103.9 MB (103882165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1077970b7ff447bda164171d709fbff427233431a1b4e67f2c042babb86581d`  
		Last Modified: Fri, 02 Sep 2022 05:10:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1623dc240f1486b24057900a44b1773cb529bb6eb79de2586e3d68e4612aca5d`  
		Last Modified: Fri, 02 Sep 2022 05:11:17 GMT  
		Size: 73.3 MB (73278501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c19349a79634056717413469829a12bf9869bc820130019d21c041134468f6a`  
		Last Modified: Fri, 02 Sep 2022 05:11:07 GMT  
		Size: 273.4 KB (273436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d38666d25b1c976245f649412489ae8d72bdaf049159320f9d06e29d9c12ab`  
		Last Modified: Fri, 02 Sep 2022 05:11:07 GMT  
		Size: 2.4 KB (2420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b5b062abae098c506dc5944c0c2dd15738658bdca2359cff971286f3a21ac3`  
		Last Modified: Fri, 02 Sep 2022 05:11:10 GMT  
		Size: 22.1 MB (22133844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7042ec89f6d891cd95e94cd61209c7e05dec6bd0e5b8cea8f7de6e185eb2ba`  
		Last Modified: Fri, 02 Sep 2022 05:11:30 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59e95c9ba69710b05bbe0a10f7f318f27145d50937efd6e935208ddd6c651e0`  
		Last Modified: Fri, 02 Sep 2022 05:11:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91760914880a09803690d5d594d1b8e2bbe9dccf90c45668e5ce3e5519fe434c`  
		Last Modified: Fri, 02 Sep 2022 05:11:44 GMT  
		Size: 78.7 MB (78704188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c0409b4aafa794ecb20b46c1cd8f1de9548ba0dbbceb823a6c697f943457ea`  
		Last Modified: Fri, 02 Sep 2022 05:11:33 GMT  
		Size: 16.5 MB (16464464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ef861301145847f95ebf92976fe0df9dd8b6488b5c0d2ecd116013da505730`  
		Last Modified: Fri, 02 Sep 2022 05:11:30 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:galactic-ros1-bridge-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:703a9eac69888790c5e9f9b0ad8b2fe7c4212aefb8f87b468de8dfa49b46c55d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.3 MB (317344219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba234e3a95450c339cd2fb32a7fe82c0b586bcd441cb1568fb85614cea506395`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:20:59 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu focal main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:21:00 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:21:02 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:24:13 GMT
ENV ROS_DISTRO=galactic
# Tue, 02 Aug 2022 15:25:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-core=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:25:05 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:25:06 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:25:07 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:25:36 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:25:41 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:25:44 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:26:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros-base=0.9.3-2*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:26:16 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:26:18 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:26:20 GMT
ENV ROS1_DISTRO=noetic
# Tue, 02 Aug 2022 15:26:21 GMT
ENV ROS2_DISTRO=galactic
# Tue, 02 Aug 2022 15:26:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-comm=1.15.14-1*     ros-noetic-roscpp-tutorials=0.10.2-1*     ros-noetic-rospy-tutorials=0.10.2-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-galactic-ros1-bridge=0.10.1-2*     ros-galactic-demo-nodes-cpp=0.14.3-1*     ros-galactic-demo-nodes-py=0.14.3-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:07 GMT
COPY file:196e0ab4e3b32a1af101eff4dfa0110eb39feb70f4f9f2df3de2e22162513085 in / 
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5618f497b1c1b8a6eae1767e0c0d3f9a8a2fb26c2f1602b04c31fb91968169`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486f2f820ed7564680a0acfc7dec6a13bd355944a9bc517c80dce4d3e58691fe`  
		Last Modified: Tue, 02 Aug 2022 15:46:29 GMT  
		Size: 1.9 KB (1948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec24629b846176e31ddaaf8b24b1ddfa5c013c36a5adc644cc1ea9cbfaf1f0d`  
		Last Modified: Tue, 02 Aug 2022 15:48:08 GMT  
		Size: 100.3 MB (100301595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb6c32d186e05482bc0d52ca6d3348f8f2135fe0ce5cb80694cbf0c402904ab`  
		Last Modified: Tue, 02 Aug 2022 15:47:51 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f1bc7aab31ae221d1d0a204692f57529cc52be37d783e9408e6091c9140e30`  
		Last Modified: Tue, 02 Aug 2022 15:48:30 GMT  
		Size: 67.4 MB (67403003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8728db5450b6ae980d219774ae0acd473093c7203a814add3754b37fa58d2f16`  
		Last Modified: Tue, 02 Aug 2022 15:48:20 GMT  
		Size: 271.8 KB (271758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b3c45ed46817bdd81a5f97bc0ac2f937e60aba727035f3fda0c52b1e8d3766`  
		Last Modified: Tue, 02 Aug 2022 15:48:20 GMT  
		Size: 2.2 KB (2208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb12350bd7ee355d38d341f83cd1fc612133c69ea151b66e1784eeb2e27e4a4`  
		Last Modified: Tue, 02 Aug 2022 15:48:23 GMT  
		Size: 21.5 MB (21453253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88423f93f307272d4821bff3ed3a92da165133eeda2d669662750e2653e243c7`  
		Last Modified: Tue, 02 Aug 2022 15:48:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71bf2097533a80b1e6a12df87577fe260936fdbfc07806dee784658e7e11a32d`  
		Last Modified: Tue, 02 Aug 2022 15:49:01 GMT  
		Size: 78.4 MB (78449708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a9110e723a98854f8a59ac27a6fb2d57d6f09837880d7ed1362ac4b6c1329b`  
		Last Modified: Tue, 02 Aug 2022 15:48:49 GMT  
		Size: 15.8 MB (15761670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3349b8ec1b44856e85ff8fbf4aebd2b687e480b88d9b9b84574936a10cb12c03`  
		Last Modified: Tue, 02 Aug 2022 15:48:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble`

```console
$ docker pull ros@sha256:62f27bdc790b1d69e9d32a0c1523b1605d465885d677afba42f262ba00dab65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble` - linux; amd64

```console
$ docker pull ros@sha256:b5afc3c15a18c85bd4472228addb045cfa1be4955efd4f7d1f5bc2bd1ea938a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262767288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0afc637f4748749ba7294a29cff472a9aff855e9b3f1c1a4641daf1c47f61306`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:35 GMT
ADD file:a7268f82a86219801950401c224cabbdd83ef510a7c71396b25f70c2639ae4fa in / 
# Thu, 01 Sep 2022 23:46:35 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:47:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:44 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:47:45 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:47:45 GMT
ENV ROS_DISTRO=humble
# Fri, 02 Sep 2022 04:49:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:49:26 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 04:49:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:49:26 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:50:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:50:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:50:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 02 Sep 2022 04:51:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b55860d4c667a7200a0cb279aec26777df61e5d3530388f223ce7859d566e7a`  
		Last Modified: Tue, 16 Aug 2022 03:03:54 GMT  
		Size: 30.4 MB (30426706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3547d30662b8f49979ed975e15692a70c7bb853c6f802402d13fae5baf9c98`  
		Last Modified: Fri, 02 Sep 2022 05:11:58 GMT  
		Size: 1.2 MB (1175731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e2de4e9186b2154434f8288f5aa7bb8a9d6dc013e0874f7f022b8ae24dfbf0`  
		Last Modified: Fri, 02 Sep 2022 05:11:56 GMT  
		Size: 3.8 MB (3827460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a3a3add45c3c8843eaf042b57f390470bedeb0ac07a77f9c6612bef030c530`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47468e731ca16770a971f055794d9d4098fc38d48dd35c9031b3076ca342047`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f3dbe0ec1046bb9bdd0276165d66b03aafb64279b2077b7fbdac5b1047b98e`  
		Last Modified: Fri, 02 Sep 2022 05:12:12 GMT  
		Size: 106.2 MB (106189810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d5ef6ac4127ac4c6d2c35e9befe4af09debd87c5e55110651f46e88a35c631`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47e8a6f8a449077cfb0901a9b21c22e899338a0bc99ca9be0951bf6b3256c1a`  
		Last Modified: Fri, 02 Sep 2022 05:12:36 GMT  
		Size: 97.8 MB (97849527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40faf29acfa4fc6c1747729238c7b69b3c05983e5f81a16389a75b6b7fad4ed7`  
		Last Modified: Fri, 02 Sep 2022 05:12:22 GMT  
		Size: 285.6 KB (285574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df57c7f1a275a97de9412ce0ca9182e86900074cda4ea3b82bb20d7a3c374a0c`  
		Last Modified: Fri, 02 Sep 2022 05:12:22 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3101d89bfa03579ba584f494cd916ad9cd928e61dec78734db0bf203c0ae68`  
		Last Modified: Fri, 02 Sep 2022 05:12:26 GMT  
		Size: 23.0 MB (23007608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:acdf5cdb5849df6e1eae707a9d59dea052812be1d5941cdc23b5773fdbcf6657
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (254989878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2561d52df82b07ddd78498fcf61efa619edf34b086a4ab5b50afb4e72d0ea9ed`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:27:39 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Aug 2022 15:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:28:29 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:28:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:28:31 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:29:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:29:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:29:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:29:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05fa5a00264cd775880db77d90a3ef55262e9fca2af5ce9b5829e8732057281`  
		Last Modified: Tue, 02 Aug 2022 15:49:30 GMT  
		Size: 103.9 MB (103889367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f851cc59237e6d46b391e74e170d98dfee8e2a0f1eeb69881e3ff47f20020f1e`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268f426f25631919b3a5f6d171d25f0b1c7eed19c2ff10805bfb5e2fd8acc246`  
		Last Modified: Tue, 02 Aug 2022 15:49:56 GMT  
		Size: 95.2 MB (95214628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c810faa1690af68f54ea46e1bdd750aac3e6e246a835ba0c70f85ce89614db`  
		Last Modified: Tue, 02 Aug 2022 15:49:43 GMT  
		Size: 283.0 KB (282977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5882ceb61cae13eccf9ebd03a7a30ce85f7bc53b71deb8705a7776522e6b03d6`  
		Last Modified: Tue, 02 Aug 2022 15:49:42 GMT  
		Size: 2.2 KB (2241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97be626b88d492edf0ca4cd8e116114811578dd05aea521639f25ccccdb848ad`  
		Last Modified: Tue, 02 Aug 2022 15:49:46 GMT  
		Size: 22.4 MB (22427651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-perception`

```console
$ docker pull ros@sha256:5ebe80ea4512d94f26bad2f9dbaa8e2eaf4318a72fdceaad7326fe4c9420cde9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception` - linux; amd64

```console
$ docker pull ros@sha256:1f7150af030fb952e645d29f203b3fcded126ff0a6266e3d555bf84f40a99d0c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1084481041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339e4abc3190c0e39084941988ade2c960baa9c0960645bab9326c3b9c7a40f0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:35 GMT
ADD file:a7268f82a86219801950401c224cabbdd83ef510a7c71396b25f70c2639ae4fa in / 
# Thu, 01 Sep 2022 23:46:35 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:47:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:44 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:47:45 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:47:45 GMT
ENV ROS_DISTRO=humble
# Fri, 02 Sep 2022 04:49:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:49:26 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 04:49:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:49:26 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:50:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:50:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:50:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 02 Sep 2022 04:51:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:59:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b55860d4c667a7200a0cb279aec26777df61e5d3530388f223ce7859d566e7a`  
		Last Modified: Tue, 16 Aug 2022 03:03:54 GMT  
		Size: 30.4 MB (30426706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3547d30662b8f49979ed975e15692a70c7bb853c6f802402d13fae5baf9c98`  
		Last Modified: Fri, 02 Sep 2022 05:11:58 GMT  
		Size: 1.2 MB (1175731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e2de4e9186b2154434f8288f5aa7bb8a9d6dc013e0874f7f022b8ae24dfbf0`  
		Last Modified: Fri, 02 Sep 2022 05:11:56 GMT  
		Size: 3.8 MB (3827460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a3a3add45c3c8843eaf042b57f390470bedeb0ac07a77f9c6612bef030c530`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47468e731ca16770a971f055794d9d4098fc38d48dd35c9031b3076ca342047`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f3dbe0ec1046bb9bdd0276165d66b03aafb64279b2077b7fbdac5b1047b98e`  
		Last Modified: Fri, 02 Sep 2022 05:12:12 GMT  
		Size: 106.2 MB (106189810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d5ef6ac4127ac4c6d2c35e9befe4af09debd87c5e55110651f46e88a35c631`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47e8a6f8a449077cfb0901a9b21c22e899338a0bc99ca9be0951bf6b3256c1a`  
		Last Modified: Fri, 02 Sep 2022 05:12:36 GMT  
		Size: 97.8 MB (97849527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40faf29acfa4fc6c1747729238c7b69b3c05983e5f81a16389a75b6b7fad4ed7`  
		Last Modified: Fri, 02 Sep 2022 05:12:22 GMT  
		Size: 285.6 KB (285574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df57c7f1a275a97de9412ce0ca9182e86900074cda4ea3b82bb20d7a3c374a0c`  
		Last Modified: Fri, 02 Sep 2022 05:12:22 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3101d89bfa03579ba584f494cd916ad9cd928e61dec78734db0bf203c0ae68`  
		Last Modified: Fri, 02 Sep 2022 05:12:26 GMT  
		Size: 23.0 MB (23007608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72b8f4b49d484fdb89a848443988e3313cabbc0d97d79fb1f0486bea4a9d3e0`  
		Last Modified: Fri, 02 Sep 2022 05:14:29 GMT  
		Size: 821.7 MB (821713753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:76edca30f7e1ef03392a3f02356d1ebdedc6fea03edf5b1e350ab5fb49312d5d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1034227178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7917f192cc7d1bb83f4d903e2ba00b8edd6a3bfd6807f9e0e22e804008f2d6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:27:39 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Aug 2022 15:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:28:29 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:28:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:28:31 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:29:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:29:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:29:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:29:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:32:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05fa5a00264cd775880db77d90a3ef55262e9fca2af5ce9b5829e8732057281`  
		Last Modified: Tue, 02 Aug 2022 15:49:30 GMT  
		Size: 103.9 MB (103889367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f851cc59237e6d46b391e74e170d98dfee8e2a0f1eeb69881e3ff47f20020f1e`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268f426f25631919b3a5f6d171d25f0b1c7eed19c2ff10805bfb5e2fd8acc246`  
		Last Modified: Tue, 02 Aug 2022 15:49:56 GMT  
		Size: 95.2 MB (95214628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c810faa1690af68f54ea46e1bdd750aac3e6e246a835ba0c70f85ce89614db`  
		Last Modified: Tue, 02 Aug 2022 15:49:43 GMT  
		Size: 283.0 KB (282977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5882ceb61cae13eccf9ebd03a7a30ce85f7bc53b71deb8705a7776522e6b03d6`  
		Last Modified: Tue, 02 Aug 2022 15:49:42 GMT  
		Size: 2.2 KB (2241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97be626b88d492edf0ca4cd8e116114811578dd05aea521639f25ccccdb848ad`  
		Last Modified: Tue, 02 Aug 2022 15:49:46 GMT  
		Size: 22.4 MB (22427651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa124ac25d3a1a83ea306f40bce0401e51ccb7cb7df5d46a4434747b1685c1d`  
		Last Modified: Tue, 02 Aug 2022 15:51:52 GMT  
		Size: 779.2 MB (779237300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-perception-jammy`

```console
$ docker pull ros@sha256:5ebe80ea4512d94f26bad2f9dbaa8e2eaf4318a72fdceaad7326fe4c9420cde9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:1f7150af030fb952e645d29f203b3fcded126ff0a6266e3d555bf84f40a99d0c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1084481041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339e4abc3190c0e39084941988ade2c960baa9c0960645bab9326c3b9c7a40f0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:35 GMT
ADD file:a7268f82a86219801950401c224cabbdd83ef510a7c71396b25f70c2639ae4fa in / 
# Thu, 01 Sep 2022 23:46:35 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:47:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:44 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:47:45 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:47:45 GMT
ENV ROS_DISTRO=humble
# Fri, 02 Sep 2022 04:49:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:49:26 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 04:49:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:49:26 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:50:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:50:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:50:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 02 Sep 2022 04:51:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:59:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b55860d4c667a7200a0cb279aec26777df61e5d3530388f223ce7859d566e7a`  
		Last Modified: Tue, 16 Aug 2022 03:03:54 GMT  
		Size: 30.4 MB (30426706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3547d30662b8f49979ed975e15692a70c7bb853c6f802402d13fae5baf9c98`  
		Last Modified: Fri, 02 Sep 2022 05:11:58 GMT  
		Size: 1.2 MB (1175731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e2de4e9186b2154434f8288f5aa7bb8a9d6dc013e0874f7f022b8ae24dfbf0`  
		Last Modified: Fri, 02 Sep 2022 05:11:56 GMT  
		Size: 3.8 MB (3827460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a3a3add45c3c8843eaf042b57f390470bedeb0ac07a77f9c6612bef030c530`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47468e731ca16770a971f055794d9d4098fc38d48dd35c9031b3076ca342047`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f3dbe0ec1046bb9bdd0276165d66b03aafb64279b2077b7fbdac5b1047b98e`  
		Last Modified: Fri, 02 Sep 2022 05:12:12 GMT  
		Size: 106.2 MB (106189810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d5ef6ac4127ac4c6d2c35e9befe4af09debd87c5e55110651f46e88a35c631`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47e8a6f8a449077cfb0901a9b21c22e899338a0bc99ca9be0951bf6b3256c1a`  
		Last Modified: Fri, 02 Sep 2022 05:12:36 GMT  
		Size: 97.8 MB (97849527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40faf29acfa4fc6c1747729238c7b69b3c05983e5f81a16389a75b6b7fad4ed7`  
		Last Modified: Fri, 02 Sep 2022 05:12:22 GMT  
		Size: 285.6 KB (285574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df57c7f1a275a97de9412ce0ca9182e86900074cda4ea3b82bb20d7a3c374a0c`  
		Last Modified: Fri, 02 Sep 2022 05:12:22 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3101d89bfa03579ba584f494cd916ad9cd928e61dec78734db0bf203c0ae68`  
		Last Modified: Fri, 02 Sep 2022 05:12:26 GMT  
		Size: 23.0 MB (23007608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72b8f4b49d484fdb89a848443988e3313cabbc0d97d79fb1f0486bea4a9d3e0`  
		Last Modified: Fri, 02 Sep 2022 05:14:29 GMT  
		Size: 821.7 MB (821713753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:76edca30f7e1ef03392a3f02356d1ebdedc6fea03edf5b1e350ab5fb49312d5d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1034227178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7917f192cc7d1bb83f4d903e2ba00b8edd6a3bfd6807f9e0e22e804008f2d6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:27:39 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Aug 2022 15:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:28:29 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:28:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:28:31 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:29:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:29:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:29:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:29:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:32:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05fa5a00264cd775880db77d90a3ef55262e9fca2af5ce9b5829e8732057281`  
		Last Modified: Tue, 02 Aug 2022 15:49:30 GMT  
		Size: 103.9 MB (103889367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f851cc59237e6d46b391e74e170d98dfee8e2a0f1eeb69881e3ff47f20020f1e`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268f426f25631919b3a5f6d171d25f0b1c7eed19c2ff10805bfb5e2fd8acc246`  
		Last Modified: Tue, 02 Aug 2022 15:49:56 GMT  
		Size: 95.2 MB (95214628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c810faa1690af68f54ea46e1bdd750aac3e6e246a835ba0c70f85ce89614db`  
		Last Modified: Tue, 02 Aug 2022 15:49:43 GMT  
		Size: 283.0 KB (282977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5882ceb61cae13eccf9ebd03a7a30ce85f7bc53b71deb8705a7776522e6b03d6`  
		Last Modified: Tue, 02 Aug 2022 15:49:42 GMT  
		Size: 2.2 KB (2241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97be626b88d492edf0ca4cd8e116114811578dd05aea521639f25ccccdb848ad`  
		Last Modified: Tue, 02 Aug 2022 15:49:46 GMT  
		Size: 22.4 MB (22427651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa124ac25d3a1a83ea306f40bce0401e51ccb7cb7df5d46a4434747b1685c1d`  
		Last Modified: Tue, 02 Aug 2022 15:51:52 GMT  
		Size: 779.2 MB (779237300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-base`

```console
$ docker pull ros@sha256:62f27bdc790b1d69e9d32a0c1523b1605d465885d677afba42f262ba00dab65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:b5afc3c15a18c85bd4472228addb045cfa1be4955efd4f7d1f5bc2bd1ea938a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262767288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0afc637f4748749ba7294a29cff472a9aff855e9b3f1c1a4641daf1c47f61306`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:35 GMT
ADD file:a7268f82a86219801950401c224cabbdd83ef510a7c71396b25f70c2639ae4fa in / 
# Thu, 01 Sep 2022 23:46:35 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:47:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:44 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:47:45 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:47:45 GMT
ENV ROS_DISTRO=humble
# Fri, 02 Sep 2022 04:49:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:49:26 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 04:49:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:49:26 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:50:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:50:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:50:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 02 Sep 2022 04:51:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b55860d4c667a7200a0cb279aec26777df61e5d3530388f223ce7859d566e7a`  
		Last Modified: Tue, 16 Aug 2022 03:03:54 GMT  
		Size: 30.4 MB (30426706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3547d30662b8f49979ed975e15692a70c7bb853c6f802402d13fae5baf9c98`  
		Last Modified: Fri, 02 Sep 2022 05:11:58 GMT  
		Size: 1.2 MB (1175731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e2de4e9186b2154434f8288f5aa7bb8a9d6dc013e0874f7f022b8ae24dfbf0`  
		Last Modified: Fri, 02 Sep 2022 05:11:56 GMT  
		Size: 3.8 MB (3827460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a3a3add45c3c8843eaf042b57f390470bedeb0ac07a77f9c6612bef030c530`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47468e731ca16770a971f055794d9d4098fc38d48dd35c9031b3076ca342047`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f3dbe0ec1046bb9bdd0276165d66b03aafb64279b2077b7fbdac5b1047b98e`  
		Last Modified: Fri, 02 Sep 2022 05:12:12 GMT  
		Size: 106.2 MB (106189810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d5ef6ac4127ac4c6d2c35e9befe4af09debd87c5e55110651f46e88a35c631`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47e8a6f8a449077cfb0901a9b21c22e899338a0bc99ca9be0951bf6b3256c1a`  
		Last Modified: Fri, 02 Sep 2022 05:12:36 GMT  
		Size: 97.8 MB (97849527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40faf29acfa4fc6c1747729238c7b69b3c05983e5f81a16389a75b6b7fad4ed7`  
		Last Modified: Fri, 02 Sep 2022 05:12:22 GMT  
		Size: 285.6 KB (285574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df57c7f1a275a97de9412ce0ca9182e86900074cda4ea3b82bb20d7a3c374a0c`  
		Last Modified: Fri, 02 Sep 2022 05:12:22 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3101d89bfa03579ba584f494cd916ad9cd928e61dec78734db0bf203c0ae68`  
		Last Modified: Fri, 02 Sep 2022 05:12:26 GMT  
		Size: 23.0 MB (23007608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:acdf5cdb5849df6e1eae707a9d59dea052812be1d5941cdc23b5773fdbcf6657
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (254989878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2561d52df82b07ddd78498fcf61efa619edf34b086a4ab5b50afb4e72d0ea9ed`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:27:39 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Aug 2022 15:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:28:29 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:28:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:28:31 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:29:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:29:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:29:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:29:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05fa5a00264cd775880db77d90a3ef55262e9fca2af5ce9b5829e8732057281`  
		Last Modified: Tue, 02 Aug 2022 15:49:30 GMT  
		Size: 103.9 MB (103889367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f851cc59237e6d46b391e74e170d98dfee8e2a0f1eeb69881e3ff47f20020f1e`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268f426f25631919b3a5f6d171d25f0b1c7eed19c2ff10805bfb5e2fd8acc246`  
		Last Modified: Tue, 02 Aug 2022 15:49:56 GMT  
		Size: 95.2 MB (95214628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c810faa1690af68f54ea46e1bdd750aac3e6e246a835ba0c70f85ce89614db`  
		Last Modified: Tue, 02 Aug 2022 15:49:43 GMT  
		Size: 283.0 KB (282977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5882ceb61cae13eccf9ebd03a7a30ce85f7bc53b71deb8705a7776522e6b03d6`  
		Last Modified: Tue, 02 Aug 2022 15:49:42 GMT  
		Size: 2.2 KB (2241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97be626b88d492edf0ca4cd8e116114811578dd05aea521639f25ccccdb848ad`  
		Last Modified: Tue, 02 Aug 2022 15:49:46 GMT  
		Size: 22.4 MB (22427651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-base-jammy`

```console
$ docker pull ros@sha256:62f27bdc790b1d69e9d32a0c1523b1605d465885d677afba42f262ba00dab65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:b5afc3c15a18c85bd4472228addb045cfa1be4955efd4f7d1f5bc2bd1ea938a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262767288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0afc637f4748749ba7294a29cff472a9aff855e9b3f1c1a4641daf1c47f61306`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:35 GMT
ADD file:a7268f82a86219801950401c224cabbdd83ef510a7c71396b25f70c2639ae4fa in / 
# Thu, 01 Sep 2022 23:46:35 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:47:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:44 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:47:45 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:47:45 GMT
ENV ROS_DISTRO=humble
# Fri, 02 Sep 2022 04:49:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:49:26 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 04:49:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:49:26 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:50:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:50:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:50:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 02 Sep 2022 04:51:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b55860d4c667a7200a0cb279aec26777df61e5d3530388f223ce7859d566e7a`  
		Last Modified: Tue, 16 Aug 2022 03:03:54 GMT  
		Size: 30.4 MB (30426706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3547d30662b8f49979ed975e15692a70c7bb853c6f802402d13fae5baf9c98`  
		Last Modified: Fri, 02 Sep 2022 05:11:58 GMT  
		Size: 1.2 MB (1175731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e2de4e9186b2154434f8288f5aa7bb8a9d6dc013e0874f7f022b8ae24dfbf0`  
		Last Modified: Fri, 02 Sep 2022 05:11:56 GMT  
		Size: 3.8 MB (3827460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a3a3add45c3c8843eaf042b57f390470bedeb0ac07a77f9c6612bef030c530`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47468e731ca16770a971f055794d9d4098fc38d48dd35c9031b3076ca342047`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f3dbe0ec1046bb9bdd0276165d66b03aafb64279b2077b7fbdac5b1047b98e`  
		Last Modified: Fri, 02 Sep 2022 05:12:12 GMT  
		Size: 106.2 MB (106189810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d5ef6ac4127ac4c6d2c35e9befe4af09debd87c5e55110651f46e88a35c631`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47e8a6f8a449077cfb0901a9b21c22e899338a0bc99ca9be0951bf6b3256c1a`  
		Last Modified: Fri, 02 Sep 2022 05:12:36 GMT  
		Size: 97.8 MB (97849527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40faf29acfa4fc6c1747729238c7b69b3c05983e5f81a16389a75b6b7fad4ed7`  
		Last Modified: Fri, 02 Sep 2022 05:12:22 GMT  
		Size: 285.6 KB (285574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df57c7f1a275a97de9412ce0ca9182e86900074cda4ea3b82bb20d7a3c374a0c`  
		Last Modified: Fri, 02 Sep 2022 05:12:22 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3101d89bfa03579ba584f494cd916ad9cd928e61dec78734db0bf203c0ae68`  
		Last Modified: Fri, 02 Sep 2022 05:12:26 GMT  
		Size: 23.0 MB (23007608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:acdf5cdb5849df6e1eae707a9d59dea052812be1d5941cdc23b5773fdbcf6657
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (254989878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2561d52df82b07ddd78498fcf61efa619edf34b086a4ab5b50afb4e72d0ea9ed`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:27:39 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Aug 2022 15:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:28:29 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:28:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:28:31 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:29:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:29:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:29:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:29:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05fa5a00264cd775880db77d90a3ef55262e9fca2af5ce9b5829e8732057281`  
		Last Modified: Tue, 02 Aug 2022 15:49:30 GMT  
		Size: 103.9 MB (103889367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f851cc59237e6d46b391e74e170d98dfee8e2a0f1eeb69881e3ff47f20020f1e`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268f426f25631919b3a5f6d171d25f0b1c7eed19c2ff10805bfb5e2fd8acc246`  
		Last Modified: Tue, 02 Aug 2022 15:49:56 GMT  
		Size: 95.2 MB (95214628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c810faa1690af68f54ea46e1bdd750aac3e6e246a835ba0c70f85ce89614db`  
		Last Modified: Tue, 02 Aug 2022 15:49:43 GMT  
		Size: 283.0 KB (282977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5882ceb61cae13eccf9ebd03a7a30ce85f7bc53b71deb8705a7776522e6b03d6`  
		Last Modified: Tue, 02 Aug 2022 15:49:42 GMT  
		Size: 2.2 KB (2241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97be626b88d492edf0ca4cd8e116114811578dd05aea521639f25ccccdb848ad`  
		Last Modified: Tue, 02 Aug 2022 15:49:46 GMT  
		Size: 22.4 MB (22427651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-core`

```console
$ docker pull ros@sha256:b85a352e7f40139d3291a0a0bf83821fd971bf54e3d224b087fc3b1d46f902b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:9563bfd3172e8574e1715fcb30492c30b83fb2df3cf85d3ea29cc7057654b280
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141622125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ff91d7a0709c149df8e6061c129ad8b19cad65d1d90d21a7c4dd39918822a3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:35 GMT
ADD file:a7268f82a86219801950401c224cabbdd83ef510a7c71396b25f70c2639ae4fa in / 
# Thu, 01 Sep 2022 23:46:35 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:47:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:44 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:47:45 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:47:45 GMT
ENV ROS_DISTRO=humble
# Fri, 02 Sep 2022 04:49:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:49:26 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 04:49:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:49:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2b55860d4c667a7200a0cb279aec26777df61e5d3530388f223ce7859d566e7a`  
		Last Modified: Tue, 16 Aug 2022 03:03:54 GMT  
		Size: 30.4 MB (30426706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3547d30662b8f49979ed975e15692a70c7bb853c6f802402d13fae5baf9c98`  
		Last Modified: Fri, 02 Sep 2022 05:11:58 GMT  
		Size: 1.2 MB (1175731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e2de4e9186b2154434f8288f5aa7bb8a9d6dc013e0874f7f022b8ae24dfbf0`  
		Last Modified: Fri, 02 Sep 2022 05:11:56 GMT  
		Size: 3.8 MB (3827460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a3a3add45c3c8843eaf042b57f390470bedeb0ac07a77f9c6612bef030c530`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47468e731ca16770a971f055794d9d4098fc38d48dd35c9031b3076ca342047`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f3dbe0ec1046bb9bdd0276165d66b03aafb64279b2077b7fbdac5b1047b98e`  
		Last Modified: Fri, 02 Sep 2022 05:12:12 GMT  
		Size: 106.2 MB (106189810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d5ef6ac4127ac4c6d2c35e9befe4af09debd87c5e55110651f46e88a35c631`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:13bf1b82f69a790ce0598ce60a1ab623d7d674831da3ae908b07b894293296e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137062381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a82769945152d9b284ed53731acfa50b3c4d02b968684c2b23e18ba2cde644`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:27:39 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Aug 2022 15:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:28:29 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:28:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:28:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05fa5a00264cd775880db77d90a3ef55262e9fca2af5ce9b5829e8732057281`  
		Last Modified: Tue, 02 Aug 2022 15:49:30 GMT  
		Size: 103.9 MB (103889367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f851cc59237e6d46b391e74e170d98dfee8e2a0f1eeb69881e3ff47f20020f1e`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:humble-ros-core-jammy`

```console
$ docker pull ros@sha256:b85a352e7f40139d3291a0a0bf83821fd971bf54e3d224b087fc3b1d46f902b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:humble-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:9563bfd3172e8574e1715fcb30492c30b83fb2df3cf85d3ea29cc7057654b280
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141622125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ff91d7a0709c149df8e6061c129ad8b19cad65d1d90d21a7c4dd39918822a3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:35 GMT
ADD file:a7268f82a86219801950401c224cabbdd83ef510a7c71396b25f70c2639ae4fa in / 
# Thu, 01 Sep 2022 23:46:35 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:47:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:44 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:47:45 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:47:45 GMT
ENV ROS_DISTRO=humble
# Fri, 02 Sep 2022 04:49:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:49:26 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 04:49:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:49:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2b55860d4c667a7200a0cb279aec26777df61e5d3530388f223ce7859d566e7a`  
		Last Modified: Tue, 16 Aug 2022 03:03:54 GMT  
		Size: 30.4 MB (30426706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3547d30662b8f49979ed975e15692a70c7bb853c6f802402d13fae5baf9c98`  
		Last Modified: Fri, 02 Sep 2022 05:11:58 GMT  
		Size: 1.2 MB (1175731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e2de4e9186b2154434f8288f5aa7bb8a9d6dc013e0874f7f022b8ae24dfbf0`  
		Last Modified: Fri, 02 Sep 2022 05:11:56 GMT  
		Size: 3.8 MB (3827460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a3a3add45c3c8843eaf042b57f390470bedeb0ac07a77f9c6612bef030c530`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47468e731ca16770a971f055794d9d4098fc38d48dd35c9031b3076ca342047`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f3dbe0ec1046bb9bdd0276165d66b03aafb64279b2077b7fbdac5b1047b98e`  
		Last Modified: Fri, 02 Sep 2022 05:12:12 GMT  
		Size: 106.2 MB (106189810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d5ef6ac4127ac4c6d2c35e9befe4af09debd87c5e55110651f46e88a35c631`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:humble-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:13bf1b82f69a790ce0598ce60a1ab623d7d674831da3ae908b07b894293296e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137062381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a82769945152d9b284ed53731acfa50b3c4d02b968684c2b23e18ba2cde644`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:27:39 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Aug 2022 15:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:28:29 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:28:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:28:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05fa5a00264cd775880db77d90a3ef55262e9fca2af5ce9b5829e8732057281`  
		Last Modified: Tue, 02 Aug 2022 15:49:30 GMT  
		Size: 103.9 MB (103889367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f851cc59237e6d46b391e74e170d98dfee8e2a0f1eeb69881e3ff47f20020f1e`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:latest`

```console
$ docker pull ros@sha256:62f27bdc790b1d69e9d32a0c1523b1605d465885d677afba42f262ba00dab65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:latest` - linux; amd64

```console
$ docker pull ros@sha256:b5afc3c15a18c85bd4472228addb045cfa1be4955efd4f7d1f5bc2bd1ea938a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262767288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0afc637f4748749ba7294a29cff472a9aff855e9b3f1c1a4641daf1c47f61306`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:35 GMT
ADD file:a7268f82a86219801950401c224cabbdd83ef510a7c71396b25f70c2639ae4fa in / 
# Thu, 01 Sep 2022 23:46:35 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:47:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:44 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:47:45 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:47:45 GMT
ENV ROS_DISTRO=humble
# Fri, 02 Sep 2022 04:49:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:49:26 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 04:49:26 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:49:26 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:50:22 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:50:28 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:50:33 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 02 Sep 2022 04:51:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b55860d4c667a7200a0cb279aec26777df61e5d3530388f223ce7859d566e7a`  
		Last Modified: Tue, 16 Aug 2022 03:03:54 GMT  
		Size: 30.4 MB (30426706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3547d30662b8f49979ed975e15692a70c7bb853c6f802402d13fae5baf9c98`  
		Last Modified: Fri, 02 Sep 2022 05:11:58 GMT  
		Size: 1.2 MB (1175731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e2de4e9186b2154434f8288f5aa7bb8a9d6dc013e0874f7f022b8ae24dfbf0`  
		Last Modified: Fri, 02 Sep 2022 05:11:56 GMT  
		Size: 3.8 MB (3827460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a3a3add45c3c8843eaf042b57f390470bedeb0ac07a77f9c6612bef030c530`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47468e731ca16770a971f055794d9d4098fc38d48dd35c9031b3076ca342047`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f3dbe0ec1046bb9bdd0276165d66b03aafb64279b2077b7fbdac5b1047b98e`  
		Last Modified: Fri, 02 Sep 2022 05:12:12 GMT  
		Size: 106.2 MB (106189810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d5ef6ac4127ac4c6d2c35e9befe4af09debd87c5e55110651f46e88a35c631`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47e8a6f8a449077cfb0901a9b21c22e899338a0bc99ca9be0951bf6b3256c1a`  
		Last Modified: Fri, 02 Sep 2022 05:12:36 GMT  
		Size: 97.8 MB (97849527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40faf29acfa4fc6c1747729238c7b69b3c05983e5f81a16389a75b6b7fad4ed7`  
		Last Modified: Fri, 02 Sep 2022 05:12:22 GMT  
		Size: 285.6 KB (285574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df57c7f1a275a97de9412ce0ca9182e86900074cda4ea3b82bb20d7a3c374a0c`  
		Last Modified: Fri, 02 Sep 2022 05:12:22 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3101d89bfa03579ba584f494cd916ad9cd928e61dec78734db0bf203c0ae68`  
		Last Modified: Fri, 02 Sep 2022 05:12:26 GMT  
		Size: 23.0 MB (23007608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:latest` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:acdf5cdb5849df6e1eae707a9d59dea052812be1d5941cdc23b5773fdbcf6657
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (254989878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2561d52df82b07ddd78498fcf61efa619edf34b086a4ab5b50afb4e72d0ea9ed`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:27:39 GMT
ENV ROS_DISTRO=humble
# Tue, 02 Aug 2022 15:28:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:28:29 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:28:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:28:31 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:29:06 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:29:11 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:29:16 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:29:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-humble-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05fa5a00264cd775880db77d90a3ef55262e9fca2af5ce9b5829e8732057281`  
		Last Modified: Tue, 02 Aug 2022 15:49:30 GMT  
		Size: 103.9 MB (103889367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f851cc59237e6d46b391e74e170d98dfee8e2a0f1eeb69881e3ff47f20020f1e`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:268f426f25631919b3a5f6d171d25f0b1c7eed19c2ff10805bfb5e2fd8acc246`  
		Last Modified: Tue, 02 Aug 2022 15:49:56 GMT  
		Size: 95.2 MB (95214628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41c810faa1690af68f54ea46e1bdd750aac3e6e246a835ba0c70f85ce89614db`  
		Last Modified: Tue, 02 Aug 2022 15:49:43 GMT  
		Size: 283.0 KB (282977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5882ceb61cae13eccf9ebd03a7a30ce85f7bc53b71deb8705a7776522e6b03d6`  
		Last Modified: Tue, 02 Aug 2022 15:49:42 GMT  
		Size: 2.2 KB (2241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97be626b88d492edf0ca4cd8e116114811578dd05aea521639f25ccccdb848ad`  
		Last Modified: Tue, 02 Aug 2022 15:49:46 GMT  
		Size: 22.4 MB (22427651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic`

```console
$ docker pull ros@sha256:6c0132c71983bc37ad850ea316d7be3ba7fdcdf74c458d28428e0b2e37472b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic` - linux; amd64

```console
$ docker pull ros@sha256:e894f44bf088cc62986b1aae33d8a8ec96810c746194983ce48d373f28c2eb60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.5 MB (437515827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e77b7e42944fc41a062c94ba1e54f9bc75737c6f1ee3293947939145ea10318`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:55:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:20:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:20:06 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Sep 2022 04:20:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:20:07 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:20:07 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:20:07 GMT
ENV ROS_DISTRO=melodic
# Fri, 02 Sep 2022 04:22:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:22:43 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Sep 2022 04:22:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:22:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:23:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:23:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:24:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210c2da7b10ffa6d0e2b3a3af917a40d5b42b1606cf3aff1dbbd48b1da768dd2`  
		Last Modified: Fri, 02 Sep 2022 03:13:02 GMT  
		Size: 831.0 KB (830989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc21f3c6df3e09da41edf5cd277be198a0b9ce9de84590bce7c7f8169fe8458`  
		Last Modified: Fri, 02 Sep 2022 05:04:14 GMT  
		Size: 4.9 MB (4873660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c601897ffb3e3526f97b7f3ac57655aa3b636d8d501e997e89629b654dd7e8dc`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff02d512a7003472763130f30478d4f0c5e440cc42c6e111764af77b527686d5`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99a32123d45b8f75cdc98623e79fe3c15f9f2da76e2827622e844770c38afa4`  
		Last Modified: Fri, 02 Sep 2022 05:04:53 GMT  
		Size: 259.6 MB (259559627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abce6b68d4012a79d622c3088e409f52f46a4c2d57e7d45df885e9a566a052c`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a0804aad7d24aedc9674dd262573672ffb24e77bd0b94b38774dd4c1344a65`  
		Last Modified: Fri, 02 Sep 2022 05:05:12 GMT  
		Size: 70.3 MB (70259712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf4c705dfb136d0edfefa4b6ea486990b27430cb1acb7e7aa9c680225f5845c`  
		Last Modified: Fri, 02 Sep 2022 05:05:02 GMT  
		Size: 284.7 KB (284711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463d8179e60fd0676ccb9cded217236342e7d2d9185a56f2f003efb6d1e597bf`  
		Last Modified: Fri, 02 Sep 2022 05:05:14 GMT  
		Size: 75.0 MB (74995198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic` - linux; arm variant v7

```console
$ docker pull ros@sha256:814af5012b36d9eed06c9cac7ad085d72ce7030a89e9b46d7c8f5c6d74d5bc25
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.0 MB (385997135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835e9afd0c76cb727206ffdc1e255cb66a4ad1f768b4a044f6316e2a544b93c0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:40:36 GMT
ADD file:c5ca169f034f6be72446c95b43cd8cc6001848067793f102e7a2b970dd21db54 in / 
# Tue, 02 Aug 2022 01:40:37 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:38:47 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:39:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:39:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 03 Aug 2022 22:39:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 03 Aug 2022 22:39:35 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 22:39:35 GMT
ENV LC_ALL=C.UTF-8
# Wed, 03 Aug 2022 22:39:35 GMT
ENV ROS_DISTRO=melodic
# Wed, 03 Aug 2022 22:42:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:42:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 03 Aug 2022 22:42:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 03 Aug 2022 22:42:42 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:43:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:44:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 03 Aug 2022 22:46:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a03a1d54dcfd6ce7007bfa41c40b1747d5553db7ee3404e88dd3ddc54ede514e`  
		Last Modified: Tue, 02 Aug 2022 01:42:53 GMT  
		Size: 22.3 MB (22305613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad475a95b77752b25dc36bec810d7cc2000f86bc50ea57592b8f988605fc4c6`  
		Last Modified: Wed, 03 Aug 2022 23:06:53 GMT  
		Size: 840.0 KB (839977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d76a2f1b035d0df7e2f785a3199e9e86fdeeda1c9f6087f594f2d8a42f0cfb`  
		Last Modified: Wed, 03 Aug 2022 23:06:51 GMT  
		Size: 4.1 MB (4087975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acdc23d18c079581f3391d042b65fd7ae55d75333914fd8cdcd0b8acdd6bf10`  
		Last Modified: Wed, 03 Aug 2022 23:06:50 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3a86db6f1e409fa1d0b2018d788c0539b214c365337f886b86db7e860ee482`  
		Last Modified: Wed, 03 Aug 2022 23:06:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79c58cc0918adb02a33e27d7ad4e74c5e0463844a26e99fb60557c3594324b5`  
		Last Modified: Wed, 03 Aug 2022 23:07:34 GMT  
		Size: 239.0 MB (239014439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094e568816932729edf86ebafaaeb847af8bda6ade01fb926c6a121f6b825974`  
		Last Modified: Wed, 03 Aug 2022 23:06:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23d14b221e943bfa66059662f80e5ae90e6e1f053ed424ca6b2a40c15876113`  
		Last Modified: Wed, 03 Aug 2022 23:07:57 GMT  
		Size: 54.7 MB (54720659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537d299c243ea0c73b05e8b607aa42ec071f847fbfa98d9ab5463a6594a04406`  
		Last Modified: Wed, 03 Aug 2022 23:07:46 GMT  
		Size: 283.1 KB (283112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d03bb1219b316469e8bd9f059ea35bbe07e5c60596349c1a2f46c2230f51e2`  
		Last Modified: Wed, 03 Aug 2022 23:08:02 GMT  
		Size: 64.7 MB (64743513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e19db181648b571c1a017e730f52145de920147e64052fa8662b7f611ac707db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.7 MB (411718282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56b623ecaac63fef2cd569acd1b109d44ce4a7318e7d3bda7b0c6d1e2ab1334`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:03:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:03:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:03:39 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:03:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:03:41 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 15:05:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:05:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:05:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:05:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:06:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87c7d887e7b961ba6c9db72dd6419c5ac455dd43d49b194dbc43680f849a6ef`  
		Last Modified: Tue, 02 Aug 2022 15:38:49 GMT  
		Size: 839.8 KB (839769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51fe758bc1275edfa803da680fe43894a9e4bdb69d83153ccca2d60ba34bbee`  
		Last Modified: Tue, 02 Aug 2022 15:38:47 GMT  
		Size: 4.3 MB (4265854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9646eaa84fc50bf88a2bca0599491e795cf8122e6fe16671e23fd8b87804e823`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4ce991e1d0bf36ab7c0c7db9323c2cc620b0d96c88f26c619287aee7598666`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a101d7b97c7577b747e3cc14cb64c408587e6489c4b2420aad7fa1dbbd8fe189`  
		Last Modified: Tue, 02 Aug 2022 15:39:22 GMT  
		Size: 252.5 MB (252503681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c716f26c3c2a680d90778a974e99dc5d04bf9e4fbd9077cdb619b311ff4f0d24`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b66bed859b212ff9f65c306618bc607825b531e9a79843b4d75f5e870b3195`  
		Last Modified: Tue, 02 Aug 2022 15:39:42 GMT  
		Size: 63.1 MB (63088414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee909ec215bcdf8f5cd2e47e3aaf397ef01b2695fd292ea49920505e539f80c9`  
		Last Modified: Tue, 02 Aug 2022 15:39:34 GMT  
		Size: 283.1 KB (283086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884a1a0922cfe088904523812cfa7b3897bc3fc1b7eb0f266e99c75d92662a17`  
		Last Modified: Tue, 02 Aug 2022 15:39:44 GMT  
		Size: 67.0 MB (67000963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-perception`

```console
$ docker pull ros@sha256:ec664cf86899bde9519b505c43177e4a7cad1c3d7b6ee82a3280f7fdd8bfd564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-perception` - linux; amd64

```console
$ docker pull ros@sha256:6161bfe6f5130cd4a735c86853cf7938719faab46bf7598700c32d9e6c905c16
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.9 MB (742863544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f193582ec5d8aa3650e7bb7af89868fd4265bcd8af0e4262805656156bf49a39`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:55:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:20:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:20:06 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Sep 2022 04:20:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:20:07 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:20:07 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:20:07 GMT
ENV ROS_DISTRO=melodic
# Fri, 02 Sep 2022 04:22:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:22:43 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Sep 2022 04:22:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:22:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:23:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:23:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:24:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210c2da7b10ffa6d0e2b3a3af917a40d5b42b1606cf3aff1dbbd48b1da768dd2`  
		Last Modified: Fri, 02 Sep 2022 03:13:02 GMT  
		Size: 831.0 KB (830989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc21f3c6df3e09da41edf5cd277be198a0b9ce9de84590bce7c7f8169fe8458`  
		Last Modified: Fri, 02 Sep 2022 05:04:14 GMT  
		Size: 4.9 MB (4873660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c601897ffb3e3526f97b7f3ac57655aa3b636d8d501e997e89629b654dd7e8dc`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff02d512a7003472763130f30478d4f0c5e440cc42c6e111764af77b527686d5`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99a32123d45b8f75cdc98623e79fe3c15f9f2da76e2827622e844770c38afa4`  
		Last Modified: Fri, 02 Sep 2022 05:04:53 GMT  
		Size: 259.6 MB (259559627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abce6b68d4012a79d622c3088e409f52f46a4c2d57e7d45df885e9a566a052c`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a0804aad7d24aedc9674dd262573672ffb24e77bd0b94b38774dd4c1344a65`  
		Last Modified: Fri, 02 Sep 2022 05:05:12 GMT  
		Size: 70.3 MB (70259712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf4c705dfb136d0edfefa4b6ea486990b27430cb1acb7e7aa9c680225f5845c`  
		Last Modified: Fri, 02 Sep 2022 05:05:02 GMT  
		Size: 284.7 KB (284711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463d8179e60fd0676ccb9cded217236342e7d2d9185a56f2f003efb6d1e597bf`  
		Last Modified: Fri, 02 Sep 2022 05:05:14 GMT  
		Size: 75.0 MB (74995198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9ad2f398f5cff0abe5f19d6199b225ec6b2591d2450a4222f6d1b8210f9bbf`  
		Last Modified: Fri, 02 Sep 2022 05:06:25 GMT  
		Size: 305.3 MB (305347717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:fb56a30a42037799cccacc2d306c93fb5b70fb26c7f5bc8d6cde583f63b68b57
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **646.0 MB (646041548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a6500c512cffcafac3324bd92bbeb06210f4ed725fb52e531a98253a8241d9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:40:36 GMT
ADD file:c5ca169f034f6be72446c95b43cd8cc6001848067793f102e7a2b970dd21db54 in / 
# Tue, 02 Aug 2022 01:40:37 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:38:47 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:39:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:39:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 03 Aug 2022 22:39:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 03 Aug 2022 22:39:35 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 22:39:35 GMT
ENV LC_ALL=C.UTF-8
# Wed, 03 Aug 2022 22:39:35 GMT
ENV ROS_DISTRO=melodic
# Wed, 03 Aug 2022 22:42:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:42:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 03 Aug 2022 22:42:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 03 Aug 2022 22:42:42 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:43:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:44:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 03 Aug 2022 22:46:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:52:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a03a1d54dcfd6ce7007bfa41c40b1747d5553db7ee3404e88dd3ddc54ede514e`  
		Last Modified: Tue, 02 Aug 2022 01:42:53 GMT  
		Size: 22.3 MB (22305613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad475a95b77752b25dc36bec810d7cc2000f86bc50ea57592b8f988605fc4c6`  
		Last Modified: Wed, 03 Aug 2022 23:06:53 GMT  
		Size: 840.0 KB (839977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d76a2f1b035d0df7e2f785a3199e9e86fdeeda1c9f6087f594f2d8a42f0cfb`  
		Last Modified: Wed, 03 Aug 2022 23:06:51 GMT  
		Size: 4.1 MB (4087975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acdc23d18c079581f3391d042b65fd7ae55d75333914fd8cdcd0b8acdd6bf10`  
		Last Modified: Wed, 03 Aug 2022 23:06:50 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3a86db6f1e409fa1d0b2018d788c0539b214c365337f886b86db7e860ee482`  
		Last Modified: Wed, 03 Aug 2022 23:06:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79c58cc0918adb02a33e27d7ad4e74c5e0463844a26e99fb60557c3594324b5`  
		Last Modified: Wed, 03 Aug 2022 23:07:34 GMT  
		Size: 239.0 MB (239014439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094e568816932729edf86ebafaaeb847af8bda6ade01fb926c6a121f6b825974`  
		Last Modified: Wed, 03 Aug 2022 23:06:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23d14b221e943bfa66059662f80e5ae90e6e1f053ed424ca6b2a40c15876113`  
		Last Modified: Wed, 03 Aug 2022 23:07:57 GMT  
		Size: 54.7 MB (54720659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537d299c243ea0c73b05e8b607aa42ec071f847fbfa98d9ab5463a6594a04406`  
		Last Modified: Wed, 03 Aug 2022 23:07:46 GMT  
		Size: 283.1 KB (283112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d03bb1219b316469e8bd9f059ea35bbe07e5c60596349c1a2f46c2230f51e2`  
		Last Modified: Wed, 03 Aug 2022 23:08:02 GMT  
		Size: 64.7 MB (64743513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3a8af3711aa61966951251c2db1ff769876ceeb475fc27d25c223cb4a7d293`  
		Last Modified: Wed, 03 Aug 2022 23:09:15 GMT  
		Size: 260.0 MB (260044413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c6099c16f7786d73e0d0aadb844b9acd7a6f7c58596b39fb0400ff8fbc5b8c3b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.2 MB (703163757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d1e45dcbdd3a8a9eb584bf7ed194f49343542bf5c85661e5c986dc1c3565e5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:03:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:03:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:03:39 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:03:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:03:41 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 15:05:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:05:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:05:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:05:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:06:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:08:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87c7d887e7b961ba6c9db72dd6419c5ac455dd43d49b194dbc43680f849a6ef`  
		Last Modified: Tue, 02 Aug 2022 15:38:49 GMT  
		Size: 839.8 KB (839769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51fe758bc1275edfa803da680fe43894a9e4bdb69d83153ccca2d60ba34bbee`  
		Last Modified: Tue, 02 Aug 2022 15:38:47 GMT  
		Size: 4.3 MB (4265854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9646eaa84fc50bf88a2bca0599491e795cf8122e6fe16671e23fd8b87804e823`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4ce991e1d0bf36ab7c0c7db9323c2cc620b0d96c88f26c619287aee7598666`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a101d7b97c7577b747e3cc14cb64c408587e6489c4b2420aad7fa1dbbd8fe189`  
		Last Modified: Tue, 02 Aug 2022 15:39:22 GMT  
		Size: 252.5 MB (252503681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c716f26c3c2a680d90778a974e99dc5d04bf9e4fbd9077cdb619b311ff4f0d24`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b66bed859b212ff9f65c306618bc607825b531e9a79843b4d75f5e870b3195`  
		Last Modified: Tue, 02 Aug 2022 15:39:42 GMT  
		Size: 63.1 MB (63088414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee909ec215bcdf8f5cd2e47e3aaf397ef01b2695fd292ea49920505e539f80c9`  
		Last Modified: Tue, 02 Aug 2022 15:39:34 GMT  
		Size: 283.1 KB (283086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884a1a0922cfe088904523812cfa7b3897bc3fc1b7eb0f266e99c75d92662a17`  
		Last Modified: Tue, 02 Aug 2022 15:39:44 GMT  
		Size: 67.0 MB (67000963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4a1da1cf397ef69011d59232aacc2b256057abfafa903e3beb919cff024a2b`  
		Last Modified: Tue, 02 Aug 2022 15:41:08 GMT  
		Size: 291.4 MB (291445475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-perception-bionic`

```console
$ docker pull ros@sha256:ec664cf86899bde9519b505c43177e4a7cad1c3d7b6ee82a3280f7fdd8bfd564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-perception-bionic` - linux; amd64

```console
$ docker pull ros@sha256:6161bfe6f5130cd4a735c86853cf7938719faab46bf7598700c32d9e6c905c16
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.9 MB (742863544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f193582ec5d8aa3650e7bb7af89868fd4265bcd8af0e4262805656156bf49a39`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:55:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:20:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:20:06 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Sep 2022 04:20:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:20:07 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:20:07 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:20:07 GMT
ENV ROS_DISTRO=melodic
# Fri, 02 Sep 2022 04:22:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:22:43 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Sep 2022 04:22:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:22:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:23:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:23:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:24:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210c2da7b10ffa6d0e2b3a3af917a40d5b42b1606cf3aff1dbbd48b1da768dd2`  
		Last Modified: Fri, 02 Sep 2022 03:13:02 GMT  
		Size: 831.0 KB (830989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc21f3c6df3e09da41edf5cd277be198a0b9ce9de84590bce7c7f8169fe8458`  
		Last Modified: Fri, 02 Sep 2022 05:04:14 GMT  
		Size: 4.9 MB (4873660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c601897ffb3e3526f97b7f3ac57655aa3b636d8d501e997e89629b654dd7e8dc`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff02d512a7003472763130f30478d4f0c5e440cc42c6e111764af77b527686d5`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99a32123d45b8f75cdc98623e79fe3c15f9f2da76e2827622e844770c38afa4`  
		Last Modified: Fri, 02 Sep 2022 05:04:53 GMT  
		Size: 259.6 MB (259559627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abce6b68d4012a79d622c3088e409f52f46a4c2d57e7d45df885e9a566a052c`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a0804aad7d24aedc9674dd262573672ffb24e77bd0b94b38774dd4c1344a65`  
		Last Modified: Fri, 02 Sep 2022 05:05:12 GMT  
		Size: 70.3 MB (70259712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf4c705dfb136d0edfefa4b6ea486990b27430cb1acb7e7aa9c680225f5845c`  
		Last Modified: Fri, 02 Sep 2022 05:05:02 GMT  
		Size: 284.7 KB (284711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463d8179e60fd0676ccb9cded217236342e7d2d9185a56f2f003efb6d1e597bf`  
		Last Modified: Fri, 02 Sep 2022 05:05:14 GMT  
		Size: 75.0 MB (74995198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9ad2f398f5cff0abe5f19d6199b225ec6b2591d2450a4222f6d1b8210f9bbf`  
		Last Modified: Fri, 02 Sep 2022 05:06:25 GMT  
		Size: 305.3 MB (305347717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:fb56a30a42037799cccacc2d306c93fb5b70fb26c7f5bc8d6cde583f63b68b57
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **646.0 MB (646041548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a6500c512cffcafac3324bd92bbeb06210f4ed725fb52e531a98253a8241d9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:40:36 GMT
ADD file:c5ca169f034f6be72446c95b43cd8cc6001848067793f102e7a2b970dd21db54 in / 
# Tue, 02 Aug 2022 01:40:37 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:38:47 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:39:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:39:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 03 Aug 2022 22:39:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 03 Aug 2022 22:39:35 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 22:39:35 GMT
ENV LC_ALL=C.UTF-8
# Wed, 03 Aug 2022 22:39:35 GMT
ENV ROS_DISTRO=melodic
# Wed, 03 Aug 2022 22:42:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:42:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 03 Aug 2022 22:42:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 03 Aug 2022 22:42:42 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:43:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:44:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 03 Aug 2022 22:46:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:52:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a03a1d54dcfd6ce7007bfa41c40b1747d5553db7ee3404e88dd3ddc54ede514e`  
		Last Modified: Tue, 02 Aug 2022 01:42:53 GMT  
		Size: 22.3 MB (22305613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad475a95b77752b25dc36bec810d7cc2000f86bc50ea57592b8f988605fc4c6`  
		Last Modified: Wed, 03 Aug 2022 23:06:53 GMT  
		Size: 840.0 KB (839977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d76a2f1b035d0df7e2f785a3199e9e86fdeeda1c9f6087f594f2d8a42f0cfb`  
		Last Modified: Wed, 03 Aug 2022 23:06:51 GMT  
		Size: 4.1 MB (4087975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acdc23d18c079581f3391d042b65fd7ae55d75333914fd8cdcd0b8acdd6bf10`  
		Last Modified: Wed, 03 Aug 2022 23:06:50 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3a86db6f1e409fa1d0b2018d788c0539b214c365337f886b86db7e860ee482`  
		Last Modified: Wed, 03 Aug 2022 23:06:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79c58cc0918adb02a33e27d7ad4e74c5e0463844a26e99fb60557c3594324b5`  
		Last Modified: Wed, 03 Aug 2022 23:07:34 GMT  
		Size: 239.0 MB (239014439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094e568816932729edf86ebafaaeb847af8bda6ade01fb926c6a121f6b825974`  
		Last Modified: Wed, 03 Aug 2022 23:06:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23d14b221e943bfa66059662f80e5ae90e6e1f053ed424ca6b2a40c15876113`  
		Last Modified: Wed, 03 Aug 2022 23:07:57 GMT  
		Size: 54.7 MB (54720659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537d299c243ea0c73b05e8b607aa42ec071f847fbfa98d9ab5463a6594a04406`  
		Last Modified: Wed, 03 Aug 2022 23:07:46 GMT  
		Size: 283.1 KB (283112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d03bb1219b316469e8bd9f059ea35bbe07e5c60596349c1a2f46c2230f51e2`  
		Last Modified: Wed, 03 Aug 2022 23:08:02 GMT  
		Size: 64.7 MB (64743513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3a8af3711aa61966951251c2db1ff769876ceeb475fc27d25c223cb4a7d293`  
		Last Modified: Wed, 03 Aug 2022 23:09:15 GMT  
		Size: 260.0 MB (260044413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-perception-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c6099c16f7786d73e0d0aadb844b9acd7a6f7c58596b39fb0400ff8fbc5b8c3b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **703.2 MB (703163757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d1e45dcbdd3a8a9eb584bf7ed194f49343542bf5c85661e5c986dc1c3565e5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:03:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:03:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:03:39 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:03:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:03:41 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 15:05:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:05:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:05:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:05:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:06:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:08:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-perception=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87c7d887e7b961ba6c9db72dd6419c5ac455dd43d49b194dbc43680f849a6ef`  
		Last Modified: Tue, 02 Aug 2022 15:38:49 GMT  
		Size: 839.8 KB (839769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51fe758bc1275edfa803da680fe43894a9e4bdb69d83153ccca2d60ba34bbee`  
		Last Modified: Tue, 02 Aug 2022 15:38:47 GMT  
		Size: 4.3 MB (4265854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9646eaa84fc50bf88a2bca0599491e795cf8122e6fe16671e23fd8b87804e823`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4ce991e1d0bf36ab7c0c7db9323c2cc620b0d96c88f26c619287aee7598666`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a101d7b97c7577b747e3cc14cb64c408587e6489c4b2420aad7fa1dbbd8fe189`  
		Last Modified: Tue, 02 Aug 2022 15:39:22 GMT  
		Size: 252.5 MB (252503681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c716f26c3c2a680d90778a974e99dc5d04bf9e4fbd9077cdb619b311ff4f0d24`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b66bed859b212ff9f65c306618bc607825b531e9a79843b4d75f5e870b3195`  
		Last Modified: Tue, 02 Aug 2022 15:39:42 GMT  
		Size: 63.1 MB (63088414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee909ec215bcdf8f5cd2e47e3aaf397ef01b2695fd292ea49920505e539f80c9`  
		Last Modified: Tue, 02 Aug 2022 15:39:34 GMT  
		Size: 283.1 KB (283086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884a1a0922cfe088904523812cfa7b3897bc3fc1b7eb0f266e99c75d92662a17`  
		Last Modified: Tue, 02 Aug 2022 15:39:44 GMT  
		Size: 67.0 MB (67000963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4a1da1cf397ef69011d59232aacc2b256057abfafa903e3beb919cff024a2b`  
		Last Modified: Tue, 02 Aug 2022 15:41:08 GMT  
		Size: 291.4 MB (291445475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-robot`

```console
$ docker pull ros@sha256:211ce267b2b27c8a4e39d6aa6a487ede931aa06c314b6c416394637ce02209fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-robot` - linux; amd64

```console
$ docker pull ros@sha256:85bc4c3c605d67ba0ef9275c4750d9cf8af7bcb8a3b01be2a686cb56e570bd51
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.6 MB (448601669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8721d889104c51a26ed1d5208079740f172ba6c73512808b54b32fa72fc2397`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:55:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:20:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:20:06 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Sep 2022 04:20:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:20:07 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:20:07 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:20:07 GMT
ENV ROS_DISTRO=melodic
# Fri, 02 Sep 2022 04:22:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:22:43 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Sep 2022 04:22:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:22:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:23:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:23:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:24:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:25:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210c2da7b10ffa6d0e2b3a3af917a40d5b42b1606cf3aff1dbbd48b1da768dd2`  
		Last Modified: Fri, 02 Sep 2022 03:13:02 GMT  
		Size: 831.0 KB (830989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc21f3c6df3e09da41edf5cd277be198a0b9ce9de84590bce7c7f8169fe8458`  
		Last Modified: Fri, 02 Sep 2022 05:04:14 GMT  
		Size: 4.9 MB (4873660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c601897ffb3e3526f97b7f3ac57655aa3b636d8d501e997e89629b654dd7e8dc`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff02d512a7003472763130f30478d4f0c5e440cc42c6e111764af77b527686d5`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99a32123d45b8f75cdc98623e79fe3c15f9f2da76e2827622e844770c38afa4`  
		Last Modified: Fri, 02 Sep 2022 05:04:53 GMT  
		Size: 259.6 MB (259559627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abce6b68d4012a79d622c3088e409f52f46a4c2d57e7d45df885e9a566a052c`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a0804aad7d24aedc9674dd262573672ffb24e77bd0b94b38774dd4c1344a65`  
		Last Modified: Fri, 02 Sep 2022 05:05:12 GMT  
		Size: 70.3 MB (70259712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf4c705dfb136d0edfefa4b6ea486990b27430cb1acb7e7aa9c680225f5845c`  
		Last Modified: Fri, 02 Sep 2022 05:05:02 GMT  
		Size: 284.7 KB (284711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463d8179e60fd0676ccb9cded217236342e7d2d9185a56f2f003efb6d1e597bf`  
		Last Modified: Fri, 02 Sep 2022 05:05:14 GMT  
		Size: 75.0 MB (74995198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f95ccd28b67e6e24906599991ef70fb02811a4e3873615747bd8af8017f7bc`  
		Last Modified: Fri, 02 Sep 2022 05:05:28 GMT  
		Size: 11.1 MB (11085842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:7f4b7e824e2c2d884a5fb5a2c9b781342f4cf8aa705a8a43780f57b072fceb77
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.1 MB (396120708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d09ce3f49835d2c880946babd1f27d25bd83fed4169ab6f73ef3ed6972266945`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:40:36 GMT
ADD file:c5ca169f034f6be72446c95b43cd8cc6001848067793f102e7a2b970dd21db54 in / 
# Tue, 02 Aug 2022 01:40:37 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:38:47 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:39:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:39:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 03 Aug 2022 22:39:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 03 Aug 2022 22:39:35 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 22:39:35 GMT
ENV LC_ALL=C.UTF-8
# Wed, 03 Aug 2022 22:39:35 GMT
ENV ROS_DISTRO=melodic
# Wed, 03 Aug 2022 22:42:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:42:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 03 Aug 2022 22:42:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 03 Aug 2022 22:42:42 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:43:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:44:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 03 Aug 2022 22:46:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:47:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a03a1d54dcfd6ce7007bfa41c40b1747d5553db7ee3404e88dd3ddc54ede514e`  
		Last Modified: Tue, 02 Aug 2022 01:42:53 GMT  
		Size: 22.3 MB (22305613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad475a95b77752b25dc36bec810d7cc2000f86bc50ea57592b8f988605fc4c6`  
		Last Modified: Wed, 03 Aug 2022 23:06:53 GMT  
		Size: 840.0 KB (839977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d76a2f1b035d0df7e2f785a3199e9e86fdeeda1c9f6087f594f2d8a42f0cfb`  
		Last Modified: Wed, 03 Aug 2022 23:06:51 GMT  
		Size: 4.1 MB (4087975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acdc23d18c079581f3391d042b65fd7ae55d75333914fd8cdcd0b8acdd6bf10`  
		Last Modified: Wed, 03 Aug 2022 23:06:50 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3a86db6f1e409fa1d0b2018d788c0539b214c365337f886b86db7e860ee482`  
		Last Modified: Wed, 03 Aug 2022 23:06:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79c58cc0918adb02a33e27d7ad4e74c5e0463844a26e99fb60557c3594324b5`  
		Last Modified: Wed, 03 Aug 2022 23:07:34 GMT  
		Size: 239.0 MB (239014439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094e568816932729edf86ebafaaeb847af8bda6ade01fb926c6a121f6b825974`  
		Last Modified: Wed, 03 Aug 2022 23:06:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23d14b221e943bfa66059662f80e5ae90e6e1f053ed424ca6b2a40c15876113`  
		Last Modified: Wed, 03 Aug 2022 23:07:57 GMT  
		Size: 54.7 MB (54720659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537d299c243ea0c73b05e8b607aa42ec071f847fbfa98d9ab5463a6594a04406`  
		Last Modified: Wed, 03 Aug 2022 23:07:46 GMT  
		Size: 283.1 KB (283112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d03bb1219b316469e8bd9f059ea35bbe07e5c60596349c1a2f46c2230f51e2`  
		Last Modified: Wed, 03 Aug 2022 23:08:02 GMT  
		Size: 64.7 MB (64743513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a494ed3d310625a6aa0f4889bc59e46085f1933560b3cf30b478de3be02dae6`  
		Last Modified: Wed, 03 Aug 2022 23:08:20 GMT  
		Size: 10.1 MB (10123573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3e6c59936fec78be28a82061db3e9537d38de8be5cc48b3206ab80d6d2b88e57
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.5 MB (422454040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e19c4cf364dd50aa1b03a9be7ab0b56d5590c1f90619f74a262d39596aede6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:03:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:03:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:03:39 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:03:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:03:41 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 15:05:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:05:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:05:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:05:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:06:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:06:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87c7d887e7b961ba6c9db72dd6419c5ac455dd43d49b194dbc43680f849a6ef`  
		Last Modified: Tue, 02 Aug 2022 15:38:49 GMT  
		Size: 839.8 KB (839769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51fe758bc1275edfa803da680fe43894a9e4bdb69d83153ccca2d60ba34bbee`  
		Last Modified: Tue, 02 Aug 2022 15:38:47 GMT  
		Size: 4.3 MB (4265854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9646eaa84fc50bf88a2bca0599491e795cf8122e6fe16671e23fd8b87804e823`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4ce991e1d0bf36ab7c0c7db9323c2cc620b0d96c88f26c619287aee7598666`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a101d7b97c7577b747e3cc14cb64c408587e6489c4b2420aad7fa1dbbd8fe189`  
		Last Modified: Tue, 02 Aug 2022 15:39:22 GMT  
		Size: 252.5 MB (252503681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c716f26c3c2a680d90778a974e99dc5d04bf9e4fbd9077cdb619b311ff4f0d24`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b66bed859b212ff9f65c306618bc607825b531e9a79843b4d75f5e870b3195`  
		Last Modified: Tue, 02 Aug 2022 15:39:42 GMT  
		Size: 63.1 MB (63088414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee909ec215bcdf8f5cd2e47e3aaf397ef01b2695fd292ea49920505e539f80c9`  
		Last Modified: Tue, 02 Aug 2022 15:39:34 GMT  
		Size: 283.1 KB (283086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884a1a0922cfe088904523812cfa7b3897bc3fc1b7eb0f266e99c75d92662a17`  
		Last Modified: Tue, 02 Aug 2022 15:39:44 GMT  
		Size: 67.0 MB (67000963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1236989f1fcde790f9d9aeda9bfc9ae97a4c7f11b790b4fb3cbd2e6872f13861`  
		Last Modified: Tue, 02 Aug 2022 15:40:05 GMT  
		Size: 10.7 MB (10735758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-robot-bionic`

```console
$ docker pull ros@sha256:211ce267b2b27c8a4e39d6aa6a487ede931aa06c314b6c416394637ce02209fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-robot-bionic` - linux; amd64

```console
$ docker pull ros@sha256:85bc4c3c605d67ba0ef9275c4750d9cf8af7bcb8a3b01be2a686cb56e570bd51
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.6 MB (448601669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8721d889104c51a26ed1d5208079740f172ba6c73512808b54b32fa72fc2397`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:55:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:20:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:20:06 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Sep 2022 04:20:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:20:07 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:20:07 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:20:07 GMT
ENV ROS_DISTRO=melodic
# Fri, 02 Sep 2022 04:22:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:22:43 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Sep 2022 04:22:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:22:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:23:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:23:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:24:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:25:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210c2da7b10ffa6d0e2b3a3af917a40d5b42b1606cf3aff1dbbd48b1da768dd2`  
		Last Modified: Fri, 02 Sep 2022 03:13:02 GMT  
		Size: 831.0 KB (830989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc21f3c6df3e09da41edf5cd277be198a0b9ce9de84590bce7c7f8169fe8458`  
		Last Modified: Fri, 02 Sep 2022 05:04:14 GMT  
		Size: 4.9 MB (4873660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c601897ffb3e3526f97b7f3ac57655aa3b636d8d501e997e89629b654dd7e8dc`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff02d512a7003472763130f30478d4f0c5e440cc42c6e111764af77b527686d5`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99a32123d45b8f75cdc98623e79fe3c15f9f2da76e2827622e844770c38afa4`  
		Last Modified: Fri, 02 Sep 2022 05:04:53 GMT  
		Size: 259.6 MB (259559627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abce6b68d4012a79d622c3088e409f52f46a4c2d57e7d45df885e9a566a052c`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a0804aad7d24aedc9674dd262573672ffb24e77bd0b94b38774dd4c1344a65`  
		Last Modified: Fri, 02 Sep 2022 05:05:12 GMT  
		Size: 70.3 MB (70259712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf4c705dfb136d0edfefa4b6ea486990b27430cb1acb7e7aa9c680225f5845c`  
		Last Modified: Fri, 02 Sep 2022 05:05:02 GMT  
		Size: 284.7 KB (284711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463d8179e60fd0676ccb9cded217236342e7d2d9185a56f2f003efb6d1e597bf`  
		Last Modified: Fri, 02 Sep 2022 05:05:14 GMT  
		Size: 75.0 MB (74995198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f95ccd28b67e6e24906599991ef70fb02811a4e3873615747bd8af8017f7bc`  
		Last Modified: Fri, 02 Sep 2022 05:05:28 GMT  
		Size: 11.1 MB (11085842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:7f4b7e824e2c2d884a5fb5a2c9b781342f4cf8aa705a8a43780f57b072fceb77
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.1 MB (396120708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d09ce3f49835d2c880946babd1f27d25bd83fed4169ab6f73ef3ed6972266945`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:40:36 GMT
ADD file:c5ca169f034f6be72446c95b43cd8cc6001848067793f102e7a2b970dd21db54 in / 
# Tue, 02 Aug 2022 01:40:37 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:38:47 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:39:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:39:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 03 Aug 2022 22:39:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 03 Aug 2022 22:39:35 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 22:39:35 GMT
ENV LC_ALL=C.UTF-8
# Wed, 03 Aug 2022 22:39:35 GMT
ENV ROS_DISTRO=melodic
# Wed, 03 Aug 2022 22:42:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:42:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 03 Aug 2022 22:42:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 03 Aug 2022 22:42:42 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:43:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:44:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 03 Aug 2022 22:46:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:47:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a03a1d54dcfd6ce7007bfa41c40b1747d5553db7ee3404e88dd3ddc54ede514e`  
		Last Modified: Tue, 02 Aug 2022 01:42:53 GMT  
		Size: 22.3 MB (22305613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad475a95b77752b25dc36bec810d7cc2000f86bc50ea57592b8f988605fc4c6`  
		Last Modified: Wed, 03 Aug 2022 23:06:53 GMT  
		Size: 840.0 KB (839977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d76a2f1b035d0df7e2f785a3199e9e86fdeeda1c9f6087f594f2d8a42f0cfb`  
		Last Modified: Wed, 03 Aug 2022 23:06:51 GMT  
		Size: 4.1 MB (4087975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acdc23d18c079581f3391d042b65fd7ae55d75333914fd8cdcd0b8acdd6bf10`  
		Last Modified: Wed, 03 Aug 2022 23:06:50 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3a86db6f1e409fa1d0b2018d788c0539b214c365337f886b86db7e860ee482`  
		Last Modified: Wed, 03 Aug 2022 23:06:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79c58cc0918adb02a33e27d7ad4e74c5e0463844a26e99fb60557c3594324b5`  
		Last Modified: Wed, 03 Aug 2022 23:07:34 GMT  
		Size: 239.0 MB (239014439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094e568816932729edf86ebafaaeb847af8bda6ade01fb926c6a121f6b825974`  
		Last Modified: Wed, 03 Aug 2022 23:06:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23d14b221e943bfa66059662f80e5ae90e6e1f053ed424ca6b2a40c15876113`  
		Last Modified: Wed, 03 Aug 2022 23:07:57 GMT  
		Size: 54.7 MB (54720659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537d299c243ea0c73b05e8b607aa42ec071f847fbfa98d9ab5463a6594a04406`  
		Last Modified: Wed, 03 Aug 2022 23:07:46 GMT  
		Size: 283.1 KB (283112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d03bb1219b316469e8bd9f059ea35bbe07e5c60596349c1a2f46c2230f51e2`  
		Last Modified: Wed, 03 Aug 2022 23:08:02 GMT  
		Size: 64.7 MB (64743513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a494ed3d310625a6aa0f4889bc59e46085f1933560b3cf30b478de3be02dae6`  
		Last Modified: Wed, 03 Aug 2022 23:08:20 GMT  
		Size: 10.1 MB (10123573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-robot-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:3e6c59936fec78be28a82061db3e9537d38de8be5cc48b3206ab80d6d2b88e57
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.5 MB (422454040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e19c4cf364dd50aa1b03a9be7ab0b56d5590c1f90619f74a262d39596aede6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:03:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:03:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:03:39 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:03:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:03:41 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 15:05:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:05:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:05:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:05:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:06:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:06:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-robot=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87c7d887e7b961ba6c9db72dd6419c5ac455dd43d49b194dbc43680f849a6ef`  
		Last Modified: Tue, 02 Aug 2022 15:38:49 GMT  
		Size: 839.8 KB (839769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51fe758bc1275edfa803da680fe43894a9e4bdb69d83153ccca2d60ba34bbee`  
		Last Modified: Tue, 02 Aug 2022 15:38:47 GMT  
		Size: 4.3 MB (4265854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9646eaa84fc50bf88a2bca0599491e795cf8122e6fe16671e23fd8b87804e823`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4ce991e1d0bf36ab7c0c7db9323c2cc620b0d96c88f26c619287aee7598666`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a101d7b97c7577b747e3cc14cb64c408587e6489c4b2420aad7fa1dbbd8fe189`  
		Last Modified: Tue, 02 Aug 2022 15:39:22 GMT  
		Size: 252.5 MB (252503681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c716f26c3c2a680d90778a974e99dc5d04bf9e4fbd9077cdb619b311ff4f0d24`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b66bed859b212ff9f65c306618bc607825b531e9a79843b4d75f5e870b3195`  
		Last Modified: Tue, 02 Aug 2022 15:39:42 GMT  
		Size: 63.1 MB (63088414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee909ec215bcdf8f5cd2e47e3aaf397ef01b2695fd292ea49920505e539f80c9`  
		Last Modified: Tue, 02 Aug 2022 15:39:34 GMT  
		Size: 283.1 KB (283086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884a1a0922cfe088904523812cfa7b3897bc3fc1b7eb0f266e99c75d92662a17`  
		Last Modified: Tue, 02 Aug 2022 15:39:44 GMT  
		Size: 67.0 MB (67000963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1236989f1fcde790f9d9aeda9bfc9ae97a4c7f11b790b4fb3cbd2e6872f13861`  
		Last Modified: Tue, 02 Aug 2022 15:40:05 GMT  
		Size: 10.7 MB (10735758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-base`

```console
$ docker pull ros@sha256:6c0132c71983bc37ad850ea316d7be3ba7fdcdf74c458d28428e0b2e37472b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:e894f44bf088cc62986b1aae33d8a8ec96810c746194983ce48d373f28c2eb60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.5 MB (437515827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e77b7e42944fc41a062c94ba1e54f9bc75737c6f1ee3293947939145ea10318`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:55:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:20:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:20:06 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Sep 2022 04:20:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:20:07 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:20:07 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:20:07 GMT
ENV ROS_DISTRO=melodic
# Fri, 02 Sep 2022 04:22:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:22:43 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Sep 2022 04:22:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:22:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:23:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:23:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:24:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210c2da7b10ffa6d0e2b3a3af917a40d5b42b1606cf3aff1dbbd48b1da768dd2`  
		Last Modified: Fri, 02 Sep 2022 03:13:02 GMT  
		Size: 831.0 KB (830989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc21f3c6df3e09da41edf5cd277be198a0b9ce9de84590bce7c7f8169fe8458`  
		Last Modified: Fri, 02 Sep 2022 05:04:14 GMT  
		Size: 4.9 MB (4873660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c601897ffb3e3526f97b7f3ac57655aa3b636d8d501e997e89629b654dd7e8dc`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff02d512a7003472763130f30478d4f0c5e440cc42c6e111764af77b527686d5`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99a32123d45b8f75cdc98623e79fe3c15f9f2da76e2827622e844770c38afa4`  
		Last Modified: Fri, 02 Sep 2022 05:04:53 GMT  
		Size: 259.6 MB (259559627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abce6b68d4012a79d622c3088e409f52f46a4c2d57e7d45df885e9a566a052c`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a0804aad7d24aedc9674dd262573672ffb24e77bd0b94b38774dd4c1344a65`  
		Last Modified: Fri, 02 Sep 2022 05:05:12 GMT  
		Size: 70.3 MB (70259712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf4c705dfb136d0edfefa4b6ea486990b27430cb1acb7e7aa9c680225f5845c`  
		Last Modified: Fri, 02 Sep 2022 05:05:02 GMT  
		Size: 284.7 KB (284711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463d8179e60fd0676ccb9cded217236342e7d2d9185a56f2f003efb6d1e597bf`  
		Last Modified: Fri, 02 Sep 2022 05:05:14 GMT  
		Size: 75.0 MB (74995198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:814af5012b36d9eed06c9cac7ad085d72ce7030a89e9b46d7c8f5c6d74d5bc25
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.0 MB (385997135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835e9afd0c76cb727206ffdc1e255cb66a4ad1f768b4a044f6316e2a544b93c0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:40:36 GMT
ADD file:c5ca169f034f6be72446c95b43cd8cc6001848067793f102e7a2b970dd21db54 in / 
# Tue, 02 Aug 2022 01:40:37 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:38:47 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:39:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:39:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 03 Aug 2022 22:39:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 03 Aug 2022 22:39:35 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 22:39:35 GMT
ENV LC_ALL=C.UTF-8
# Wed, 03 Aug 2022 22:39:35 GMT
ENV ROS_DISTRO=melodic
# Wed, 03 Aug 2022 22:42:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:42:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 03 Aug 2022 22:42:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 03 Aug 2022 22:42:42 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:43:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:44:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 03 Aug 2022 22:46:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a03a1d54dcfd6ce7007bfa41c40b1747d5553db7ee3404e88dd3ddc54ede514e`  
		Last Modified: Tue, 02 Aug 2022 01:42:53 GMT  
		Size: 22.3 MB (22305613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad475a95b77752b25dc36bec810d7cc2000f86bc50ea57592b8f988605fc4c6`  
		Last Modified: Wed, 03 Aug 2022 23:06:53 GMT  
		Size: 840.0 KB (839977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d76a2f1b035d0df7e2f785a3199e9e86fdeeda1c9f6087f594f2d8a42f0cfb`  
		Last Modified: Wed, 03 Aug 2022 23:06:51 GMT  
		Size: 4.1 MB (4087975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acdc23d18c079581f3391d042b65fd7ae55d75333914fd8cdcd0b8acdd6bf10`  
		Last Modified: Wed, 03 Aug 2022 23:06:50 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3a86db6f1e409fa1d0b2018d788c0539b214c365337f886b86db7e860ee482`  
		Last Modified: Wed, 03 Aug 2022 23:06:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79c58cc0918adb02a33e27d7ad4e74c5e0463844a26e99fb60557c3594324b5`  
		Last Modified: Wed, 03 Aug 2022 23:07:34 GMT  
		Size: 239.0 MB (239014439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094e568816932729edf86ebafaaeb847af8bda6ade01fb926c6a121f6b825974`  
		Last Modified: Wed, 03 Aug 2022 23:06:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23d14b221e943bfa66059662f80e5ae90e6e1f053ed424ca6b2a40c15876113`  
		Last Modified: Wed, 03 Aug 2022 23:07:57 GMT  
		Size: 54.7 MB (54720659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537d299c243ea0c73b05e8b607aa42ec071f847fbfa98d9ab5463a6594a04406`  
		Last Modified: Wed, 03 Aug 2022 23:07:46 GMT  
		Size: 283.1 KB (283112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d03bb1219b316469e8bd9f059ea35bbe07e5c60596349c1a2f46c2230f51e2`  
		Last Modified: Wed, 03 Aug 2022 23:08:02 GMT  
		Size: 64.7 MB (64743513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e19db181648b571c1a017e730f52145de920147e64052fa8662b7f611ac707db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.7 MB (411718282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56b623ecaac63fef2cd569acd1b109d44ce4a7318e7d3bda7b0c6d1e2ab1334`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:03:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:03:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:03:39 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:03:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:03:41 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 15:05:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:05:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:05:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:05:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:06:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87c7d887e7b961ba6c9db72dd6419c5ac455dd43d49b194dbc43680f849a6ef`  
		Last Modified: Tue, 02 Aug 2022 15:38:49 GMT  
		Size: 839.8 KB (839769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51fe758bc1275edfa803da680fe43894a9e4bdb69d83153ccca2d60ba34bbee`  
		Last Modified: Tue, 02 Aug 2022 15:38:47 GMT  
		Size: 4.3 MB (4265854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9646eaa84fc50bf88a2bca0599491e795cf8122e6fe16671e23fd8b87804e823`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4ce991e1d0bf36ab7c0c7db9323c2cc620b0d96c88f26c619287aee7598666`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a101d7b97c7577b747e3cc14cb64c408587e6489c4b2420aad7fa1dbbd8fe189`  
		Last Modified: Tue, 02 Aug 2022 15:39:22 GMT  
		Size: 252.5 MB (252503681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c716f26c3c2a680d90778a974e99dc5d04bf9e4fbd9077cdb619b311ff4f0d24`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b66bed859b212ff9f65c306618bc607825b531e9a79843b4d75f5e870b3195`  
		Last Modified: Tue, 02 Aug 2022 15:39:42 GMT  
		Size: 63.1 MB (63088414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee909ec215bcdf8f5cd2e47e3aaf397ef01b2695fd292ea49920505e539f80c9`  
		Last Modified: Tue, 02 Aug 2022 15:39:34 GMT  
		Size: 283.1 KB (283086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884a1a0922cfe088904523812cfa7b3897bc3fc1b7eb0f266e99c75d92662a17`  
		Last Modified: Tue, 02 Aug 2022 15:39:44 GMT  
		Size: 67.0 MB (67000963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-base-bionic`

```console
$ docker pull ros@sha256:6c0132c71983bc37ad850ea316d7be3ba7fdcdf74c458d28428e0b2e37472b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-base-bionic` - linux; amd64

```console
$ docker pull ros@sha256:e894f44bf088cc62986b1aae33d8a8ec96810c746194983ce48d373f28c2eb60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.5 MB (437515827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e77b7e42944fc41a062c94ba1e54f9bc75737c6f1ee3293947939145ea10318`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:55:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:20:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:20:06 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Sep 2022 04:20:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:20:07 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:20:07 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:20:07 GMT
ENV ROS_DISTRO=melodic
# Fri, 02 Sep 2022 04:22:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:22:43 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Sep 2022 04:22:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:22:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:23:25 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:23:32 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:24:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210c2da7b10ffa6d0e2b3a3af917a40d5b42b1606cf3aff1dbbd48b1da768dd2`  
		Last Modified: Fri, 02 Sep 2022 03:13:02 GMT  
		Size: 831.0 KB (830989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc21f3c6df3e09da41edf5cd277be198a0b9ce9de84590bce7c7f8169fe8458`  
		Last Modified: Fri, 02 Sep 2022 05:04:14 GMT  
		Size: 4.9 MB (4873660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c601897ffb3e3526f97b7f3ac57655aa3b636d8d501e997e89629b654dd7e8dc`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff02d512a7003472763130f30478d4f0c5e440cc42c6e111764af77b527686d5`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99a32123d45b8f75cdc98623e79fe3c15f9f2da76e2827622e844770c38afa4`  
		Last Modified: Fri, 02 Sep 2022 05:04:53 GMT  
		Size: 259.6 MB (259559627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abce6b68d4012a79d622c3088e409f52f46a4c2d57e7d45df885e9a566a052c`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a0804aad7d24aedc9674dd262573672ffb24e77bd0b94b38774dd4c1344a65`  
		Last Modified: Fri, 02 Sep 2022 05:05:12 GMT  
		Size: 70.3 MB (70259712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf4c705dfb136d0edfefa4b6ea486990b27430cb1acb7e7aa9c680225f5845c`  
		Last Modified: Fri, 02 Sep 2022 05:05:02 GMT  
		Size: 284.7 KB (284711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463d8179e60fd0676ccb9cded217236342e7d2d9185a56f2f003efb6d1e597bf`  
		Last Modified: Fri, 02 Sep 2022 05:05:14 GMT  
		Size: 75.0 MB (74995198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:814af5012b36d9eed06c9cac7ad085d72ce7030a89e9b46d7c8f5c6d74d5bc25
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.0 MB (385997135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835e9afd0c76cb727206ffdc1e255cb66a4ad1f768b4a044f6316e2a544b93c0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:40:36 GMT
ADD file:c5ca169f034f6be72446c95b43cd8cc6001848067793f102e7a2b970dd21db54 in / 
# Tue, 02 Aug 2022 01:40:37 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:38:47 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:39:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:39:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 03 Aug 2022 22:39:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 03 Aug 2022 22:39:35 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 22:39:35 GMT
ENV LC_ALL=C.UTF-8
# Wed, 03 Aug 2022 22:39:35 GMT
ENV ROS_DISTRO=melodic
# Wed, 03 Aug 2022 22:42:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:42:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 03 Aug 2022 22:42:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 03 Aug 2022 22:42:42 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:43:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:44:00 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 03 Aug 2022 22:46:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a03a1d54dcfd6ce7007bfa41c40b1747d5553db7ee3404e88dd3ddc54ede514e`  
		Last Modified: Tue, 02 Aug 2022 01:42:53 GMT  
		Size: 22.3 MB (22305613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad475a95b77752b25dc36bec810d7cc2000f86bc50ea57592b8f988605fc4c6`  
		Last Modified: Wed, 03 Aug 2022 23:06:53 GMT  
		Size: 840.0 KB (839977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d76a2f1b035d0df7e2f785a3199e9e86fdeeda1c9f6087f594f2d8a42f0cfb`  
		Last Modified: Wed, 03 Aug 2022 23:06:51 GMT  
		Size: 4.1 MB (4087975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acdc23d18c079581f3391d042b65fd7ae55d75333914fd8cdcd0b8acdd6bf10`  
		Last Modified: Wed, 03 Aug 2022 23:06:50 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3a86db6f1e409fa1d0b2018d788c0539b214c365337f886b86db7e860ee482`  
		Last Modified: Wed, 03 Aug 2022 23:06:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79c58cc0918adb02a33e27d7ad4e74c5e0463844a26e99fb60557c3594324b5`  
		Last Modified: Wed, 03 Aug 2022 23:07:34 GMT  
		Size: 239.0 MB (239014439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094e568816932729edf86ebafaaeb847af8bda6ade01fb926c6a121f6b825974`  
		Last Modified: Wed, 03 Aug 2022 23:06:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23d14b221e943bfa66059662f80e5ae90e6e1f053ed424ca6b2a40c15876113`  
		Last Modified: Wed, 03 Aug 2022 23:07:57 GMT  
		Size: 54.7 MB (54720659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537d299c243ea0c73b05e8b607aa42ec071f847fbfa98d9ab5463a6594a04406`  
		Last Modified: Wed, 03 Aug 2022 23:07:46 GMT  
		Size: 283.1 KB (283112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d03bb1219b316469e8bd9f059ea35bbe07e5c60596349c1a2f46c2230f51e2`  
		Last Modified: Wed, 03 Aug 2022 23:08:02 GMT  
		Size: 64.7 MB (64743513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-base-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e19db181648b571c1a017e730f52145de920147e64052fa8662b7f611ac707db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.7 MB (411718282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56b623ecaac63fef2cd569acd1b109d44ce4a7318e7d3bda7b0c6d1e2ab1334`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:03:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:03:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:03:39 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:03:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:03:41 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 15:05:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:05:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:05:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:05:33 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:40 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:06:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-base=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87c7d887e7b961ba6c9db72dd6419c5ac455dd43d49b194dbc43680f849a6ef`  
		Last Modified: Tue, 02 Aug 2022 15:38:49 GMT  
		Size: 839.8 KB (839769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51fe758bc1275edfa803da680fe43894a9e4bdb69d83153ccca2d60ba34bbee`  
		Last Modified: Tue, 02 Aug 2022 15:38:47 GMT  
		Size: 4.3 MB (4265854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9646eaa84fc50bf88a2bca0599491e795cf8122e6fe16671e23fd8b87804e823`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4ce991e1d0bf36ab7c0c7db9323c2cc620b0d96c88f26c619287aee7598666`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a101d7b97c7577b747e3cc14cb64c408587e6489c4b2420aad7fa1dbbd8fe189`  
		Last Modified: Tue, 02 Aug 2022 15:39:22 GMT  
		Size: 252.5 MB (252503681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c716f26c3c2a680d90778a974e99dc5d04bf9e4fbd9077cdb619b311ff4f0d24`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b66bed859b212ff9f65c306618bc607825b531e9a79843b4d75f5e870b3195`  
		Last Modified: Tue, 02 Aug 2022 15:39:42 GMT  
		Size: 63.1 MB (63088414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee909ec215bcdf8f5cd2e47e3aaf397ef01b2695fd292ea49920505e539f80c9`  
		Last Modified: Tue, 02 Aug 2022 15:39:34 GMT  
		Size: 283.1 KB (283086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884a1a0922cfe088904523812cfa7b3897bc3fc1b7eb0f266e99c75d92662a17`  
		Last Modified: Tue, 02 Aug 2022 15:39:44 GMT  
		Size: 67.0 MB (67000963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-core`

```console
$ docker pull ros@sha256:f2cca8f42679f9951e48bb7cdf10367f5fc84004d43aacaf204c50dd24767902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:9b669165378423e81a191798b5e52aa75e944399105596a518f4b552cd63afbb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (291976206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379814066976db125a7e5d64cfcda1c2e9f57f003358ac3442eb1e117bae9d7a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:55:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:20:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:20:06 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Sep 2022 04:20:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:20:07 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:20:07 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:20:07 GMT
ENV ROS_DISTRO=melodic
# Fri, 02 Sep 2022 04:22:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:22:43 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Sep 2022 04:22:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:22:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210c2da7b10ffa6d0e2b3a3af917a40d5b42b1606cf3aff1dbbd48b1da768dd2`  
		Last Modified: Fri, 02 Sep 2022 03:13:02 GMT  
		Size: 831.0 KB (830989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc21f3c6df3e09da41edf5cd277be198a0b9ce9de84590bce7c7f8169fe8458`  
		Last Modified: Fri, 02 Sep 2022 05:04:14 GMT  
		Size: 4.9 MB (4873660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c601897ffb3e3526f97b7f3ac57655aa3b636d8d501e997e89629b654dd7e8dc`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff02d512a7003472763130f30478d4f0c5e440cc42c6e111764af77b527686d5`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99a32123d45b8f75cdc98623e79fe3c15f9f2da76e2827622e844770c38afa4`  
		Last Modified: Fri, 02 Sep 2022 05:04:53 GMT  
		Size: 259.6 MB (259559627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abce6b68d4012a79d622c3088e409f52f46a4c2d57e7d45df885e9a566a052c`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:517a5cd34d4f76ea5bd0e123281d4ebaf06483d151b29d5852bcf1199d1462e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266249851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3807b97ce7468b1b2aedbfc07777530bf31cb68749123cd0ee0cf10c2c4f1ae6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:40:36 GMT
ADD file:c5ca169f034f6be72446c95b43cd8cc6001848067793f102e7a2b970dd21db54 in / 
# Tue, 02 Aug 2022 01:40:37 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:38:47 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:39:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:39:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 03 Aug 2022 22:39:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 03 Aug 2022 22:39:35 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 22:39:35 GMT
ENV LC_ALL=C.UTF-8
# Wed, 03 Aug 2022 22:39:35 GMT
ENV ROS_DISTRO=melodic
# Wed, 03 Aug 2022 22:42:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:42:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 03 Aug 2022 22:42:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 03 Aug 2022 22:42:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a03a1d54dcfd6ce7007bfa41c40b1747d5553db7ee3404e88dd3ddc54ede514e`  
		Last Modified: Tue, 02 Aug 2022 01:42:53 GMT  
		Size: 22.3 MB (22305613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad475a95b77752b25dc36bec810d7cc2000f86bc50ea57592b8f988605fc4c6`  
		Last Modified: Wed, 03 Aug 2022 23:06:53 GMT  
		Size: 840.0 KB (839977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d76a2f1b035d0df7e2f785a3199e9e86fdeeda1c9f6087f594f2d8a42f0cfb`  
		Last Modified: Wed, 03 Aug 2022 23:06:51 GMT  
		Size: 4.1 MB (4087975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acdc23d18c079581f3391d042b65fd7ae55d75333914fd8cdcd0b8acdd6bf10`  
		Last Modified: Wed, 03 Aug 2022 23:06:50 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3a86db6f1e409fa1d0b2018d788c0539b214c365337f886b86db7e860ee482`  
		Last Modified: Wed, 03 Aug 2022 23:06:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79c58cc0918adb02a33e27d7ad4e74c5e0463844a26e99fb60557c3594324b5`  
		Last Modified: Wed, 03 Aug 2022 23:07:34 GMT  
		Size: 239.0 MB (239014439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094e568816932729edf86ebafaaeb847af8bda6ade01fb926c6a121f6b825974`  
		Last Modified: Wed, 03 Aug 2022 23:06:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a3c706160ea294c6d504493c8788aba76ccfc4301d5a8ac1a7d89fe87c5cdeea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281345819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd9332cdc364c841103f5a91024056914be62095a4f80226a0efda07ffc73da`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:03:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:03:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:03:39 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:03:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:03:41 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 15:05:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:05:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:05:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87c7d887e7b961ba6c9db72dd6419c5ac455dd43d49b194dbc43680f849a6ef`  
		Last Modified: Tue, 02 Aug 2022 15:38:49 GMT  
		Size: 839.8 KB (839769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51fe758bc1275edfa803da680fe43894a9e4bdb69d83153ccca2d60ba34bbee`  
		Last Modified: Tue, 02 Aug 2022 15:38:47 GMT  
		Size: 4.3 MB (4265854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9646eaa84fc50bf88a2bca0599491e795cf8122e6fe16671e23fd8b87804e823`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4ce991e1d0bf36ab7c0c7db9323c2cc620b0d96c88f26c619287aee7598666`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a101d7b97c7577b747e3cc14cb64c408587e6489c4b2420aad7fa1dbbd8fe189`  
		Last Modified: Tue, 02 Aug 2022 15:39:22 GMT  
		Size: 252.5 MB (252503681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c716f26c3c2a680d90778a974e99dc5d04bf9e4fbd9077cdb619b311ff4f0d24`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:melodic-ros-core-bionic`

```console
$ docker pull ros@sha256:f2cca8f42679f9951e48bb7cdf10367f5fc84004d43aacaf204c50dd24767902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:melodic-ros-core-bionic` - linux; amd64

```console
$ docker pull ros@sha256:9b669165378423e81a191798b5e52aa75e944399105596a518f4b552cd63afbb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.0 MB (291976206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379814066976db125a7e5d64cfcda1c2e9f57f003358ac3442eb1e117bae9d7a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:18 GMT
ADD file:8b379a8fd96e76d10db6f9ae4e9675de33d227db0431ca2a7ca799119e905e8f in / 
# Thu, 01 Sep 2022 23:46:18 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:55:19 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:20:05 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:20:06 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Sep 2022 04:20:07 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:20:07 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:20:07 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:20:07 GMT
ENV ROS_DISTRO=melodic
# Fri, 02 Sep 2022 04:22:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:22:43 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Sep 2022 04:22:43 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:22:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:dad0f37c70a668d101c86b5c769d452ff29c6d51f811891384cc7da00fce192f`  
		Last Modified: Wed, 31 Aug 2022 06:57:55 GMT  
		Size: 26.7 MB (26710085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210c2da7b10ffa6d0e2b3a3af917a40d5b42b1606cf3aff1dbbd48b1da768dd2`  
		Last Modified: Fri, 02 Sep 2022 03:13:02 GMT  
		Size: 831.0 KB (830989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc21f3c6df3e09da41edf5cd277be198a0b9ce9de84590bce7c7f8169fe8458`  
		Last Modified: Fri, 02 Sep 2022 05:04:14 GMT  
		Size: 4.9 MB (4873660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c601897ffb3e3526f97b7f3ac57655aa3b636d8d501e997e89629b654dd7e8dc`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff02d512a7003472763130f30478d4f0c5e440cc42c6e111764af77b527686d5`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f99a32123d45b8f75cdc98623e79fe3c15f9f2da76e2827622e844770c38afa4`  
		Last Modified: Fri, 02 Sep 2022 05:04:53 GMT  
		Size: 259.6 MB (259559627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abce6b68d4012a79d622c3088e409f52f46a4c2d57e7d45df885e9a566a052c`  
		Last Modified: Fri, 02 Sep 2022 05:04:13 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-bionic` - linux; arm variant v7

```console
$ docker pull ros@sha256:517a5cd34d4f76ea5bd0e123281d4ebaf06483d151b29d5852bcf1199d1462e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266249851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3807b97ce7468b1b2aedbfc07777530bf31cb68749123cd0ee0cf10c2c4f1ae6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:40:36 GMT
ADD file:c5ca169f034f6be72446c95b43cd8cc6001848067793f102e7a2b970dd21db54 in / 
# Tue, 02 Aug 2022 01:40:37 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:38:47 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:39:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:39:33 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 03 Aug 2022 22:39:34 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 03 Aug 2022 22:39:35 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 22:39:35 GMT
ENV LC_ALL=C.UTF-8
# Wed, 03 Aug 2022 22:39:35 GMT
ENV ROS_DISTRO=melodic
# Wed, 03 Aug 2022 22:42:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:42:42 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 03 Aug 2022 22:42:42 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 03 Aug 2022 22:42:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a03a1d54dcfd6ce7007bfa41c40b1747d5553db7ee3404e88dd3ddc54ede514e`  
		Last Modified: Tue, 02 Aug 2022 01:42:53 GMT  
		Size: 22.3 MB (22305613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad475a95b77752b25dc36bec810d7cc2000f86bc50ea57592b8f988605fc4c6`  
		Last Modified: Wed, 03 Aug 2022 23:06:53 GMT  
		Size: 840.0 KB (839977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d76a2f1b035d0df7e2f785a3199e9e86fdeeda1c9f6087f594f2d8a42f0cfb`  
		Last Modified: Wed, 03 Aug 2022 23:06:51 GMT  
		Size: 4.1 MB (4087975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acdc23d18c079581f3391d042b65fd7ae55d75333914fd8cdcd0b8acdd6bf10`  
		Last Modified: Wed, 03 Aug 2022 23:06:50 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3a86db6f1e409fa1d0b2018d788c0539b214c365337f886b86db7e860ee482`  
		Last Modified: Wed, 03 Aug 2022 23:06:51 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79c58cc0918adb02a33e27d7ad4e74c5e0463844a26e99fb60557c3594324b5`  
		Last Modified: Wed, 03 Aug 2022 23:07:34 GMT  
		Size: 239.0 MB (239014439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094e568816932729edf86ebafaaeb847af8bda6ade01fb926c6a121f6b825974`  
		Last Modified: Wed, 03 Aug 2022 23:06:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:melodic-ros-core-bionic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:a3c706160ea294c6d504493c8788aba76ccfc4301d5a8ac1a7d89fe87c5cdeea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281345819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd9332cdc364c841103f5a91024056914be62095a4f80226a0efda07ffc73da`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:43 GMT
ADD file:7002810c3cfdef12d2e13c49037e759257e42f5972f300411294e0239f3bdfe9 in / 
# Tue, 02 Aug 2022 01:18:44 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:03:25 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:35 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:03:36 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:03:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:03:39 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:03:40 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:03:41 GMT
ENV ROS_DISTRO=melodic
# Tue, 02 Aug 2022 15:05:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-melodic-ros-core=1.4.1-0*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:05:05 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:05:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:05:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d2f2687beb6dd5f04849c57d6d83cabdfa44ec5cc5062369416bff4844045533`  
		Last Modified: Tue, 02 Aug 2022 01:20:09 GMT  
		Size: 23.7 MB (23734714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87c7d887e7b961ba6c9db72dd6419c5ac455dd43d49b194dbc43680f849a6ef`  
		Last Modified: Tue, 02 Aug 2022 15:38:49 GMT  
		Size: 839.8 KB (839769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51fe758bc1275edfa803da680fe43894a9e4bdb69d83153ccca2d60ba34bbee`  
		Last Modified: Tue, 02 Aug 2022 15:38:47 GMT  
		Size: 4.3 MB (4265854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9646eaa84fc50bf88a2bca0599491e795cf8122e6fe16671e23fd8b87804e823`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4ce991e1d0bf36ab7c0c7db9323c2cc620b0d96c88f26c619287aee7598666`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a101d7b97c7577b747e3cc14cb64c408587e6489c4b2420aad7fa1dbbd8fe189`  
		Last Modified: Tue, 02 Aug 2022 15:39:22 GMT  
		Size: 252.5 MB (252503681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c716f26c3c2a680d90778a974e99dc5d04bf9e4fbd9077cdb619b311ff4f0d24`  
		Last Modified: Tue, 02 Aug 2022 15:38:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic`

```console
$ docker pull ros@sha256:60f7aaee609f26cc98bea2cfd9fc4ed5c3adda68b49303e02bbf00755f383fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic` - linux; amd64

```console
$ docker pull ros@sha256:a3668b236d93abbfedcf72a51abc193842193459fdb8aac6b642ed95441a6cbc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343151353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b356ccf86aa9679666fabf6c6ce440b45f40baf7f272adee0eca54f31d4d6b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:03:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:45 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Sep 2022 04:30:46 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:30:46 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:30:46 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:30:47 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Sep 2022 04:32:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:32:46 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Sep 2022 04:32:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:32:46 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:33:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:33:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:34:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf19bc0e0d1d8bf1ec9b593eb3ddedecefdf4aff5f519ad585667a258956af1`  
		Last Modified: Fri, 02 Sep 2022 03:15:37 GMT  
		Size: 1.2 MB (1163757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff483ca449e233e69f18eb71e430f67ec1b4c8f5a965b4d7efc759a0ba2f18c4`  
		Last Modified: Fri, 02 Sep 2022 05:06:36 GMT  
		Size: 5.5 MB (5546993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e933af47665655d97d902ecb6d264063a041b2c12dfcbaf849a05672cafc9044`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1916d550484243d392ddc6fdca4ba34710bd3305a578bf9d241f2ad6d944c099`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d152bd7bb3b1335dd05a53828858de8ceab15c85e96fdc0181b2e38f72323b8`  
		Last Modified: Fri, 02 Sep 2022 05:07:05 GMT  
		Size: 177.0 MB (176996015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edc8aa6732f94d22820aa0f96400c620b51e015fa6a940c03e9b579f0de306f`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b38aa1dd8b74095a973aa1b1fe9d7495fcbf895f954b66adbff905119d10103`  
		Last Modified: Fri, 02 Sep 2022 05:07:22 GMT  
		Size: 50.9 MB (50940098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5cec93c265dc40fb6eb4790e71c25ac877e2addb6eddf96377e4336554651e`  
		Last Modified: Fri, 02 Sep 2022 05:07:14 GMT  
		Size: 325.7 KB (325719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca383d78ab41bd8631ac0ef8afce8de1b461c6b95a74094926636a7d8ff9c57`  
		Last Modified: Fri, 02 Sep 2022 05:07:26 GMT  
		Size: 79.6 MB (79603671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm variant v7

```console
$ docker pull ros@sha256:dc89df4c67ffb8e35dcb232a71956399e39b3575cfa1e8389e74e1d5a0782638
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289240180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5a83264b759495b4caae5a5c49c6f2dbf31890cf1b28ffedbd7d55f94c0279`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:40:45 GMT
ADD file:7de7e2c2eb5b05b2449f1e73da223081e27d073990c979ec73afd1893c58c551 in / 
# Tue, 02 Aug 2022 01:40:45 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:53:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:53:45 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:53:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 03 Aug 2022 22:53:47 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 03 Aug 2022 22:53:47 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 22:53:47 GMT
ENV LC_ALL=C.UTF-8
# Wed, 03 Aug 2022 22:53:47 GMT
ENV ROS_DISTRO=noetic
# Wed, 03 Aug 2022 22:55:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:55:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 03 Aug 2022 22:55:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 03 Aug 2022 22:55:11 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:56:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:56:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 03 Aug 2022 22:57:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:de6f11ffeeef9e471776e52baf8cc454a1249e8caf2d8944a5b0387143608310`  
		Last Modified: Tue, 02 Aug 2022 01:43:13 GMT  
		Size: 24.6 MB (24589273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d345e3aeca1c4dd8930e961af9d46712aa474a7ce53acba4f54b4ff3b113a84`  
		Last Modified: Wed, 03 Aug 2022 23:09:30 GMT  
		Size: 1.2 MB (1181992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cf40d14b8b7f81b4f192b1708fbdb0a57c3626f5b72be630a041c1f634f266`  
		Last Modified: Wed, 03 Aug 2022 23:09:28 GMT  
		Size: 4.7 MB (4676289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3223d85d87ee35ea3ab4535feef031631e281f3c617de4cdc218c4983c9b6f`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5bf7f51f5d7e24eec5395780a42aebd0c726cb0466dd5e0b2c492c6d0c84b3`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c66f511399e2f2993ed8fd014bb457c6d6a9483ae665aea0e9eb01fb0a54b4`  
		Last Modified: Wed, 03 Aug 2022 23:10:06 GMT  
		Size: 157.5 MB (157479986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa138f7b3214bda7dc2ae9534dff610b8c2a41d8de8dfb7c8a69ab5eba596887`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e956f29112fb883f35fde1c1d67fc064ab659310ef5bc2f894fd7fabc7cb1b53`  
		Last Modified: Wed, 03 Aug 2022 23:10:25 GMT  
		Size: 40.5 MB (40505939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b4fa88c4ff97cf49d78a40c699333d1182e8a7a0cdb62a65b76e6d6ba39208`  
		Last Modified: Wed, 03 Aug 2022 23:10:18 GMT  
		Size: 323.5 KB (323517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0f054c04c983a4aa345e62e3a2df78c234e061aab4b29b964612f3ff52473c`  
		Last Modified: Wed, 03 Aug 2022 23:10:30 GMT  
		Size: 60.5 MB (60480770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8d2c3160385c2f5a6449fff4905f7290543a28713ffc6e1550747d5e0dcdb0ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322192151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108358074c3289edba33e14e8130004770bde5dd9106d446db28dd2548498a48`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:09:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:09:06 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:09:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:09:08 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 15:10:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:06 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:10:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:10:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:10:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:11:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c7d1bf2cea5d6a7f0ef5ba787e95aa344e3e67e349bbdcaedd088b0732e48e`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ac26fe78d80a057263cfc59c64582efef7caaa111eb4b639861056cf0df95`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f493394889994de604dd62e022d4827365c0de34ad6cac870ea6af5dca4bba40`  
		Last Modified: Tue, 02 Aug 2022 15:41:50 GMT  
		Size: 171.4 MB (171424725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c191fa5a5fa889fff525b13caa35fb805e0bac7c673aebce455ffc8876fce9`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9227bd4aa30a597598fbc456d5aa784c527937a1f88d2ad2787b48b0ad396d6`  
		Last Modified: Tue, 02 Aug 2022 15:42:10 GMT  
		Size: 45.0 MB (44988903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80df4890a016b37679e242280f4c5981f02725f7e081609daba03d47c99cb3ab`  
		Last Modified: Tue, 02 Aug 2022 15:42:03 GMT  
		Size: 323.5 KB (323472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9700876cb7bd2a4af8a21af304524eafef9645266e38f92be7594dbf40519b67`  
		Last Modified: Tue, 02 Aug 2022 15:42:13 GMT  
		Size: 71.8 MB (71754502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception`

```console
$ docker pull ros@sha256:7b840893b4139564fc29fbda07d59fe1ae32bdec7da6d1e97606925abd3d3d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception` - linux; amd64

```console
$ docker pull ros@sha256:92a9a61a2bbca7538207c06e045a7a5e686090a54831516ffa488a491aa1c4ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.1 MB (835120913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536572ffb5a95c08ca27649d9209f61d60a1f36a15acdb55bfb3efe0650d171d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:03:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:45 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Sep 2022 04:30:46 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:30:46 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:30:46 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:30:47 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Sep 2022 04:32:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:32:46 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Sep 2022 04:32:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:32:46 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:33:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:33:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:34:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:41:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf19bc0e0d1d8bf1ec9b593eb3ddedecefdf4aff5f519ad585667a258956af1`  
		Last Modified: Fri, 02 Sep 2022 03:15:37 GMT  
		Size: 1.2 MB (1163757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff483ca449e233e69f18eb71e430f67ec1b4c8f5a965b4d7efc759a0ba2f18c4`  
		Last Modified: Fri, 02 Sep 2022 05:06:36 GMT  
		Size: 5.5 MB (5546993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e933af47665655d97d902ecb6d264063a041b2c12dfcbaf849a05672cafc9044`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1916d550484243d392ddc6fdca4ba34710bd3305a578bf9d241f2ad6d944c099`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d152bd7bb3b1335dd05a53828858de8ceab15c85e96fdc0181b2e38f72323b8`  
		Last Modified: Fri, 02 Sep 2022 05:07:05 GMT  
		Size: 177.0 MB (176996015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edc8aa6732f94d22820aa0f96400c620b51e015fa6a940c03e9b579f0de306f`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b38aa1dd8b74095a973aa1b1fe9d7495fcbf895f954b66adbff905119d10103`  
		Last Modified: Fri, 02 Sep 2022 05:07:22 GMT  
		Size: 50.9 MB (50940098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5cec93c265dc40fb6eb4790e71c25ac877e2addb6eddf96377e4336554651e`  
		Last Modified: Fri, 02 Sep 2022 05:07:14 GMT  
		Size: 325.7 KB (325719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca383d78ab41bd8631ac0ef8afce8de1b461c6b95a74094926636a7d8ff9c57`  
		Last Modified: Fri, 02 Sep 2022 05:07:26 GMT  
		Size: 79.6 MB (79603671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec642114a0fb290bf0ad8660843fcd6f3653247c1aedf51d36e3b9afa30a2a4`  
		Last Modified: Fri, 02 Sep 2022 05:09:04 GMT  
		Size: 492.0 MB (491969560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm variant v7

```console
$ docker pull ros@sha256:1ecaf8e232748957ac86a63221733c7593239f1c1f6e1f806933b288509f4c99
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726125169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea4e067cd70525d9e125993cb33ef7c1d7b685b94254c7e68f9bd1e3f34d89f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:40:45 GMT
ADD file:7de7e2c2eb5b05b2449f1e73da223081e27d073990c979ec73afd1893c58c551 in / 
# Tue, 02 Aug 2022 01:40:45 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:53:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:53:45 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:53:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 03 Aug 2022 22:53:47 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 03 Aug 2022 22:53:47 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 22:53:47 GMT
ENV LC_ALL=C.UTF-8
# Wed, 03 Aug 2022 22:53:47 GMT
ENV ROS_DISTRO=noetic
# Wed, 03 Aug 2022 22:55:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:55:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 03 Aug 2022 22:55:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 03 Aug 2022 22:55:11 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:56:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:56:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 03 Aug 2022 22:57:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 23:05:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:de6f11ffeeef9e471776e52baf8cc454a1249e8caf2d8944a5b0387143608310`  
		Last Modified: Tue, 02 Aug 2022 01:43:13 GMT  
		Size: 24.6 MB (24589273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d345e3aeca1c4dd8930e961af9d46712aa474a7ce53acba4f54b4ff3b113a84`  
		Last Modified: Wed, 03 Aug 2022 23:09:30 GMT  
		Size: 1.2 MB (1181992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cf40d14b8b7f81b4f192b1708fbdb0a57c3626f5b72be630a041c1f634f266`  
		Last Modified: Wed, 03 Aug 2022 23:09:28 GMT  
		Size: 4.7 MB (4676289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3223d85d87ee35ea3ab4535feef031631e281f3c617de4cdc218c4983c9b6f`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5bf7f51f5d7e24eec5395780a42aebd0c726cb0466dd5e0b2c492c6d0c84b3`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c66f511399e2f2993ed8fd014bb457c6d6a9483ae665aea0e9eb01fb0a54b4`  
		Last Modified: Wed, 03 Aug 2022 23:10:06 GMT  
		Size: 157.5 MB (157479986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa138f7b3214bda7dc2ae9534dff610b8c2a41d8de8dfb7c8a69ab5eba596887`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e956f29112fb883f35fde1c1d67fc064ab659310ef5bc2f894fd7fabc7cb1b53`  
		Last Modified: Wed, 03 Aug 2022 23:10:25 GMT  
		Size: 40.5 MB (40505939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b4fa88c4ff97cf49d78a40c699333d1182e8a7a0cdb62a65b76e6d6ba39208`  
		Last Modified: Wed, 03 Aug 2022 23:10:18 GMT  
		Size: 323.5 KB (323517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0f054c04c983a4aa345e62e3a2df78c234e061aab4b29b964612f3ff52473c`  
		Last Modified: Wed, 03 Aug 2022 23:10:30 GMT  
		Size: 60.5 MB (60480770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802d1642a23d0013e97d3851823d3d1d2bb88f1ffa90be40d87e65a988ea2a9a`  
		Last Modified: Wed, 03 Aug 2022 23:12:10 GMT  
		Size: 436.9 MB (436884989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0a06825f28b50c090d1b79874eddcb235ab8977dc3f26205d86f96307e14fbaf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **784.7 MB (784729415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73229aac1c29ad65732bf715e6cefa795fbbe38f93ce6348d12ae7e77d182811`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:09:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:09:06 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:09:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:09:08 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 15:10:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:06 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:10:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:10:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:10:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:11:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:13:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c7d1bf2cea5d6a7f0ef5ba787e95aa344e3e67e349bbdcaedd088b0732e48e`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ac26fe78d80a057263cfc59c64582efef7caaa111eb4b639861056cf0df95`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f493394889994de604dd62e022d4827365c0de34ad6cac870ea6af5dca4bba40`  
		Last Modified: Tue, 02 Aug 2022 15:41:50 GMT  
		Size: 171.4 MB (171424725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c191fa5a5fa889fff525b13caa35fb805e0bac7c673aebce455ffc8876fce9`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9227bd4aa30a597598fbc456d5aa784c527937a1f88d2ad2787b48b0ad396d6`  
		Last Modified: Tue, 02 Aug 2022 15:42:10 GMT  
		Size: 45.0 MB (44988903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80df4890a016b37679e242280f4c5981f02725f7e081609daba03d47c99cb3ab`  
		Last Modified: Tue, 02 Aug 2022 15:42:03 GMT  
		Size: 323.5 KB (323472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9700876cb7bd2a4af8a21af304524eafef9645266e38f92be7594dbf40519b67`  
		Last Modified: Tue, 02 Aug 2022 15:42:13 GMT  
		Size: 71.8 MB (71754502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3ba7b86422cfbb851f49e5b6c651bbc5d3d24e15ac8200fa9c8341a38b6ff3`  
		Last Modified: Tue, 02 Aug 2022 15:43:50 GMT  
		Size: 462.5 MB (462537264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception-buster`

```console
$ docker pull ros@sha256:afd8ccf1909bb6cface65b28097fb1099c41d2543775444a5635f0ce4a51a4c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-perception-buster` - linux; amd64

```console
$ docker pull ros@sha256:97cbd624fa29bbb7b96ff26b8a56d64177ad5f70daac01c05374b03b3ad5f58f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **951.4 MB (951401294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9934f52c622a20cac28951203d192a341dc6bf5ca1390702b2c22c818448c29c`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 00:21:00 GMT
ADD file:d420ffdf63082e03517284553796e5a100e425201458860f07b1aa8598c5929a in / 
# Tue, 23 Aug 2022 00:21:00 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 11:10:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:10:43 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 23 Aug 2022 11:10:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 23 Aug 2022 11:10:45 GMT
ENV LANG=C.UTF-8
# Tue, 23 Aug 2022 11:10:45 GMT
ENV LC_ALL=C.UTF-8
# Tue, 23 Aug 2022 11:10:45 GMT
ENV ROS_DISTRO=noetic
# Tue, 23 Aug 2022 11:11:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:11:49 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 23 Aug 2022 11:11:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 23 Aug 2022 11:11:49 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 11:12:18 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:12:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 23 Aug 2022 11:12:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:15:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:76dff75df4d9dbdf29a4459adaec745740bfb476cd915906e33eddd9cd94db93`  
		Last Modified: Tue, 23 Aug 2022 00:25:20 GMT  
		Size: 50.4 MB (50440273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd91dd5198cc577c5556c7c5c335e0ea5701168d8c2ded40b83bc24be1434e47`  
		Last Modified: Tue, 23 Aug 2022 11:17:01 GMT  
		Size: 10.9 MB (10893537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385a586942561cc66fbd30195e87e96f1b39c6350f5ecd935dab71ef933e1bca`  
		Last Modified: Tue, 23 Aug 2022 11:16:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3402e2486e536bf44469c2ce583b71937b7cbff76618e426dd63ed6b7dfe0cc5`  
		Last Modified: Tue, 23 Aug 2022 11:16:59 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c2873f607da18c9f2623d952abd04118f7d0778f3599821850f1919eafc164`  
		Last Modified: Tue, 23 Aug 2022 11:17:33 GMT  
		Size: 239.2 MB (239186445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d17c4e21a19faebaa430ee698b7cb100d2e778f790784743bdc70da09436a41`  
		Last Modified: Tue, 23 Aug 2022 11:16:59 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7245c288a141189c997601cc51df3c78474637e0eaaf193d9ff374f766648200`  
		Last Modified: Tue, 23 Aug 2022 11:17:55 GMT  
		Size: 86.6 MB (86569601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3ced040e753b4661b1383d3e5ed1eeb33533efbd4f2e5f6a9b9bd9fe4ca902`  
		Last Modified: Tue, 23 Aug 2022 11:17:42 GMT  
		Size: 319.4 KB (319418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0737249fff82a9ae2caa5144493e9d2fcf088027709fe87ee86f79726d1ae7fd`  
		Last Modified: Tue, 23 Aug 2022 11:17:52 GMT  
		Size: 76.0 MB (75976837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c173bb5a05c73c32307f7778ed744e43ef32a24abee76dcb9bed1c4f60562ea8`  
		Last Modified: Tue, 23 Aug 2022 11:19:25 GMT  
		Size: 488.0 MB (488012770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:e9b3c1ce9dd2ed273198e7f47fdb4d01c140daec8afd44b1805c27bc38517c8a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 MB (867666349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b035c99685d1be45df5e6768994c6926d03c9fdd19fe3087a1939619cc3e37c7`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:43 GMT
ADD file:a3ba1802e6680a14c605fbe754f9fb56a642f0799f51ce0010d253cb66c9691f in / 
# Tue, 23 Aug 2022 01:52:44 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 11:18:53 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:18:54 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 23 Aug 2022 11:18:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 23 Aug 2022 11:18:57 GMT
ENV LANG=C.UTF-8
# Tue, 23 Aug 2022 11:18:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 23 Aug 2022 11:18:59 GMT
ENV ROS_DISTRO=noetic
# Tue, 23 Aug 2022 11:20:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:20:21 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 23 Aug 2022 11:20:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 23 Aug 2022 11:20:24 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 11:20:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:21:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 23 Aug 2022 11:21:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:25:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3332e5c67ba650c61dbca801cf2739a1f5b6faac33f7b0543f97f4ab1165fe69`  
		Last Modified: Tue, 23 Aug 2022 01:58:23 GMT  
		Size: 49.2 MB (49228066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc5b8055a31acea8cf6858fb7058f9828cf856d7ca15408120754ef8e582e8b`  
		Last Modified: Tue, 23 Aug 2022 11:28:27 GMT  
		Size: 10.7 MB (10689268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3e051ec8c4f50bc9206c4036995d09b8baf8a208b4aae22a2deeb7a246a5f0`  
		Last Modified: Tue, 23 Aug 2022 11:28:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad3dbf6ff20222664e13d9f371430b5b76a850b135d2cd6876f8239ebf2cf26`  
		Last Modified: Tue, 23 Aug 2022 11:28:25 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b972b9d90022d411ed9be6a75b03629caf11045e410b85bf532d9b574973f`  
		Last Modified: Tue, 23 Aug 2022 11:28:56 GMT  
		Size: 184.4 MB (184373802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bebe4a80f1367e9d727dcccb4679e5590d80dd2a8d0b00100b06f21a5e20bc0`  
		Last Modified: Tue, 23 Aug 2022 11:28:25 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97614d076b0337a5bf133b8ea0f63b2a64fd4907f6242d84556146524077b032`  
		Last Modified: Tue, 23 Aug 2022 11:29:14 GMT  
		Size: 84.4 MB (84370471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a86f0adf69a256428f0eb97e4d0a6ebb4c333ee833fa76731d8b0526eb88d5d`  
		Last Modified: Tue, 23 Aug 2022 11:29:04 GMT  
		Size: 319.4 KB (319361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a577fe3ce43ebe0d1f7719dc2286b8f2cead9743255d3f8f71caebb62632e29e`  
		Last Modified: Tue, 23 Aug 2022 11:29:13 GMT  
		Size: 73.9 MB (73865202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4ba63562a66f6afe3ebe16c242c26e8178e665b54612c145c479b1e9748026`  
		Last Modified: Tue, 23 Aug 2022 11:30:41 GMT  
		Size: 464.8 MB (464817808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-perception-focal`

```console
$ docker pull ros@sha256:7b840893b4139564fc29fbda07d59fe1ae32bdec7da6d1e97606925abd3d3d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-perception-focal` - linux; amd64

```console
$ docker pull ros@sha256:92a9a61a2bbca7538207c06e045a7a5e686090a54831516ffa488a491aa1c4ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **835.1 MB (835120913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536572ffb5a95c08ca27649d9209f61d60a1f36a15acdb55bfb3efe0650d171d`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:03:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:45 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Sep 2022 04:30:46 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:30:46 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:30:46 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:30:47 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Sep 2022 04:32:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:32:46 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Sep 2022 04:32:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:32:46 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:33:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:33:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:34:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:41:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf19bc0e0d1d8bf1ec9b593eb3ddedecefdf4aff5f519ad585667a258956af1`  
		Last Modified: Fri, 02 Sep 2022 03:15:37 GMT  
		Size: 1.2 MB (1163757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff483ca449e233e69f18eb71e430f67ec1b4c8f5a965b4d7efc759a0ba2f18c4`  
		Last Modified: Fri, 02 Sep 2022 05:06:36 GMT  
		Size: 5.5 MB (5546993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e933af47665655d97d902ecb6d264063a041b2c12dfcbaf849a05672cafc9044`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1916d550484243d392ddc6fdca4ba34710bd3305a578bf9d241f2ad6d944c099`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d152bd7bb3b1335dd05a53828858de8ceab15c85e96fdc0181b2e38f72323b8`  
		Last Modified: Fri, 02 Sep 2022 05:07:05 GMT  
		Size: 177.0 MB (176996015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edc8aa6732f94d22820aa0f96400c620b51e015fa6a940c03e9b579f0de306f`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b38aa1dd8b74095a973aa1b1fe9d7495fcbf895f954b66adbff905119d10103`  
		Last Modified: Fri, 02 Sep 2022 05:07:22 GMT  
		Size: 50.9 MB (50940098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5cec93c265dc40fb6eb4790e71c25ac877e2addb6eddf96377e4336554651e`  
		Last Modified: Fri, 02 Sep 2022 05:07:14 GMT  
		Size: 325.7 KB (325719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca383d78ab41bd8631ac0ef8afce8de1b461c6b95a74094926636a7d8ff9c57`  
		Last Modified: Fri, 02 Sep 2022 05:07:26 GMT  
		Size: 79.6 MB (79603671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec642114a0fb290bf0ad8660843fcd6f3653247c1aedf51d36e3b9afa30a2a4`  
		Last Modified: Fri, 02 Sep 2022 05:09:04 GMT  
		Size: 492.0 MB (491969560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:1ecaf8e232748957ac86a63221733c7593239f1c1f6e1f806933b288509f4c99
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **726.1 MB (726125169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea4e067cd70525d9e125993cb33ef7c1d7b685b94254c7e68f9bd1e3f34d89f`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:40:45 GMT
ADD file:7de7e2c2eb5b05b2449f1e73da223081e27d073990c979ec73afd1893c58c551 in / 
# Tue, 02 Aug 2022 01:40:45 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:53:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:53:45 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:53:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 03 Aug 2022 22:53:47 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 03 Aug 2022 22:53:47 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 22:53:47 GMT
ENV LC_ALL=C.UTF-8
# Wed, 03 Aug 2022 22:53:47 GMT
ENV ROS_DISTRO=noetic
# Wed, 03 Aug 2022 22:55:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:55:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 03 Aug 2022 22:55:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 03 Aug 2022 22:55:11 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:56:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:56:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 03 Aug 2022 22:57:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 23:05:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:de6f11ffeeef9e471776e52baf8cc454a1249e8caf2d8944a5b0387143608310`  
		Last Modified: Tue, 02 Aug 2022 01:43:13 GMT  
		Size: 24.6 MB (24589273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d345e3aeca1c4dd8930e961af9d46712aa474a7ce53acba4f54b4ff3b113a84`  
		Last Modified: Wed, 03 Aug 2022 23:09:30 GMT  
		Size: 1.2 MB (1181992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cf40d14b8b7f81b4f192b1708fbdb0a57c3626f5b72be630a041c1f634f266`  
		Last Modified: Wed, 03 Aug 2022 23:09:28 GMT  
		Size: 4.7 MB (4676289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3223d85d87ee35ea3ab4535feef031631e281f3c617de4cdc218c4983c9b6f`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5bf7f51f5d7e24eec5395780a42aebd0c726cb0466dd5e0b2c492c6d0c84b3`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c66f511399e2f2993ed8fd014bb457c6d6a9483ae665aea0e9eb01fb0a54b4`  
		Last Modified: Wed, 03 Aug 2022 23:10:06 GMT  
		Size: 157.5 MB (157479986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa138f7b3214bda7dc2ae9534dff610b8c2a41d8de8dfb7c8a69ab5eba596887`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e956f29112fb883f35fde1c1d67fc064ab659310ef5bc2f894fd7fabc7cb1b53`  
		Last Modified: Wed, 03 Aug 2022 23:10:25 GMT  
		Size: 40.5 MB (40505939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b4fa88c4ff97cf49d78a40c699333d1182e8a7a0cdb62a65b76e6d6ba39208`  
		Last Modified: Wed, 03 Aug 2022 23:10:18 GMT  
		Size: 323.5 KB (323517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0f054c04c983a4aa345e62e3a2df78c234e061aab4b29b964612f3ff52473c`  
		Last Modified: Wed, 03 Aug 2022 23:10:30 GMT  
		Size: 60.5 MB (60480770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802d1642a23d0013e97d3851823d3d1d2bb88f1ffa90be40d87e65a988ea2a9a`  
		Last Modified: Wed, 03 Aug 2022 23:12:10 GMT  
		Size: 436.9 MB (436884989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-perception-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:0a06825f28b50c090d1b79874eddcb235ab8977dc3f26205d86f96307e14fbaf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **784.7 MB (784729415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73229aac1c29ad65732bf715e6cefa795fbbe38f93ce6348d12ae7e77d182811`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:09:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:09:06 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:09:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:09:08 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 15:10:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:06 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:10:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:10:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:10:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:11:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:13:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-perception=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c7d1bf2cea5d6a7f0ef5ba787e95aa344e3e67e349bbdcaedd088b0732e48e`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ac26fe78d80a057263cfc59c64582efef7caaa111eb4b639861056cf0df95`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f493394889994de604dd62e022d4827365c0de34ad6cac870ea6af5dca4bba40`  
		Last Modified: Tue, 02 Aug 2022 15:41:50 GMT  
		Size: 171.4 MB (171424725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c191fa5a5fa889fff525b13caa35fb805e0bac7c673aebce455ffc8876fce9`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9227bd4aa30a597598fbc456d5aa784c527937a1f88d2ad2787b48b0ad396d6`  
		Last Modified: Tue, 02 Aug 2022 15:42:10 GMT  
		Size: 45.0 MB (44988903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80df4890a016b37679e242280f4c5981f02725f7e081609daba03d47c99cb3ab`  
		Last Modified: Tue, 02 Aug 2022 15:42:03 GMT  
		Size: 323.5 KB (323472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9700876cb7bd2a4af8a21af304524eafef9645266e38f92be7594dbf40519b67`  
		Last Modified: Tue, 02 Aug 2022 15:42:13 GMT  
		Size: 71.8 MB (71754502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3ba7b86422cfbb851f49e5b6c651bbc5d3d24e15ac8200fa9c8341a38b6ff3`  
		Last Modified: Tue, 02 Aug 2022 15:43:50 GMT  
		Size: 462.5 MB (462537264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot`

```console
$ docker pull ros@sha256:3eb89d0f6eff241f739fe53973b23cc79f2c8842c36360683264883f548c7a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot` - linux; amd64

```console
$ docker pull ros@sha256:669c18fe44b20f61149f51771c40553202d44d46ec86a74600eb1e7431000bd4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (359011850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33234d459a19d3a4bbe5ae8699e82192f9a9f50eb461757a4dbee1be52429ab`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:03:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:45 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Sep 2022 04:30:46 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:30:46 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:30:46 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:30:47 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Sep 2022 04:32:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:32:46 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Sep 2022 04:32:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:32:46 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:33:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:33:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:34:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:35:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf19bc0e0d1d8bf1ec9b593eb3ddedecefdf4aff5f519ad585667a258956af1`  
		Last Modified: Fri, 02 Sep 2022 03:15:37 GMT  
		Size: 1.2 MB (1163757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff483ca449e233e69f18eb71e430f67ec1b4c8f5a965b4d7efc759a0ba2f18c4`  
		Last Modified: Fri, 02 Sep 2022 05:06:36 GMT  
		Size: 5.5 MB (5546993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e933af47665655d97d902ecb6d264063a041b2c12dfcbaf849a05672cafc9044`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1916d550484243d392ddc6fdca4ba34710bd3305a578bf9d241f2ad6d944c099`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d152bd7bb3b1335dd05a53828858de8ceab15c85e96fdc0181b2e38f72323b8`  
		Last Modified: Fri, 02 Sep 2022 05:07:05 GMT  
		Size: 177.0 MB (176996015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edc8aa6732f94d22820aa0f96400c620b51e015fa6a940c03e9b579f0de306f`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b38aa1dd8b74095a973aa1b1fe9d7495fcbf895f954b66adbff905119d10103`  
		Last Modified: Fri, 02 Sep 2022 05:07:22 GMT  
		Size: 50.9 MB (50940098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5cec93c265dc40fb6eb4790e71c25ac877e2addb6eddf96377e4336554651e`  
		Last Modified: Fri, 02 Sep 2022 05:07:14 GMT  
		Size: 325.7 KB (325719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca383d78ab41bd8631ac0ef8afce8de1b461c6b95a74094926636a7d8ff9c57`  
		Last Modified: Fri, 02 Sep 2022 05:07:26 GMT  
		Size: 79.6 MB (79603671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0626adf2cf42b6dad9a292e7d21a2c1206ef600a05e321e33d906aee3aa891cf`  
		Last Modified: Fri, 02 Sep 2022 05:07:41 GMT  
		Size: 15.9 MB (15860497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:d047da019eed0ae7d07f4483f4f6dca6ddb5aab8834d63bcee903ecff0073bc7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303305191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6388f41565b185241b75e7dc046ca9f15971530341e6c9d8aabf93ee93145659`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:40:45 GMT
ADD file:7de7e2c2eb5b05b2449f1e73da223081e27d073990c979ec73afd1893c58c551 in / 
# Tue, 02 Aug 2022 01:40:45 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:53:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:53:45 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:53:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 03 Aug 2022 22:53:47 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 03 Aug 2022 22:53:47 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 22:53:47 GMT
ENV LC_ALL=C.UTF-8
# Wed, 03 Aug 2022 22:53:47 GMT
ENV ROS_DISTRO=noetic
# Wed, 03 Aug 2022 22:55:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:55:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 03 Aug 2022 22:55:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 03 Aug 2022 22:55:11 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:56:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:56:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 03 Aug 2022 22:57:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:58:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:de6f11ffeeef9e471776e52baf8cc454a1249e8caf2d8944a5b0387143608310`  
		Last Modified: Tue, 02 Aug 2022 01:43:13 GMT  
		Size: 24.6 MB (24589273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d345e3aeca1c4dd8930e961af9d46712aa474a7ce53acba4f54b4ff3b113a84`  
		Last Modified: Wed, 03 Aug 2022 23:09:30 GMT  
		Size: 1.2 MB (1181992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cf40d14b8b7f81b4f192b1708fbdb0a57c3626f5b72be630a041c1f634f266`  
		Last Modified: Wed, 03 Aug 2022 23:09:28 GMT  
		Size: 4.7 MB (4676289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3223d85d87ee35ea3ab4535feef031631e281f3c617de4cdc218c4983c9b6f`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5bf7f51f5d7e24eec5395780a42aebd0c726cb0466dd5e0b2c492c6d0c84b3`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c66f511399e2f2993ed8fd014bb457c6d6a9483ae665aea0e9eb01fb0a54b4`  
		Last Modified: Wed, 03 Aug 2022 23:10:06 GMT  
		Size: 157.5 MB (157479986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa138f7b3214bda7dc2ae9534dff610b8c2a41d8de8dfb7c8a69ab5eba596887`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e956f29112fb883f35fde1c1d67fc064ab659310ef5bc2f894fd7fabc7cb1b53`  
		Last Modified: Wed, 03 Aug 2022 23:10:25 GMT  
		Size: 40.5 MB (40505939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b4fa88c4ff97cf49d78a40c699333d1182e8a7a0cdb62a65b76e6d6ba39208`  
		Last Modified: Wed, 03 Aug 2022 23:10:18 GMT  
		Size: 323.5 KB (323517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0f054c04c983a4aa345e62e3a2df78c234e061aab4b29b964612f3ff52473c`  
		Last Modified: Wed, 03 Aug 2022 23:10:30 GMT  
		Size: 60.5 MB (60480770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:714bead958c0893197e557905b695ea7e2e9f9a621b7b00a14bc25d104d1e307`  
		Last Modified: Wed, 03 Aug 2022 23:10:48 GMT  
		Size: 14.1 MB (14065011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2363394d63c9226e43f228d4f6b516a73c354406130b4eb794b53417f9e4fc4d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.6 MB (337641286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff135b7f4c695d352453bda4841ae8e7de427860245023f07b02fb4e71368dba`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:09:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:09:06 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:09:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:09:08 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 15:10:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:06 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:10:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:10:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:10:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:11:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:11:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c7d1bf2cea5d6a7f0ef5ba787e95aa344e3e67e349bbdcaedd088b0732e48e`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ac26fe78d80a057263cfc59c64582efef7caaa111eb4b639861056cf0df95`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f493394889994de604dd62e022d4827365c0de34ad6cac870ea6af5dca4bba40`  
		Last Modified: Tue, 02 Aug 2022 15:41:50 GMT  
		Size: 171.4 MB (171424725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c191fa5a5fa889fff525b13caa35fb805e0bac7c673aebce455ffc8876fce9`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9227bd4aa30a597598fbc456d5aa784c527937a1f88d2ad2787b48b0ad396d6`  
		Last Modified: Tue, 02 Aug 2022 15:42:10 GMT  
		Size: 45.0 MB (44988903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80df4890a016b37679e242280f4c5981f02725f7e081609daba03d47c99cb3ab`  
		Last Modified: Tue, 02 Aug 2022 15:42:03 GMT  
		Size: 323.5 KB (323472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9700876cb7bd2a4af8a21af304524eafef9645266e38f92be7594dbf40519b67`  
		Last Modified: Tue, 02 Aug 2022 15:42:13 GMT  
		Size: 71.8 MB (71754502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd26413b5f7234b4810d580a8d95d41b71e839575515cae1e1326b6750e1ec62`  
		Last Modified: Tue, 02 Aug 2022 15:42:31 GMT  
		Size: 15.4 MB (15449135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot-buster`

```console
$ docker pull ros@sha256:1d95973b3645afe08b3007d6b8f0111f7d0e2517dba58181323adf9cb45b1558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-robot-buster` - linux; amd64

```console
$ docker pull ros@sha256:7956e83e77838e68d1587d3ef479c4cd0a188a4fb62c0e161ef14dc872c07c4c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.8 MB (484837064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4760c478875c153123f1ae6782861cbb93a39312ce3b453fe25f12676ed92b4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 00:21:00 GMT
ADD file:d420ffdf63082e03517284553796e5a100e425201458860f07b1aa8598c5929a in / 
# Tue, 23 Aug 2022 00:21:00 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 11:10:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:10:43 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 23 Aug 2022 11:10:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 23 Aug 2022 11:10:45 GMT
ENV LANG=C.UTF-8
# Tue, 23 Aug 2022 11:10:45 GMT
ENV LC_ALL=C.UTF-8
# Tue, 23 Aug 2022 11:10:45 GMT
ENV ROS_DISTRO=noetic
# Tue, 23 Aug 2022 11:11:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:11:49 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 23 Aug 2022 11:11:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 23 Aug 2022 11:11:49 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 11:12:18 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:12:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 23 Aug 2022 11:12:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:13:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:76dff75df4d9dbdf29a4459adaec745740bfb476cd915906e33eddd9cd94db93`  
		Last Modified: Tue, 23 Aug 2022 00:25:20 GMT  
		Size: 50.4 MB (50440273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd91dd5198cc577c5556c7c5c335e0ea5701168d8c2ded40b83bc24be1434e47`  
		Last Modified: Tue, 23 Aug 2022 11:17:01 GMT  
		Size: 10.9 MB (10893537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385a586942561cc66fbd30195e87e96f1b39c6350f5ecd935dab71ef933e1bca`  
		Last Modified: Tue, 23 Aug 2022 11:16:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3402e2486e536bf44469c2ce583b71937b7cbff76618e426dd63ed6b7dfe0cc5`  
		Last Modified: Tue, 23 Aug 2022 11:16:59 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c2873f607da18c9f2623d952abd04118f7d0778f3599821850f1919eafc164`  
		Last Modified: Tue, 23 Aug 2022 11:17:33 GMT  
		Size: 239.2 MB (239186445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d17c4e21a19faebaa430ee698b7cb100d2e778f790784743bdc70da09436a41`  
		Last Modified: Tue, 23 Aug 2022 11:16:59 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7245c288a141189c997601cc51df3c78474637e0eaaf193d9ff374f766648200`  
		Last Modified: Tue, 23 Aug 2022 11:17:55 GMT  
		Size: 86.6 MB (86569601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3ced040e753b4661b1383d3e5ed1eeb33533efbd4f2e5f6a9b9bd9fe4ca902`  
		Last Modified: Tue, 23 Aug 2022 11:17:42 GMT  
		Size: 319.4 KB (319418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0737249fff82a9ae2caa5144493e9d2fcf088027709fe87ee86f79726d1ae7fd`  
		Last Modified: Tue, 23 Aug 2022 11:17:52 GMT  
		Size: 76.0 MB (75976837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a2c6bdee82b6f5b3558161c7d266c7601397cdce5456823e53e9f9d9841814`  
		Last Modified: Tue, 23 Aug 2022 11:18:04 GMT  
		Size: 21.4 MB (21448540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b1aac759bc9e577f5db35de92baf881e54af98a96df414359245b20d7c1d676c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.0 MB (423955218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc754b36f0fcd0f2a9690a792420df38b5c3060eb927369b9abc9df0e6c93b89`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:43 GMT
ADD file:a3ba1802e6680a14c605fbe754f9fb56a642f0799f51ce0010d253cb66c9691f in / 
# Tue, 23 Aug 2022 01:52:44 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 11:18:53 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:18:54 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 23 Aug 2022 11:18:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 23 Aug 2022 11:18:57 GMT
ENV LANG=C.UTF-8
# Tue, 23 Aug 2022 11:18:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 23 Aug 2022 11:18:59 GMT
ENV ROS_DISTRO=noetic
# Tue, 23 Aug 2022 11:20:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:20:21 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 23 Aug 2022 11:20:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 23 Aug 2022 11:20:24 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 11:20:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:21:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 23 Aug 2022 11:21:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:22:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3332e5c67ba650c61dbca801cf2739a1f5b6faac33f7b0543f97f4ab1165fe69`  
		Last Modified: Tue, 23 Aug 2022 01:58:23 GMT  
		Size: 49.2 MB (49228066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc5b8055a31acea8cf6858fb7058f9828cf856d7ca15408120754ef8e582e8b`  
		Last Modified: Tue, 23 Aug 2022 11:28:27 GMT  
		Size: 10.7 MB (10689268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3e051ec8c4f50bc9206c4036995d09b8baf8a208b4aae22a2deeb7a246a5f0`  
		Last Modified: Tue, 23 Aug 2022 11:28:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad3dbf6ff20222664e13d9f371430b5b76a850b135d2cd6876f8239ebf2cf26`  
		Last Modified: Tue, 23 Aug 2022 11:28:25 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b972b9d90022d411ed9be6a75b03629caf11045e410b85bf532d9b574973f`  
		Last Modified: Tue, 23 Aug 2022 11:28:56 GMT  
		Size: 184.4 MB (184373802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bebe4a80f1367e9d727dcccb4679e5590d80dd2a8d0b00100b06f21a5e20bc0`  
		Last Modified: Tue, 23 Aug 2022 11:28:25 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97614d076b0337a5bf133b8ea0f63b2a64fd4907f6242d84556146524077b032`  
		Last Modified: Tue, 23 Aug 2022 11:29:14 GMT  
		Size: 84.4 MB (84370471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a86f0adf69a256428f0eb97e4d0a6ebb4c333ee833fa76731d8b0526eb88d5d`  
		Last Modified: Tue, 23 Aug 2022 11:29:04 GMT  
		Size: 319.4 KB (319361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a577fe3ce43ebe0d1f7719dc2286b8f2cead9743255d3f8f71caebb62632e29e`  
		Last Modified: Tue, 23 Aug 2022 11:29:13 GMT  
		Size: 73.9 MB (73865202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d546ca9c14f09149deff55dacc44fd6006a70d77da691d40d69b36372a3c7f86`  
		Last Modified: Tue, 23 Aug 2022 11:29:25 GMT  
		Size: 21.1 MB (21106677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-robot-focal`

```console
$ docker pull ros@sha256:3eb89d0f6eff241f739fe53973b23cc79f2c8842c36360683264883f548c7a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-robot-focal` - linux; amd64

```console
$ docker pull ros@sha256:669c18fe44b20f61149f51771c40553202d44d46ec86a74600eb1e7431000bd4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (359011850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33234d459a19d3a4bbe5ae8699e82192f9a9f50eb461757a4dbee1be52429ab`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:03:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:45 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Sep 2022 04:30:46 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:30:46 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:30:46 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:30:47 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Sep 2022 04:32:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:32:46 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Sep 2022 04:32:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:32:46 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:33:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:33:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:34:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:35:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf19bc0e0d1d8bf1ec9b593eb3ddedecefdf4aff5f519ad585667a258956af1`  
		Last Modified: Fri, 02 Sep 2022 03:15:37 GMT  
		Size: 1.2 MB (1163757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff483ca449e233e69f18eb71e430f67ec1b4c8f5a965b4d7efc759a0ba2f18c4`  
		Last Modified: Fri, 02 Sep 2022 05:06:36 GMT  
		Size: 5.5 MB (5546993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e933af47665655d97d902ecb6d264063a041b2c12dfcbaf849a05672cafc9044`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1916d550484243d392ddc6fdca4ba34710bd3305a578bf9d241f2ad6d944c099`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d152bd7bb3b1335dd05a53828858de8ceab15c85e96fdc0181b2e38f72323b8`  
		Last Modified: Fri, 02 Sep 2022 05:07:05 GMT  
		Size: 177.0 MB (176996015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edc8aa6732f94d22820aa0f96400c620b51e015fa6a940c03e9b579f0de306f`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b38aa1dd8b74095a973aa1b1fe9d7495fcbf895f954b66adbff905119d10103`  
		Last Modified: Fri, 02 Sep 2022 05:07:22 GMT  
		Size: 50.9 MB (50940098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5cec93c265dc40fb6eb4790e71c25ac877e2addb6eddf96377e4336554651e`  
		Last Modified: Fri, 02 Sep 2022 05:07:14 GMT  
		Size: 325.7 KB (325719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca383d78ab41bd8631ac0ef8afce8de1b461c6b95a74094926636a7d8ff9c57`  
		Last Modified: Fri, 02 Sep 2022 05:07:26 GMT  
		Size: 79.6 MB (79603671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0626adf2cf42b6dad9a292e7d21a2c1206ef600a05e321e33d906aee3aa891cf`  
		Last Modified: Fri, 02 Sep 2022 05:07:41 GMT  
		Size: 15.9 MB (15860497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:d047da019eed0ae7d07f4483f4f6dca6ddb5aab8834d63bcee903ecff0073bc7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303305191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6388f41565b185241b75e7dc046ca9f15971530341e6c9d8aabf93ee93145659`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:40:45 GMT
ADD file:7de7e2c2eb5b05b2449f1e73da223081e27d073990c979ec73afd1893c58c551 in / 
# Tue, 02 Aug 2022 01:40:45 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:53:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:53:45 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:53:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 03 Aug 2022 22:53:47 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 03 Aug 2022 22:53:47 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 22:53:47 GMT
ENV LC_ALL=C.UTF-8
# Wed, 03 Aug 2022 22:53:47 GMT
ENV ROS_DISTRO=noetic
# Wed, 03 Aug 2022 22:55:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:55:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 03 Aug 2022 22:55:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 03 Aug 2022 22:55:11 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:56:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:56:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 03 Aug 2022 22:57:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:58:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:de6f11ffeeef9e471776e52baf8cc454a1249e8caf2d8944a5b0387143608310`  
		Last Modified: Tue, 02 Aug 2022 01:43:13 GMT  
		Size: 24.6 MB (24589273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d345e3aeca1c4dd8930e961af9d46712aa474a7ce53acba4f54b4ff3b113a84`  
		Last Modified: Wed, 03 Aug 2022 23:09:30 GMT  
		Size: 1.2 MB (1181992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cf40d14b8b7f81b4f192b1708fbdb0a57c3626f5b72be630a041c1f634f266`  
		Last Modified: Wed, 03 Aug 2022 23:09:28 GMT  
		Size: 4.7 MB (4676289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3223d85d87ee35ea3ab4535feef031631e281f3c617de4cdc218c4983c9b6f`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5bf7f51f5d7e24eec5395780a42aebd0c726cb0466dd5e0b2c492c6d0c84b3`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c66f511399e2f2993ed8fd014bb457c6d6a9483ae665aea0e9eb01fb0a54b4`  
		Last Modified: Wed, 03 Aug 2022 23:10:06 GMT  
		Size: 157.5 MB (157479986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa138f7b3214bda7dc2ae9534dff610b8c2a41d8de8dfb7c8a69ab5eba596887`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e956f29112fb883f35fde1c1d67fc064ab659310ef5bc2f894fd7fabc7cb1b53`  
		Last Modified: Wed, 03 Aug 2022 23:10:25 GMT  
		Size: 40.5 MB (40505939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b4fa88c4ff97cf49d78a40c699333d1182e8a7a0cdb62a65b76e6d6ba39208`  
		Last Modified: Wed, 03 Aug 2022 23:10:18 GMT  
		Size: 323.5 KB (323517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0f054c04c983a4aa345e62e3a2df78c234e061aab4b29b964612f3ff52473c`  
		Last Modified: Wed, 03 Aug 2022 23:10:30 GMT  
		Size: 60.5 MB (60480770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:714bead958c0893197e557905b695ea7e2e9f9a621b7b00a14bc25d104d1e307`  
		Last Modified: Wed, 03 Aug 2022 23:10:48 GMT  
		Size: 14.1 MB (14065011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-robot-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2363394d63c9226e43f228d4f6b516a73c354406130b4eb794b53417f9e4fc4d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.6 MB (337641286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff135b7f4c695d352453bda4841ae8e7de427860245023f07b02fb4e71368dba`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:09:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:09:06 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:09:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:09:08 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 15:10:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:06 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:10:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:10:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:10:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:11:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:11:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-robot=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c7d1bf2cea5d6a7f0ef5ba787e95aa344e3e67e349bbdcaedd088b0732e48e`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ac26fe78d80a057263cfc59c64582efef7caaa111eb4b639861056cf0df95`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f493394889994de604dd62e022d4827365c0de34ad6cac870ea6af5dca4bba40`  
		Last Modified: Tue, 02 Aug 2022 15:41:50 GMT  
		Size: 171.4 MB (171424725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c191fa5a5fa889fff525b13caa35fb805e0bac7c673aebce455ffc8876fce9`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9227bd4aa30a597598fbc456d5aa784c527937a1f88d2ad2787b48b0ad396d6`  
		Last Modified: Tue, 02 Aug 2022 15:42:10 GMT  
		Size: 45.0 MB (44988903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80df4890a016b37679e242280f4c5981f02725f7e081609daba03d47c99cb3ab`  
		Last Modified: Tue, 02 Aug 2022 15:42:03 GMT  
		Size: 323.5 KB (323472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9700876cb7bd2a4af8a21af304524eafef9645266e38f92be7594dbf40519b67`  
		Last Modified: Tue, 02 Aug 2022 15:42:13 GMT  
		Size: 71.8 MB (71754502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd26413b5f7234b4810d580a8d95d41b71e839575515cae1e1326b6750e1ec62`  
		Last Modified: Tue, 02 Aug 2022 15:42:31 GMT  
		Size: 15.4 MB (15449135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base`

```console
$ docker pull ros@sha256:60f7aaee609f26cc98bea2cfd9fc4ed5c3adda68b49303e02bbf00755f383fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:a3668b236d93abbfedcf72a51abc193842193459fdb8aac6b642ed95441a6cbc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343151353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b356ccf86aa9679666fabf6c6ce440b45f40baf7f272adee0eca54f31d4d6b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:03:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:45 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Sep 2022 04:30:46 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:30:46 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:30:46 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:30:47 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Sep 2022 04:32:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:32:46 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Sep 2022 04:32:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:32:46 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:33:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:33:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:34:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf19bc0e0d1d8bf1ec9b593eb3ddedecefdf4aff5f519ad585667a258956af1`  
		Last Modified: Fri, 02 Sep 2022 03:15:37 GMT  
		Size: 1.2 MB (1163757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff483ca449e233e69f18eb71e430f67ec1b4c8f5a965b4d7efc759a0ba2f18c4`  
		Last Modified: Fri, 02 Sep 2022 05:06:36 GMT  
		Size: 5.5 MB (5546993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e933af47665655d97d902ecb6d264063a041b2c12dfcbaf849a05672cafc9044`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1916d550484243d392ddc6fdca4ba34710bd3305a578bf9d241f2ad6d944c099`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d152bd7bb3b1335dd05a53828858de8ceab15c85e96fdc0181b2e38f72323b8`  
		Last Modified: Fri, 02 Sep 2022 05:07:05 GMT  
		Size: 177.0 MB (176996015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edc8aa6732f94d22820aa0f96400c620b51e015fa6a940c03e9b579f0de306f`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b38aa1dd8b74095a973aa1b1fe9d7495fcbf895f954b66adbff905119d10103`  
		Last Modified: Fri, 02 Sep 2022 05:07:22 GMT  
		Size: 50.9 MB (50940098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5cec93c265dc40fb6eb4790e71c25ac877e2addb6eddf96377e4336554651e`  
		Last Modified: Fri, 02 Sep 2022 05:07:14 GMT  
		Size: 325.7 KB (325719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca383d78ab41bd8631ac0ef8afce8de1b461c6b95a74094926636a7d8ff9c57`  
		Last Modified: Fri, 02 Sep 2022 05:07:26 GMT  
		Size: 79.6 MB (79603671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm variant v7

```console
$ docker pull ros@sha256:dc89df4c67ffb8e35dcb232a71956399e39b3575cfa1e8389e74e1d5a0782638
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289240180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5a83264b759495b4caae5a5c49c6f2dbf31890cf1b28ffedbd7d55f94c0279`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:40:45 GMT
ADD file:7de7e2c2eb5b05b2449f1e73da223081e27d073990c979ec73afd1893c58c551 in / 
# Tue, 02 Aug 2022 01:40:45 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:53:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:53:45 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:53:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 03 Aug 2022 22:53:47 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 03 Aug 2022 22:53:47 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 22:53:47 GMT
ENV LC_ALL=C.UTF-8
# Wed, 03 Aug 2022 22:53:47 GMT
ENV ROS_DISTRO=noetic
# Wed, 03 Aug 2022 22:55:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:55:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 03 Aug 2022 22:55:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 03 Aug 2022 22:55:11 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:56:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:56:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 03 Aug 2022 22:57:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:de6f11ffeeef9e471776e52baf8cc454a1249e8caf2d8944a5b0387143608310`  
		Last Modified: Tue, 02 Aug 2022 01:43:13 GMT  
		Size: 24.6 MB (24589273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d345e3aeca1c4dd8930e961af9d46712aa474a7ce53acba4f54b4ff3b113a84`  
		Last Modified: Wed, 03 Aug 2022 23:09:30 GMT  
		Size: 1.2 MB (1181992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cf40d14b8b7f81b4f192b1708fbdb0a57c3626f5b72be630a041c1f634f266`  
		Last Modified: Wed, 03 Aug 2022 23:09:28 GMT  
		Size: 4.7 MB (4676289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3223d85d87ee35ea3ab4535feef031631e281f3c617de4cdc218c4983c9b6f`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5bf7f51f5d7e24eec5395780a42aebd0c726cb0466dd5e0b2c492c6d0c84b3`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c66f511399e2f2993ed8fd014bb457c6d6a9483ae665aea0e9eb01fb0a54b4`  
		Last Modified: Wed, 03 Aug 2022 23:10:06 GMT  
		Size: 157.5 MB (157479986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa138f7b3214bda7dc2ae9534dff610b8c2a41d8de8dfb7c8a69ab5eba596887`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e956f29112fb883f35fde1c1d67fc064ab659310ef5bc2f894fd7fabc7cb1b53`  
		Last Modified: Wed, 03 Aug 2022 23:10:25 GMT  
		Size: 40.5 MB (40505939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b4fa88c4ff97cf49d78a40c699333d1182e8a7a0cdb62a65b76e6d6ba39208`  
		Last Modified: Wed, 03 Aug 2022 23:10:18 GMT  
		Size: 323.5 KB (323517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0f054c04c983a4aa345e62e3a2df78c234e061aab4b29b964612f3ff52473c`  
		Last Modified: Wed, 03 Aug 2022 23:10:30 GMT  
		Size: 60.5 MB (60480770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8d2c3160385c2f5a6449fff4905f7290543a28713ffc6e1550747d5e0dcdb0ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322192151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108358074c3289edba33e14e8130004770bde5dd9106d446db28dd2548498a48`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:09:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:09:06 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:09:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:09:08 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 15:10:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:06 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:10:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:10:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:10:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:11:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c7d1bf2cea5d6a7f0ef5ba787e95aa344e3e67e349bbdcaedd088b0732e48e`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ac26fe78d80a057263cfc59c64582efef7caaa111eb4b639861056cf0df95`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f493394889994de604dd62e022d4827365c0de34ad6cac870ea6af5dca4bba40`  
		Last Modified: Tue, 02 Aug 2022 15:41:50 GMT  
		Size: 171.4 MB (171424725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c191fa5a5fa889fff525b13caa35fb805e0bac7c673aebce455ffc8876fce9`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9227bd4aa30a597598fbc456d5aa784c527937a1f88d2ad2787b48b0ad396d6`  
		Last Modified: Tue, 02 Aug 2022 15:42:10 GMT  
		Size: 45.0 MB (44988903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80df4890a016b37679e242280f4c5981f02725f7e081609daba03d47c99cb3ab`  
		Last Modified: Tue, 02 Aug 2022 15:42:03 GMT  
		Size: 323.5 KB (323472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9700876cb7bd2a4af8a21af304524eafef9645266e38f92be7594dbf40519b67`  
		Last Modified: Tue, 02 Aug 2022 15:42:13 GMT  
		Size: 71.8 MB (71754502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base-buster`

```console
$ docker pull ros@sha256:460b5270d8efd9366df37679e97b7ff112e3fd9dd49e121c3b66d95a341e050d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-buster` - linux; amd64

```console
$ docker pull ros@sha256:9b31f35802dbd4e2692766a1e4c26fb0455819e121512024c4d26fed8bf7bce0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.4 MB (463388524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe749cdeaebe2e2a4c64221e28a6de9e135c4e290c652a948c231ba1889cfb03`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 00:21:00 GMT
ADD file:d420ffdf63082e03517284553796e5a100e425201458860f07b1aa8598c5929a in / 
# Tue, 23 Aug 2022 00:21:00 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 11:10:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:10:43 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 23 Aug 2022 11:10:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 23 Aug 2022 11:10:45 GMT
ENV LANG=C.UTF-8
# Tue, 23 Aug 2022 11:10:45 GMT
ENV LC_ALL=C.UTF-8
# Tue, 23 Aug 2022 11:10:45 GMT
ENV ROS_DISTRO=noetic
# Tue, 23 Aug 2022 11:11:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:11:49 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 23 Aug 2022 11:11:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 23 Aug 2022 11:11:49 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 11:12:18 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:12:24 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 23 Aug 2022 11:12:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:76dff75df4d9dbdf29a4459adaec745740bfb476cd915906e33eddd9cd94db93`  
		Last Modified: Tue, 23 Aug 2022 00:25:20 GMT  
		Size: 50.4 MB (50440273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd91dd5198cc577c5556c7c5c335e0ea5701168d8c2ded40b83bc24be1434e47`  
		Last Modified: Tue, 23 Aug 2022 11:17:01 GMT  
		Size: 10.9 MB (10893537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385a586942561cc66fbd30195e87e96f1b39c6350f5ecd935dab71ef933e1bca`  
		Last Modified: Tue, 23 Aug 2022 11:16:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3402e2486e536bf44469c2ce583b71937b7cbff76618e426dd63ed6b7dfe0cc5`  
		Last Modified: Tue, 23 Aug 2022 11:16:59 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c2873f607da18c9f2623d952abd04118f7d0778f3599821850f1919eafc164`  
		Last Modified: Tue, 23 Aug 2022 11:17:33 GMT  
		Size: 239.2 MB (239186445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d17c4e21a19faebaa430ee698b7cb100d2e778f790784743bdc70da09436a41`  
		Last Modified: Tue, 23 Aug 2022 11:16:59 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7245c288a141189c997601cc51df3c78474637e0eaaf193d9ff374f766648200`  
		Last Modified: Tue, 23 Aug 2022 11:17:55 GMT  
		Size: 86.6 MB (86569601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3ced040e753b4661b1383d3e5ed1eeb33533efbd4f2e5f6a9b9bd9fe4ca902`  
		Last Modified: Tue, 23 Aug 2022 11:17:42 GMT  
		Size: 319.4 KB (319418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0737249fff82a9ae2caa5144493e9d2fcf088027709fe87ee86f79726d1ae7fd`  
		Last Modified: Tue, 23 Aug 2022 11:17:52 GMT  
		Size: 76.0 MB (75976837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:28c09a531af4f7df69d166a66ce447dae5c9390d17ee2a394f84640e8a68dc50
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.8 MB (402848541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36620262bf72864e1023de7d7016850d3ea306b7222a6c6daa19dec3713f1025`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:43 GMT
ADD file:a3ba1802e6680a14c605fbe754f9fb56a642f0799f51ce0010d253cb66c9691f in / 
# Tue, 23 Aug 2022 01:52:44 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 11:18:53 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:18:54 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 23 Aug 2022 11:18:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 23 Aug 2022 11:18:57 GMT
ENV LANG=C.UTF-8
# Tue, 23 Aug 2022 11:18:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 23 Aug 2022 11:18:59 GMT
ENV ROS_DISTRO=noetic
# Tue, 23 Aug 2022 11:20:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:20:21 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 23 Aug 2022 11:20:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 23 Aug 2022 11:20:24 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 11:20:50 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:21:02 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 23 Aug 2022 11:21:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3332e5c67ba650c61dbca801cf2739a1f5b6faac33f7b0543f97f4ab1165fe69`  
		Last Modified: Tue, 23 Aug 2022 01:58:23 GMT  
		Size: 49.2 MB (49228066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc5b8055a31acea8cf6858fb7058f9828cf856d7ca15408120754ef8e582e8b`  
		Last Modified: Tue, 23 Aug 2022 11:28:27 GMT  
		Size: 10.7 MB (10689268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3e051ec8c4f50bc9206c4036995d09b8baf8a208b4aae22a2deeb7a246a5f0`  
		Last Modified: Tue, 23 Aug 2022 11:28:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad3dbf6ff20222664e13d9f371430b5b76a850b135d2cd6876f8239ebf2cf26`  
		Last Modified: Tue, 23 Aug 2022 11:28:25 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b972b9d90022d411ed9be6a75b03629caf11045e410b85bf532d9b574973f`  
		Last Modified: Tue, 23 Aug 2022 11:28:56 GMT  
		Size: 184.4 MB (184373802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bebe4a80f1367e9d727dcccb4679e5590d80dd2a8d0b00100b06f21a5e20bc0`  
		Last Modified: Tue, 23 Aug 2022 11:28:25 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97614d076b0337a5bf133b8ea0f63b2a64fd4907f6242d84556146524077b032`  
		Last Modified: Tue, 23 Aug 2022 11:29:14 GMT  
		Size: 84.4 MB (84370471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a86f0adf69a256428f0eb97e4d0a6ebb4c333ee833fa76731d8b0526eb88d5d`  
		Last Modified: Tue, 23 Aug 2022 11:29:04 GMT  
		Size: 319.4 KB (319361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a577fe3ce43ebe0d1f7719dc2286b8f2cead9743255d3f8f71caebb62632e29e`  
		Last Modified: Tue, 23 Aug 2022 11:29:13 GMT  
		Size: 73.9 MB (73865202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-base-focal`

```console
$ docker pull ros@sha256:60f7aaee609f26cc98bea2cfd9fc4ed5c3adda68b49303e02bbf00755f383fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-base-focal` - linux; amd64

```console
$ docker pull ros@sha256:a3668b236d93abbfedcf72a51abc193842193459fdb8aac6b642ed95441a6cbc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.2 MB (343151353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b356ccf86aa9679666fabf6c6ce440b45f40baf7f272adee0eca54f31d4d6b`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:03:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:45 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Sep 2022 04:30:46 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:30:46 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:30:46 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:30:47 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Sep 2022 04:32:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:32:46 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Sep 2022 04:32:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:32:46 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:33:11 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:33:17 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 04:34:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf19bc0e0d1d8bf1ec9b593eb3ddedecefdf4aff5f519ad585667a258956af1`  
		Last Modified: Fri, 02 Sep 2022 03:15:37 GMT  
		Size: 1.2 MB (1163757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff483ca449e233e69f18eb71e430f67ec1b4c8f5a965b4d7efc759a0ba2f18c4`  
		Last Modified: Fri, 02 Sep 2022 05:06:36 GMT  
		Size: 5.5 MB (5546993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e933af47665655d97d902ecb6d264063a041b2c12dfcbaf849a05672cafc9044`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1916d550484243d392ddc6fdca4ba34710bd3305a578bf9d241f2ad6d944c099`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d152bd7bb3b1335dd05a53828858de8ceab15c85e96fdc0181b2e38f72323b8`  
		Last Modified: Fri, 02 Sep 2022 05:07:05 GMT  
		Size: 177.0 MB (176996015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edc8aa6732f94d22820aa0f96400c620b51e015fa6a940c03e9b579f0de306f`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b38aa1dd8b74095a973aa1b1fe9d7495fcbf895f954b66adbff905119d10103`  
		Last Modified: Fri, 02 Sep 2022 05:07:22 GMT  
		Size: 50.9 MB (50940098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5cec93c265dc40fb6eb4790e71c25ac877e2addb6eddf96377e4336554651e`  
		Last Modified: Fri, 02 Sep 2022 05:07:14 GMT  
		Size: 325.7 KB (325719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca383d78ab41bd8631ac0ef8afce8de1b461c6b95a74094926636a7d8ff9c57`  
		Last Modified: Fri, 02 Sep 2022 05:07:26 GMT  
		Size: 79.6 MB (79603671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:dc89df4c67ffb8e35dcb232a71956399e39b3575cfa1e8389e74e1d5a0782638
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289240180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5a83264b759495b4caae5a5c49c6f2dbf31890cf1b28ffedbd7d55f94c0279`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:40:45 GMT
ADD file:7de7e2c2eb5b05b2449f1e73da223081e27d073990c979ec73afd1893c58c551 in / 
# Tue, 02 Aug 2022 01:40:45 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:53:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:53:45 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:53:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 03 Aug 2022 22:53:47 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 03 Aug 2022 22:53:47 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 22:53:47 GMT
ENV LC_ALL=C.UTF-8
# Wed, 03 Aug 2022 22:53:47 GMT
ENV ROS_DISTRO=noetic
# Wed, 03 Aug 2022 22:55:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:55:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 03 Aug 2022 22:55:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 03 Aug 2022 22:55:11 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:56:05 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:56:10 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Wed, 03 Aug 2022 22:57:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:de6f11ffeeef9e471776e52baf8cc454a1249e8caf2d8944a5b0387143608310`  
		Last Modified: Tue, 02 Aug 2022 01:43:13 GMT  
		Size: 24.6 MB (24589273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d345e3aeca1c4dd8930e961af9d46712aa474a7ce53acba4f54b4ff3b113a84`  
		Last Modified: Wed, 03 Aug 2022 23:09:30 GMT  
		Size: 1.2 MB (1181992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cf40d14b8b7f81b4f192b1708fbdb0a57c3626f5b72be630a041c1f634f266`  
		Last Modified: Wed, 03 Aug 2022 23:09:28 GMT  
		Size: 4.7 MB (4676289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3223d85d87ee35ea3ab4535feef031631e281f3c617de4cdc218c4983c9b6f`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5bf7f51f5d7e24eec5395780a42aebd0c726cb0466dd5e0b2c492c6d0c84b3`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c66f511399e2f2993ed8fd014bb457c6d6a9483ae665aea0e9eb01fb0a54b4`  
		Last Modified: Wed, 03 Aug 2022 23:10:06 GMT  
		Size: 157.5 MB (157479986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa138f7b3214bda7dc2ae9534dff610b8c2a41d8de8dfb7c8a69ab5eba596887`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e956f29112fb883f35fde1c1d67fc064ab659310ef5bc2f894fd7fabc7cb1b53`  
		Last Modified: Wed, 03 Aug 2022 23:10:25 GMT  
		Size: 40.5 MB (40505939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b4fa88c4ff97cf49d78a40c699333d1182e8a7a0cdb62a65b76e6d6ba39208`  
		Last Modified: Wed, 03 Aug 2022 23:10:18 GMT  
		Size: 323.5 KB (323517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0f054c04c983a4aa345e62e3a2df78c234e061aab4b29b964612f3ff52473c`  
		Last Modified: Wed, 03 Aug 2022 23:10:30 GMT  
		Size: 60.5 MB (60480770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-base-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8d2c3160385c2f5a6449fff4905f7290543a28713ffc6e1550747d5e0dcdb0ba
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 MB (322192151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:108358074c3289edba33e14e8130004770bde5dd9106d446db28dd2548498a48`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:09:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:09:06 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:09:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:09:08 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 15:10:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:06 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:10:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:10:08 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:10:41 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     python3-rosdep     python3-rosinstall     python3-vcstools     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:48 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:11:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-base=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c7d1bf2cea5d6a7f0ef5ba787e95aa344e3e67e349bbdcaedd088b0732e48e`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ac26fe78d80a057263cfc59c64582efef7caaa111eb4b639861056cf0df95`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f493394889994de604dd62e022d4827365c0de34ad6cac870ea6af5dca4bba40`  
		Last Modified: Tue, 02 Aug 2022 15:41:50 GMT  
		Size: 171.4 MB (171424725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c191fa5a5fa889fff525b13caa35fb805e0bac7c673aebce455ffc8876fce9`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9227bd4aa30a597598fbc456d5aa784c527937a1f88d2ad2787b48b0ad396d6`  
		Last Modified: Tue, 02 Aug 2022 15:42:10 GMT  
		Size: 45.0 MB (44988903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80df4890a016b37679e242280f4c5981f02725f7e081609daba03d47c99cb3ab`  
		Last Modified: Tue, 02 Aug 2022 15:42:03 GMT  
		Size: 323.5 KB (323472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9700876cb7bd2a4af8a21af304524eafef9645266e38f92be7594dbf40519b67`  
		Last Modified: Tue, 02 Aug 2022 15:42:13 GMT  
		Size: 71.8 MB (71754502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core`

```console
$ docker pull ros@sha256:d764b670e0f25556a150598c6ea1e4d7e2f66e6b45d9e602779a93ceb1bf6801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:15787f4244d2c4f18c65ff9f5e7aa63bad77a3174d734e44c5d2efe18ccedbf6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212281865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b851b252f464f1ba9e081c21053a32f21ce69a6ec8af25754576fe7b6efd082`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:03:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:45 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Sep 2022 04:30:46 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:30:46 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:30:46 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:30:47 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Sep 2022 04:32:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:32:46 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Sep 2022 04:32:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:32:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf19bc0e0d1d8bf1ec9b593eb3ddedecefdf4aff5f519ad585667a258956af1`  
		Last Modified: Fri, 02 Sep 2022 03:15:37 GMT  
		Size: 1.2 MB (1163757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff483ca449e233e69f18eb71e430f67ec1b4c8f5a965b4d7efc759a0ba2f18c4`  
		Last Modified: Fri, 02 Sep 2022 05:06:36 GMT  
		Size: 5.5 MB (5546993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e933af47665655d97d902ecb6d264063a041b2c12dfcbaf849a05672cafc9044`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1916d550484243d392ddc6fdca4ba34710bd3305a578bf9d241f2ad6d944c099`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d152bd7bb3b1335dd05a53828858de8ceab15c85e96fdc0181b2e38f72323b8`  
		Last Modified: Fri, 02 Sep 2022 05:07:05 GMT  
		Size: 177.0 MB (176996015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edc8aa6732f94d22820aa0f96400c620b51e015fa6a940c03e9b579f0de306f`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm variant v7

```console
$ docker pull ros@sha256:b627329429c292b2ec2942cf25941025bba74bdd29b28271ffa3758060d0ee56
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187929954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7324654dea2b039973f3b058244c1f5bf15eb28690dbe2fd8426e09c3f10323`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:40:45 GMT
ADD file:7de7e2c2eb5b05b2449f1e73da223081e27d073990c979ec73afd1893c58c551 in / 
# Tue, 02 Aug 2022 01:40:45 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:53:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:53:45 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:53:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 03 Aug 2022 22:53:47 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 03 Aug 2022 22:53:47 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 22:53:47 GMT
ENV LC_ALL=C.UTF-8
# Wed, 03 Aug 2022 22:53:47 GMT
ENV ROS_DISTRO=noetic
# Wed, 03 Aug 2022 22:55:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:55:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 03 Aug 2022 22:55:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 03 Aug 2022 22:55:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:de6f11ffeeef9e471776e52baf8cc454a1249e8caf2d8944a5b0387143608310`  
		Last Modified: Tue, 02 Aug 2022 01:43:13 GMT  
		Size: 24.6 MB (24589273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d345e3aeca1c4dd8930e961af9d46712aa474a7ce53acba4f54b4ff3b113a84`  
		Last Modified: Wed, 03 Aug 2022 23:09:30 GMT  
		Size: 1.2 MB (1181992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cf40d14b8b7f81b4f192b1708fbdb0a57c3626f5b72be630a041c1f634f266`  
		Last Modified: Wed, 03 Aug 2022 23:09:28 GMT  
		Size: 4.7 MB (4676289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3223d85d87ee35ea3ab4535feef031631e281f3c617de4cdc218c4983c9b6f`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5bf7f51f5d7e24eec5395780a42aebd0c726cb0466dd5e0b2c492c6d0c84b3`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c66f511399e2f2993ed8fd014bb457c6d6a9483ae665aea0e9eb01fb0a54b4`  
		Last Modified: Wed, 03 Aug 2022 23:10:06 GMT  
		Size: 157.5 MB (157479986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa138f7b3214bda7dc2ae9534dff610b8c2a41d8de8dfb7c8a69ab5eba596887`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2de7b235c0f81dd7f2400b18a72f2e37c2eaff057a552ff4018d27b6e9283537
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.1 MB (205125274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef973504c6d304f7f2ee2f0be2414109ac868cf40926997b3d262097d2c63aa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:09:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:09:06 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:09:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:09:08 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 15:10:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:06 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:10:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:10:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c7d1bf2cea5d6a7f0ef5ba787e95aa344e3e67e349bbdcaedd088b0732e48e`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ac26fe78d80a057263cfc59c64582efef7caaa111eb4b639861056cf0df95`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f493394889994de604dd62e022d4827365c0de34ad6cac870ea6af5dca4bba40`  
		Last Modified: Tue, 02 Aug 2022 15:41:50 GMT  
		Size: 171.4 MB (171424725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c191fa5a5fa889fff525b13caa35fb805e0bac7c673aebce455ffc8876fce9`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core-buster`

```console
$ docker pull ros@sha256:2909b34c7b1c64431ca0f75bec7eda0857c4815c58da9e62d4858e2973582a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-buster` - linux; amd64

```console
$ docker pull ros@sha256:1a1d06b35677ea6f17b411b6bcb701c371187b5cde9933440638403a1a3f3a33
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.5 MB (300522668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0366cedccb9e45dc41095871119e8aebed346194dab88db7bd95ba5f71e98c4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 00:21:00 GMT
ADD file:d420ffdf63082e03517284553796e5a100e425201458860f07b1aa8598c5929a in / 
# Tue, 23 Aug 2022 00:21:00 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 11:10:42 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:10:43 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 23 Aug 2022 11:10:44 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 23 Aug 2022 11:10:45 GMT
ENV LANG=C.UTF-8
# Tue, 23 Aug 2022 11:10:45 GMT
ENV LC_ALL=C.UTF-8
# Tue, 23 Aug 2022 11:10:45 GMT
ENV ROS_DISTRO=noetic
# Tue, 23 Aug 2022 11:11:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:11:49 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 23 Aug 2022 11:11:49 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 23 Aug 2022 11:11:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:76dff75df4d9dbdf29a4459adaec745740bfb476cd915906e33eddd9cd94db93`  
		Last Modified: Tue, 23 Aug 2022 00:25:20 GMT  
		Size: 50.4 MB (50440273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd91dd5198cc577c5556c7c5c335e0ea5701168d8c2ded40b83bc24be1434e47`  
		Last Modified: Tue, 23 Aug 2022 11:17:01 GMT  
		Size: 10.9 MB (10893537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385a586942561cc66fbd30195e87e96f1b39c6350f5ecd935dab71ef933e1bca`  
		Last Modified: Tue, 23 Aug 2022 11:16:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3402e2486e536bf44469c2ce583b71937b7cbff76618e426dd63ed6b7dfe0cc5`  
		Last Modified: Tue, 23 Aug 2022 11:16:59 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c2873f607da18c9f2623d952abd04118f7d0778f3599821850f1919eafc164`  
		Last Modified: Tue, 23 Aug 2022 11:17:33 GMT  
		Size: 239.2 MB (239186445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d17c4e21a19faebaa430ee698b7cb100d2e778f790784743bdc70da09436a41`  
		Last Modified: Tue, 23 Aug 2022 11:16:59 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-buster` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:b8a2f95e3a3e173aaa2bb444bccdca8fc2e86c556b35596b039e7fccbbe9633b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.3 MB (244293507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89673ed8d38d107a06ec46cc1af47c271e78a4301bd71e7e62fcfa10850e23fb`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:43 GMT
ADD file:a3ba1802e6680a14c605fbe754f9fb56a642f0799f51ce0010d253cb66c9691f in / 
# Tue, 23 Aug 2022 01:52:44 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 11:18:53 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:18:54 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu buster main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 23 Aug 2022 11:18:56 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 23 Aug 2022 11:18:57 GMT
ENV LANG=C.UTF-8
# Tue, 23 Aug 2022 11:18:58 GMT
ENV LC_ALL=C.UTF-8
# Tue, 23 Aug 2022 11:18:59 GMT
ENV ROS_DISTRO=noetic
# Tue, 23 Aug 2022 11:20:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 11:20:21 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 23 Aug 2022 11:20:23 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 23 Aug 2022 11:20:24 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3332e5c67ba650c61dbca801cf2739a1f5b6faac33f7b0543f97f4ab1165fe69`  
		Last Modified: Tue, 23 Aug 2022 01:58:23 GMT  
		Size: 49.2 MB (49228066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc5b8055a31acea8cf6858fb7058f9828cf856d7ca15408120754ef8e582e8b`  
		Last Modified: Tue, 23 Aug 2022 11:28:27 GMT  
		Size: 10.7 MB (10689268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3e051ec8c4f50bc9206c4036995d09b8baf8a208b4aae22a2deeb7a246a5f0`  
		Last Modified: Tue, 23 Aug 2022 11:28:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad3dbf6ff20222664e13d9f371430b5b76a850b135d2cd6876f8239ebf2cf26`  
		Last Modified: Tue, 23 Aug 2022 11:28:25 GMT  
		Size: 1.9 KB (1949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6b972b9d90022d411ed9be6a75b03629caf11045e410b85bf532d9b574973f`  
		Last Modified: Tue, 23 Aug 2022 11:28:56 GMT  
		Size: 184.4 MB (184373802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bebe4a80f1367e9d727dcccb4679e5590d80dd2a8d0b00100b06f21a5e20bc0`  
		Last Modified: Tue, 23 Aug 2022 11:28:25 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:noetic-ros-core-focal`

```console
$ docker pull ros@sha256:d764b670e0f25556a150598c6ea1e4d7e2f66e6b45d9e602779a93ceb1bf6801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:noetic-ros-core-focal` - linux; amd64

```console
$ docker pull ros@sha256:15787f4244d2c4f18c65ff9f5e7aa63bad77a3174d734e44c5d2efe18ccedbf6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212281865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b851b252f464f1ba9e081c21053a32f21ce69a6ec8af25754576fe7b6efd082`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:03:55 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:44 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:30:45 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Fri, 02 Sep 2022 04:30:46 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:30:46 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:30:46 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:30:47 GMT
ENV ROS_DISTRO=noetic
# Fri, 02 Sep 2022 04:32:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:32:46 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Fri, 02 Sep 2022 04:32:46 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 04:32:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf19bc0e0d1d8bf1ec9b593eb3ddedecefdf4aff5f519ad585667a258956af1`  
		Last Modified: Fri, 02 Sep 2022 03:15:37 GMT  
		Size: 1.2 MB (1163757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff483ca449e233e69f18eb71e430f67ec1b4c8f5a965b4d7efc759a0ba2f18c4`  
		Last Modified: Fri, 02 Sep 2022 05:06:36 GMT  
		Size: 5.5 MB (5546993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e933af47665655d97d902ecb6d264063a041b2c12dfcbaf849a05672cafc9044`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1916d550484243d392ddc6fdca4ba34710bd3305a578bf9d241f2ad6d944c099`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d152bd7bb3b1335dd05a53828858de8ceab15c85e96fdc0181b2e38f72323b8`  
		Last Modified: Fri, 02 Sep 2022 05:07:05 GMT  
		Size: 177.0 MB (176996015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9edc8aa6732f94d22820aa0f96400c620b51e015fa6a940c03e9b579f0de306f`  
		Last Modified: Fri, 02 Sep 2022 05:06:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm variant v7

```console
$ docker pull ros@sha256:b627329429c292b2ec2942cf25941025bba74bdd29b28271ffa3758060d0ee56
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187929954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7324654dea2b039973f3b058244c1f5bf15eb28690dbe2fd8426e09c3f10323`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:40:45 GMT
ADD file:7de7e2c2eb5b05b2449f1e73da223081e27d073990c979ec73afd1893c58c551 in / 
# Tue, 02 Aug 2022 01:40:45 GMT
CMD ["bash"]
# Wed, 03 Aug 2022 22:53:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:53:45 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:53:46 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Wed, 03 Aug 2022 22:53:47 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Wed, 03 Aug 2022 22:53:47 GMT
ENV LANG=C.UTF-8
# Wed, 03 Aug 2022 22:53:47 GMT
ENV LC_ALL=C.UTF-8
# Wed, 03 Aug 2022 22:53:47 GMT
ENV ROS_DISTRO=noetic
# Wed, 03 Aug 2022 22:55:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 22:55:10 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Wed, 03 Aug 2022 22:55:10 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 03 Aug 2022 22:55:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:de6f11ffeeef9e471776e52baf8cc454a1249e8caf2d8944a5b0387143608310`  
		Last Modified: Tue, 02 Aug 2022 01:43:13 GMT  
		Size: 24.6 MB (24589273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d345e3aeca1c4dd8930e961af9d46712aa474a7ce53acba4f54b4ff3b113a84`  
		Last Modified: Wed, 03 Aug 2022 23:09:30 GMT  
		Size: 1.2 MB (1181992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cf40d14b8b7f81b4f192b1708fbdb0a57c3626f5b72be630a041c1f634f266`  
		Last Modified: Wed, 03 Aug 2022 23:09:28 GMT  
		Size: 4.7 MB (4676289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3223d85d87ee35ea3ab4535feef031631e281f3c617de4cdc218c4983c9b6f`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5bf7f51f5d7e24eec5395780a42aebd0c726cb0466dd5e0b2c492c6d0c84b3`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 2.0 KB (1988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44c66f511399e2f2993ed8fd014bb457c6d6a9483ae665aea0e9eb01fb0a54b4`  
		Last Modified: Wed, 03 Aug 2022 23:10:06 GMT  
		Size: 157.5 MB (157479986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa138f7b3214bda7dc2ae9534dff610b8c2a41d8de8dfb7c8a69ab5eba596887`  
		Last Modified: Wed, 03 Aug 2022 23:09:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:noetic-ros-core-focal` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:2de7b235c0f81dd7f2400b18a72f2e37c2eaff057a552ff4018d27b6e9283537
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.1 MB (205125274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef973504c6d304f7f2ee2f0be2414109ac868cf40926997b3d262097d2c63aa`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:51 GMT
ADD file:151548d1bfac57d762f2c0b18b2378c363ffd1568da9fecd4be611db4832e8e2 in / 
# Tue, 02 Aug 2022 01:18:51 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:08:52 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:02 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:09:03 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros1-latest.list
# Tue, 02 Aug 2022 15:09:05 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:09:06 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:09:07 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:09:08 GMT
ENV ROS_DISTRO=noetic
# Tue, 02 Aug 2022 15:10:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-noetic-ros-core=1.5.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:10:06 GMT
COPY file:b48a3fff5008212a0bcdc238d0e8be930aa89d2336e357e1f628c98db523efeb in / 
# Tue, 02 Aug 2022 15:10:07 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:10:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a749a280e3e905de447c3d95a39e8aa1ede5835a6eadeb0c11596051592b675b`  
		Last Modified: Tue, 02 Aug 2022 01:20:32 GMT  
		Size: 27.2 MB (27191804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c8ebbb56369bd1ed2d75b8a0a88d9d1bc47b0a1cfccb1e93dc48e9a8625ef5`  
		Last Modified: Tue, 02 Aug 2022 15:41:24 GMT  
		Size: 1.2 MB (1182921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c3f36ad7dd9a934fe1ffaa3cdb30e2f32f650f9c0809903abc7be683bd8be9`  
		Last Modified: Tue, 02 Aug 2022 15:41:22 GMT  
		Size: 5.3 MB (5323455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c7d1bf2cea5d6a7f0ef5ba787e95aa344e3e67e349bbdcaedd088b0732e48e`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623ac26fe78d80a057263cfc59c64582efef7caaa111eb4b639861056cf0df95`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 1.9 KB (1945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f493394889994de604dd62e022d4827365c0de34ad6cac870ea6af5dca4bba40`  
		Last Modified: Tue, 02 Aug 2022 15:41:50 GMT  
		Size: 171.4 MB (171424725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c191fa5a5fa889fff525b13caa35fb805e0bac7c673aebce455ffc8876fce9`  
		Last Modified: Tue, 02 Aug 2022 15:41:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling`

```console
$ docker pull ros@sha256:d9c4acfa3a63436c457734cfe1a1c2bb23f80a5d7b3ad0a962e4833c3ccf4aa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling` - linux; amd64

```console
$ docker pull ros@sha256:7b4c586e54c27743aab2a47e40c9703663d5a9e8de1e08173aafbce70150359c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (262952620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223af4769b7faa40e705248499c92752b2b8291256bf897cda3f27d405b0fe59`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:35 GMT
ADD file:a7268f82a86219801950401c224cabbdd83ef510a7c71396b25f70c2639ae4fa in / 
# Thu, 01 Sep 2022 23:46:35 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:47:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:44 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:47:45 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:59:53 GMT
ENV ROS_DISTRO=rolling
# Fri, 02 Sep 2022 05:00:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:00:33 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 05:00:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 05:00:33 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:00:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:01:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 05:01:07 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 02 Sep 2022 05:01:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b55860d4c667a7200a0cb279aec26777df61e5d3530388f223ce7859d566e7a`  
		Last Modified: Tue, 16 Aug 2022 03:03:54 GMT  
		Size: 30.4 MB (30426706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3547d30662b8f49979ed975e15692a70c7bb853c6f802402d13fae5baf9c98`  
		Last Modified: Fri, 02 Sep 2022 05:11:58 GMT  
		Size: 1.2 MB (1175731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e2de4e9186b2154434f8288f5aa7bb8a9d6dc013e0874f7f022b8ae24dfbf0`  
		Last Modified: Fri, 02 Sep 2022 05:11:56 GMT  
		Size: 3.8 MB (3827460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a3a3add45c3c8843eaf042b57f390470bedeb0ac07a77f9c6612bef030c530`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47468e731ca16770a971f055794d9d4098fc38d48dd35c9031b3076ca342047`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3dc50070b191638388b8a6f45838ba98380554ae338b31cc128a05d2395988`  
		Last Modified: Fri, 02 Sep 2022 05:14:57 GMT  
		Size: 106.2 MB (106166428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd81258fb9cb69dfc99169ad3cb6e4fdf405255a94947c3080addd04660088d9`  
		Last Modified: Fri, 02 Sep 2022 05:14:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06230df102e423df05671bcf3524ba4a66b7948f791b968310ce88c3912d891b`  
		Last Modified: Fri, 02 Sep 2022 05:15:20 GMT  
		Size: 97.8 MB (97849361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fba9b08f3c34427866a17b95897c2bbf6d0ddaa0388e56fec786cc5e8b03e9`  
		Last Modified: Fri, 02 Sep 2022 05:15:07 GMT  
		Size: 280.9 KB (280936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8408c6380a2368a7fad097e912751c17f613c5e60923c6797b34c7146889011c`  
		Last Modified: Fri, 02 Sep 2022 05:15:06 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd491e285c840733c080cbbbbaaff463949c9101c61e114e1827f6c8bcac997`  
		Last Modified: Fri, 02 Sep 2022 05:15:10 GMT  
		Size: 23.2 MB (23221130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:566852956ea3fc90533a5cc44c021d66b0693c4b85ae92313ee24a1ef567c481
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (254967875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd12507a1529223aa1d1c513771d5b2cacd63d1157d0fe6ee02c9b4c1bb00a3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:32:25 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Aug 2022 15:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:33:12 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:33:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:33:14 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:33:49 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:33:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:33:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:34:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c096920dab8b763106ab108f7f67ffd78e3a0a5b90062661f6e79ba6e5531450`  
		Last Modified: Tue, 02 Aug 2022 15:52:21 GMT  
		Size: 103.9 MB (103851243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca559a4d1d3cf5ca59d168e6032d9f6eb60609afefe51b8d4c582817823f711b`  
		Last Modified: Tue, 02 Aug 2022 15:52:05 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b563ebf532fc1a5282df03ef5138b18f01216151873445a92258c9638e56a2`  
		Last Modified: Tue, 02 Aug 2022 15:52:47 GMT  
		Size: 95.2 MB (95214507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dae2ccab1eb80eed07380bc35d064a2158a70931c354fef8471c6211d2d1172`  
		Last Modified: Tue, 02 Aug 2022 15:52:33 GMT  
		Size: 278.5 KB (278490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b858516da0fdda5810073563cd5fc6d2cb426f0c32a930e5b0791d373993a1c`  
		Last Modified: Tue, 02 Aug 2022 15:52:33 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a02b086f89c57f355fd6f8e3324803ad1643c2f655acb78f836780b0bb2fbd`  
		Last Modified: Tue, 02 Aug 2022 15:52:37 GMT  
		Size: 22.4 MB (22448437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-perception`

```console
$ docker pull ros@sha256:80f99783a43f285c7a782a3b6c5dd5609dc5ad4db23e7de5f7aa91a1089f22a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception` - linux; amd64

```console
$ docker pull ros@sha256:5da4c659ca33880dde2f1c81b6090f5fe36d146c2220ec69778c2a7553c46779
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1084630290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1e0191400b6a2d7a2b735a66b6136ebd11c56de6a117c0c9aa49d15c5964d5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:35 GMT
ADD file:a7268f82a86219801950401c224cabbdd83ef510a7c71396b25f70c2639ae4fa in / 
# Thu, 01 Sep 2022 23:46:35 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:47:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:44 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:47:45 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:59:53 GMT
ENV ROS_DISTRO=rolling
# Fri, 02 Sep 2022 05:00:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:00:33 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 05:00:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 05:00:33 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:00:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:01:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 05:01:07 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 02 Sep 2022 05:01:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:03:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b55860d4c667a7200a0cb279aec26777df61e5d3530388f223ce7859d566e7a`  
		Last Modified: Tue, 16 Aug 2022 03:03:54 GMT  
		Size: 30.4 MB (30426706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3547d30662b8f49979ed975e15692a70c7bb853c6f802402d13fae5baf9c98`  
		Last Modified: Fri, 02 Sep 2022 05:11:58 GMT  
		Size: 1.2 MB (1175731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e2de4e9186b2154434f8288f5aa7bb8a9d6dc013e0874f7f022b8ae24dfbf0`  
		Last Modified: Fri, 02 Sep 2022 05:11:56 GMT  
		Size: 3.8 MB (3827460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a3a3add45c3c8843eaf042b57f390470bedeb0ac07a77f9c6612bef030c530`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47468e731ca16770a971f055794d9d4098fc38d48dd35c9031b3076ca342047`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3dc50070b191638388b8a6f45838ba98380554ae338b31cc128a05d2395988`  
		Last Modified: Fri, 02 Sep 2022 05:14:57 GMT  
		Size: 106.2 MB (106166428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd81258fb9cb69dfc99169ad3cb6e4fdf405255a94947c3080addd04660088d9`  
		Last Modified: Fri, 02 Sep 2022 05:14:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06230df102e423df05671bcf3524ba4a66b7948f791b968310ce88c3912d891b`  
		Last Modified: Fri, 02 Sep 2022 05:15:20 GMT  
		Size: 97.8 MB (97849361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fba9b08f3c34427866a17b95897c2bbf6d0ddaa0388e56fec786cc5e8b03e9`  
		Last Modified: Fri, 02 Sep 2022 05:15:07 GMT  
		Size: 280.9 KB (280936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8408c6380a2368a7fad097e912751c17f613c5e60923c6797b34c7146889011c`  
		Last Modified: Fri, 02 Sep 2022 05:15:06 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd491e285c840733c080cbbbbaaff463949c9101c61e114e1827f6c8bcac997`  
		Last Modified: Fri, 02 Sep 2022 05:15:10 GMT  
		Size: 23.2 MB (23221130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed4b59ab5f03f5776c1e0a48cdcd05a090c9d07c58d47bf3c3cdfafb3d497b0`  
		Last Modified: Fri, 02 Sep 2022 05:17:11 GMT  
		Size: 821.7 MB (821677670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:071f3c85c0ea3b4c8e0cd48cbbc904d375dfe2afbc171873b764fa7fb58dbcaa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1034200608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75310d9ea6a87a4b0b7c8b72b22175139ee533f9d4daa46b6aa355ae8eb0d782`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:32:25 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Aug 2022 15:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:33:12 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:33:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:33:14 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:33:49 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:33:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:33:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:34:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:36:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c096920dab8b763106ab108f7f67ffd78e3a0a5b90062661f6e79ba6e5531450`  
		Last Modified: Tue, 02 Aug 2022 15:52:21 GMT  
		Size: 103.9 MB (103851243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca559a4d1d3cf5ca59d168e6032d9f6eb60609afefe51b8d4c582817823f711b`  
		Last Modified: Tue, 02 Aug 2022 15:52:05 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b563ebf532fc1a5282df03ef5138b18f01216151873445a92258c9638e56a2`  
		Last Modified: Tue, 02 Aug 2022 15:52:47 GMT  
		Size: 95.2 MB (95214507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dae2ccab1eb80eed07380bc35d064a2158a70931c354fef8471c6211d2d1172`  
		Last Modified: Tue, 02 Aug 2022 15:52:33 GMT  
		Size: 278.5 KB (278490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b858516da0fdda5810073563cd5fc6d2cb426f0c32a930e5b0791d373993a1c`  
		Last Modified: Tue, 02 Aug 2022 15:52:33 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a02b086f89c57f355fd6f8e3324803ad1643c2f655acb78f836780b0bb2fbd`  
		Last Modified: Tue, 02 Aug 2022 15:52:37 GMT  
		Size: 22.4 MB (22448437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad0bc827b724b94ce49ee200b6dc031d69314c093ee84831ebbc91fe0c13ac5`  
		Last Modified: Tue, 02 Aug 2022 15:54:38 GMT  
		Size: 779.2 MB (779232733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-perception-jammy`

```console
$ docker pull ros@sha256:80f99783a43f285c7a782a3b6c5dd5609dc5ad4db23e7de5f7aa91a1089f22a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-perception-jammy` - linux; amd64

```console
$ docker pull ros@sha256:5da4c659ca33880dde2f1c81b6090f5fe36d146c2220ec69778c2a7553c46779
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1084630290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1e0191400b6a2d7a2b735a66b6136ebd11c56de6a117c0c9aa49d15c5964d5`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:35 GMT
ADD file:a7268f82a86219801950401c224cabbdd83ef510a7c71396b25f70c2639ae4fa in / 
# Thu, 01 Sep 2022 23:46:35 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:47:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:44 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:47:45 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:59:53 GMT
ENV ROS_DISTRO=rolling
# Fri, 02 Sep 2022 05:00:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:00:33 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 05:00:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 05:00:33 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:00:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:01:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 05:01:07 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 02 Sep 2022 05:01:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:03:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b55860d4c667a7200a0cb279aec26777df61e5d3530388f223ce7859d566e7a`  
		Last Modified: Tue, 16 Aug 2022 03:03:54 GMT  
		Size: 30.4 MB (30426706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3547d30662b8f49979ed975e15692a70c7bb853c6f802402d13fae5baf9c98`  
		Last Modified: Fri, 02 Sep 2022 05:11:58 GMT  
		Size: 1.2 MB (1175731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e2de4e9186b2154434f8288f5aa7bb8a9d6dc013e0874f7f022b8ae24dfbf0`  
		Last Modified: Fri, 02 Sep 2022 05:11:56 GMT  
		Size: 3.8 MB (3827460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a3a3add45c3c8843eaf042b57f390470bedeb0ac07a77f9c6612bef030c530`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47468e731ca16770a971f055794d9d4098fc38d48dd35c9031b3076ca342047`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3dc50070b191638388b8a6f45838ba98380554ae338b31cc128a05d2395988`  
		Last Modified: Fri, 02 Sep 2022 05:14:57 GMT  
		Size: 106.2 MB (106166428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd81258fb9cb69dfc99169ad3cb6e4fdf405255a94947c3080addd04660088d9`  
		Last Modified: Fri, 02 Sep 2022 05:14:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06230df102e423df05671bcf3524ba4a66b7948f791b968310ce88c3912d891b`  
		Last Modified: Fri, 02 Sep 2022 05:15:20 GMT  
		Size: 97.8 MB (97849361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fba9b08f3c34427866a17b95897c2bbf6d0ddaa0388e56fec786cc5e8b03e9`  
		Last Modified: Fri, 02 Sep 2022 05:15:07 GMT  
		Size: 280.9 KB (280936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8408c6380a2368a7fad097e912751c17f613c5e60923c6797b34c7146889011c`  
		Last Modified: Fri, 02 Sep 2022 05:15:06 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd491e285c840733c080cbbbbaaff463949c9101c61e114e1827f6c8bcac997`  
		Last Modified: Fri, 02 Sep 2022 05:15:10 GMT  
		Size: 23.2 MB (23221130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed4b59ab5f03f5776c1e0a48cdcd05a090c9d07c58d47bf3c3cdfafb3d497b0`  
		Last Modified: Fri, 02 Sep 2022 05:17:11 GMT  
		Size: 821.7 MB (821677670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-perception-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:071f3c85c0ea3b4c8e0cd48cbbc904d375dfe2afbc171873b764fa7fb58dbcaa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1034200608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75310d9ea6a87a4b0b7c8b72b22175139ee533f9d4daa46b6aa355ae8eb0d782`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:32:25 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Aug 2022 15:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:33:12 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:33:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:33:14 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:33:49 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:33:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:33:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:34:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:36:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-perception=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c096920dab8b763106ab108f7f67ffd78e3a0a5b90062661f6e79ba6e5531450`  
		Last Modified: Tue, 02 Aug 2022 15:52:21 GMT  
		Size: 103.9 MB (103851243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca559a4d1d3cf5ca59d168e6032d9f6eb60609afefe51b8d4c582817823f711b`  
		Last Modified: Tue, 02 Aug 2022 15:52:05 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b563ebf532fc1a5282df03ef5138b18f01216151873445a92258c9638e56a2`  
		Last Modified: Tue, 02 Aug 2022 15:52:47 GMT  
		Size: 95.2 MB (95214507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dae2ccab1eb80eed07380bc35d064a2158a70931c354fef8471c6211d2d1172`  
		Last Modified: Tue, 02 Aug 2022 15:52:33 GMT  
		Size: 278.5 KB (278490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b858516da0fdda5810073563cd5fc6d2cb426f0c32a930e5b0791d373993a1c`  
		Last Modified: Tue, 02 Aug 2022 15:52:33 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a02b086f89c57f355fd6f8e3324803ad1643c2f655acb78f836780b0bb2fbd`  
		Last Modified: Tue, 02 Aug 2022 15:52:37 GMT  
		Size: 22.4 MB (22448437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad0bc827b724b94ce49ee200b6dc031d69314c093ee84831ebbc91fe0c13ac5`  
		Last Modified: Tue, 02 Aug 2022 15:54:38 GMT  
		Size: 779.2 MB (779232733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base`

```console
$ docker pull ros@sha256:d9c4acfa3a63436c457734cfe1a1c2bb23f80a5d7b3ad0a962e4833c3ccf4aa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base` - linux; amd64

```console
$ docker pull ros@sha256:7b4c586e54c27743aab2a47e40c9703663d5a9e8de1e08173aafbce70150359c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (262952620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223af4769b7faa40e705248499c92752b2b8291256bf897cda3f27d405b0fe59`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:35 GMT
ADD file:a7268f82a86219801950401c224cabbdd83ef510a7c71396b25f70c2639ae4fa in / 
# Thu, 01 Sep 2022 23:46:35 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:47:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:44 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:47:45 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:59:53 GMT
ENV ROS_DISTRO=rolling
# Fri, 02 Sep 2022 05:00:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:00:33 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 05:00:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 05:00:33 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:00:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:01:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 05:01:07 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 02 Sep 2022 05:01:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b55860d4c667a7200a0cb279aec26777df61e5d3530388f223ce7859d566e7a`  
		Last Modified: Tue, 16 Aug 2022 03:03:54 GMT  
		Size: 30.4 MB (30426706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3547d30662b8f49979ed975e15692a70c7bb853c6f802402d13fae5baf9c98`  
		Last Modified: Fri, 02 Sep 2022 05:11:58 GMT  
		Size: 1.2 MB (1175731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e2de4e9186b2154434f8288f5aa7bb8a9d6dc013e0874f7f022b8ae24dfbf0`  
		Last Modified: Fri, 02 Sep 2022 05:11:56 GMT  
		Size: 3.8 MB (3827460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a3a3add45c3c8843eaf042b57f390470bedeb0ac07a77f9c6612bef030c530`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47468e731ca16770a971f055794d9d4098fc38d48dd35c9031b3076ca342047`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3dc50070b191638388b8a6f45838ba98380554ae338b31cc128a05d2395988`  
		Last Modified: Fri, 02 Sep 2022 05:14:57 GMT  
		Size: 106.2 MB (106166428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd81258fb9cb69dfc99169ad3cb6e4fdf405255a94947c3080addd04660088d9`  
		Last Modified: Fri, 02 Sep 2022 05:14:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06230df102e423df05671bcf3524ba4a66b7948f791b968310ce88c3912d891b`  
		Last Modified: Fri, 02 Sep 2022 05:15:20 GMT  
		Size: 97.8 MB (97849361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fba9b08f3c34427866a17b95897c2bbf6d0ddaa0388e56fec786cc5e8b03e9`  
		Last Modified: Fri, 02 Sep 2022 05:15:07 GMT  
		Size: 280.9 KB (280936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8408c6380a2368a7fad097e912751c17f613c5e60923c6797b34c7146889011c`  
		Last Modified: Fri, 02 Sep 2022 05:15:06 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd491e285c840733c080cbbbbaaff463949c9101c61e114e1827f6c8bcac997`  
		Last Modified: Fri, 02 Sep 2022 05:15:10 GMT  
		Size: 23.2 MB (23221130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:566852956ea3fc90533a5cc44c021d66b0693c4b85ae92313ee24a1ef567c481
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (254967875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd12507a1529223aa1d1c513771d5b2cacd63d1157d0fe6ee02c9b4c1bb00a3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:32:25 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Aug 2022 15:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:33:12 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:33:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:33:14 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:33:49 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:33:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:33:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:34:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c096920dab8b763106ab108f7f67ffd78e3a0a5b90062661f6e79ba6e5531450`  
		Last Modified: Tue, 02 Aug 2022 15:52:21 GMT  
		Size: 103.9 MB (103851243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca559a4d1d3cf5ca59d168e6032d9f6eb60609afefe51b8d4c582817823f711b`  
		Last Modified: Tue, 02 Aug 2022 15:52:05 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b563ebf532fc1a5282df03ef5138b18f01216151873445a92258c9638e56a2`  
		Last Modified: Tue, 02 Aug 2022 15:52:47 GMT  
		Size: 95.2 MB (95214507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dae2ccab1eb80eed07380bc35d064a2158a70931c354fef8471c6211d2d1172`  
		Last Modified: Tue, 02 Aug 2022 15:52:33 GMT  
		Size: 278.5 KB (278490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b858516da0fdda5810073563cd5fc6d2cb426f0c32a930e5b0791d373993a1c`  
		Last Modified: Tue, 02 Aug 2022 15:52:33 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a02b086f89c57f355fd6f8e3324803ad1643c2f655acb78f836780b0bb2fbd`  
		Last Modified: Tue, 02 Aug 2022 15:52:37 GMT  
		Size: 22.4 MB (22448437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-base-jammy`

```console
$ docker pull ros@sha256:d9c4acfa3a63436c457734cfe1a1c2bb23f80a5d7b3ad0a962e4833c3ccf4aa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-base-jammy` - linux; amd64

```console
$ docker pull ros@sha256:7b4c586e54c27743aab2a47e40c9703663d5a9e8de1e08173aafbce70150359c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (262952620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:223af4769b7faa40e705248499c92752b2b8291256bf897cda3f27d405b0fe59`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:35 GMT
ADD file:a7268f82a86219801950401c224cabbdd83ef510a7c71396b25f70c2639ae4fa in / 
# Thu, 01 Sep 2022 23:46:35 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:47:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:44 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:47:45 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:59:53 GMT
ENV ROS_DISTRO=rolling
# Fri, 02 Sep 2022 05:00:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:00:33 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 05:00:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 05:00:33 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:00:57 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:01:03 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Fri, 02 Sep 2022 05:01:07 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Fri, 02 Sep 2022 05:01:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b55860d4c667a7200a0cb279aec26777df61e5d3530388f223ce7859d566e7a`  
		Last Modified: Tue, 16 Aug 2022 03:03:54 GMT  
		Size: 30.4 MB (30426706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3547d30662b8f49979ed975e15692a70c7bb853c6f802402d13fae5baf9c98`  
		Last Modified: Fri, 02 Sep 2022 05:11:58 GMT  
		Size: 1.2 MB (1175731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e2de4e9186b2154434f8288f5aa7bb8a9d6dc013e0874f7f022b8ae24dfbf0`  
		Last Modified: Fri, 02 Sep 2022 05:11:56 GMT  
		Size: 3.8 MB (3827460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a3a3add45c3c8843eaf042b57f390470bedeb0ac07a77f9c6612bef030c530`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47468e731ca16770a971f055794d9d4098fc38d48dd35c9031b3076ca342047`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3dc50070b191638388b8a6f45838ba98380554ae338b31cc128a05d2395988`  
		Last Modified: Fri, 02 Sep 2022 05:14:57 GMT  
		Size: 106.2 MB (106166428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd81258fb9cb69dfc99169ad3cb6e4fdf405255a94947c3080addd04660088d9`  
		Last Modified: Fri, 02 Sep 2022 05:14:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06230df102e423df05671bcf3524ba4a66b7948f791b968310ce88c3912d891b`  
		Last Modified: Fri, 02 Sep 2022 05:15:20 GMT  
		Size: 97.8 MB (97849361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fba9b08f3c34427866a17b95897c2bbf6d0ddaa0388e56fec786cc5e8b03e9`  
		Last Modified: Fri, 02 Sep 2022 05:15:07 GMT  
		Size: 280.9 KB (280936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8408c6380a2368a7fad097e912751c17f613c5e60923c6797b34c7146889011c`  
		Last Modified: Fri, 02 Sep 2022 05:15:06 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd491e285c840733c080cbbbbaaff463949c9101c61e114e1827f6c8bcac997`  
		Last Modified: Fri, 02 Sep 2022 05:15:10 GMT  
		Size: 23.2 MB (23221130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-base-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:566852956ea3fc90533a5cc44c021d66b0693c4b85ae92313ee24a1ef567c481
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 MB (254967875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd12507a1529223aa1d1c513771d5b2cacd63d1157d0fe6ee02c9b4c1bb00a3`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:32:25 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Aug 2022 15:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:33:12 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:33:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:33:14 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:33:49 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     build-essential     git     python3-colcon-common-extensions     python3-colcon-mixin     python3-rosdep     python3-vcstool     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:33:55 GMT
RUN rosdep init &&   rosdep update --rosdistro $ROS_DISTRO
# Tue, 02 Aug 2022 15:33:57 GMT
RUN colcon mixin add default       https://raw.githubusercontent.com/colcon/colcon-mixin-repository/master/index.yaml &&     colcon mixin update &&     colcon metadata add default       https://raw.githubusercontent.com/colcon/colcon-metadata-repository/master/index.yaml &&     colcon metadata update
# Tue, 02 Aug 2022 15:34:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-base=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c096920dab8b763106ab108f7f67ffd78e3a0a5b90062661f6e79ba6e5531450`  
		Last Modified: Tue, 02 Aug 2022 15:52:21 GMT  
		Size: 103.9 MB (103851243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca559a4d1d3cf5ca59d168e6032d9f6eb60609afefe51b8d4c582817823f711b`  
		Last Modified: Tue, 02 Aug 2022 15:52:05 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b563ebf532fc1a5282df03ef5138b18f01216151873445a92258c9638e56a2`  
		Last Modified: Tue, 02 Aug 2022 15:52:47 GMT  
		Size: 95.2 MB (95214507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dae2ccab1eb80eed07380bc35d064a2158a70931c354fef8471c6211d2d1172`  
		Last Modified: Tue, 02 Aug 2022 15:52:33 GMT  
		Size: 278.5 KB (278490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b858516da0fdda5810073563cd5fc6d2cb426f0c32a930e5b0791d373993a1c`  
		Last Modified: Tue, 02 Aug 2022 15:52:33 GMT  
		Size: 2.2 KB (2183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a02b086f89c57f355fd6f8e3324803ad1643c2f655acb78f836780b0bb2fbd`  
		Last Modified: Tue, 02 Aug 2022 15:52:37 GMT  
		Size: 22.4 MB (22448437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core`

```console
$ docker pull ros@sha256:8a84777a42bd750116cb50a62cdd2c9b41fa6ed3c73c7ab3bd66da7d6a1258b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core` - linux; amd64

```console
$ docker pull ros@sha256:62b636750693d82af6038d86ef97419fe9b50715b452f8f5629fbff16916cd82
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141598742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06b95e4ada0c24e36fd8a8f9f13030fe23ea7867e50f915a0829bfddd89e5d4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:35 GMT
ADD file:a7268f82a86219801950401c224cabbdd83ef510a7c71396b25f70c2639ae4fa in / 
# Thu, 01 Sep 2022 23:46:35 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:47:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:44 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:47:45 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:59:53 GMT
ENV ROS_DISTRO=rolling
# Fri, 02 Sep 2022 05:00:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:00:33 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 05:00:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 05:00:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2b55860d4c667a7200a0cb279aec26777df61e5d3530388f223ce7859d566e7a`  
		Last Modified: Tue, 16 Aug 2022 03:03:54 GMT  
		Size: 30.4 MB (30426706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3547d30662b8f49979ed975e15692a70c7bb853c6f802402d13fae5baf9c98`  
		Last Modified: Fri, 02 Sep 2022 05:11:58 GMT  
		Size: 1.2 MB (1175731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e2de4e9186b2154434f8288f5aa7bb8a9d6dc013e0874f7f022b8ae24dfbf0`  
		Last Modified: Fri, 02 Sep 2022 05:11:56 GMT  
		Size: 3.8 MB (3827460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a3a3add45c3c8843eaf042b57f390470bedeb0ac07a77f9c6612bef030c530`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47468e731ca16770a971f055794d9d4098fc38d48dd35c9031b3076ca342047`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3dc50070b191638388b8a6f45838ba98380554ae338b31cc128a05d2395988`  
		Last Modified: Fri, 02 Sep 2022 05:14:57 GMT  
		Size: 106.2 MB (106166428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd81258fb9cb69dfc99169ad3cb6e4fdf405255a94947c3080addd04660088d9`  
		Last Modified: Fri, 02 Sep 2022 05:14:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:32b569f822e027e13aaa6a7defc9e5bc87dbc8543f7a090bd99582d533b28dc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137024258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f0bcc8e53596876721fb6d7cd1a4600b4346e0fe4b57fc6166399d665e0144`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:32:25 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Aug 2022 15:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:33:12 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:33:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:33:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c096920dab8b763106ab108f7f67ffd78e3a0a5b90062661f6e79ba6e5531450`  
		Last Modified: Tue, 02 Aug 2022 15:52:21 GMT  
		Size: 103.9 MB (103851243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca559a4d1d3cf5ca59d168e6032d9f6eb60609afefe51b8d4c582817823f711b`  
		Last Modified: Tue, 02 Aug 2022 15:52:05 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `ros:rolling-ros-core-jammy`

```console
$ docker pull ros@sha256:8a84777a42bd750116cb50a62cdd2c9b41fa6ed3c73c7ab3bd66da7d6a1258b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:rolling-ros-core-jammy` - linux; amd64

```console
$ docker pull ros@sha256:62b636750693d82af6038d86ef97419fe9b50715b452f8f5629fbff16916cd82
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141598742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06b95e4ada0c24e36fd8a8f9f13030fe23ea7867e50f915a0829bfddd89e5d4`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:35 GMT
ADD file:a7268f82a86219801950401c224cabbdd83ef510a7c71396b25f70c2639ae4fa in / 
# Thu, 01 Sep 2022 23:46:35 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:47:27 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:43 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:47:44 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Fri, 02 Sep 2022 04:47:45 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LANG=C.UTF-8
# Fri, 02 Sep 2022 04:47:45 GMT
ENV LC_ALL=C.UTF-8
# Fri, 02 Sep 2022 04:59:53 GMT
ENV ROS_DISTRO=rolling
# Fri, 02 Sep 2022 05:00:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:00:33 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Fri, 02 Sep 2022 05:00:33 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 02 Sep 2022 05:00:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2b55860d4c667a7200a0cb279aec26777df61e5d3530388f223ce7859d566e7a`  
		Last Modified: Tue, 16 Aug 2022 03:03:54 GMT  
		Size: 30.4 MB (30426706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3547d30662b8f49979ed975e15692a70c7bb853c6f802402d13fae5baf9c98`  
		Last Modified: Fri, 02 Sep 2022 05:11:58 GMT  
		Size: 1.2 MB (1175731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e2de4e9186b2154434f8288f5aa7bb8a9d6dc013e0874f7f022b8ae24dfbf0`  
		Last Modified: Fri, 02 Sep 2022 05:11:56 GMT  
		Size: 3.8 MB (3827460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a3a3add45c3c8843eaf042b57f390470bedeb0ac07a77f9c6612bef030c530`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47468e731ca16770a971f055794d9d4098fc38d48dd35c9031b3076ca342047`  
		Last Modified: Fri, 02 Sep 2022 05:11:55 GMT  
		Size: 2.0 KB (1990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3dc50070b191638388b8a6f45838ba98380554ae338b31cc128a05d2395988`  
		Last Modified: Fri, 02 Sep 2022 05:14:57 GMT  
		Size: 106.2 MB (106166428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd81258fb9cb69dfc99169ad3cb6e4fdf405255a94947c3080addd04660088d9`  
		Last Modified: Fri, 02 Sep 2022 05:14:39 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:rolling-ros-core-jammy` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:32b569f822e027e13aaa6a7defc9e5bc87dbc8543f7a090bd99582d533b28dc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.0 MB (137024258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f0bcc8e53596876721fb6d7cd1a4600b4346e0fe4b57fc6166399d665e0144`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 15:27:24 GMT
RUN echo 'Etc/UTC' > /etc/timezone &&     ln -s /usr/share/zoneinfo/Etc/UTC /etc/localtime &&     apt-get update &&     apt-get install -q -y --no-install-recommends tzdata &&     rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:33 GMT
RUN apt-get update && apt-get install -q -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:27:34 GMT
RUN echo "deb http://packages.ros.org/ros2/ubuntu jammy main" > /etc/apt/sources.list.d/ros2-latest.list
# Tue, 02 Aug 2022 15:27:36 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654
# Tue, 02 Aug 2022 15:27:37 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 15:27:38 GMT
ENV LC_ALL=C.UTF-8
# Tue, 02 Aug 2022 15:32:25 GMT
ENV ROS_DISTRO=rolling
# Tue, 02 Aug 2022 15:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     ros-rolling-ros-core=0.10.0-1*     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 15:33:12 GMT
COPY file:ec5b16a0e777d7d7d041a72ffc817bf5f7b375662afa0c404f3ca36fad1afb90 in / 
# Tue, 02 Aug 2022 15:33:13 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Tue, 02 Aug 2022 15:33:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdbae432836572c0a5a70dd93fdd525eb0522866e704e5d0448ef2bcade2fa`  
		Last Modified: Tue, 02 Aug 2022 15:49:16 GMT  
		Size: 1.2 MB (1193935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3f3a62e758fc4e1cba7101a491d1d2f7a4c7994f496a387f8b7bb86eb0729f`  
		Last Modified: Tue, 02 Aug 2022 15:49:14 GMT  
		Size: 3.6 MB (3595554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d6cc9185a6e97bc7eed8ed0cf9c088e4d628ac26459eb421f24af30525bb1c`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3491f7b5086834c17f0803cf85c214af78fb7a44e0ca04e9e9b61ce0be19c3`  
		Last Modified: Tue, 02 Aug 2022 15:49:13 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c096920dab8b763106ab108f7f67ffd78e3a0a5b90062661f6e79ba6e5531450`  
		Last Modified: Tue, 02 Aug 2022 15:52:21 GMT  
		Size: 103.9 MB (103851243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca559a4d1d3cf5ca59d168e6032d9f6eb60609afefe51b8d4c582817823f711b`  
		Last Modified: Tue, 02 Aug 2022 15:52:05 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
